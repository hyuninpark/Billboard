This is a program that when input any lyrics, will return a Billboard artist
who has the most similar lyrics style.

Ex.
Input: "Twinkle twinkle little star, how I wonder what you are"
Returns: "The Beatles"

All of the data and the models are accessible in the files,
which means that the program can be run as it is.
However, it is also possible to regenerate all the data from
scratch using the .py files within the folder. Note that it
will take 30 ~ 40 minutes to do so.

To run the program, 
1. In terminal, type:
    python3 manage.py runserver
2. click on the http link
3. The initial page will say:
    "Page not found (404)"
4. On the url at the top, add:
    /create

To get all the data from scratch,
1. In terminal, type:
    python3 lyrics_crawler.py
    (This scrapes the lyrics from the web,
    and creates the "artist_lyrics.txt" file)
2. In terminal, type:
    python3 preprocess.py
    (This filters the lyrics in "artist_lyrics.txt",
    and creates a new file called "processed_lyrics.csv".
    It also creates "billboard.model". This model is
    slightly different everytime we run this file.
3. In terminal, type:
    python3 prepare_side_task.py
    (This creates "most_similar.csv".)
