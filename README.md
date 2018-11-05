# apatite
|Back-end code for serving multiuser apps and AI using Python, Flask, and PodSixNet|
|:---:|
|[dwn.herokuapp.com](http://dwn.herokuapp.com)|
|![](logo.gif)|

## Linux

    git clone https://github.com/dwn/apatite.git
    nano ~/.apatite

#### Add and save the following to the file, filling in your information for 'XXXXXX'

    # -*- coding: utf-8 -*-
    from os import environ
    DISABLE_CACHE = False
    APP_NAME = 'apatite'
    ADMIN_EMAIL = 'XXXXXX'
    SECRET_KEY = 'XXXXXX'
    if 'HEROKU' in environ:
      DEBUG = False
      DB = 'XXXXXX'
      DB_USERNAME = 'XXXXXX'
      DB_PASSWORD = 'XXXXXX'
      DB_HOST = 'XXXXXX'
      MAIL_SERVER = 'XXXXXX'
      MAIL_USERNAME = 'XXXXXX'
      MAIL_PASSWORD = 'XXXXXX'
    else:
      DEBUG = True
      DB = 'XXXXXX'
      DB_USERNAME = 'XXXXXX'
      DB_PASSWORD = 'XXXXXX'
      DB_HOST = 'localhost'
      MAIL_SERVER = 'XXXXXX'
      MAIL_USERNAME = 'XXXXXX'
      MAIL_PASSWORD = 'XXXXXX'
    MAIL_PORT = 465
    MAIL_USE_TLS = False
    MAIL_USE_SSL = True
    MAIL_DEBUG = False
    MAIL_MAX_EMAILS = None
    MAIL_SUPPRESS_SEND = False
    MAIL_ASCII_ATTACHMENTS = False
    MAIL_DEFAULT_SENDER = 'no.reply@' + APP_NAME + '.com'
    ALLOWED_IMAGE_EXTENSIONS = set(['png', 'jpg', 'jpeg', 'gif'])
    STATIC_FOLDER = 'static/'
    UPLOAD_FOLDER = STATIC_FOLDER
