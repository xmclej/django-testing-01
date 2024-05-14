# Setup

- add a django secret to .envs\.production\.django



# To run:

Run
- docker compose -f production.yml up

Exit, then change this line in  .envs\.production\.django
    DJANGO_SETTINGS_MODULE="config.settings.base"
to
    DJANGO_SETTINGS_MODULE="config.settings.trial"

Then run again
- docker compose -f production.yml up

# Background
The file trial.py is an exact copy of base.py

So then why does this work
    DJANGO_SETTINGS_MODULE="config.settings.base"

And this gives an error
    DJANGO_SETTINGS_MODULE="config.settings.trial"