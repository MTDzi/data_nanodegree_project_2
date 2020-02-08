## Purpose
This projects purpose is to write an ETL pipeline that stores data in a NoSQL database, namely: Apache Cassandra.

### More details

There are three resulting tables: `songs_in_session`, `user_songs`, and `users_who_played_songs`.
They're adapted to support three queries:

```sql
    SELECT
        artist, song, length
    FROM
        songs_in_session
    WHERE
        sessionId=338 AND itemInSession=4;
```

```sql
    SELECT
        artist, song, firstName, lastName
    FROM
        user_songs
    WHERE
        userId=10 AND sessionId=182;
```

and finally:
```sql
    SELECT
        firstName, lastName
    FROM
        users_who_played_song
    WHERE
        song='All Hands Against His Own';
```


## Commands
You can create a conda env by calling:

```
conda create --name SOME_NAME --file requirements_conda.txt
```

and after that, run
```
jupyter-notebook
```
and then run all the cells in the `Project_1B_ Project_Template.ipynb` notebook.

The steps are explained in the notebook and that's also the place in which all the code is defined, so there isn't much I can add in this README, go check it out.
