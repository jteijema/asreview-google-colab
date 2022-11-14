# ASReview on Colab

With this simple tool you can start an ASReview session on Google Colab.

The project files are stored to either your google drive or the user files found
in the window to the left of the screen, depending on your settings. If saved to
the user files, they can be accessed only as long as the runtime is live. If
saved to your google drive, they will be saved permanently and can be accessed
during a next session.

## How to use

To use this tool, you will need to follow the steps in the colab session. This
will include the following steps:

1. Open the colab session with the button below.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JTeijema/ASReview-Google-Colab/blob/main/ASReview_in_colab.ipynb)

2. Create an account on ngrok.

Navigate to [ngrok.com](https://ngrok.com/) and create an account. You do not
have to install anything.

3. Find your ngrok authentication token.

To use ngrok, you will first you will need a authentication token. This can be
found on [ngrok.com/auth](https://dashboard.ngrok.com/auth)

4. Enter your ngrok authentication token in the colab session.

Copy the authentication code and fill in the `NGROK_AUTH_TOKEN` field in the
colab session.

> If you want to protect the session with a password, mark the
> `set_password_access` checkbox. The default username and password are
> `asreview` and `colab`. You can change these in the `password_access` field.

5. Run the colab session.

Finally run all cells in the colab session. This will start ASReview. The
key-combination for running all cells is `Ctrl+F9`.

> You might need to allow access to your google drive if you want to save
project files.

6. Open the ASReview session.

The ASReview session can be opened by clicking on the link in cell below
**Start ASReview**. It will look something like this: `http://xx-xx-xx-xx.ngrok.io/`

If prompted, click `visit site`.

> if the ASReview session has been stopped, you can restart it by running the
> cells under `Set up ASReview` and `Start ASReview` again.

## Project files

Colab blocks uploading project files. The way around this is to upload them
directly to your google drive. To simplify this, you can use the cells at the
end of the notebook, titled `Import ASReview files`. These cells will upload the
files to your google drive and extract them, ready to use in asreview.

## How it works

ASReview is run as a server you can access with your browser. Instead of running
this server locally, we are using google colab, and connecting to their local
url using ngrok via the pyngrok package. The notebook also mounts a drive session to store
project files.

## License

MIT License (see LICENSE file)
