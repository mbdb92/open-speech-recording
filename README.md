**Open Speech Recording** is a small web application to collect short snippets of speech, and upload them to cloud storage. It's designed to help gather open speech data sets to train machine learning systems.

This is a fork of Pete Wardens repository, I only cut out the Google Cloud SDK dependency, as I didn't want to use the cloud service. The side effect of this change is the ability to run it with Python 3 instead of 2.7 only. 

## Running

You first have to change the value of `app.secret_key` inside of `main.py` to another value. You may want to use this short shellcode snippet to generate a new secret:
```
head -c 500 /dev/urandom | tr -dc 'a-f0-9' | fold -w 32 | head -n 1
```
Additional you should change the arrays in `wordlist.js` so the user get prompted for the words you want ot record

## Credits

Thanks to Pete Warden, pete@petewarden.com, for his original word on this program.
