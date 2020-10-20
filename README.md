# BlazorwithAzureAuth
In my personal azure portal I have registered a new app and copied its tenant and client id in appsettings.json file.
In Application manifest file I have added two roles (Manager,Member)
I assigned Manager role to a user.
I am log in with same user.
Authentication is successfull and when I decode token at browser end I get following things.
{
  "typ": "JWT",
  "alg": "RS256",
  "kid": "kg2LYs2T0CTjIfj4rt6JIynen38"
}.{
  "aud": "7a0762f5-8f5b-48a7-aa04-7646a99cd4ef",
  "iss": "https://login.microsoftonline.com/67e6b053-49cf-4e7e-b288-51f16e682196/v2.0",
  "iat": 1603212558,
  "nbf": 1603212558,
  "exp": 1603216458,
  "aio": "AWQAm/8RAAAArtyFb+pfG52bF0afpSzWmqlkhRxyJdNDB/S1+EwKWfQp/NQqjAEqDuYZsxTO9DqN+kmqwxncJqgd/1Ey63HfnlW2iS3r9srpxFxIzGVjmt41UGSiX5FFk4T3CfZcDidH",
  "idp": "https://sts.windows.net/9188040d-6c67-4c5b-b112-36a304b66dad/",
  "name": "Prakash Buddhabhatti",
  "nonce": "94a2e7c9-2011-440c-9ffc-10003bd8f6e3",
  "oid": "98964447-d90a-44ce-97c3-866fb3670ed6",
  "preferred_username": "prakash.20201007@gmail.com",
  "rh": "0.AAAAU7DmZ89Jfk6yiFHxbmghlvViB3pbj6dIqgR2Rqmc1O9wAIQ.",
  "roles": [
    "Manager"
  ],
  "sub": "egaSaWN0Ciw_DNXqsek9ChM3G6gMtfIAJG7sz5ve4Eg",
  "tid": "67e6b053-49cf-4e7e-b288-51f16e682196",
  "uti": "b6ZbFbZjnky7v-uUWiZAAA",
  "ver": "2.0"
}.[Signature]

In the above token I can see that I get Manager as a role.
In Conter component I set authorization for "Manager" role but there it doesnt work.
