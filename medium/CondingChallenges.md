# Coding Challenges

Julia asked her students to create some coding challenges. Write a query to print the hacker_id, name, and the total number of challenges created by each student. Sort your results by the total number of challenges in descending order. If more than one student created the same number of challenges, then sort the result by hacker_id. If more than one student created the same number of challenges and the count is less than the maximum number of challenges created, then exclude those students from the result.

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/41462c4b65b65a520c8b99d1e8e4fa3c0230b780/medium/assets/condingChallenges.PNG)
 
### How to run this project?

#### Precondition: Oracle SQL Developer

```SQL

-- create table functions

create table Hackers (
hacker_id Integer,
name varchar(30));

create table Challenges (
challenge_id integer,
hacker_id integer);

-- inserting records

insert into Hackers(hacker_id,name) values (trim('10')  ,trim('ose       '));
insert into Hackers(hacker_id,name) values (trim('91')  ,trim('ngela     '));
insert into Hackers(hacker_id,name) values (trim('158') ,trim('rank      '));
insert into Hackers(hacker_id,name) values (trim('810') ,trim('atrick    '));
insert into Hackers(hacker_id,name) values (trim('1195'),trim('isa       '));
insert into Hackers(hacker_id,name) values (trim('1315'),trim('imberly   '));
insert into Hackers(hacker_id,name) values (trim('1468'),trim('onnie     '));
insert into Hackers(hacker_id,name) values (trim('1632'),trim('ichael    '));
insert into Hackers(hacker_id,name) values (trim('1799'),trim('odd       '));
insert into Hackers(hacker_id,name) values (trim('1804'),trim('oe        '));
insert into Hackers(hacker_id,name) values (trim('1974'),trim('arl       '));
insert into Hackers(hacker_id,name) values (trim('2069'),trim('obert     '));
insert into Hackers(hacker_id,name) values (trim('2245'),trim('my        '));
insert into Hackers(hacker_id,name) values (trim('2289'),trim('amela     '));
insert into Hackers(hacker_id,name) values (trim('2373'),trim('aria      '));
insert into Hackers(hacker_id,name) values (trim('2689'),trim('oe        '));
insert into Hackers(hacker_id,name) values (trim('3432'),trim('inda      '));
insert into Hackers(hacker_id,name) values (trim('3487'),trim('elissa    '));
insert into Hackers(hacker_id,name) values (trim('3640'),trim('arol      '));
insert into Hackers(hacker_id,name) values (trim('3740'),trim('aula      '));
insert into Hackers(hacker_id,name) values (trim('3834'),trim('arilyn    '));
insert into Hackers(hacker_id,name) values (trim('4087'),trim('ennifer   '));
insert into Hackers(hacker_id,name) values (trim('4148'),trim('arry      '));
insert into Hackers(hacker_id,name) values (trim('4586'),trim('avid      '));
insert into Hackers(hacker_id,name) values (trim('5120'),trim('ulia      '));
insert into Hackers(hacker_id,name) values (trim('5367'),trim('evin      '));
insert into Hackers(hacker_id,name) values (trim('5443'),trim('aul       '));
insert into Hackers(hacker_id,name) values (trim('5734'),trim('ames      '));
insert into Hackers(hacker_id,name) values (trim('5827'),trim('elly      '));
insert into Hackers(hacker_id,name) values (trim('6011'),trim('obin      '));
insert into Hackers(hacker_id,name) values (trim('6116'),trim('alph      '));
insert into Hackers(hacker_id,name) values (trim('6973'),trim('loria     '));
insert into Hackers(hacker_id,name) values (trim('7302'),trim('ictor     '));
insert into Hackers(hacker_id,name) values (trim('7537'),trim('avid      '));
insert into Hackers(hacker_id,name) values (trim('7565'),trim('oyce      '));
insert into Hackers(hacker_id,name) values (trim('7846'),trim('onna      '));
insert into Hackers(hacker_id,name) values (trim('7961'),trim('ichelle   '));
insert into Hackers(hacker_id,name) values (trim('8096'),trim('tephanie  '));
insert into Hackers(hacker_id,name) values (trim('8125'),trim('erald     '));
insert into Hackers(hacker_id,name) values (trim('8157'),trim('alter     '));
insert into Hackers(hacker_id,name) values (trim('8505'),trim('hristina  '));
insert into Hackers(hacker_id,name) values (trim('8549'),trim('randon    '));
insert into Hackers(hacker_id,name) values (trim('9064'),trim('lizabeth  '));
insert into Hackers(hacker_id,name) values (trim('9642'),trim('oseph     '));
insert into Hackers(hacker_id,name) values (trim('9901'),trim('awrence   '));
insert into Hackers(hacker_id,name) values (trim('9910'),trim('arilyn    '));
insert into Hackers(hacker_id,name) values (trim('1005'),trim('Lori      '));
insert into Hackers(hacker_id,name) values (trim('1006'),trim('Matthew   '));
insert into Hackers(hacker_id,name) values (trim('1040'),trim('Jesse     '));
insert into Hackers(hacker_id,name) values (trim('1073'),trim('John      '));
insert into Hackers(hacker_id,name) values (trim('1093'),trim('Martha    '));
insert into Hackers(hacker_id,name) values (trim('1094'),trim('Timothy   '));
insert into Hackers(hacker_id,name) values (trim('1097'),trim('Christine '));
insert into Hackers(hacker_id,name) values (trim('1101'),trim('Anthony   '));
insert into Hackers(hacker_id,name) values (trim('1140'),trim('Paula     '));
insert into Hackers(hacker_id,name) values (trim('1165'),trim('Kimberly  '));
insert into Hackers(hacker_id,name) values (trim('1171'),trim('Louise    '));
insert into Hackers(hacker_id,name) values (trim('1211'),trim('Martin    '));
insert into Hackers(hacker_id,name) values (trim('1211'),trim('Paul      '));
insert into Hackers(hacker_id,name) values (trim('1246'),trim('Antonio   '));
insert into Hackers(hacker_id,name) values (trim('1276'),trim('Jacqueline'));
insert into Hackers(hacker_id,name) values (trim('1289'),trim('Diana     '));
insert into Hackers(hacker_id,name) values (trim('1307'),trim('John      '));
insert into Hackers(hacker_id,name) values (trim('1320'),trim('Dorothy   '));
insert into Hackers(hacker_id,name) values (trim('1379'),trim('Evelyn    '));
insert into Hackers(hacker_id,name) values (trim('1383'),trim('Phillip   '));
insert into Hackers(hacker_id,name) values (trim('1390'),trim('Evelyn    '));
insert into Hackers(hacker_id,name) values (trim('1421'),trim('Debra     '));
insert into Hackers(hacker_id,name) values (trim('1430'),trim('David     '));
insert into Hackers(hacker_id,name) values (trim('1438'),trim('Willie    '));
insert into Hackers(hacker_id,name) values (trim('1439'),trim('Brandon   '));
insert into Hackers(hacker_id,name) values (trim('1439'),trim('Ann       '));
insert into Hackers(hacker_id,name) values (trim('1472'),trim('Emily     '));
insert into Hackers(hacker_id,name) values (trim('1510'),trim('Dorothy   '));
insert into Hackers(hacker_id,name) values (trim('1514'),trim('Jonathan  '));
insert into Hackers(hacker_id,name) values (trim('1686'),trim('Dorothy   '));
insert into Hackers(hacker_id,name) values (trim('1701'),trim('Marilyn   '));
insert into Hackers(hacker_id,name) values (trim('1728'),trim('Norma     '));
insert into Hackers(hacker_id,name) values (trim('1728'),trim('Nancy     '));
insert into Hackers(hacker_id,name) values (trim('1731'),trim('Andrew    '));
insert into Hackers(hacker_id,name) values (trim('1741'),trim('Keith     '));
insert into Hackers(hacker_id,name) values (trim('1766'),trim('Benjamin  '));
insert into Hackers(hacker_id,name) values (trim('1772'),trim('Charles   '));
insert into Hackers(hacker_id,name) values (trim('1784'),trim('Alan      '));
insert into Hackers(hacker_id,name) values (trim('1786'),trim('Tammy     '));
insert into Hackers(hacker_id,name) values (trim('1842'),trim('Anna      '));
insert into Hackers(hacker_id,name) values (trim('1870'),trim('James     '));
insert into Hackers(hacker_id,name) values (trim('1883'),trim('Robin     '));
insert into Hackers(hacker_id,name) values (trim('1893'),trim('Jean      '));
insert into Hackers(hacker_id,name) values (trim('1903'),trim('Andrew    '));
insert into Hackers(hacker_id,name) values (trim('1925'),trim('Roy       '));
insert into Hackers(hacker_id,name) values (trim('1963'),trim('Diana     '));
insert into Hackers(hacker_id,name) values (trim('1970'),trim('Christina '));
insert into Hackers(hacker_id,name) values (trim('1978'),trim('Jesse     '));
insert into Hackers(hacker_id,name) values (trim('1983'),trim('Joyce     '));
insert into Hackers(hacker_id,name) values (trim('1996'),trim('Patricia  '));
insert into Hackers(hacker_id,name) values (trim('1998'),trim('Gregory   '));
insert into Hackers(hacker_id,name) values (trim('2002'),trim('Brian     '));
insert into Hackers(hacker_id,name) values (trim('2007'),trim('Christine '));
insert into Hackers(hacker_id,name) values (trim('2008'),trim('Lillian   '));
insert into Hackers(hacker_id,name) values (trim('2019'),trim('Aaron     '));
insert into Hackers(hacker_id,name) values (trim('2026'),trim('Dorothy   '));
insert into Hackers(hacker_id,name) values (trim('2038'),trim('Christophe'));r
insert into Hackers(hacker_id,name) values (trim('2083'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('2135'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('2181'),trim('Gerald    '));
insert into Hackers(hacker_id,name) values (trim('2182'),trim('Carol     '));
insert into Hackers(hacker_id,name) values (trim('2190'),trim('Jeremy    '));
insert into Hackers(hacker_id,name) values (trim('2191'),trim('Clarence  '));
insert into Hackers(hacker_id,name) values (trim('2239'),trim('Wayne     '));
insert into Hackers(hacker_id,name) values (trim('2245'),trim('Carolyn   '));
insert into Hackers(hacker_id,name) values (trim('2249'),trim('Margaret  '));
insert into Hackers(hacker_id,name) values (trim('2255'),trim('Andrew    '));
insert into Hackers(hacker_id,name) values (trim('2257'),trim('Albert    '));
insert into Hackers(hacker_id,name) values (trim('2262'),trim('Judy      '));
insert into Hackers(hacker_id,name) values (trim('2342'),trim('Arthur    '));
insert into Hackers(hacker_id,name) values (trim('2354'),trim('Cynthia   '));
insert into Hackers(hacker_id,name) values (trim('2381'),trim('Jerry     '));
insert into Hackers(hacker_id,name) values (trim('2382'),trim('Thomas    '));
insert into Hackers(hacker_id,name) values (trim('2404'),trim('Elizabeth '));
insert into Hackers(hacker_id,name) values (trim('2439'),trim('Justin    '));
insert into Hackers(hacker_id,name) values (trim('2453'),trim('Albert    '));
insert into Hackers(hacker_id,name) values (trim('2536'),trim('James     '));
insert into Hackers(hacker_id,name) values (trim('2563'),trim('Stephen   '));
insert into Hackers(hacker_id,name) values (trim('2568'),trim('Alan      '));
insert into Hackers(hacker_id,name) values (trim('2568'),trim('Joshua    '));
insert into Hackers(hacker_id,name) values (trim('2575'),trim('Norma     '));
insert into Hackers(hacker_id,name) values (trim('2599'),trim('Mildred   '));
insert into Hackers(hacker_id,name) values (trim('2633'),trim('Melissa   '));
insert into Hackers(hacker_id,name) values (trim('2680'),trim('Paul      '));
insert into Hackers(hacker_id,name) values (trim('2707'),trim('Gerald    '));
insert into Hackers(hacker_id,name) values (trim('2725'),trim('Ronald    '));
insert into Hackers(hacker_id,name) values (trim('2727'),trim('Sandra    '));
insert into Hackers(hacker_id,name) values (trim('2779'),trim('Helen     '));
insert into Hackers(hacker_id,name) values (trim('2780'),trim('Larry     '));
insert into Hackers(hacker_id,name) values (trim('2818'),trim('Alan      '));
insert into Hackers(hacker_id,name) values (trim('2876'),trim('Paul      '));
insert into Hackers(hacker_id,name) values (trim('2880'),trim('Chris     '));
insert into Hackers(hacker_id,name) values (trim('2887'),trim('Steven    '));
insert into Hackers(hacker_id,name) values (trim('2924'),trim('Jennifer  '));
insert into Hackers(hacker_id,name) values (trim('2934'),trim('Bonnie    '));
insert into Hackers(hacker_id,name) values (trim('2942'),trim('Shirley   '));
insert into Hackers(hacker_id,name) values (trim('2948'),trim('Jeffrey   '));
insert into Hackers(hacker_id,name) values (trim('2954'),trim('Janet     '));
insert into Hackers(hacker_id,name) values (trim('2959'),trim('Albert    '));
insert into Hackers(hacker_id,name) values (trim('2984'),trim('Charles   '));
insert into Hackers(hacker_id,name) values (trim('2998'),trim('Kelly     '));
insert into Hackers(hacker_id,name) values (trim('3013'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('3040'),trim('Elizabeth '));
insert into Hackers(hacker_id,name) values (trim('3067'),trim('Keith     '));
insert into Hackers(hacker_id,name) values (trim('3077'),trim('Jose      '));
insert into Hackers(hacker_id,name) values (trim('3089'),trim('Ann       '));
insert into Hackers(hacker_id,name) values (trim('3090'),trim('Helen     '));
insert into Hackers(hacker_id,name) values (trim('3125'),trim('Jason     '));
insert into Hackers(hacker_id,name) values (trim('3126'),trim('Gerald    '));
insert into Hackers(hacker_id,name) values (trim('3142'),trim('Carlos    '));
insert into Hackers(hacker_id,name) values (trim('3146'),trim('Ryan      '));
insert into Hackers(hacker_id,name) values (trim('3177'),trim('Ashley    '));
insert into Hackers(hacker_id,name) values (trim('3187'),trim('Julia     '));
insert into Hackers(hacker_id,name) values (trim('3195'),trim('Harry     '));
insert into Hackers(hacker_id,name) values (trim('3206'),trim('Sean      '));
insert into Hackers(hacker_id,name) values (trim('3236'),trim('Julia     '));
insert into Hackers(hacker_id,name) values (trim('3240'),trim('Marilyn   '));
insert into Hackers(hacker_id,name) values (trim('3273'),trim('Cheryl    '));
insert into Hackers(hacker_id,name) values (trim('3279'),trim('Susan     '));
insert into Hackers(hacker_id,name) values (trim('3281'),trim('Judith    '));
insert into Hackers(hacker_id,name) values (trim('3306'),trim('Ruth      '));
insert into Hackers(hacker_id,name) values (trim('3317'),trim('Jane      '));
insert into Hackers(hacker_id,name) values (trim('3327'),trim('Sara      '));
insert into Hackers(hacker_id,name) values (trim('3348'),trim('Denise    '));
insert into Hackers(hacker_id,name) values (trim('3362'),trim('Jason     '));
insert into Hackers(hacker_id,name) values (trim('3371'),trim('Rose      '));
insert into Hackers(hacker_id,name) values (trim('3378'),trim('Susan     '));
insert into Hackers(hacker_id,name) values (trim('3418'),trim('Irene     '));
insert into Hackers(hacker_id,name) values (trim('3438'),trim('Jonathan  '));
insert into Hackers(hacker_id,name) values (trim('3570'),trim('Shawn     '));
insert into Hackers(hacker_id,name) values (trim('3612'),trim('Julia     '));
insert into Hackers(hacker_id,name) values (trim('3655'),trim('Linda     '));
insert into Hackers(hacker_id,name) values (trim('3656'),trim('Melissa   '));
insert into Hackers(hacker_id,name) values (trim('3660'),trim('Dennis    '));
insert into Hackers(hacker_id,name) values (trim('3706'),trim('Jeremy    '));
insert into Hackers(hacker_id,name) values (trim('3706'),trim('Patrick   '));
insert into Hackers(hacker_id,name) values (trim('3709'),trim('Jennifer  '));
insert into Hackers(hacker_id,name) values (trim('3731'),trim('Lillian   '));
insert into Hackers(hacker_id,name) values (trim('3733'),trim('Charles   '));
insert into Hackers(hacker_id,name) values (trim('3764'),trim('Philip    '));
insert into Hackers(hacker_id,name) values (trim('3776'),trim('Jimmy     '));
insert into Hackers(hacker_id,name) values (trim('3803'),trim('Doris     '));
insert into Hackers(hacker_id,name) values (trim('3812'),trim('Craig     '));
insert into Hackers(hacker_id,name) values (trim('3831'),trim('Walter    '));
insert into Hackers(hacker_id,name) values (trim('3850'),trim('Wayne     '));
insert into Hackers(hacker_id,name) values (trim('3854'),trim('Katherine '));
insert into Hackers(hacker_id,name) values (trim('3882'),trim('Mark      '));
insert into Hackers(hacker_id,name) values (trim('3887'),trim('Barbara   '));
insert into Hackers(hacker_id,name) values (trim('3930'),trim('Mark      '));
insert into Hackers(hacker_id,name) values (trim('3939'),trim('Joe       '));
insert into Hackers(hacker_id,name) values (trim('3958'),trim('Maria     '));
insert into Hackers(hacker_id,name) values (trim('3961'),trim('John      '));
insert into Hackers(hacker_id,name) values (trim('4017'),trim('Brian     '));
insert into Hackers(hacker_id,name) values (trim('4037'),trim('Kimberly  '));
insert into Hackers(hacker_id,name) values (trim('4075'),trim('Bonnie    '));
insert into Hackers(hacker_id,name) values (trim('4079'),trim('Terry     '));
insert into Hackers(hacker_id,name) values (trim('4084'),trim('Brian     '));
insert into Hackers(hacker_id,name) values (trim('4103'),trim('Ruby      '));
insert into Hackers(hacker_id,name) values (trim('4109'),trim('Wayne     '));
insert into Hackers(hacker_id,name) values (trim('4115'),trim('Rebecca   '));
insert into Hackers(hacker_id,name) values (trim('4136'),trim('Joyce     '));
insert into Hackers(hacker_id,name) values (trim('4161'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('4163'),trim('Philip    '));
insert into Hackers(hacker_id,name) values (trim('4177'),trim('Lori      '));
insert into Hackers(hacker_id,name) values (trim('4180'),trim('Benjamin  '));
insert into Hackers(hacker_id,name) values (trim('4226'),trim('Dennis    '));
insert into Hackers(hacker_id,name) values (trim('4227'),trim('Sara      '));
insert into Hackers(hacker_id,name) values (trim('4243'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('4246'),trim('Dennis    '));
insert into Hackers(hacker_id,name) values (trim('4246'),trim('Ernest    '));
insert into Hackers(hacker_id,name) values (trim('4285'),trim('Clarence  '));
insert into Hackers(hacker_id,name) values (trim('4324'),trim('Diana     '));
insert into Hackers(hacker_id,name) values (trim('4339'),trim('Steve     '));
insert into Hackers(hacker_id,name) values (trim('4357'),trim('Amy       '));
insert into Hackers(hacker_id,name) values (trim('4359'),trim('Adam      '));
insert into Hackers(hacker_id,name) values (trim('4371'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('4448'),trim('Scott     '));
insert into Hackers(hacker_id,name) values (trim('4486'),trim('Samuel    '));
insert into Hackers(hacker_id,name) values (trim('4501'),trim('Louis     '));
insert into Hackers(hacker_id,name) values (trim('4548'),trim('Jason     '));
insert into Hackers(hacker_id,name) values (trim('4568'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('4577'),trim('Janet     '));
insert into Hackers(hacker_id,name) values (trim('4585'),trim('Clarence  '));
insert into Hackers(hacker_id,name) values (trim('4597'),trim('Dorothy   '));
insert into Hackers(hacker_id,name) values (trim('4614'),trim('Sharon    '));
insert into Hackers(hacker_id,name) values (trim('4618'),trim('Brandon   '));
insert into Hackers(hacker_id,name) values (trim('4646'),trim('Timothy   '));
insert into Hackers(hacker_id,name) values (trim('4660'),trim('Christina '));
insert into Hackers(hacker_id,name) values (trim('4696'),trim('Barbara   '));
insert into Hackers(hacker_id,name) values (trim('4706'),trim('Jose      '));
insert into Hackers(hacker_id,name) values (trim('4715'),trim('Kelly     '));
insert into Hackers(hacker_id,name) values (trim('4779'),trim('Paul      '));
insert into Hackers(hacker_id,name) values (trim('4782'),trim('Clarence  '));
insert into Hackers(hacker_id,name) values (trim('4792'),trim('Lillian   '));
insert into Hackers(hacker_id,name) values (trim('4847'),trim('Christine '));
insert into Hackers(hacker_id,name) values (trim('4896'),trim('Russell   '));
insert into Hackers(hacker_id,name) values (trim('4902'),trim('Marie     '));
insert into Hackers(hacker_id,name) values (trim('4926'),trim('Richard   '));
insert into Hackers(hacker_id,name) values (trim('4935'),trim('Kenneth   '));
insert into Hackers(hacker_id,name) values (trim('4969'),trim('Judy      '));
insert into Hackers(hacker_id,name) values (trim('4976'),trim('Arthur    '));
insert into Hackers(hacker_id,name) values (trim('5023'),trim('Lori      '));
insert into Hackers(hacker_id,name) values (trim('5023'),trim('Scott     '));
insert into Hackers(hacker_id,name) values (trim('5056'),trim('Brian     '));
insert into Hackers(hacker_id,name) values (trim('5079'),trim('Larry     '));
insert into Hackers(hacker_id,name) values (trim('5181'),trim('Karen     '));
insert into Hackers(hacker_id,name) values (trim('5205'),trim('Steve     '));
insert into Hackers(hacker_id,name) values (trim('5235'),trim('Teresa    '));
insert into Hackers(hacker_id,name) values (trim('5246'),trim('Nicholas  '));
insert into Hackers(hacker_id,name) values (trim('5246'),trim('Robin     '));
insert into Hackers(hacker_id,name) values (trim('5264'),trim('Bruce     '));
insert into Hackers(hacker_id,name) values (trim('5278'),trim('Harry     '));
insert into Hackers(hacker_id,name) values (trim('5285'),trim('Harold    '));
insert into Hackers(hacker_id,name) values (trim('5291'),trim('Richard   '));
insert into Hackers(hacker_id,name) values (trim('5296'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('5299'),trim('Deborah   '));
insert into Hackers(hacker_id,name) values (trim('5345'),trim('Jeffrey   '));
insert into Hackers(hacker_id,name) values (trim('5346'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('5359'),trim('Rose      '));
insert into Hackers(hacker_id,name) values (trim('5376'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('5378'),trim('Brian     '));
insert into Hackers(hacker_id,name) values (trim('5401'),trim('Carolyn   '));
insert into Hackers(hacker_id,name) values (trim('5404'),trim('Denise    '));
insert into Hackers(hacker_id,name) values (trim('5446'),trim('Janet     '));
insert into Hackers(hacker_id,name) values (trim('5448'),trim('Kathy     '));
insert into Hackers(hacker_id,name) values (trim('5448'),trim('Catherine '));
insert into Hackers(hacker_id,name) values (trim('5451'),trim('Paula     '));
insert into Hackers(hacker_id,name) values (trim('5472'),trim('Sara      '));
insert into Hackers(hacker_id,name) values (trim('5511'),trim('Thomas    '));
insert into Hackers(hacker_id,name) values (trim('5519'),trim('Daniel    '));
insert into Hackers(hacker_id,name) values (trim('5541'),trim('Amy       '));
insert into Hackers(hacker_id,name) values (trim('5550'),trim('Kenneth   '));
insert into Hackers(hacker_id,name) values (trim('5567'),trim('Jerry     '));
insert into Hackers(hacker_id,name) values (trim('5572'),trim('Randy     '));
insert into Hackers(hacker_id,name) values (trim('5603'),trim('Teresa    '));
insert into Hackers(hacker_id,name) values (trim('5610'),trim('Kelly     '));
insert into Hackers(hacker_id,name) values (trim('5633'),trim('Jose      '));
insert into Hackers(hacker_id,name) values (trim('5719'),trim('Beverly   '));
insert into Hackers(hacker_id,name) values (trim('5723'),trim('Arthur    '));
insert into Hackers(hacker_id,name) values (trim('5755'),trim('Melissa   '));
insert into Hackers(hacker_id,name) values (trim('5770'),trim('Earl      '));
insert into Hackers(hacker_id,name) values (trim('5779'),trim('Ryan      '));
insert into Hackers(hacker_id,name) values (trim('5779'),trim('Margaret  '));
insert into Hackers(hacker_id,name) values (trim('5787'),trim('Diana     '));
insert into Hackers(hacker_id,name) values (trim('5797'),trim('Nicholas  '));
insert into Hackers(hacker_id,name) values (trim('5808'),trim('Debra     '));
insert into Hackers(hacker_id,name) values (trim('5816'),trim('David     '));
insert into Hackers(hacker_id,name) values (trim('5820'),trim('Nicole    '));
insert into Hackers(hacker_id,name) values (trim('5835'),trim('Kevin     '));
insert into Hackers(hacker_id,name) values (trim('5854'),trim('Rachel    '));
insert into Hackers(hacker_id,name) values (trim('5889'),trim('Janet     '));
insert into Hackers(hacker_id,name) values (trim('5945'),trim('Virginia  '));
insert into Hackers(hacker_id,name) values (trim('5952'),trim('Philip    '));
insert into Hackers(hacker_id,name) values (trim('5974'),trim('Shirley   '));
insert into Hackers(hacker_id,name) values (trim('5987'),trim('Martin    '));
insert into Hackers(hacker_id,name) values (trim('5989'),trim('Martha    '));
insert into Hackers(hacker_id,name) values (trim('6007'),trim('Rachel    '));
insert into Hackers(hacker_id,name) values (trim('6017'),trim('Brian     '));
insert into Hackers(hacker_id,name) values (trim('6100'),trim('Philip    '));
insert into Hackers(hacker_id,name) values (trim('6109'),trim('Mark      '));
insert into Hackers(hacker_id,name) values (trim('6110'),trim('Kenneth   '));
insert into Hackers(hacker_id,name) values (trim('6120'),trim('Lillian   '));
insert into Hackers(hacker_id,name) values (trim('6171'),trim('Lawrence  '));
insert into Hackers(hacker_id,name) values (trim('6176'),trim('Marie     '));
insert into Hackers(hacker_id,name) values (trim('6187'),trim('Earl      '));
insert into Hackers(hacker_id,name) values (trim('6198'),trim('Brenda    '));
insert into Hackers(hacker_id,name) values (trim('6225'),trim('Sean      '));
insert into Hackers(hacker_id,name) values (trim('6256'),trim('Donald    '));
insert into Hackers(hacker_id,name) values (trim('6285'),trim('Anna      '));
insert into Hackers(hacker_id,name) values (trim('6302'),trim('Frances   '));
insert into Hackers(hacker_id,name) values (trim('6310'),trim('Mark      '));
insert into Hackers(hacker_id,name) values (trim('6326'),trim('Dorothy   '));
insert into Hackers(hacker_id,name) values (trim('6337'),trim('Bruce     '));
insert into Hackers(hacker_id,name) values (trim('6346'),trim('Stephanie '));
insert into Hackers(hacker_id,name) values (trim('6363'),trim('Lawrence  '));
insert into Hackers(hacker_id,name) values (trim('6368'),trim('Randy     '));
insert into Hackers(hacker_id,name) values (trim('6373'),trim('Sarah     '));
insert into Hackers(hacker_id,name) values (trim('6380'),trim('Carolyn   '));
insert into Hackers(hacker_id,name) values (trim('6396'),trim('Anna      '));
insert into Hackers(hacker_id,name) values (trim('6403'),trim('Craig     '));
insert into Hackers(hacker_id,name) values (trim('6434'),trim('Virginia  '));
insert into Hackers(hacker_id,name) values (trim('6439'),trim('Nicholas  '));
insert into Hackers(hacker_id,name) values (trim('6488'),trim('Roy       '));
insert into Hackers(hacker_id,name) values (trim('6517'),trim('Janice    '));
insert into Hackers(hacker_id,name) values (trim('6527'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('6574'),trim('Charles   '));
insert into Hackers(hacker_id,name) values (trim('6584'),trim('Thomas    '));
insert into Hackers(hacker_id,name) values (trim('6598'),trim('Karen     '));
insert into Hackers(hacker_id,name) values (trim('6638'),trim('Harry     '));
insert into Hackers(hacker_id,name) values (trim('6644'),trim('Carl      '));
insert into Hackers(hacker_id,name) values (trim('6645'),trim('Stephen   '));
insert into Hackers(hacker_id,name) values (trim('6655'),trim('Elizabeth '));
insert into Hackers(hacker_id,name) values (trim('6664'),trim('Shirley   '));
insert into Hackers(hacker_id,name) values (trim('6665'),trim('Matthew   '));
insert into Hackers(hacker_id,name) values (trim('6730'),trim('Paula     '));
insert into Hackers(hacker_id,name) values (trim('6739'),trim('Chris     '));
insert into Hackers(hacker_id,name) values (trim('6753'),trim('Stephen   '));
insert into Hackers(hacker_id,name) values (trim('6817'),trim('Gloria    '));
insert into Hackers(hacker_id,name) values (trim('6818'),trim('George    '));
insert into Hackers(hacker_id,name) values (trim('6856'),trim('Joan      '));
insert into Hackers(hacker_id,name) values (trim('6864'),trim('Paula     '));
insert into Hackers(hacker_id,name) values (trim('6886'),trim('Frank     '));
insert into Hackers(hacker_id,name) values (trim('6938'),trim('Brandon   '));
insert into Hackers(hacker_id,name) values (trim('6947'),trim('Michelle  '));
insert into Hackers(hacker_id,name) values (trim('7049'),trim('Dennis    '));
insert into Hackers(hacker_id,name) values (trim('7091'),trim('Maria     '));
insert into Hackers(hacker_id,name) values (trim('7216'),trim('Doris     '));
insert into Hackers(hacker_id,name) values (trim('7225'),trim('Edward    '));
insert into Hackers(hacker_id,name) values (trim('7231'),trim('Paul      '));
insert into Hackers(hacker_id,name) values (trim('7232'),trim('Julie     '));
insert into Hackers(hacker_id,name) values (trim('7260'),trim('Bobby     '));
insert into Hackers(hacker_id,name) values (trim('7276'),trim('Julie     '));
insert into Hackers(hacker_id,name) values (trim('7286'),trim('Eugene    '));
insert into Hackers(hacker_id,name) values (trim('7301'),trim('Ruby      '));
insert into Hackers(hacker_id,name) values (trim('7317'),trim('Russell   '));
insert into Hackers(hacker_id,name) values (trim('7326'),trim('Jeremy    '));
insert into Hackers(hacker_id,name) values (trim('7327'),trim('Frances   '));
insert into Hackers(hacker_id,name) values (trim('7345'),trim('Ralph     '));
insert into Hackers(hacker_id,name) values (trim('7367'),trim('Linda     '));
insert into Hackers(hacker_id,name) values (trim('7379'),trim('Jessica   '));
insert into Hackers(hacker_id,name) values (trim('7412'),trim('Fred      '));
insert into Hackers(hacker_id,name) values (trim('7428'),trim('Catherine '));
insert into Hackers(hacker_id,name) values (trim('7432'),trim('Pamela    '));
insert into Hackers(hacker_id,name) values (trim('7443'),trim('Eric      '));
insert into Hackers(hacker_id,name) values (trim('7474'),trim('Jeremy    '));
insert into Hackers(hacker_id,name) values (trim('7495'),trim('Rebecca   '));
insert into Hackers(hacker_id,name) values (trim('7505'),trim('John      '));
insert into Hackers(hacker_id,name) values (trim('7567'),trim('Barbara   '));
insert into Hackers(hacker_id,name) values (trim('7571'),trim('Susan     '));
insert into Hackers(hacker_id,name) values (trim('7602'),trim('Sarah     '));
insert into Hackers(hacker_id,name) values (trim('7631'),trim('Kathryn   '));
insert into Hackers(hacker_id,name) values (trim('7644'),trim('Sarah     '));
insert into Hackers(hacker_id,name) values (trim('7678'),trim('Michelle  '));
insert into Hackers(hacker_id,name) values (trim('7685'),trim('Emily     '));
insert into Hackers(hacker_id,name) values (trim('7710'),trim('Diana     '));
insert into Hackers(hacker_id,name) values (trim('7716'),trim('Jose      '));
insert into Hackers(hacker_id,name) values (trim('7717'),trim('Mildred   '));
insert into Hackers(hacker_id,name) values (trim('7781'),trim('Theresa   '));
insert into Hackers(hacker_id,name) values (trim('7786'),trim('Jeremy    '));
insert into Hackers(hacker_id,name) values (trim('7809'),trim('Beverly   '));
insert into Hackers(hacker_id,name) values (trim('7857'),trim('Jennifer  '));
insert into Hackers(hacker_id,name) values (trim('7861'),trim('Phyllis   '));
insert into Hackers(hacker_id,name) values (trim('7861'),trim('Kathryn   '));
insert into Hackers(hacker_id,name) values (trim('7917'),trim('Roy       '));
insert into Hackers(hacker_id,name) values (trim('7961'),trim('Tina      '));
insert into Hackers(hacker_id,name) values (trim('7973'),trim('Anne      '));
insert into Hackers(hacker_id,name) values (trim('8000'),trim('Carolyn   '));
insert into Hackers(hacker_id,name) values (trim('8049'),trim('Nicholas  '));
insert into Hackers(hacker_id,name) values (trim('8056'),trim('Nicholas  '));
insert into Hackers(hacker_id,name) values (trim('8066'),trim('Ralph     '));
insert into Hackers(hacker_id,name) values (trim('8112'),trim('Michael   '));
insert into Hackers(hacker_id,name) values (trim('8150'),trim('Deborah   '));
insert into Hackers(hacker_id,name) values (trim('8155'),trim('Alan      '));
insert into Hackers(hacker_id,name) values (trim('8158'),trim('Julia     '));
insert into Hackers(hacker_id,name) values (trim('8165'),trim('Albert    '));
insert into Hackers(hacker_id,name) values (trim('8210'),trim('Brenda    '));
insert into Hackers(hacker_id,name) values (trim('8219'),trim('Frances   '));
insert into Hackers(hacker_id,name) values (trim('8228'),trim('Denise    '));
insert into Hackers(hacker_id,name) values (trim('8253'),trim('Mark      '));
insert into Hackers(hacker_id,name) values (trim('8299'),trim('Bonnie    '));
insert into Hackers(hacker_id,name) values (trim('8304'),trim('Ralph     '));
insert into Hackers(hacker_id,name) values (trim('8318'),trim('Howard    '));
insert into Hackers(hacker_id,name) values (trim('8330'),trim('Roy       '));
insert into Hackers(hacker_id,name) values (trim('8340'),trim('Roy       '));
insert into Hackers(hacker_id,name) values (trim('8372'),trim('Christina '));
insert into Hackers(hacker_id,name) values (trim('8382'),trim('Steve     '));
insert into Hackers(hacker_id,name) values (trim('8408'),trim('Johnny    '));
insert into Hackers(hacker_id,name) values (trim('8442'),trim('Cynthia   '));
insert into Hackers(hacker_id,name) values (trim('8453'),trim('Walter    '));
insert into Hackers(hacker_id,name) values (trim('8465'),trim('Sharon    '));
insert into Hackers(hacker_id,name) values (trim('8470'),trim('Earl      '));
insert into Hackers(hacker_id,name) values (trim('8473'),trim('Alan      '));
insert into Hackers(hacker_id,name) values (trim('8493'),trim('Judy      '));
insert into Hackers(hacker_id,name) values (trim('8509'),trim('Matthew   '));
insert into Hackers(hacker_id,name) values (trim('8583'),trim('Julie     '));
insert into Hackers(hacker_id,name) values (trim('8607'),trim('Jerry     '));
insert into Hackers(hacker_id,name) values (trim('8608'),trim('Diane     '));
insert into Hackers(hacker_id,name) values (trim('8612'),trim('Evelyn    '));
insert into Hackers(hacker_id,name) values (trim('8613'),trim('Dennis    '));
insert into Hackers(hacker_id,name) values (trim('8614'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('8620'),trim('Martha    '));
insert into Hackers(hacker_id,name) values (trim('8628'),trim('Beverly   '));
insert into Hackers(hacker_id,name) values (trim('8641'),trim('Mark      '));
insert into Hackers(hacker_id,name) values (trim('8659'),trim('Samuel    '));
insert into Hackers(hacker_id,name) values (trim('8693'),trim('Janet     '));
insert into Hackers(hacker_id,name) values (trim('8704'),trim('Craig     '));
insert into Hackers(hacker_id,name) values (trim('8711'),trim('Howard    '));
insert into Hackers(hacker_id,name) values (trim('8730'),trim('Kathleen  '));
insert into Hackers(hacker_id,name) values (trim('8752'),trim('Norma     '));
insert into Hackers(hacker_id,name) values (trim('8754'),trim('Wayne     '));
insert into Hackers(hacker_id,name) values (trim('8756'),trim('Phyllis   '));
insert into Hackers(hacker_id,name) values (trim('8758'),trim('Jimmy     '));
insert into Hackers(hacker_id,name) values (trim('8786'),trim('Jerry     '));
insert into Hackers(hacker_id,name) values (trim('8788'),trim('Gregory   '));
insert into Hackers(hacker_id,name) values (trim('8806'),trim('Jean      '));
insert into Hackers(hacker_id,name) values (trim('8808'),trim('Anna      '));
insert into Hackers(hacker_id,name) values (trim('8808'),trim('Alan      '));
insert into Hackers(hacker_id,name) values (trim('8853'),trim('Steve     '));
insert into Hackers(hacker_id,name) values (trim('8885'),trim('Bruce     '));
insert into Hackers(hacker_id,name) values (trim('8887'),trim('Douglas   '));
insert into Hackers(hacker_id,name) values (trim('8888'),trim('Antonio   '));
insert into Hackers(hacker_id,name) values (trim('8895'),trim('Jeremy    '));
insert into Hackers(hacker_id,name) values (trim('8929'),trim('Willie    '));
insert into Hackers(hacker_id,name) values (trim('8951'),trim('Jeffrey   '));
insert into Hackers(hacker_id,name) values (trim('8981'),trim('Jane      '));
insert into Hackers(hacker_id,name) values (trim('8986'),trim('Larry     '));
insert into Hackers(hacker_id,name) values (trim('8990'),trim('Katherine '));
insert into Hackers(hacker_id,name) values (trim('8999'),trim('Martin    '));
insert into Hackers(hacker_id,name) values (trim('9012'),trim('Jesse     '));
insert into Hackers(hacker_id,name) values (trim('9014'),trim('Shawn     '));
insert into Hackers(hacker_id,name) values (trim('9016'),trim('Jack      '));
insert into Hackers(hacker_id,name) values (trim('9026'),trim('Edward    '));
insert into Hackers(hacker_id,name) values (trim('9027'),trim('Joyce     '));
insert into Hackers(hacker_id,name) values (trim('9036'),trim('Christina '));
insert into Hackers(hacker_id,name) values (trim('9076'),trim('Doris     '));
insert into Hackers(hacker_id,name) values (trim('9080'),trim('Cynthia   '));
insert into Hackers(hacker_id,name) values (trim('9162'),trim('Debra     '));
insert into Hackers(hacker_id,name) values (trim('9177'),trim('Harold    '));
insert into Hackers(hacker_id,name) values (trim('9223'),trim('Shirley   '));
insert into Hackers(hacker_id,name) values (trim('9226'),trim('Joyce     '));
insert into Hackers(hacker_id,name) values (trim('9253'),trim('Justin    '));
insert into Hackers(hacker_id,name) values (trim('9287'),trim('Harold    '));
insert into Hackers(hacker_id,name) values (trim('9290'),trim('Amy       '));
insert into Hackers(hacker_id,name) values (trim('9292'),trim('Louis     '));
insert into Hackers(hacker_id,name) values (trim('9301'),trim('Tina      '));
insert into Hackers(hacker_id,name) values (trim('9308'),trim('Laura     '));
insert into Hackers(hacker_id,name) values (trim('9331'),trim('Keith     '));
insert into Hackers(hacker_id,name) values (trim('9427'),trim('Dennis    '));
insert into Hackers(hacker_id,name) values (trim('9433'),trim('Lillian   '));
insert into Hackers(hacker_id,name) values (trim('9467'),trim('Patrick   '));
insert into Hackers(hacker_id,name) values (trim('9474'),trim('Adam      '));
insert into Hackers(hacker_id,name) values (trim('9498'),trim('Clarence  '));
insert into Hackers(hacker_id,name) values (trim('9501'),trim('Victor    '));
insert into Hackers(hacker_id,name) values (trim('9513'),trim('Lawrence  '));
insert into Hackers(hacker_id,name) values (trim('9538'),trim('Nicholas  '));
insert into Hackers(hacker_id,name) values (trim('9543'),trim('George    '));
insert into Hackers(hacker_id,name) values (trim('9580'),trim('Charles   '));
insert into Hackers(hacker_id,name) values (trim('9582'),trim('Christine '));
insert into Hackers(hacker_id,name) values (trim('9600'),trim('Russell   '));
insert into Hackers(hacker_id,name) values (trim('9652'),trim('Christine '));
insert into Hackers(hacker_id,name) values (trim('9657'),trim('Linda     '));
insert into Hackers(hacker_id,name) values (trim('9663'),trim('Carlos    '));
insert into Hackers(hacker_id,name) values (trim('9671'),trim('Emily     '));
insert into Hackers(hacker_id,name) values (trim('9677'),trim('Angela    '));
insert into Hackers(hacker_id,name) values (trim('9690'),trim('Lawrence  '));
insert into Hackers(hacker_id,name) values (trim('9733'),trim('Amy       '));
insert into Hackers(hacker_id,name) values (trim('9735'),trim('Carol     '));
insert into Hackers(hacker_id,name) values (trim('9763'),trim('Nancy     '));
insert into Hackers(hacker_id,name) values (trim('9783'),trim('Gary      '));
insert into Hackers(hacker_id,name) values (trim('9878'),trim('Rose      '));
insert into Hackers(hacker_id,name) values (trim('9910'),trim('Timothy   '));
insert into Hackers(hacker_id,name) values (trim('9916'),trim('Nancy     '));
insert into Hackers(hacker_id,name) values (trim('9938'),trim('Mary      '));
insert into Hackers(hacker_id,name) values (trim('9967'),trim('Joshua    ')); 
```

### Solution

```SQL

SELECT a.X, a.Y
FROM FUNCTIONS A, FUNCTIONS B
WHERE b.y = a.x 
and b.x = a.y
and a.y >= a.x
GROUP BY a.X, a.Y
having count(*) > 1 or a.y>a.x
order by a.x asc;

```

### Results

```SQL

2 24 
4 22 
5 21 
6 20 
8 18 
9 17 
11 15
13 13

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
