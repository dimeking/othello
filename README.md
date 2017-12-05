# channels-othello
A simple game of Othello created to explore Django + Django Channels + ReactJS


## Synopsis

This project is based on Cody Parker's Channel Obstruction with updated logic, content to Othello (or Reversi) by Hari Raja as well as other fixes.

Explore the [Django Channels](https://github.com/django/channels), which is an upcoming core app that adds asynchronous WebSocket support to the wonderful [Django Framework](http://www.djangoproject.com). Channels makes it very easy to build "real-time" apps in pure Django and Python, providing a great way to develop applications that require features such as "real-time" collaboration or chat for example.  

[Othello](hhttps://en.wikipedia.org/wiki/Reversi) is a strategy board game for two players, played on an 8×8 uncheckered board. There are sixty-four identical game pieces called disks (often spelled "discs"), which are light on one side and dark on the other. Players take turns placing disks on the board with their assigned color facing up. During a play, any disks of the opponent's color that are in a straight line and bounded by the disk just placed and another disk of the current player's color are turned over to the current player's color.

The object of the game is to have the majority of disks turned to display your color when the last playable empty square is filled. Reversi was most recently marketed by Mattel under the trademark Othello.

This project also uses [React](https://facebook.github.io/react/) to handle the reactive, client-side components. I picked React because I like it, but it could be swapped out with Angular/Vue/Knockout/etc....

## Features

* Full game functionality:
    * Authentication - Signup / Login
    * Game Lobby with live updating list of available games
    * Ability to create a game that will show up in other users' availiable games list
    * Gameboard that enforces Othello rules and allows players to take turns and see the results in real-time
    * Game log that tracks all moves and reports them live as they occur
    * Players can chat in the game log
* Lobby and Gameboard are made up of ReactJS components on the client-side
* Examples of how to mix standard Django templating with ReactJS
* Webpack integration to create separate bundles needed for different parts of the application
* Django Rest Framework used to help serialize data needed by React as well as provides API endpoints for client-side data calls
* Mixed use of DRF, standard Django context sent from the view, as well as communication through channels to demostrate multiple ways to interact with data and the Django backend

## Requirements

* Django >= 1.9
* [Django Channels](https://github.com/django/channels)
* [Django Rest Framework](http://www.django-rest-framework.org/)
* [Django Webpack Loader](https://github.com/owais/django-webpack-loader)
* Node & Node Package Manager

## Installation

* Fork and clone this repository
* Create a Python virtual environemnt
* In that environment, run ```pip install -r requirements.txt``` inside your project
* Install node modules with ```npm install```
* Create the local database with ```python manage.py migrate```
* Run webpack to build the components with ```webpack``` 
* Run Django development server on port 8080 - ```python manage.py runserver 8080```

## License

MIT License
