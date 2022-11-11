# ASReview on Colab

With this simple tool you can start an ASReview session on Google Colab.

The project files are stored to either your google drive or the user files found
in the window to the left of the screen, depending on your settings. If saved to
the user files, they can be accessed only as long as the runtime is live. If
saved to your google drive, they will be saved permanently and can be accessed
during a next session.

## How to use

To use ngrok, you will need a authentication token. This can be found on their
website:

[ngrok.com/auth](https://dashboard.ngrok.com/auth)

Copy the authentication code and click on the button below to start a new
ASReview session on Colab. You will need to fill in your authentication code in
the notebook manually.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JTeijema/ASReview-Google-Colab/blob/main/ASReview_in_colab.ipynb)

## How it works

ASReview is run as a server you can access with your browser. Instead of running
this server locally, we are using google colab, and connecting to their local
url using ngrok via the pyngrok package.

## License

MIT License (see LICENSE file)
