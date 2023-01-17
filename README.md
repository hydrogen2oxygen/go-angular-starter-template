# go-angular-starter-template
An angular application embedded inside a golang application

## How it was realized
The angular application was initialized as usual with the cli command
````shell
ng new ui
````
Then the angular.json was modified to distill the production build into a static folder.

The main.go use the 
````go
//go:embed static
var embededFiles embed.FS
````
to include the distilled angular application inside the executable application.