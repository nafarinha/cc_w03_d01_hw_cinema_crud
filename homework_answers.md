## Questions

1.  Return ALL the data in the 'movies' table.
#
	SELECT * FROM movies;
#
		id |                title                | year | show_time
		----+-------------------------------------+------+-----------
		 1 | Iron Man                            | 2008 | 23:10
		 2 | The Incredible Hulk                 | 2008 | 15:55
		 3 | Iron Man 2                          | 2010 | 14:05
		 4 | Thor                                | 2011 | 12:25
		 5 | Captain America: The First Avenger  | 2011 | 14:00
		 6 | Avengers Assemble                   | 2012 | 12:45
		 7 | Iron Man 3                          | 2013 | 12:05
		 8 | Thor: The Dark World                | 2013 | 21:25
		 9 | Batman Begins                       | 2005 | 17:10
		10 | Captain America: The Winter Soldier | 2014 | 19:30
		11 | Guardians of the Galaxy             | 2014 | 12:55
		12 | Avengers: Age of Ultron             | 2015 | 23:40
		13 | Ant-Man                             | 2015 | 19:45
		14 | Captain America: Civil War          | 2016 | 12:45
		15 | Doctor Strange                      | 2016 | 19:05
		16 | Guardians of the Galaxy 2           | 2017 | 21:55
		17 | Spider-Man: Homecoming              | 2017 | 14:05
		18 | Thor: Ragnarok                      | 2017 | 13:05
		19 | Black Panther                       | 2018 | 19:55
		20 | Avengers Infinity War               | 2018 | 18:50
		21 | Ant-Man and the Wasp                | 2018 | 19:55
		(21 rows) 


2.  Return ONLY the name column from the 'people' table
#
	SELECT name FROM people;
#
	name         
	----------------------
	Gábor Budai
	Abigaila Ekiert
	Nuno Farinha
	Ruben Franco Sanchez
	Richard Haigh
	Chika Kanu
	Aaron McFaull
	Craig Morton
	John Polson
	Kiran Qureshi
	Ethan Radcliffe
	Janapoles Ramos
	Gordon Renfrew
	Pauline Rudge
	Martin Selis
	Alex Shing
	Anita Squires
	Anthatony Starkes
	Elisa Sveinsdottir
	Hamish Whyte
	Matthew Woodley
	Emil Zacharczuk
	(22 rows)


3.  Oops! Someone at CodeClan spelled Anthony's name wrong! Change it to reflect the proper spelling ('Anthatony Starkes' should be 'Anthony Starke').
#
	UPDATE people SET name = 'Anthony Starke' WHERE id = 18;
#
	id |         name         
	----+----------------------
	 1 | Gábor Budai
	 2 | Abigaila Ekiert
	 3 | Nuno Farinha
	 4 | Ruben Franco Sanchez
	 5 | Richard Haigh
	 6 | Chika Kanu
	 7 | Aaron McFaull
	 8 | Craig Morton
	 9 | John Polson
	10 | Kiran Qureshi
	11 | Ethan Radcliffe
	12 | Janapoles Ramos
	13 | Gordon Renfrew
	14 | Pauline Rudge
	15 | Martin Selis
	16 | Alex Shing
	17 | Anita Squires
	19 | Elisa Sveinsdottir
	20 | Hamish Whyte
	21 | Matthew Woodley
	22 | Emil Zacharczuk
	18 | Anthony Starke
	(22 rows)


4.  Return ONLY your name from the 'people' table.
#
	SELECT name from people WHERE name LIKE 'Nuno%';
#
	name     
	--------------
	Nuno Farinha
	(1 row)


5.  The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
#
	DELETE FROM movies WHERE title = 'Batman Begins';
