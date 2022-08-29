# README

Created following the [guide @ guides.rubyonrails.org](https://guides.rubyonrails.org/getting_started.html)

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

    - Ruby 3.0.0
    - SQLite3

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## Using Rails CLI

Create a project

    rails new blog
    cd blog

Start server using

    rails server

Stop server

    ctrl+c

Create a model

    rails generate model [Model_Name]

Create a controller

    rails generate controller [Model_Name]

Migrate Schemas

    rails db:migrate

Use rails shell to manually add data

    rails console
    ...
    > article = Article.new(title:"...", body:"...")
    ...
    > article.save

## Routes

Adding a GET route: `GET /articles` is mapped to the `index` action of the controller

```rb
Rails.application.routes.draw do
  get "/articles", to: "articles#index"
end
```

## Controller

Create a controller to handle Article routes 

    rails generate controller Articles

The controller's methods (called `actions`) handle rendering views or returning data when a route is accessed.

```rb
class ArticlesController < ApplicationController
  def index
    # returns a list of articles, GET /articles
    @articles = Article.all 
  end

  def show
    @articles = Article.find(params[:id])
  end

  # other actions (new, create, edit, update, destroy)
end
```

## Model



## View
