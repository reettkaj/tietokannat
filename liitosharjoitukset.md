# Relaatiotietokannan peruskäsitteiden harjoitukset
###1
5
![image](https://github.com/user-attachments/assets/c84025c9-b8b2-4fc5-ab26-40b7a0425a99)

###2
4
![image](https://github.com/user-attachments/assets/5a518584-9d4e-41ab-911e-b875f0b6fb65)

###3
ident
![image](https://github.com/user-attachments/assets/944dfc0e-710e-43b0-9511-e86d6f227122)

###4
varchar
![image](https://github.com/user-attachments/assets/d57f69af-7fe2-4c9b-ba47-e3e62c907377)

###5
iso_country
![image](https://github.com/user-attachments/assets/bfb80e15-ee91-4fe0-956f-f7f51a058cf7)

###6
country
![image](https://github.com/user-attachments/assets/e5e3fcdc-ea0d-403c-87f5-71c3c2133f62)

###7
country
![image](https://github.com/user-attachments/assets/37e845f5-7bd2-4262-a289-eb505ca0de47)

###8
char
![image](https://github.com/user-attachments/assets/14c14be8-07dd-445d-aaab-432af2272e96)

###9
70942
![image](https://github.com/user-attachments/assets/ba144489-392c-46d6-a2dd-cfc4fdc587b7)

###10
iso country
![image](https://github.com/user-attachments/assets/7ce451aa-2cb0-41d1-8672-68328eceea27)

###11
char
![image](https://github.com/user-attachments/assets/15696268-a992-4503-bf00-8796f25f7acb)

###12
248
![image](https://github.com/user-attachments/assets/eee23ab7-a673-4fc8-8f8b-41264b94cb36)

###13
name
![image](https://github.com/user-attachments/assets/79f422c1-71c1-4a8c-9e89-28f2f5c1bc70)


###14
3
![image](https://github.com/user-attachments/assets/905f96ef-fe85-4953-aef1-ecd4456a2475)

###15
id
![image](https://github.com/user-attachments/assets/fe12e63d-d23b-422b-a426-447f047b5437)

###16
epätosi
![image](https://github.com/user-attachments/assets/b2630e34-7163-43c6-8fc7-1525da64d47b)

###17
game
![image](https://github.com/user-attachments/assets/42b39ba5-91ed-4dab-86b6-01933de46004)

###18
game
![image](https://github.com/user-attachments/assets/1ee1dae7-fc49-4e7f-8559-fab86efaf69a)

###19
game
![image](https://github.com/user-attachments/assets/80f9afdc-a74f-4aca-8951-2fae6ecd8a56)

###20
airport
![image](https://github.com/user-attachments/assets/0580497e-9d82-44db-9692-617dca73237d)

###21
id
![image](https://github.com/user-attachments/assets/b4035f05-cf9d-49fd-9854-066cf6559ace)

###22
airport
![image](https://github.com/user-attachments/assets/c9630b02-a4e7-4e85-bfc3-e3c2d52995b9)

###23
airport
![image](https://github.com/user-attachments/assets/ffdcf10b-cb74-4d60-89c1-35d100d81b62)

###24
goal, game
![image](https://github.com/user-attachments/assets/0eb21220-4f14-409d-b5b4-645be0871837)

###25
2
![image](https://github.com/user-attachments/assets/6212bfdd-a29f-4d4e-812d-56eeb4ee9514)

# Yhteen tauluun kohdistuvien kyselyiden harjoitukset

###1
select * from goal;
![image](https://github.com/user-attachments/assets/d648f1d5-dab3-4aa2-814d-ca333f706eaf)

###2
select name, type from airports where iso_country = 'FI';
![image](https://github.com/user-attachments/assets/712b33ac-f219-4ee4-acdf-30fb4a7b7d3d)

###3
select name from airports where iso_country = 'FI' order by name asc;
![image](https://github.com/user-attachments/assets/4d138b48-f413-4fa3-9b1d-f60050c5bdd7)

###4
select name, type from airports where so_country = 'FI' order by type asc, name asc;
![image](https://github.com/user-attachments/assets/2b72d32d-df92-484f-a62e-3b1e73f03163)
![image](https://github.com/user-attachments/assets/29c4d241-2b04-49eb-b2a2-f085f069f558)

###5
select name from country where name like 'f%'';
![image](https://github.com/user-attachments/assets/cb6bdea1-4118-4517-98da-db7dbc4255af)

###6
select name from country where name like '%f%';
![image](https://github.com/user-attachments/assets/4c2673dd-cb32-4d81-83c9-c0383ff826c4)

###7
select location from game where screen_name = 'Vesa';
![image](https://github.com/user-attachments/assets/f386cc3e-7e6b-4735-a532-5c7743e309be)

###8
select co2_consumed from game where screen_name = 'Ilkka';
![image](https://github.com/user-attachments/assets/bdf7f6df-dc4b-46c5-9d62-f16c84543aa4)

###9
select distinct co2_budget from game;
![image](https://github.com/user-attachments/assets/038272dd-12c7-48c5-9358-1e493db428a6)

# Where-osan liitosehto harjoitukset

###1
select iso_country.name as "country name", airport.name as "airport name"
from airport
join iso_country on airport.iso_country = iso.country_name
where iso_country.name = "Iceland";
![image](https://github.com/user-attachments/assets/d2c06b7a-f9d0-4ab8-9925-866ad5d679b2)

###2
select airport.name as "airport name"
from airport
join iso_country on airport.iso_country = iso_country.name
where iso_country.name = "France" and airport.type 'large_airport';
![image](https://github.com/user-attachments/assets/aa7c84eb-4870-41ed-adbb-6b33632c6701)

###3
select iso_country.name as country_name and airport.name as airport_name
from airport
join iso_country from airport.iso_country = iso_country.name
where airport.continent = 'AN';
![image](https://github.com/user-attachments/assets/a97ad4d1-ef67-4979-8eb9-f03068874930)

###4
select elevation_ft
from airport, game
where location = ident and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/90aaa41f-1dfc-4fec-9fc6-114834218175)

###5
select elevation_ft * 0,3048 as elevation_m
from airport, game
where location = ident and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/a052d4a7-01f3-4030-baeb-c319a28f9564)

###6
select name
from airport, game
where location = ident and screen_name = "Ilkka"
![image](https://github.com/user-attachments/assets/56986786-348e-4888-854b-b8a96d07b9df)

###7
select country.name
from airport, game, country
where location = ident and airport iso_country = country.iso_country and screen_name = "Ilkka";
![image](https://github.com/user-attachments/assets/9deff0f3-c7f4-4c52-925e-b3da1823675c)
![image](https://github.com/user-attachments/assets/8a910117-ee33-40f1-a627-cd29ab6e540e)

###8
select name
from goal, goal_reached, game
where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
![image](https://github.com/user-attachments/assets/d1dc3fb3-4c8d-44fc-95f2-9dfda13aa69b)

###9
select airport.name
from airport, game, goal, goal_reached
where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS"
![image](https://github.com/user-attachments/assets/c1b4f904-24c1-4046-91fa-30d545e39b46)
![image](https://github.com/user-attachments/assets/3319021d-67f1-4697-b2e5-96bd07c9353f)

###10
select country.name
from airport, country, game, goal, goal_reached
where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS"
![image](https://github.com/user-attachments/assets/a25690c8-196e-47fa-92a2-40392d189ee6)
![image](https://github.com/user-attachments/assets/41fe80af-2a2d-4ac2-82a5-02f150184db4)

# Join harjoitukset
###1
select country.name as "country name" and airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
![image](https://github.com/user-attachments/assets/bc1b015e-ba7f-4f72-be21-b4a88a2f8a64)

###2
select screen_name, airport.name
from game inner join airport on location = ident;
![image](https://github.com/user-attachments/assets/c6dc0fca-90e8-497a-a05b-f3bd476a867c)

###3
select screen_name, country.name
from game inner join airport on location = inner join country on airport.iso_country = country.iso_country;
![image](https://github.com/user-attachments/assets/dc33a0d5-0988-4cb1-b6c6-0d4f47690233)
![image](https://github.com/user-attachments/assets/f6f0ebf4-9d45-475a-9cf0-d752da5e32f8)

###4
select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";
![image](https://github.com/user-attachments/assets/f1f9e857-3669-4934-a489-cc6c742e651a)

###5
select name, screen name
from goal left join goal_reached on goal.id = goal.id left join game on game.id = game_id;
![image](https://github.com/user-attachments/assets/40d69958-cf80-416d-95fc-b931edc75a83)
![image](https://github.com/user-attachments/assets/76fd44bc-f1c3-4103-a964-bd3edecf2678)

where country.name = "Finland" and scheduled_service = "yes";

# sisäkyselyharjoitukset
###1
select name
from country
where iso_country in(select iso_country from airport where name like "Satsuma%");
![image](https://github.com/user-attachments/assets/f6f073bf-9633-44e4-a53d-14e038d3f0dc)

###2
select name
from airport where iso_country in(select iso_country where name "Monaco");
![image](https://github.com/user-attachments/assets/68637686-dccf-46bb-a7ee-360674a51c5d)

###3
select screen_name
from game where id in (select game_id from goal_reached where goal_id in(select id from goal where name = "CLOUDS"));
![image](https://github.com/user-attachments/assets/3e9a2bb8-ac1f-4831-a4ef-fd0c051fa270)
![image](https://github.com/user-attachments/assets/5f830c5c-72b7-4aa3-8b34-726616b4c772)

###4
select name
from country
where iso_country not in (select airport.iso_country from airport);
![image](https://github.com/user-attachments/assets/24b1ba15-bf99-4e6e-bdb4-bf1edaf4f495)

###5
select name
from goal
where id not in (select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name "Heini");
![image](https://github.com/user-attachments/assets/f0ad6ab3-8b6c-4869-9367-87705fd2e873)
![image](https://github.com/user-attachments/assets/6d7dc878-d7e0-4870-bffe-7db8cd861d3c)

# koostetieto kyselyt harjoitukset
###1
select max(elevation_ft)
from airport;
![image](https://github.com/user-attachments/assets/06e667cf-e3da-428b-9b73-630e9fea1df9)

###2
select continent, count(*)
from country
group by continent;
![image](https://github.com/user-attachments/assets/39e7b7cc-0e07-4e3a-a7bc-65883bc56360)

###3
select screen_name, count(*)
from game, goal reached
where id = game_id group by screen_name;
![image](https://github.com/user-attachments/assets/900aff35-ef60-45b8-b1e3-7d9d66d26270)

###4
select screen_name
from game
where co2_consumed in (select min (co2_consumed) from game);
![image](https://github.com/user-attachments/assets/a86b8195-815c-4551-8724-25b28d6ccd31)

###5
select name, count(*)
from country, airport
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;
![image](https://github.com/user-attachments/assets/54827dbc-b7a1-4401-95c0-1723d31a533f)

###6
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;
![image](https://github.com/user-attachments/assets/45e4349c-f5e1-4574-84c3-1c2f2424924b)

###7
select name
from airport
where elevation_ft in (select max(elevation_ft)from airport);
![image](https://github.com/user-attachments/assets/9f14774f-516e-4c10-b212-0d3dfa08369d)

###8
select name
from country
where iso_country in (select iso_country
from airport
where elevation_ft in(select max(elevation_ft) from airport));
![image](https://github.com/user-attachments/assets/20bc71d2-bf3b-4db3-b9f0-8310d55d18bd)

###9
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by scree_name;
![image](https://github.com/user-attachments/assets/74dd6d46-656c-47e8-b7c4-5c8cbe7bce01)

###10
select name
from airport
where latitude.deg in(select min(latitude_deg) from airport);
![image](https://github.com/user-attachments/assets/76134616-d5fd-4848-a216-90c9b4962a7a)

# Päivityskyselyt harjoitukset
###1
update game
set location
set location = (select ident from airport where name = "Nottinghman Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";

select * from game;
![image](https://github.com/user-attachments/assets/1b78d5f5-2eda-4aa9-a83c-dc77e4a9cf93)

###2
goal_reached
![image](https://github.com/user-attachments/assets/79c4e705-6bd0-4338-aea0-4b5e4c23b239)

###3
delete from goal_reached;
select * from goal_reached;
![image](https://github.com/user-attachments/assets/dd2a3981-ead6-4ca3-8a49-86f4c90320da)

###4
delete from game;
select * from game;
![image](https://github.com/user-attachments/assets/df9230e3-bc25-4b78-b451-10e175233e57)

# tietokannan suunnittelu harjoitukset

###1
ident
![image](https://github.com/user-attachments/assets/ef9bba52-b6b4-418f-987e-cc63a8faf486)

###2
airport
![image](https://github.com/user-attachments/assets/8d51a9fc-da3d-46a6-867b-125d1a9c67b6)

###3
maassa voi olla monta lentokenttää
![image](https://github.com/user-attachments/assets/514e05c1-59f8-448c-9b04-72826e5eca39)

###4
tosi
![image](https://github.com/user-attachments/assets/0ef6319d-892f-4eb2-8116-517c9f8c0c11)

###5
epätosi
![image](https://github.com/user-attachments/assets/45879d81-7b6e-41d7-8212-26154840d228)

###6
airport tauluun tulee viiteavain country tauluun
![image](https://github.com/user-attachments/assets/030a64e8-a57e-4147-bf55-dbc0f055cca9)

###7
game tauluun tulee viiteavain airport tauluun
![image](https://github.com/user-attachments/assets/aaf97bf7-14ed-41e9-a26e-60ea5e475b50)

###8
tosi
![image](https://github.com/user-attachments/assets/424121aa-21dd-44c6-88c9-4373b86a2480)

###9
yhteyden salmiakista tulee omaan tauluunsa
![image](https://github.com/user-attachments/assets/e0dab86f-7397-4320-9e82-7642245968e3)

###10
viiteavain sekä goal tauluun että game tauluun
![image](https://github.com/user-attachments/assets/641814b0-47c8-4538-b9ce-28d4ed5f4fca)
