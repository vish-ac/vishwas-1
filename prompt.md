build a web app that dose chats analysis
The idea is simple. People often miss a lot of messages in WhatsApp groups, especially when they are busy or haven't checked their phone for a few hours or days. Going through hundreds of messages just to understand what happened is frustrating.

I want to build an app where users can upload a downloaded WhatsApp chat export (.txt file), and the app analyses the conversation and tells them what happened while they were away.

The main goal is that when someone opens the app, they should be able to understand the important parts of a long conversation in a few seconds instead of reading every single message.

What I want the app to do

When the user opens the website, they should see a clean, modern dashboard with an option to upload or drag and drop their exported WhatsApp chat file. After uploading, they should be able to select the date or point from which they want to catch up.

The app should then show:

A short summary of what the conversation is about.
The important things that happened while the user was away.
Important messages and discussions, arranged by priority.
Decisions made by the group.
Tasks, deadlines, meetings, and upcoming events.
Messages where the user was mentioned or asked to do something.
Questions that are still waiting for a response.
Changes in plans or important updates.
A timeline of the main events in the conversation.

I also want a section called "What Needs My Attention?" that shows the most important things first, so the user doesn't have to search through the entire summary.

The user should be able to enter their name or common aliases so the app can identify relevant mentions and tasks. It should not assume that every task belongs to the user.
 Add a search feature so users can find messages by keyword, sender, date, or topic. When someone clicks on a summary point, task, or decision, the app should take them to the original message that supports it.

I would also like an "Ask Your Chat" feature where users can ask questions such as:

What did I miss yesterday?
What did the group decide?
Is there anything I need to do?
When is the next meeting?
Who is waiting for my response?

Answers should be based on the uploaded conversation, and the app should show the messages used to generate each answer. If the information isn't available, it should say so rather than make something up.

Allow users to export their summary as a text or Markdown file.

Privacy is extremely important

I want this app to work locally on the user's computer because WhatsApp conversations can contain personal and sensitive information.

The chat file must not be uploaded to a server or sent to external AI APIs. Messages, names, phone numbers, summaries, and analysis results must stay on the user's device.

I want two modes:

Quick Analysis: Works without installing an AI model. It should use local parsing and rule-based techniques to identify useful information and generate basic summaries. Make its limitations clear.
Local AI Analysis: Uses a language model running locally on the user's computer, such as Ollama, to provide better summaries and answer questions. If the model isn't installed, show the user how to set it up and let them continue using Quick Analysis.

Do not secretly switch to a cloud AI service if local analysis fails.

The app should also have a clear privacy indicator and a button to delete the imported chat and its analysis. Avoid saving private chat data permanently unless the user explicitly chooses to do so.

Design and user experience

I want the website to look like a real, polished product that could impress hackathon judges. Avoid the appearance of a generic template.

Use a dark theme with a near-black background, clean typography, subtle teal or violet accents, well-designed cards, and smooth but restrained animations. Make it responsive so it works on laptops and mobile screens.

The dashboard should feel interactive and easy to navigate. Include sections for the summary, priority messages, tasks, decisions, timeline, search, and Ask Your Chat. Show useful loading states while analysis is running, clear errors when a file cannot be parsed, and helpful empty states before a chat is uploaded.

Don't fill the interface with fake statistics or pretend analysis results. If you include demo data, label it as demo data.

Technical requirements

i should be able to upload the files to my repo and directly deploy it ,make the code  . 
Use a suitable stack such as React, TypeScript, and Vite for the frontend. Choose a practical approach for local chat parsing and AI analysis. A Python backend running on localhost is fine if needed.

The parser should handle common WhatsApp exports from Android and iPhone, different timestamp formats, multiline messages, system messages, media placeholders, and Unicode text. It should not silently lose messages when the format differs.

Keep references to the original messages so the user can verify extracted information. Treat chat contents as untrusted data, and don't let instructions inside messages interfere with the app's own analysis.

Publishing the website

I need to publish this project through my GitHub repository for the hackathon.

Please make sure the public repository contains the app's source code and setup instructions, not any real WhatsApp chats or private information. Add an appropriate .gitignore.

If possible, make the frontend deployable through GitHub Pages. However, the published website must not require users to upload private conversations to a remote server. Explain how the public website and local analysis mode work together, including any local setup requirements.

Include a README with beginner-friendly instructions for running the project on Windows 11, installing the required dependencies, setting up a local AI model, running tests, and publishing the frontend.

Please build the actual application

my reo is a new one and dosenot contain any files.

Make sure the important features actually work. Test the WhatsApp parser with different message formats, test the analysis features, check that the original-message references work, and run the production build. Fix any errors you find.

make the website easy to navigate and user friendly.

If something cannot be implemented fully, explain why and provide the best working alternative. Don't claim a feature is complete unless it really works.

The final result should help someone understand an overwhelming WhatsApp conversation in a few seconds, identify what they missed, and know what needs their attention, all while keeping their private data on their own computer.