#
	id |                title                | year | show_time
	----+-------------------------------------+------+-----------
	 1 | Iron Man                            | 2008 | 23:10
	 2 | The Incredible Hulk                 | 2008 | 15:55
	 3 | Iron Man 2                          | 2010 | 14:05
	 4 | Thor                                | 2011 | 12:25
	 5 | Captain America: The First Avenger  | 2011 | 14:00
	 6 | Avengers Assemble                   | 2012 | 12:45
	 7 | Iron Man 3                          | 2013 | 12:05
	 8 | Thor: The Dark World                | 2013 | 21:25
	10 | Captain America: The Winter Soldier | 2014 | 19:30
	11 | Guardians of the Galaxy             | 2014 | 12:55
	12 | Avengers: Age of Ultron             | 2015 | 23:40
	13 | Ant-Man                             | 2015 | 19:45
	14 | Captain America: Civil War          | 2016 | 12:45
	15 | Doctor Strange                      | 2016 | 19:05
	16 | Guardians of the Galaxy 2           | 2017 | 21:55
	17 | Spider-Man: Homecoming              | 2017 | 14:05
	18 | Thor: Ragnarok                      | 2017 | 13:05
	19 | Black Panther                       | 2018 | 19:55
	20 | Avengers Infinity War               | 2018 | 18:50
	21 | Ant-Man and the Wasp                | 2018 | 19:55
	(20 rows)


6.  Create a new entry in the 'people' table with the name of one of the instructors.
#
	INSERT INTO people (name) VALUES ('Sandy McMillan');
#
	id |         name         
	----+----------------------
	 1 | Gábor Budai
	 2 | Abigaila Ekiert
	 3 | Nuno Farinha
	 4 | Ruben Franco Sanchez
	 5 | Richard Haigh
	 6 | Chika Kanu
	 7 | Aaron McFaull
	 8 | Craig Morton
	 9 | John Polson
	10 | Kiran Qureshi
	11 | Ethan Radcliffe
	12 | Janapoles Ramos
	13 | Gordon Renfrew
	14 | Pauline Rudge
	15 | Martin Selis
	16 | Alex Shing
	17 | Anita Squires
	19 | Elisa Sveinsdottir
	20 | Hamish Whyte
	21 | Matthew Woodley
	22 | Emil Zacharczuk
	18 | Anthony Starke
	23 | Sandy McMillan
	(23 rows)


7.  Craig Morton has decided to hijack our movie evening, remove him from the table of people.
#
	DELETE FROM people WHERE name = 'Craig Morton';
#
	id |         name         
	----+----------------------
	  1 | Gábor Budai
	  2 | Abigaila Ekiert
	  3 | Nuno Farinha
	  4 | Ruben Franco Sanchez
	  5 | Richard Haigh
	  6 | Chika Kanu
	  7 | Aaron McFaull
	  9 | John Polson
	 10 | Kiran Qureshi
	 11 | Ethan Radcliffe
	 12 | Janapoles Ramos
	 13 | Gordon Renfrew
	 14 | Pauline Rudge
	 15 | Martin Selis
	 16 | Alex Shing
	 17 | Anita Squires
	 19 | Elisa Sveinsdottir
	 20 | Hamish Whyte
	 21 | Matthew Woodley
	 22 | Emil Zacharczuk
	 18 | Anthony Starke
	 23 | Sandy McMillan
	(22 rows)
	

8.  The cinema has just heard that they will be holding an exclusive midnight showing of 'Captain Marvel'!! Create a new entry in the 'movies' table to reflect this.
#
	INSERT INTO movies (title, year, show_time) VALUES ('Captain Marvel', 2019, '00:00');
