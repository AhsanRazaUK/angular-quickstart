# Angular Quickstart For Web Applications
Just copy these files in your web application root folder and update your index.html.

## Getting Started
Main purpose is to quickly set up Angular in a web application created in Visual Studio. Following steps will let you have an Angular app running with ```angular-cli``` support in dotnetcore web application in no time.

### Prerequisites
* <a href='https://docs.npmjs.com/getting-started/installing-node'>NodeJS and npm.</a>
* Following example is in accordance with dotnetcore web application created in Visual Studio.

### Installing
Clone this repository to a folder with project name e-g ```my-angular-quickstart```

```
git clone https://github.com/AhsanRazaUK/angular-quickstart my-angular-quickstart
cd my-angular-quickstart
```
### Set it up
* Copy all files/folders (except ```index.html```) from ```my-angular-quickstart``` folder to your ```wwwroot``` folder of the web application
* Right-Click ```package.json``` file and ```Restore Packages```
* Click ```Show All Files``` from top of *Solution Explorer* to verify either ```node_modules``` folder has been created
* Open ```index.html``` file in notepad, copy script tags and past in the *head* section of ```_Layout.cshtml```. And Save
```environment``` tag in head must look like this now

```
   <environment include="Development">
        <link rel="stylesheet" href="~/lib/bootstrap/dist/css/bootstrap.css" />
        <link rel="stylesheet" href="~/css/site.css" />
        <!-- Polyfill(s) for older browsers -->
        <script src="~/node_modules/core-js/client/shim.min.js"></script>
        <script src="~/node_modules/zone.js/dist/zone.js"></script>
        <script src="~/node_modules/systemjs/dist/system.src.js"></script>
        <script src="~/systemjs.config.js"></script>
        <script>
            System.import('app/main.js').catch(function (err) { console.error(err); });
        </script>
    </environment>
```
* From *body* ```index.html``` file copy Angular component tag and replace html of ```Index.cshtml``` file with that. And Save
```
<div class="row">
    <div class="container">
        <!-- Angular Component -->
        <my-app>Loading AppComponent content here ...</my-app>
    </div>
</div>
```
* Run the application (```F5```) and you must see Angular component loaded. Press ```F12``` and click ```console```, you may see this message.
```
Angular is running in the development mode. Call enableProdMode() to enable the production mode.
```
## Authors

* **Ahsan Raza** 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* https://github.com/angular/quickstart
