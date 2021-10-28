# Simple Fastify Demo

## The task

Taking marks as input for a specific student, display a table with student marks

## Tech

This app uses a some of open source projects to work properly:

- Node.js - Backend!
- Fastify - Server Side Framework
- UUID - Generated Unique IDs

## Installation

This Application requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd Fastify Crud
npm i
node app
```

## Inputs

| Student Name | Student Id | Subject 1 | Subject 2 | Subject 3 | Subject 4 | Subject 5 |
| ------------ | ---------- | --------- | --------- | --------- | --------- | --------- |
| Student 1    | 01         | 95        | 95        | 95        | 95        | 95        |
| Student 2    | 02         | 95        | 95        | 95        | 95        | 95        |
| Student 3    | 03         | 95        | 95        | 95        | 95        | 95        |
| Student 4    | 04         | 95        | 95        | 95        | 95        | 95        |

## What The Application Do

Creates a simple student marksheet system, where we are able to add student
details (data given in the above table), update/delete data. Also shows a simple
report like the table given above.

## Data Store

Store the data in memory. Use a simple json object to store information.

```javascript
var students = {};
```

## Endpoints

#### GET /report

This endpoint is used to get a report for all the students. This does not take
any parameter. The response should a json, simply return the students object

#### POST /add

This endpoint is used to add new records to the students object. Parameters to
be passed will be a key/value pair and the same is given in the table below as
an example:

| Key         | Value               |
| ----------- | ------------------- |
| studentName | Name of the student |
| studentID   | Unique ID           |
| subject1    | mark 1              |
| subject2    | mark 2              |
| subject3    | mark 3              |
| subject4    | mark 4              |
| subject5    | mark 5              |

#### GET /report/:id

This endpoint is used to get the mark of a particular student. Parameters to be
passed will be a key/value pair and the same is given in the table below as an
example:

| Key       | Value                                                  |
| --------- | ------------------------------------------------------ |
| studentID | unique ID of the student whose mark need to be updated |

#### POST /update

This endpoint is used to update the mark of a particular student. Parameters to
be passed will be a key/value pair and the same is given in the table below as
an example:

| Key                                         | Value                                                          |
| ------------------------------------------- | -------------------------------------------------------------- |
| studentID                                   | unique ID of the student whose mark need to be updated         |
| subject name (like subject1, subject2, etc) | subject name (like subject1, subject2, etc) updated mark value |

#### DELETE /delete

This endpoint is used to delete the details of a student. Parameters to be
passed will be a key/value pair and the same is given in the table below as an
example:

| Key       | Value                                                                 |
| --------- | --------------------------------------------------------------------- |
| studentID | studentID unique ID of the student whose information is to be deleted |
