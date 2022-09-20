# MSQL_HW_ASGM
Queries
insert into DOCTOR_MASTER(doctor_id,doctor_name,Dept)values('D0001','Ram','ENT'),('D0002','Rajan','ENT'),('D0003','Smita','Eye'),('D0004','Bhavan','Surgery'),('D0005','Sheela','Surgery');
select * from DOCTOR_MASTER;


insert into ROOM_MASTER(room_no,room_type,status)values('R0001','AC','occupied'),('R0002',	'Suite','vacant'),('R0003','NonAC',	'vacant'),('R0004','NonAC',	'occupied'),('R0005','AC','vacant'),('R0006','AC','occupied');
select * from ROOM_MASTER;

(P0001,	Gita,	35,	65,	F,	Chennai,	9867145678,	Eye Infection,	D0003),(P0002,	Ashish,	40,	70,	M,	Delhi,	9845675678,	Asthma,	D0003),(P0003,	Radha,	25,	60,	F,	Chennai,	9867166678,	Pain in heart,	D0005),(P0004,	Chandra,	28,	55,	F,	Bangalore,	9978675567,	Asthma,	D0001)(P0005,	Goyal,	42,	65,	M,	Delhi,	8967533223,	Pain in Stomach,	D0004)

 (R0001,P0001,15-oct-16,26-oct-16),(R0002,P0002,	15-nov-16,26-nov-16),(R0002,P0003,01-dec-16,	30-dec-16),(R0004,P0001,01-jan-17,	30-jan-17);


SELECT* FROM   ROOM_MASTER where admission_date < '2013-12-13' and admission_date >= '2013-12-12;

_________________________
Passenger
(P0001,Ram,Ram@gmail.com,01-dec-80),(P0002,Rajan,Rajan@gmail.com,11-nov-39),(P0003,Smita,Smita@gmail.com,06-feb-88),(P0004,Bhavan,Bhavan@gmail.com,18-sep-73)(P0005,Sheela,Sheela@gmail.com,09-may-76),(P0006,Nethra,Nethra@gmail.com,08-oct-55);

Flight
(F0001,	Kolkata,	Hyderabad,	01-dec-12,	100,	2000),(F0002,	Chennai,	Hyderabad,	02-dec-12,	100,	3000),(F0003,	Pune,	Kolkata,	02-dec-12,	100,	2500),(F0004,	Bangalore,	Pune,	18-nov-12,	100,	2300),(F0005,	Hyderabad,	Bangalore,	09-apr-12,	100,	2600),(F0006,	Pune,	Hyderabad,	08-aug-12,	100,	3500),(F0007,	Pune,	Kolkata,	04-dec-12,	100,	2900)
(F0008,	Kolkata,	Hyderabad,	06-dec-12,	100,	3500);

Booking
(B0001,	F0001,	01-dec-12),(B0002,	F0004,	02-dec-12),(B0003,	F0005,	03-dec-12),(B0004,	F0003,	04-dec-12),(B0005,	F0001,	02-dec-12),(B0006,	F0004,	02-dec-12),(B0007,	F0003,	02-dec-16);

booking_details
(B0001,P0001),(B0001,P0002),(B0001,P0003),(B0002,P0004),(B0002,P0005),(B0003,P0006),(B0003,	P0001),(B0004,P0002),(B0005,P0003);

select p.name , a.admission_date from PATIENT _MASTER P , ROOM_ALLOCATION a where p.pid = a.pid AND month(a.admission_date) = 01 ;
