# _Volunteer Tracker_

#### _A volunteer tracking web application, 9.22.2017_

#### By _**Kristen Marie Kulha**_

## Description

This web application allows users to create projects and assign volunteers to projects that have been created. From the landing page, the user view a list of ongoing projects and also add a new project. When a particular project is clicked, the user is taken to that projects unique page where a list of volunteers assigned to that specific project is listed. The user can then update the title of the project if they so choose and also add volunteers to the project. There is also a delete button that will remove the project and all associated volunteers and redirect the user to the Home page.

## Specifications
* _It will create an instance of a project class._
  * Example input: project = project.new({:title => "Teaching Kids to Code", :id => nil})
  * Example output: project.name = "Teaching Kids to Code"
* _It will save an instance of the project to the database._
  * Example input: project.save
  * Example output: Innerstellar Pig, William Sleator, nil
* _It will return a list of projects from the database._
  * Example input: Project.all
  * Example output: [project]
* _It will allow user to delete projects from the database._
  * Example input: project.delete({:title => "Teaching Kids to Code", :id => nil})
  * Example output: Project.all != [project]
* _It will return a project when given the id._
  * Example input: Project.(id)
  * Example output: project
* _It will create an instance of the volunteer class._
  * Example input: volunteer = Volunteer.new({:name => "Jónsi", :project_id => 1, :id => nil})
  * Example output: volunteer.name = "Jónsi"
* _It will save an instance of a volunteer to the database._
  * Example input: volunteer.save
  * Example output: Volunteer.all = [volunteer]
* _It will return a list of volunteers from the database._
  * Example input: Volunteer.all
  * Example output: [volunteer]
* _It will update a project in the database._
  * Example input: project.update ({:title => "Jónsi Birgisson Project"})
  * Example output: project.title = "Jónsi Birgisson Project"
* _It will delete a project from the database._
  * Example input: project.delete
  * Example output: Project.all != [project]

## Setup/Installation Requirements

* _Clone directory from github using git_

* __NOTE: These instructions assume you already have Ruby and Sinatra installed.__

### Installing the necessary database:

* _Do you have postgres and psql installed? [Download](https://www.postgresql.org/download/)_

* _In your terminal enter:_ ``` $postgres```

* _Now enter_ ```$psql```

* _Create the needed database by entering_ ```$CREATE DATABASE volunteer_tracker;```

* _Connect to new database by entering_ ```$c\ volunteer_tracker```

* _Enter the following:_

```CREATE TABLE projects (id serial PRIMARY KEY, title varchar);```

_The terminal should echo back CREATE TABLE. Then enter:_

```CREATE TABLE volunteers (id serial PRIMARY KEY, name varchar, project_id int);```



* _In terminal, navigate into main project directory folder_

* _Enter:_ ```$ruby app.rb```

* _In web browser of choice copy and paste the following into the address field :_ ```http://localhost:4567/```


## Known Bugs

_There are no known bugs at this time._

## Support and contact details

_Feel free to contact me at kristen.m.kulha@gmail.com_

## Technologies Used

_Ruby, Sinatra, SQL, HTML, CSS, Bootstrap_

### License

*This software is licensed under the MIT license.*

Copyright (c) 2017 **_Kristen Marie Kulha_**