#
	id |                title                | year | show_time
	----+-------------------------------------+------+-----------
	 1 | Iron Man                            | 2008 | 23:10
	 2 | The Incredible Hulk                 | 2008 | 15:55
	 3 | Iron Man 2                          | 2010 | 14:05
	 4 | Thor                                | 2011 | 12:25
	 5 | Captain America: The First Avenger  | 2011 | 14:00
	 6 | Avengers Assemble                   | 2012 | 12:45
	 7 | Iron Man 3                          | 2013 | 12:05
	 8 | Thor: The Dark World                | 2013 | 21:25
	10 | Captain America: The Winter Soldier | 2014 | 19:30
	11 | Guardians of the Galaxy             | 2014 | 12:55
	12 | Avengers: Age of Ultron             | 2015 | 23:40
	13 | Ant-Man                             | 2015 | 19:45
	14 | Captain America: Civil War          | 2016 | 12:45
	15 | Doctor Strange                      | 2016 | 19:05
	16 | Guardians of the Galaxy 2           | 2017 | 21:55
	17 | Spider-Man: Homecoming              | 2017 | 14:05
	18 | Thor: Ragnarok                      | 2017 | 13:05
	19 | Black Panther                       | 2018 | 19:55
	20 | Avengers Infinity War               | 2018 | 18:50
	21 | Ant-Man and the Wasp                | 2018 | 19:55
	22 | Captain Marvel                      | 2019 | 00:00
	(21 rows)
	

9.  The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.
#
	SELECT * FROM movies where title LIKE 'Guardians%';
#
	id |           title           | year | show_time
	----+---------------------------+------+-----------
	11 | Guardians of the Galaxy   | 2014 | 12:55
	16 | Guardians of the Galaxy 2 | 2017 | 21:55
	(2 rows)
#
	UPDATE movies set show_time = '14:55' WHERE id = 16;
	SELECT * FROM movies;
#
	id |                title                | year | show_time
	----+-------------------------------------+------+-----------
	 1 | Iron Man                            | 2008 | 23:10
	 2 | The Incredible Hulk                 | 2008 | 15:55
	 3 | Iron Man 2                          | 2010 | 14:05
	 4 | Thor                                | 2011 | 12:25
	 5 | Captain America: The First Avenger  | 2011 | 14:00
	 6 | Avengers Assemble                   | 2012 | 12:45
	 7 | Iron Man 3                          | 2013 | 12:05
	 8 | Thor: The Dark World                | 2013 | 21:25
	10 | Captain America: The Winter Soldier | 2014 | 19:30
	11 | Guardians of the Galaxy             | 2014 | 12:55
	12 | Avengers: Age of Ultron             | 2015 | 23:40
	13 | Ant-Man                             | 2015 | 19:45
	14 | Captain America: Civil War          | 2016 | 12:45
	15 | Doctor Strange                      | 2016 | 19:05
	17 | Spider-Man: Homecoming              | 2017 | 14:05
	18 | Thor: Ragnarok                      | 2017 | 13:05
	19 | Black Panther                       | 2018 | 19:55
	20 | Avengers Infinity War               | 2018 | 18:50
	21 | Ant-Man and the Wasp                | 2018 | 19:55
	22 | Captain Marvel                      | 2019 | 00:00
	16 | Guardians of the Galaxy 2           | 2017 | 14:55
	(21 rows)


## Extension

1.  Research how to delete multiple entries from your table in a single command.

Option 1:
#
	DELETE FROM people WHERE id = 1 OR id = 2;

Option 2:
#
	DELETE FROM people WHERE id IN (1, 2);
#
	id |         name         
	----+----------------------
	 3 | Nuno Farinha
	 4 | Ruben Franco Sanchez
	 5 | Richard Haigh
	 6 | Chika Kanu
	 7 | Aaron McFaull
	 9 | John Polson
	10 | Kiran Qureshi
	11 | Ethan Radcliffe
	12 | Janapoles Ramos
	13 | Gordon Renfrew
	14 | Pauline Rudge
	15 | Martin Selis
	16 | Alex Shing
	17 | Anita Squires
	19 | Elisa Sveinsdottir
	20 | Hamish Whyte
	21 | Matthew Woodley
	22 | Emil Zacharczuk
	18 | Anthony Starke
	23 | Sandy McMillan
	(20 rows)
	