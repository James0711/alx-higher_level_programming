# 0x0DE. SQL - More queries

This is a continuation of SQL queries, working with permissions, joins, and constraints.
Usage 🐬

•	Scripts 3-force_name.sql forward take the database to query from as a MySQL command line argument.

$ cat 3-force_name.sql | mysql -hlocalhost -uroot -p hbtn_0d_2

•	Tasks 10-101 query from the database hbtn_0d_tvshows.sql.

•	Tasks 102-103 query from the database hbtn_0d_tvshows_rate.sql.

# Tasks 📃
• 0. My privileges!
o	0-privileges.sql: MySQL script that lists all privileges of the users user_0d_1 and user_0d_2.

• 1. Root user
o	1-create_user.sql: MySQL script that creates the user user_0d_1 with all privileges and password user_0d_1_pwd.

• 2. Read user
o	2-create_read_user.sql: MySQL script that creates the database hbtn_0d_2 and user user_0d_2 with password user_0d_2_pwd.
o	user_0d_2 only has SELECT privilege on the database hbtn_0d_2.

• 3. Always a name
o	3-force_name.sql: MySQL script that creates the table force_name.
o	Description:
	id: INT
	name: VARCHAR(256) (cannot be null)

• 4. ID can't be null
o	4-never_empty.sql: MySQL script that creates the table id_not_null.
o	Description:
	id: INT (default value = 1)
	name: VARCHAR(256)

• 5. Unique ID
o	5-unique_id.sql: MySQL script that creates the table unique_id.
o	Description:
	id: INT (default value = 1, must be unique)
	name: VARCHAR(256)

• 6. States table
o	6-states.sql: MySQL script that creates the database hbtn_0d_usa with a table states.
o	states description:
	id: INT (unique, auto-generated, cannot be null and is a primary key)
	name: VARCHAR(256) (cannot be null)

• 7. Cities table
o	7-cities.sql: MySQL script that creates the database hbtn_0d_usa with a table cities.
o	cities description:
	id: INT (unique, auto-generated, cannot be null and is a primary key)
	state_id: INT (cannot be null, foreign key that references to id of the states table)
	name: VARCHAR(256) (cannot be null)

• 8. Cities of California
o	8-cities_of_california_subquery.sql: MySQL script that lists all the cities of California that can be found in the database hbtn_0d_usa, ordered by ascending city id.

• 9. Cities by States
o	9-cities_by_state_join.sql: MySQL script that lists all cities contained in the database hbtn_0d_usa, ordered by ascending city id.

• 10. Genre ID by show
o	10-genre_id_by_show.sql: MySQL script that lists all shows contained in hbtn_0d_tvshows that have at least one genre linked, in order of ascending tv_shows.title and tv_show_genres.genre_id.

• 11. Genre ID for all shows
o	11-genre_id_all_shows.sql: MySQL script that lists all shows contained in the database hbtn_0d_tvshows, in order of ascending tv_shows.title and tv_show_genres.genre_id.
o	If a show does not have a genre, displays NULL.

• 12. No genre
o	12-no_genre.sql: MySQL script that lists all shows contained in hbtn_0d_tvshows without a genre linked, in order of ascending tv_shows.title and tv_show_genres.genre_id.

• 13. Number of shows by genre
o	13-count_shows_by_genre.sql: MySQL script that lists all genres from hbtn_0d_tvshows and displays the number of shows linked to each, in order of descending number of shows linked.
o	Does not display a genre if it has no linked shows.

• 14. My genres
o	14-my_genres.sql: MySQL script that uses the hbtn_0d_tvshows database to list all genres of the show Dexter, in order of ascending genre name.

• 15. Only Comedy
o	15-comedy_only.sql: MySQL script that lists all comedy shows in the database hbtn_0d_tvshows, in order of ascending show title.

• 16. List shows and genres
o	16-shows_by_genre.sql: MySQL script that lists all shows, and all genres linked to that show, from the database hbtn_0d_tvshows, in order of ascending show title and genre name.

• 17. Not my genre
o	100-not_my_genres.sql MySQL script that uses the hbtn_0d_tvshows database to list all genres not linked to the show Dexter, in order of ascending genre name.

• 18. No Comedy tonight!
o	101-not_a_comedy.sql: MySQL script that lists all shows without the genre comedy in the database hbtn_0d_tvshows, in order of ascending show title.

• 19. Rotten tomatoes
o	102-rating_shows.sql: MySQL script that lists all shows from hbtn_0d_tvshows_rate by their rating, in order of descending rating.

• 20. Best genre
o	103-rating_genres.sql: MySQL script that lists all genres in the database hbtn_0d_tvshows_rate by their rating, in order of descending rating.



