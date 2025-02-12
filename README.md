Initial Setup:
This repo currently contains the starter files.

Clone repo and create a virtual environment

$ git clone https://github.com/bhosxrucel/Chatbot.git
$ cd chatbot-deployment
$ python -m venv venv
$ venv\Scripts\activate

Install dependencies
$ (venv) pip install Flask torch torchvision nltk

Install nltk package
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')
>>> nltk.download('punkt_tab') (optional)

Modify intents.json with different intents and responses for your Chatbot
Run
$ (venv) python train.py

This will dump data.pth file. And then run the following command to test it in the console.
$ (venv) python chat.py

------------------------------------------------------------------------------------------------------------------------------------
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": [
        "Hi",
        "Hey",
        "Hello",
        "Good day",
        "Is anyone there?",
        "How can I sign up for the e-wallet?"
      ],
      "responses": [
        "Hello! How can I assist you with our e-wallet today?",
        "Hi there! Do you have any questions about using the e-wallet?",
        "Hey! Need help with the e-wallet?"
      ]
    },
    {
      "tag": "goodbye",
      "patterns": ["Bye", "See you later", "Goodbye"],
      "responses": [
        "Goodbye! Thanks for using our e-wallet.",
        "See you later, and happy transactions!",
        "Bye! Come back if you have more questions about the e-wallet."
      ]
    },
    {
      "tag": "thanks",
      "patterns": ["Thanks", "Thank you", "That's helpful", "Thanks a lot!"],
      "responses": [
        "Happy to help with your e-wallet queries!",
        "Any time! Feel free to ask more about the e-wallet.",
        "My pleasure!"
      ]
    },
    {
      "tag": "account_creation",
      "patterns": [
        "How do I create an e-wallet account?",
        "Sign me up for the e-wallet",
        "How to register for an e-wallet?"
      ],
      "responses": [
        "To create an e-wallet account, download our app and follow the registration steps.",
        "Signing up is easy! Just download the app, click on 'Register', and fill in your details.",
        "You can register for our e-wallet through the app or on our website by clicking 'Sign Up'."
      ]
    },
    {
      "tag": "payment_methods",
      "patterns": [
        "What payment methods can I use with the e-wallet?",
        "Can I link my bank account to the e-wallet?",
        "Do you support credit cards?"
      ],
      "responses": [
        "You can link your bank account, credit card, or use PayPal with our e-wallet.",
        "Our e-wallet supports major credit cards, bank transfers, and PayPal.",
        "Yes, you can use credit cards, bank accounts, and other popular payment methods."
      ]
    },
    {
      "tag": "transactions",
      "patterns": [
        "How do I send money with the e-wallet?",
        "Can I transfer money to someone?",
        "How to make a payment using the e-wallet?"
      ],
      "responses": [
        "To send money, open the app, select 'Send Money', and enter the recipient's details.",
        "Transferring money is simple—just choose 'Transfer' in the app and follow the instructions.",
        "You can make payments directly through the app by selecting 'Pay' and entering the necessary information."
      ]
    },
    {
      "tag": "security",
      "patterns": [
        "Is the e-wallet secure?",
        "How safe is my information in the e-wallet?",
        "What security features does the e-wallet have?"
      ],
      "responses": [
        "Our e-wallet uses advanced encryption and two-factor authentication to ensure your data is secure.",
        "We prioritize your security with features like biometric login and encrypted transactions.",
        "Your information is safe with us, thanks to our state-of-the-art security protocols."
      ]
    },
    {
      "tag": "troubleshooting",
      "patterns": [
        "I'm having trouble logging in to the e-wallet.",
        "My transaction failed, what should I do?",
        "The e-wallet app is not working."
      ],
      "responses": [
        "If you're having trouble logging in, try resetting your password or contact support.",
        "For failed transactions, please check your internet connection and try again. If the issue persists, contact our support team.",
        "If the app isn't working, try reinstalling it or updating to the latest version."
      ]
    }
  ]
}

