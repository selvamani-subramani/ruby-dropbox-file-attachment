# ruby-dropbox-file-attachment
Demo app for save & retrieve the files from dropbox by using `paperclip-dropbox` gem. 

I added the demo app for upload the files to `Dropbox` and retrieve the files from `Dropbox`. 

#What I did 

  What I did was, created a rails project and run scaffold commend for user. Then I configured the dropbox and upload the files to dropbox
  
Added `paperclip-dropbox` gem to my gem file.

#What you have to do
Create an app on your dropbox https://www.dropbox.com/developers/apps then get `api_key` and `api_secret` from your dropbox app.
Once you got the api, run the following commends

    bundle install
    rake dropbox:authorize APP_KEY=api_key APP_SECRET=api_secret ACCESS_TYPE="app_folder"

On rack commend will show a link like `https://www.dropbox.com/1/oauth/authorize?oauth_token=12345`

Open you browser and access that link and click Allow, again go back to your commend prompt and give `y`. Now it will shows the 

    access_token: 123456, 
    access_token_secret: 123456, 
    user_id: 123456

Go to `config/dropbox.yml` and update the credential

run the following commends

    rake db:create
    rake db:migrate
    rails s

Now you are ready to upload the file to dropbox and enjoy!
  
