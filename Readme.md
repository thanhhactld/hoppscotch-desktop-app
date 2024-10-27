# Why do i built this ?
Because running application hoppscotch in official require CORS, we can by pass by using Proxy or Disable CORS extensions with some effort.
But i want to deliver an better approach for everyone by using wrap electron app to by pass CORS policy


# Setup dependencies

yarn


# Start dev mode

yarn start


# Build Step

## Generate Self Sign for Sign Code

```powershell
./generate-selfsign.ps1
```


## Replace config endpoint app
```javascript
// change from endpoint at main.js file 
// to your endpoint
mainWindow.loadURL('http://myendpoint.com')
// mainWindow.loadURL('http://localhost:8080')
```

## Start Build

```
yarn make
```

After build, the ``out`` directory will contain the portable app. Please run to start app


# Trouble shoots

## User don't have permission to run app
Please copy portable app in ~/User/{{your_app_name}} to work correctly

## Clear cache app

If your app is not work correctly!,
Please remove the ``.cache`` folder to get your app back, remember that all temporatory data will be remove, any data has done in logged will be reversed !!