# Polypheny-UI Development Environment

This guideline describes how to setup-up a development environment for the [Polypheny-UI](https://github.com/polypheny/Polypheny-UI). In the following, we describe two approaches.


## Prerequisites
First, make sure you have [node.js](https://nodejs.org/en/) installed.

Then, clone [Polypheny-UI](https://github.com/polypheny/Polypheny-UI), open the root folder and run

```
npm install
```


## Using gradle
If you want to build the project without having to install Angular, you can do so by executing

```
./gradlew npm_install
```

You should now be able to open the UI in your browser by entering the url [http://localhost:4200/](http://localhost:4200/).



## Using angular
If you haven't installed Angular yet, do so by executing

```
npm install -g @angular/cli
```

Now you can run
```
ng serve --aot -o
```

You should now be able to open the UI in your browser by entering the url [http://localhost:4200/](http://localhost:4200/).
