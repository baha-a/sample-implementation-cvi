# Draft readme

# About

This is a repo to showcase how to implement different CVI components when building Bürokratt.

In order to run it via docker, froom root directory run command 'docker-compose up -d'
In order to run project as react app, run 'npm install --legacy-peer-deps' followed by 'npm run dev'

# References

### Gov CVI

https://github.com/orgs/buerokratt/projects/34
https://github.com/buerokratt/cvi

# Creating package

To create npm package for header:
* navitage to : src > exportcomponents
* run 'npm pack' command to create package locally

To publish npm package:
* run 'npm publish --access public'
* Authorize in npm and package would be published
  * If you want to use local package, put created package to the root of react app and add depenency like "@exirain/header": "file:exirain-header-0.0.5.tgz" (use proper version)

To USE header package
* in order for header package to work you need to do some steps
  * in main.tsx/index.tsx 
    * Use imprort and import mockApi to mock apis or make sure all data is being fetched
    * If data is being mocked by provided mock api make sure to import * as mock from header package and use it
  * Make sure that App.tsx fetches initial user info and stores it in store that provided by application
  * In layout component you need to provide userState to the header component <Header user={useUserInfoStore.getState()}/>

Implemented header with examples could be found in:
* https://github.com/buerokratt/Training-Module
* https://github.com/buerokratt/Service-Module
* https://github.com/buerokratt/Analytics-Module


