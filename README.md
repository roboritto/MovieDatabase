# Movie Database
This template can be used as a personal database for movies. This database uses TheMovieDataBase (https://www.themoviedb.org/) as the source. Note that this database is an excel macro enable workbook, so all the macros/function on mobile version. All the macros is written in VBA.

## Pre-requisite:
1. You would need a tmdb api key for the movie posters
    - Go to https://www.themoviedb.org/, and login or register and then, on the main page go to more>api documentation and then follow the instructions.
    - Go to the Developer tab and open Visual Basic on the top left.
    - Replace YOUR_TMDB_API_KEY on Module2, Module4, Module5 & Module11 with the key.

2. Enable Macros
   - Click Enable Macros/Enable Content to make sure the macros can work.

3. If you don't currently have the Developer tab enabled, go to File>Option>Customize Ribbon. Then find Developer from the list on the left and add.

## How to use:
Do not sort any of the columns before you completed all the steps to make sure everything works as intended.  
Don't remove the ♡ on both of the sheets if you want the rating system. Though, you can replace the shape with any shape you want but make sure to name it HeartSample to ensure that the rating system works well.

**Database Sheet**
1. Type in the name of the name.
2. You can also specify the year of the movie.
3. Press ctrl+k to autofill the remaining columns.
- If you added multiple movies, select all the movies you want to autofill.
- If the movie is wrong, you would have to specify more. Resident Evil might be the 2002 instead of the 2026 one.
- Don't forget to place the movie poster in cell by clicking the poster and then the little icon on the top right of the poster. This is to make sure the poster move with the row you sort the columns.
- If let's say you wanted to add a movie that isn't available on the tmdb, just copy any of the movie link but replace the numbers at the end of the link to >5000000 or any number as long as it doesn't belong to any movie on the tmdb. >5000000 is just a safe point to start since tmdb is not that big currently. You can copy the link to your browser to ensure that a movie with that id exist. ie. https://www.themoviedb.org/movie/8000000.
- If you don't like the movie poster that was autofilled, you can go to the movie tmdb link, click on the poster and find the one you liked better, copy the image link, paste it into the movie poster cell, then press ctrl+d. Also don't forget to place the image inside the cell to make sure it moves with the row.

**Rating Sheet**
1. Copy the first 3 cells of the movie/s you just added on the Database Sheet, and paste it into the same column on the Rating Sheet.
   - This is to make sure that the movie tmdb link is on the same cell on both sheets for later use.
2. Press ctrl+l to autofill the the director/s and actor/s of the movies.
   - You can also autofill multiple movies at once for this one too.
3. Go to the Rating column of the and press ctrl+g.
   - This generate the hearts for the rating system. It uses the movie tmdb link I mentioned earlier.

Now, you can sort both sheets however you like.

## Use cases:
Navigation Buttons
- ↑ to go to the top
- ↓ to go to the bottom of the table
- ? to suggest a random movie
- Hide Bar to hide the freeze top rows

Export  
You can export your database into a csv by pressing ctrl+e. This would export the database into your document folder on your computer with the name Movies.csv. You can change the directory and name of the csv by going to Module10 and find this (savepath = ).

**Database Sheet**

Genre Filter
- 1st click to include the genre, 2nd click to exclude, 3rd click to remove filter 
- You can filter as many as you like.
- To clear all filter click clear filter button
- If you want to add a filter for a specific words anywhere in the excel, like maybe Youtube, you can go to Module14, copy paste any of the Sub at the top and replace the word inside the "" with the word you would like to filter and rename the Sub with the word. Then, to assign it to a button on the sheets, right click any buttons, copy and paste it, and then right click it again to assign the new filter you just made.

**Rating Sheet**

Rating System
- Click once inside the heart for full heart, 2nd click for half heart, 3rd click to blank again.
- It would also register the date and time to the next cell when you rate.

Rating Filter
- 1st click to include the genre, 2nd click to remove filter.
- Filter multiple hearts at once.
- Clear the filter by clicking the ❤️🚫 at the end of the filters.

Search System
- To search for movie name, just type in the name and click the ⌕ button, it won't work if you click enter. You have to write the movie name without misspell for it to work, though incomplete name does work.
- To search movies by some directors, type (by Director Name). If the movie have multiple directors, you can write each of the directors name separated by comma (,), order doesn't matter.
- To search actor/s, type (Actor Name,). If you want to search for multiple actors, you can type (1st Actor Name, 2nd Actor Name), the order doesn't matter here. Meaning (Zendaya, Tom Holland) and (Tom Holland, Zendaya) would return the same result.
- To reset the search just click the x at the end of the search bar.
- This system might cause some glitches when you clicked the ⌕ and immediately scroll to the right, it would scroll to the bottom of the table. To avoid this, click anywhere within the search result, and then use the arrow buttons on your keyboard to go the next cell.
