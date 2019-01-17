# JDBC_Assignment1

SQL:
create database sqlandjava;

CREATE TABLE `sqlandjava`.`people` (
  `person_id` INT NOT NULL,
  `firstname` VARCHAR(45) NOT NULL,
  `lastname` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`person_id`));
  
INSERT INTO `sqlandjava`.`people` (`person_id`, `firstname`, `lastname`) VALUES ('1', 'Anna', 'Bolt');
INSERT INTO `sqlandjava`.`people` (`person_id`, `firstname`, `lastname`) VALUES ('2', 'Carl', 'Dolk');
INSERT INTO `sqlandjava`.`people` (`person_id`, `firstname`, `lastname`) VALUES ('3', 'Erik', 'Fram');
INSERT INTO `sqlandjava`.`people` (`person_id`, `firstname`, `lastname`) VALUES ('4', 'Gina', 'Hult');

CREATE USER user@localhost IDENTIFIED by 'password';
GRANT SELECT ON sqlandjava.people TO user@localhost;


CREATE TABLE `sqlandjava`.`cars` (
  `car_id` INT NOT NULL,
  `brand` VARCHAR(45) NOT NULL,
  `color` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`car_id`));

INSERT INTO `sqlandjava`.`cars` (`car_id`, `brand`, `color`) VALUES ('1', 'Volvo', 'Black');
INSERT INTO `sqlandjava`.`cars` (`car_id`, `brand`, `color`) VALUES ('2', 'Saab', 'Blue');
INSERT INTO `sqlandjava`.`cars` (`car_id`, `brand`, `color`) VALUES ('3', 'Audi', 'Red');
INSERT INTO `sqlandjava`.`cars` (`car_id`, `brand`, `color`) VALUES ('4', 'Ford', 'Green');

GRANT SELECT ON sqlandjava.cars TO user@localhost;
