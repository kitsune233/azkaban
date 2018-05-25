# AZCABÁN
## MCD

```
drop table if exists delicte;
drop table if exists condemna;
drop table if exists permis;
drop table if exists pres;
drop table if exists [cel·la];

create table [cel·la](
	id int identity(100,1) not null,
	aforament int not null,
	modul int not null,
	constraint cela_pk
		primary key(id)
);

create table pres(
	id int identity not null,
	nom varchar(300) not null,
	data_ingres datetime default getdate() not null,
	id_cela int not null,
	constraint pres_pk
		primary key (id),
	constraint pres_cela_fk
		foreign key (id_cela)
		references [cel·la] (id)
);

create table permis(
	des_de datetime not null,
	fins_a datetime not null,
	id_pres int not null,
	constraint permis_pk
		primary key (des_de,id_pres),
	constraint permis_pres_fk
		foreign key (id_pres)
		references pres (id)
);

create table condemna(
	dies_pel_delicte int not null,
	id_pres int not null,
	constraint condemna_pk
		primary key (id_pres),
	constraint condemna_pres_fk
		foreign key (id_pres)
		references pres (id)
);

create table delicte(
	id int not null,
	nom varchar(300) not null,
	id_pres int not null,
	constraint delicte_pk
		primary key (id_pres,id),
	constraint delicte_condemna_fk
		foreign key (id_pres)
		references pres (id)
);
```
