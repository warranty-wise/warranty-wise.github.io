# warranty-wise.github.io

There is a pervasive problem with underutilization of product and service warranties. Often people forget or are unaware of warranties available to them  To create a user-friendly web application that helps individuals track and manage their product and service warranties in one centralized location, reducing the risk of missing warranty claims and helping users maximize the value of their purchases. The platform allows individuals to track and manage all their product warranties in one place, including details like purchase dates, expiration dates, coverage terms, and repair history, essentially acting as a personal record keeper for all their warranties across various products, helping them stay organized and easily access warranty information when needed. 

## Installation guide

This application utilizes Next.js, which requires version 18.18 or higher of Node.js
You can download Node.js [here](https://nodejs.org/en/download).

OR:

```
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"
# Download and install Node.js:
nvm install 22
# Verify the Node.js version:
node -v # Should print "v22.15.0".
nvm current # Should print "v22.15.0".
# Verify npm version:
npm -v # Should print "10.9.2".
```

Afterwards, navigate to the github repo that holds the code base for this application located [here](https://github.com/warranty-wise/warranty-wise) and clone the repo to your local environment.

Then, create an .env.local file in the top level directory of the application and populate with the API keys, as shown in the env.example file.

Finally:

cd into the directory where you cloned the repo and install the required libraries with:

```
npm install
```

And run the local development application with:

```
npm run dev
```

If all goes right, the application should show up at [http://localhost:3000](http://localhost:3000).


## Notable features & future implementation plans

Most of the features are rendered as components from the homepage, this was thought of and implemented by Derek. 

### Features

#### AI chatbot
The AI chatbot resides in the bottom right of the screen. However, it is a very barebones chatbot with no training done. In the future, it would be nice to have the chatbot have access to multiple pieces of the application, including the database, the page that the user is currently on, as well as the notifications system. From there, the AI can make better recommendations based on the user's warranties, expiration dates, and warranty renewal information. It can also help out during the claims process whenever that does get implemented. 

#### Warranty creation
Users are able to create warranties, either manually through the insertion form, or by uploading images of supporting documents and automatically fill out the insertion form for them by the AI. The image upload involves two main parts, the OCR and then the AI parser. OCR utilizes [Tesseract.js](https://tesseract.projectnaptha.com/), while the AI parser uses [openAI](https://platform.openai.com/docs/overview). After OCR scans the image and returns the information in raw text, the AI parser takes that text and outputs any useful information and inserts into the midpoint table. The entry would then get fetched and put into an insertion form for the user to double check before submitting into the actual warranties table.

#### Warranty document view
When users choose to upload documents to create their warranties, these documents are inserted into buckets, where each user has its own folder where they access their documents from. Users can then view all their documents in a separate page, where they can view/download the files, or choose to delete them. In the future, it would be nice to move this document view to the warranty details page, so that users are able to view the associated documents under its corresponding warranty. This is to make it easier for users to know which documents correspond to which warranty, as in most cases, users don't name their files in an organized manner. One way this could be done would be to create folders for each warranty, and upload the document file under that. Because a temporary warranty entry is made in the midpoint table, the file can be first uploaded there, and then moved under the actual warranty entry once the warranty has been confirmed by the user and submitted. However, there might be a problem of too many empty folders. 

#### Notifications/Calendar events
Currently, the calendar event system is used in place of notifications, mainly due to the limitations of a local development environment. The notifications system is there to support active reminders, where users would get emails/notifications when they have warranties that are close to expiring. The AI can also play a part in this by giving them recommendations on renewal options or upgrades. 

### Project Day Feedback

#### Feedback
Majority of the people who came by to the booth had great things to say, many talked about how useful this application would be if it was launched, and some talked about how the application can be improved on. Overall, the feedback was extremely positive, and we were praised for our work. 

#### Potential features
After listening our presentation, some people brought up future connections/features that could be implemented, including 3rd party support for acquiring receipts, expanding the scope to include other important documents and just make the application a document tracker. There were also some technical advice given for the OCR process. Two people suggested creating structured data using Pydantic and using it to help give almost 100% accurate OCR results through AI. By using this process instead of OCRing through tesseract, we can do text recognition and parsing using the same AI process. 