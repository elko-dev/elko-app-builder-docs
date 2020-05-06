# elko-app-builder-docs

## Common issues:

1. Unknown Blog - you may see the following error in GithubActions:
```219
8452468a5e50: Pushed
220
afcb3ff18118: Pushed
221
unknown blob
222
```

This is an intermittent error i believe caused by network bandwidth issues in GithubActions.  The workaround currently is to just re-run the pipeline and it should eventually succeed.  We are working on a long term solution

2. Occasionally the API will deploy successfully but will not come up.  Unfortunately we just need to bounce the API on Heroku and it will eventually come up.  This has to do with our current need to run the typescript build on the heroku server (which is what they recommend) but that eats up too much RAM.  We are working to move that build process into our build step - this will be solved soon
