# EchoBot

Bot Framework v4 echo bot sample.

This bot has been created using [Bot Framework](https://dev.botframework.com), it shows how to create a simple bot that accepts input from the user and echoes it back.

## To try this sample

- Clone the repository
```bash
git clone https://github.com/Microsoft/botbuilder-samples.git
```
- In a terminal, navigate to `botbuilder-samples\samples\python\02.echo-bot` folder
- Activate your desired virtual environment
- In the terminal, type `pip install -r requirements.txt`
- Run your bot with `python app.py`

## Testing the bot using Bot Framework Emulator

[Bot Framework Emulator](https://github.com/microsoft/botframework-emulator) is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the latest Bot Framework Emulator from [here](https://github.com/Microsoft/BotFramework-Emulator/releases)

### Connect to the bot using Bot Framework Emulator

- Launch Bot Framework Emulator
- File -> Open Bot
- Enter a Bot URL of `http://localhost:3978/api/messages`

## Interacting with the bot

Enter text in the emulator.  The text will be echoed back by the bot.

## Deploy the bot to Azure

To learn more about deploying a bot to Azure, see [Deploy your bot to Azure](https://aka.ms/azuredeployment) for a complete list of deployment instructions.

## Further reading

- [Bot Framework Documentation](https://docs.botframework.com)
- [Bot Basics](https://docs.microsoft.com/azure/bot-service/bot-builder-basics?view=azure-bot-service-4.0)
- [Activity processing](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-concept-activity-processing?view=azure-bot-service-4.0)
- [Azure Bot Service Introduction](https://docs.microsoft.com/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0)
- [Azure Bot Service Documentation](https://docs.microsoft.com/azure/bot-service/?view=azure-bot-service-4.0)
- [Azure CLI](https://docs.microsoft.com/cli/azure/?view=azure-cli-latest)
- [Azure Portal](https://portal.azure.com)
- [Channels and Bot Connector Service](https://docs.microsoft.com/en-us/azure/bot-service/bot-concepts?view=azure-bot-service-4.0)


## My Steps

[Microsoft Resource](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-quickstart-create-bot?view=azure-bot-service-4.0&tabs=python%2Cvs)
### Create and enable a virtual environment

#### macOS/Linux

```
python3 -m venv venv
source venv/bin/activate
```

```
pip3 install botbuilder-core
pip3 install aiohttp
pip3 install cookiecutter==1.7.0
```

The packages will be installed on `venv/lib/python3.9/site-packages/`

### Create a bot

1. From your working directory, run the following command to download the echo bot template and its dependencies:

```
cookiecutter https://github.com/microsoft/BotBuilder-Samples/releases/download/Templates/echo.zip
```

2. You'll be prompted to give your bot a name and description. Enter the following values:

* **bot_name:** *echo_bot*
* **bot_description:** *A bot that echoes back user response.*

## Test the Bot

Install ngrok via Homebrew

```bash
brew install ngrok/ngrok/ngrok
```

### How to find the fucking `MicrosoftAppPassword`?

That's almost a mystery, cause Microsoft documentation about this SUCKS!

```bash
1. go to your Azure bot Configuration (the same place where you have the field "Messaging endpoint")
2. Next to the label for the field "Microsoft App ID (Manage)", click on the hyperlink "Manage"
3. Click on the section "Certificate & Secrets"
4. Go to the tab "Client Secrets"
5. Generate a "New client secret", copy the "Value" column
```
