# lyrics
This project enables the user to scrap and process lyrics by the requested artists and grasp some insights related to the words they sing. For instance, the user is able to sort artists on the sentiment their words represent.

Example of basic visualization on Tableu Public:
https://public.tableau.com/profile/javier.reina#!/vizhome/Artistsmostfrequenttokens/Artistsandtokenssortedbysentiment

The user would process the lyrics and create useful datasets by following the next steps:

1. Populate the file input.csv in a way the lyrics portal azlyrics.com is able to resolve (explore the url of the artist in every case, for instance 's' and 'spears' for https://www.azlyrics.com/s/spears.html and 'm' and 'metallica' for https://www.azlyrics.com/m/metallica.html)
2. Run the Kettle Job get_tokens_dataset_from_artists. This job will find the songs of the requested artists and scrap their lyrics, saving one file for every song.
3. Run the Kettle Transformation write_fact_table. This transformation will process the previously extracted lyrics and generate some analytical outputs.