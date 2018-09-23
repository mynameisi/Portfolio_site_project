# Portfolio Site Project
This project contains server side code(HTML,CSS and related resources) that builds a static portfolio web page. The page is layed out according to the project markup. This is an assignment project from the UDacity Course [Programming Foundations with Python](https://classroom.udacity.com/courses/ud036).

My realization of the project is based on a MVC structure.
* Model : 
	* `movie_db.csv`: this file contains only movie data, separated by comma, with each line corresponds to 1 movie. It's a table-like data-structure:
		* 1st column: movie title
		* 2nd column: movie trailer URL
		* 3rd column: movie poster URL
	* `media.py`:this file contains the design of Movie class
* View : `fresh_tomatoes.py`
	* this file is provided by udacity, with the main goal of producing a webpage with data from `movie_db.csv`
* Control : `entertainment_center.py`
	* this file contains the main control flow of the project:
		1. loop through data file : movie_db.csv
		2. with each line of the data, create a corresponding Movie object
		3. append the object into the final movie list
		4. call function: `open_movies_page` to produce and show the webpage using the list
for detailed realization, please refer to the code themselves.

### Prerequisites

`python 2` or `python 3` is required for this project

### Deployment

clone the project from my GitHub repository

```
git clone https://github.com/mynameisi/MovieTrailerProject.git
```
contained in the `MovieTrailerProject` folder are the following files:
1. `entertainment_center.py` the main python file to run to create the webpage
2. `fresh_tomatoes.py` helper code in charge of building the outlook of the webpage
3. `media.py` contains the class definition of `Movie`
4. `movie_db.csv` a comma seperated file with each line representing one movie. each line has 3 columns:
   1. movie title
   2. movie trailer url
   3. movie poster url

## Running the program

### create the web-page with pre-existing movies
File `movie_db.csv` contains a few movies already. Just by executing the following line of code, a movie web page with those movies, runing on the default web browser on your computer would pop up.

`python entertainment_center.py`

### input new movies
The design of this project has MVC in mind. The data layer of the webpage `movie_db.csv` is completely seperate with the control layer `entertainment_center.py` and the presentation layer `fresh_tomatoes.py`. 

one advantage of doing this is the user don't have to modify any python code to change the movies. Simply open the data file `movie_db.csv` and add new lines to the file with required information of the movie and then run `python entertainment_center.py`, the web page would pop up with the list of newly inserted movies.

## Built With

* [Udacity Starter Code](https://github.com/udacity/ud036_StarterCode) - This is the starter project containing the `fresh_tomatoes.py` and a readme file.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details