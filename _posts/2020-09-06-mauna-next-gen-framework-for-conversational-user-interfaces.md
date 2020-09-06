 
**Introduction**  
There has been a need for interactions with computers using human voice apart from the visual interfaces. There has been a significant innovation for Conversational UI, we have Siri, Alexa, Cortana etc. But, they fall short to perform well often. Deep knowledge of AI is required to build the complete solution from scratch. Rasa, Dialog Flow provide frameworks to the developers for building such applications. Developing the app using these tools is time consuming.  The tools also have limited features. Developers need to handle some of the complex concepts, like management of state, context, etc.
Mauna is building a framework that makes it very simple for any developer. Developers are not expected to have any knowledge of AI to build using Conversational UI capable applications.

This video explains [Our Vision](https://drive.google.com/file/d/1M8Qk6EUvMDgzaj-HIwAZK7NmiQmFKZWw/view)

**History of Conversational UI**  
The natural languages are very complex, but there has been a lot of innovation to master the natural languages for computing. It started with solutions like Shurdlu, Alice, which based the interactions on pattern matching at the character level. We all have used the google search, the auto complete feature and search using synonyms and stemming to operate at the word level. The further improvements were done by Siri and Alexa to be able to measure similarity between sentences. The cutting edge models are the Transformers like BERT and GPT3. The transformers can not only understand the sentences but they can generate the content in natural language.


This video elicits the [innovations and evolution in CUI](https://drive.google.com/file/d/1et1DtB5r7QVtzF2dWRE0wtthD42pDwjk/view)


 
**NLU Primer**  
Most of the platforms like Rasa, Lex, DialogFlow are capable of identifying the intents from given text and for slot filling.
The intent detection is achieved by training the model so that phrases or keywords in the natural language text can be classified as an intent.
The slot filling is achieved by using a fuzzy search on the pre-tagged data set to match the entities from a predefined set.
To build a chat bot application, we need to have a list of intent and slots. We also need a large text data to train the language model and use the model to extract the intents and slots from the input text.
 
Following video provides brief [understanding of NLU](https://drive.google.com/file/d/1ZsMusnX0uMfGHSslHreKcLnOmBeQIhth/view)
 
 
 
**Example Chat-bot using Rasa tool**  
A very [simple chatbot is built using Rasa](https://drive.google.com/file/d/1JUpZdnoE6tT3BOnUhjj9Ljr4S4o1QNU4/view) in this video.  It explains the steps the chat-bot developer has to take to build the bot.
 
 
**Key Challenges**  
There are few challenges a developer faces when building applications in Rasa.


* First of all there is a data set to be created to train the model in Rasa on your machines. Correctly training the model and computing resources costs can be a huge challenge.
* Dialog Management is very rudimentary. The dialogs are defined in stories and any variations in the input text should be handled by manually adding those variations to the story. This can be a daunting task for bigger applications.
* Context Tracking is completely missing in Rasa. Programmer will have to build the context on his own if some inputs or outputs from the bot are to be used in a later dialog.
* Semantic Understanding is to be able to decipher the correct value for any entity based on its type. Rasa does not provide such capability
* Rasa does not have the State management to keep track of all the events and state changes from the beginning of the conversation. It is very useful to consider the entire context for a more appropriate response.
* Error handling is generally not meaningful and may throw a message "something went wrong".
 
Video explains the [key challenges with current tools](https://drive.google.com/file/d/1a6MTZCfmOLMRFyZbo3gl9xp3JGoFc-3m/view) to build interactive applications using natural languages.
 
**Example Chat-bot using Mauna Framework**  
The same example as we built using Rasa can be built using Mauna with much ease and in less time.

Please watch the video for [building the application using Mauna Framework](https://drive.google.com/file/d/1-GzWMJpq7xznM5iaSrI6L2P3fzY52qSm/view)
 
**Our Solution**  
We have solved these challenges to make our solution much better.
* The programmer does not need to have any AI knowledge. We are using ontology or knowledge base.
* Powerful framework for dialogs, context, and error handling. The framework is based on the React ecosystem. The reusable components built using Mauna can be shared publicly. The Mauna applications can run on a browser, mobile phone, CLI etc.
* On the fly training can be achieved for better outcomes for special scenarios.
* Provides voice styling using Voice CSS and SSML. Voice styling is used to control the speech parameters like pitch, volume, gender, delay, emphasis.  This helps to convey the output message correctly.
* Context Awareness is a very important need for a meaningful conversation. Framework can remember the context of the conversation in the past and use it for meaningful responses.
* We use Inbuilt reasoning for Slot filling. The Slot filling is backed by Ontology and uses all of the owl rules when resolving and mapping information from the input. For instance, we can tell that the pizza cannot be negative or floating point because `Slot<Pizza>` inherits those attributes.
 
The following video throws more light on [Our Solution](https://drive.google.com/file/d/1WEjXQDVERe5LKjlIYZr7VrL18719d-x2/view)
 
Mauna Framework is a very powerful framework. The developers can build the rich applications quickly and easily using our framework. We would like you to join us in this journey. Please reach out to diwank@mauna.ai for further questions and feedback.
