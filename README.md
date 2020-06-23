# README

Rails Pods API - Generating three models called Team, Membership, and Employee:

1. Run the following command in the terminal:
rails g model Team name:string lead:string active:boolean

In the command above the model generated is Team. 
The attributes are:
name, which is of string type, 
lead, which is of string type and 
active, which is of boolean type.

2. Run the following command in the terminal:
Run rails g model Membership google_user_id:string team_id:string active:boolean

In the command above the model generated is Membership. 
The attributes are:
google_user_id, which is of string type, 
team_id, which is of string type and 
active, which is of boolean type.

3. Run the following command in the terminal:
Run rails g model Employee first_name:string last_name:string google_user_id:string

In the command above the model generated is Employee. 
The attributes are:
first_name, which is of string type, 
last_name, which is of string type and 
google_user_id, which is of string type.