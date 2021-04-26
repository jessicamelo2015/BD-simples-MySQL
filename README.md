# BD-simples-MySQL
Banco de Dados de uma Biblioteca feita em MySQL 

create database biblioteca
default character set utf8mb4
default collate utf8mb4_general_ci;

create table `biblioteca`(
`cod_livro` int not null auto_increment,
`nome_livro` varchar(30) not null,
`autor` varchar(30) not null,
`ano_publicaçao` year not null,
primary key (cod_livro)
)default charset utf8mb4;

alter table `biblioteca`
add column genero varchar(15) not null;
desc biblioteca;

insert into `biblioteca` values
(default ,'Pequeno Principe', 'Antoine De Saint Exupery','2018','Fantasia'),
(default,'As Crônicas de Nárnia','C. S. Lewis' ,'2009','Fantasia'),
(default,'A Culpa É das Estrelas','John Green','2012','Romance'),
(default,'A Menina que Roubava Livros','Markus Zusak','2007','Ficção'),
(default,'Eu sou Malala','Malala Yousafzai','2013','Biografia'),
(default,'O diário de Anne Frank' ,'Anne Frank','1995','Biografia'), 
(default,'Os miseráveis','Victor Hugo','2014','Romance'),
(default,'A sombra do vento','Carlos Ruiz Zafón','2017','Romance'),
(default,'Harry potter e a pedra filosofal','J. K. Rowling','2000','Aventura'),
(default,'Querido John','Nicholas Sparks','2017','Romance'),
(default,' A cabana','William P. Young', '2008','Ficçao'),
(default,'A Mala de Hana','Karen Levine','2007','Biografia'),
(default,'Lucíola','José de Alencar','1862','Romance');

alter table `biblioteca`
modify column nome_livro text not null;

alter table `biblioteca`
modify column  ano_publicaçao bigint not null;

select*from biblioteca

