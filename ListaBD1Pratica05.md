use pratica05;

create table dados_multimidia(
Codigo integer not null,
Nome varchar(30) not null,
Tipo varchar(20) not null,
Dados longblob not null,
primary key (Codigo));
  
insert into dados_multimidia (Codigo, Nome, Tipo, Dados)
Values(1, 'LOL0','png', ('C://ProgramData//MySQL//MySQL Server 5.7//Uploads//1.png'));	

insert into dados_multimidia (Codigo, Nome, Tipo, Dados)
Values(2, 'LOL1', 'png', ('C://ProgramData//MySQL//MySQL Server 5.7//Uploads//2.png'));

insert into dados_multimidia (Codigo, Nome, Tipo, Dados)
Values(3, 'LOL2', 'png', ('C://ProgramData//MySQL//MySQL Server 5.7//Uploads//3.png'));

insert into dados_multimidia (Codigo, Nome, Tipo, Dados)
Values(5, 'LOL3', 'JPEG', ('C://ProgramData//MySQL//MySQL Server 5.7//Uploads//4.png'));

Select* from dados_multimidia;

Select Dados INTO DUMPFILE "C://ProgramData//MySQL//MySQL Server 5.7//Uploads//122.png" FROM DADOS_MULTIMIDIA WHERE 'Codigo'=1 ;
