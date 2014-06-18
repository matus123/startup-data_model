startup-data_model
==================

Data model

v subore data_model.png je namodelovany model pre e-shop ako bolo v zadani

Entita "Produkt" obsahuje nazov produkty a jeho ID. Tabulka je spojena s tabulkou "Cena" cez cudzi kluc v tabulke "Cena". Cim sa udrzuje aj historia cien pre dany produkt.

Entita "Objednavka" obsahuje datum kedy bola vytvorena, cudzim klucom na tabulku "Zakaznik" pre zistenie kym bola objednavka vytvorena, a cudzim klucom na tabulku "Kupon" pre zistenie ci bol pouzity kupon pri platbe objednavky.

Objednavka je prepojena cez spajaciu entitu "Produkt_v_objednavke" cim si vedieme zoznam vsetkych produktov pre danu objednavku. V pripade potreby zistenia sumy zaplatanej pri objednavke sa to da zistit pomocou sql dopytov.

Entita "Produkt_v_objednavke" obsahuje cudzie kluce na tabulku "Produkt" a "Objednavku"

Entita "Zakaznik" obsahuje prihlasovaci e-mail a zacryptovane heslo.

Entita "Kupon" obsahuje percentualnu zlavu, Identifikator(SALE2014), Datum splatnosti OD-DO, pocet kolko krat sa moze dany kupon pouzit, a momentalne pouzitie kupona.
