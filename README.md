# Epicodus Independent Project - March 20, 2020

### Created by: Brandan Sayarath

## Description

This is the Epicodus independent end-of-week assignment for Friday, March 20, 2020.  The purpose of this assignment is to create an MVC web application to help manage a hair salon's stylists and their clients. The salon owner should be able to add a list of stylists working at the salon, and for each stylist, add clients who see that stylist.  The stylists have specific specialties, so each client can only see (belong to) a single stylist.

## Behavior Driven Development Specifications

| Specification             | Input 	|     Output      |
|-------------------------	|-------	|----------------	|
|When user visits '/' root route, display splash page with link to '/stylists' and '/clients' | user visits '/' route | display home|
| When user visits '/stylists' display list of all stylists, each with 'view detail' link, and 'add new stylist' button | user visits '/stylists' | display list of stylists, and 'Add new stylist' button|
| When user clicks 'Add new stylist' button, redirect to stylist form | clicks 'add new stylist' | redirect to '/stylists/create'|
| When user visits '/stylists/create' show new stylists form with field for "Stylist Name" and "Stylist Speciality" | user visits '/stylists/create' | show stylist form |
| When user clicks submit on stylist form, add new stylist to List and redirect to '/stylists' | clicks submit | Add new stylist to List, redirect to '/stylists' |
| When user visits '/stylists/{id}', they will see the details of the stylist | user visits stylist page | show stylist info |
| When user visits '/clients' display list of all clients, each with 'view detail' link, and 'add new client' button | user visits '/clients' | display list of clients, and 'Add new client' button|
| When user clicks 'Add new client' button, redirect to client form | clicks 'add new client' | redirect to '/client/create'|
| When user visits '/client/create' show new client form with field for "Client Name" | user visits '/client/create' | show stylist form |
| When user clicks submit on client form, add new client to List and redirect to '/clients' | clicks submit | Add new client to List, redirect to '/clients' |

## Setup/Installation Requirements

Clone this repository via Terminal using the following commands:
* ```$ cd desktop```
* ```$ git clone https://github.com/brandanpdx/hair-salon```
* ```$ cd hair-salon```

To run the program, navigate to the HairSalon production folder by typing the following into the terminal: 

* ```$ cd HairSalon```

Then restore dependencies by typing:
* ```$ dotnet restore```

Setup MySQL Database by running the commands below in MySQL Workbench: 

```
CREATE DATABASE `brandan_sayarath`;
USE `brandan_sayarath`;
CREATE TABLE `stylists` (
  `StylistId` int(11) NOT NULL AUTO_INCREMENT,
  `StylistName` varchar(255) DEFAULT NULL,
  `StylistSpeciality` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`StylistId`)
);
CREATE TABLE `clients` (
  `ClientId` int(11) NOT NULL AUTO_INCREMENT,
  `ClientName` varchar(255) DEFAULT NULL,
  `StylistId` int(11) DEFAULT '0',
  PRIMARY KEY (`ClientId`)
);
```

You can now run the program by typing:
* ```$ dotnet run```


## Support and Contact

Please email Brandan Sayarath: brandan@brandan.tech for any questions.

## Technologies Used

This program was created with:

* C#
* ASP.NET Core MVC 2.2
* Entity Framework
* MySQL
* MySQL Workbench 
* HTML5

## License

This code is licensed under MIT permissive free software license

Copyright (c) 2020 Brandan Sayarath

