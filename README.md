# Covid19-FAQ-Bot

The goal of this bot / voice-assistant is to provide answers to questions asked on the Corona FAQ website provided by the [https://www.bag.admin.ch/bag/en/home.html](https://www.bag.admin.ch/bag/en/home.html) and collect questions which there is not an official answer to.

## Inspiration
There are many different sources of information related to Covid19 available on the internet. Not all of them are reliable. We would like to make official information and questions/answers regarding Covid19 available to the Suisse population in a more user friendly way. Also we would like to collect all frequent questions that do not exist on official websites and inform administrations to provide answers to those frequent questions.

## What it does
It is a voice assistant and chatbot in 3 different languages English, German and French answering questions regarding Covid19. The content is from: [https://www.bag.admin.ch/bag/en/home/krankheiten/ausbrueche-epidemien-pandemien/aktuelle-ausbrueche-epidemien/novel-cov/haeufig-gestellte-fragen.html](https://www.bag.admin.ch/bag/en/home/krankheiten/ausbrueche-epidemien-pandemien/aktuelle-ausbrueche-epidemien/novel-cov/haeufig-gestellte-fragen.html)

## How we built it
We used DialogFlow from Google to make a PoC for this simple voice assistant using Google assistant. For the voice assistant we integrated it with the Dialogflow Phone Gateway (English) and Voximplant (German and French). The chatbot in English is integrated with Telegram.

## Challenges we ran into
We had very limited time to work on this project and wanted to support 3 languages. Also, we had to adapt the questions in order for them to be closer to what people would ask for in a chatbot or voice assistant.

## Accomplishments that we're proud of
The voice assistant works pretty well and answers some basic questions related to Covid19.

## What we learned
We learned how well Google DialogFlow works and what are its limitations.

## What's next for COVID19 FAQ Bot
- Fine tune questions and answers in existing languages
- Add more questions and answers based on the collected frequent questions
- Extend it for Italian

## Built with
- dialogflow
- googleassistant

## Try it out
1. Using phone numers:

**English:**

- (option 1): call +41435087297
- (option 2): call +1 484-232-8515

**German:**

- (option 1): call +41315280731
- (option 2): call one the following numbers and then enter code 699103145
    - +74993504126 (Russia)
    - +19292240694 (US)
    - +48223970842 (Poland)
    - +81345790139 (Japan)
    - +97243720980 (Israel)
    - +420228880669 (Czech Republic)
    - +14388002812 (Canada)
    - +61283104145 (Australia)
    - +442038083060 (UK)

**French:**

- (option 1): call +41215881577
- (option 2): call one the following numbers and then enter code 699103150
    - +74993504126 (Russia)
    - +19292240694 (US)
    - +48223970842 (Poland)
    - +81345790139 (Japan)
    - +97243720980 (Israel)
    - +420228880669 (Czech Republic)
    - +14388002812 (Canada)
    - +61283104145 (Australia)
    - +442038083060 (UK)
    

2. Using web demo: [https://bot.dialogflow.com/f16afd53-ea1f-4f93-a272-23259b022e23](https://bot.dialogflow.com/f16afd53-ea1f-4f93-a272-23259b022e23)

## Rebuild the project
1. Dowload this project and make a zip file.
2. Go to [https://dialogflow.cloud.google.com/](https://dialogflow.cloud.google.com/) You need your google account to login.
3. Create new agent: provide a name.
4. Go to the settings: "Export and Import". Choose "RESTORE FROM ZIP" and upload the zip file that you made at step 1.
5. Write IMPORT and press IMPORT.
6. To test you can choose the language from left side and then start talking or writing on the left side.

## Integration with Voximplant

This section will guide you through the steps you need to take in order to integrate your Dialogflow with Voximplant to support a telephony voice assistant.

### Dialogflow
There are a few things to do in your Dialogflow project.

**Text to Speech**

In your Dialogflow project, please make sure the feature Text to Speech is enabled. You can check this by going to you project settings > Speech. The output audio encoding should be set to mp3.

**Export key**
In order for Voximplant to be able to access your Dialogflow project, you need to export a service key. In your project setting > General click on the Service Account link (similar to dialogflow-txlcac@yourproject.iam.gserviceaccount.com). Click on the three dots next to the Dialog Integrations entry and click on "create key". Download the generated .json file. 

## Voximplant
**Installation**
First, sign up to Voximplant. Then select Marketplace from the Menu and install the Dialogflow Connector. Provide the .json file containing the service key for the installation.

**Numbers**
In the Numbers tab you can check which number(s) is/are attached to your application and edit them according to your needs. You can also buy new phone numbers. This has the advantage that you can offer phone numbers in countries which are not covered by Voximplant's default numbers and you don't require a code to set off the voice assistant

**Support multiple languages**
If you want to support multiple languages, you need to install an application in Voximplant as described above for every language and attach them to separate phone numbers/separate codes.

To select the language supported by the application you need to open the application and go to "Scenarios". There on the lines 16 and 20 you need to adapt the language according to your requirements. 

## Contributors:
- Mostafa Ajallooeian
- Giancarlo Bergamin
- Fatemeh Borran
- Melanie Calame

## DISCLAIMER: 
We do not in any form represent the official authorities. We simply consume the information available to the public. Nevertheless we are looking forward to receive advice from information providers at [https://www.bag.admin.ch/bag/en/home.html](https://www.bag.admin.ch/bag/en/home.html)
