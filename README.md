# forum-app

For this project I decided to use Angular 13 and Node.js with MySql database.

For Database creation use following: 

```
CREATE SCHEMA `posts`;

create table `posts`.`users`(
	`id` int not null auto_increment,
    `name` varchar(255) not null,
    `email` varchar(255) not null,
    `password` varchar(255) not null,
   primary key(`id`)
)

create table `posts`.`posts`(
	`id` int not null auto_increment,
    `title` varchar(255) not null,
    `body` varchar(255) not null,
    `user` varchar(255) not null,
    `created` timestamp not null default current_timestamp,
   primary key(`id`)
)
```

I decided to approach this project by working on back-end and database first. After verifying I have set up the database, I organized my back-end based on the different functionalities needed from the task. Specific controllers are present for different functionalities. Similar to back-end, I have organized my components based on the solution I had in mind.

What I liked is the multi-user authentication implementation, as I had to use tokens for authentication, extract and manipulate the data I get with them, as well as using an emmitter for dispatching needed action.

What was a challenge is the scope of the task and I committed myself the amount I could at this time.
