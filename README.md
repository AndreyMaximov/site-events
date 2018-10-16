# Instruction of install site
You must have utilities `drush`, `composer` and `git` on our server.

## INSTALLATION
1. Clone git repository `git clone git@github.com:miroslav-lee/site-events.git .` in core directory of the site
2. Download Drupal with modules of project `composer install`
3. Install Drupal
    * Choose language and click the button "Save and continue"
    ![Step 1](https://i.paste.pics/1234cc059b8d92b4138211220ead452f.png "Step 1")
    * Select an installation profile
    ![Step 2](https://i.paste.pics/ce148a0c1cbbd60d4e29580757b76c08.png "Step 2")
    * Enter your data for connecting to the database
    ![Step 3](https://i.paste.pics/8a7c838a095254ffdf2e6c59e0d390a5.png "Step 3")
    * Wait to finish install Drupal
    ![Step 4](https://i.paste.pics/00b496f4f0ff4ac18c8fa74c4c74d740.png "Step 4")
    * Specify site information
    ![Step 5](https://i.paste.pics/ef7432b97fe59683f20b147fb12cc82f.png "Step 5")
4. `drush cset system.site uuid 6dc1d2bc-bbeb-4d2a-81d3-ce12b3cf307b -y`
5. `drush ev "entity_delete_multiple('shortcut', \Drupal::entityQuery('shortcut')->execute());"`
6. Import config files of site `drush cim -y`

![drush cim](https://i.paste.pics/9303ff1116df35b71dec33e760719ccf.png "drush cim")

7. Command `drush en events -y` enable module Events
8. `drush updb && drush entity-updates`

## ADD CONTENT TO EVENT TOPIC
1. Click on _Content->Add content->Events_ or go to `/node/add/events`
![Add event](https://i.paste.pics/19d835b0888e0aaf46c17e4b6bb8e135.png "Add event")
2. Specify event information and save
![Event information](https://i.paste.pics/e9992791d1a9cef5d2821e9494c26fe7.png "Event information")
3. You can see our event content
![Event](https://i.paste.pics/b2b7600a357e576e318f995919ff8d7f.png "Event")