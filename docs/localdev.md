## Local Development

### Setup Mattermost
1. `docker run -d --publish 8065:8065 --add-host dockerhost:127.0.0.1 mattermost/mattermost-preview`
2. Login and create a user for your bot
3. Navigate to **System Console** -> **Integration Management**
  - Select _Enable Personal Access Tokens_ 
4. **System Console** -> **Users** -> BOTUSER -> **Manage Roles**
  - Select _Allow this account to generate personal access tokens._
5. Logout and login as your bot account
  - **Account Settings** -> **Security** -> Create new token
    - Make sure to save this!!!!
6. I'd reccommend using ngrok to proxy your local instance
  - `ngrok http 8065`
  - The URL would become your new MATTERMOST_HOST value