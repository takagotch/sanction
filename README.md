### sanction
---
https://github.com/demianbrecht/sanction

```py
from sanction.client import Client

c = Client(auth_endpoint="https://accounts.google.com/o/oauth2/auth",
  client_id=config["google.client_id"],
  redirect_uri="http://localhost:8080/login/google")

c = Client(token_endpoint="https://accounts.google.com/o/oauth2/token",
  resource_endpoint="https://www.googleapis.com/oauth2/v1",
  redirect_uri="http://localhost:8080/login/google",
  client_id=config["google.client_id"],
  client_secret=config["google.client_secret"])

scope_req = 'scope1,scope2'
my_redirect(c.auth_uri(scope_req))

my_redirect(c.auth_uri(state=my_state))

c.request_token(response_dict)

c.request_token(grant_type='refresh_token',
  refresh_token=my_refresh_token)
  
c.request("/userinfo")

c.request("/userinfo", parser=lambda c: dosomething(c))
```

```
```

```
```


