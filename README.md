# ChatGpt-Clone

## Introduction:
This JavaScript code creates an interactive chatbot interface that leverages OpenAI's API to generate responses. The chatbot features include theme toggling, chat deletion, and copying responses. It enhances user interaction by saving chat history in local storage and adapting to user input dynamically.

## Working:
### Initialize and Load Data:

####loadDataFromLocalstorage: This function loads the chat history and theme preferences from local storage when the page loads. It applies the saved theme (light or dark mode) and displays previous chat conversations or a default welcome message.
Chat Elements Creation:

#### createChatElement: 
This utility function creates and returns a chat message element with specified content and CSS class (either "incoming" or "outgoing").
Get Chat Response:

#### getChatResponse: 
This asynchronous function interacts with the OpenAI API to fetch a response based on the user's input. It sends a POST request to the OpenAI API with the user's message and updates the chat with the response.

### Copy Response:

#### copyResponse: 
This function allows users to copy the chatbot's response text to the clipboard. It temporarily changes the copy button's text to indicate success.
Show Typing Animation:

#### showTypingAnimation: 
This function displays a "typing" animation to simulate the chatbot thinking. It then calls getChatResponse to fetch and display the response.

###Handle Outgoing Chat:

####handleOutgoingChat:
This function processes the user's input message, creates an outgoing chat element, and triggers the chatbot's response simulation. It clears the input field and adjusts its height dynamically.
Delete Chat History:

####Delete Button: 
Clicking the delete button clears the chat history from local storage after confirming the action with the user.
Theme Toggle:

####Theme Button: 
Clicking the theme button toggles between light and dark modes. The current theme preference is saved to local storage.

###Input Handling:

####Adjusting Input Height: 
The height of the chat input field adjusts automatically based on the content.
####Enter Key Handling: 
Pressing Enter without holding Shift sends the message if the window width is greater than 800 pixels.
