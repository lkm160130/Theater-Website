Written By: Logan Moon
Course: CS 4336.0U1
Email: lkm160130@utdallas.edu

Overview: This README covers Final Project for Prof. Greg Ozbir's Advanced Java class at UT Dallas. It will go over the 
  individual files of the project and their purpose within the the project as a whole.

Notes about importing/running the Program: The program uses a DB named MovieTheater with username scott and password tiger. The included SQL script
                                    should be run on this DB to give it all the necessary data. If the DB is empty, 5 errors will occur as the
                                    script tries to drop and previous versions of the tables it is about to create. These errors can be ignored.
                                    From there the program should be ready to run. Just be sure to use the netbeans unzip option when importing 
                                    the project.

Web Files:
   AllTheaters.xhtml: This jsf page displays all the theaters that are accessible through the application.
   Home.xhtml: This jsf page serves as the home page of the application. It is the first page that is displayed when running the program
   Movies.xhtml: This jsf page displays all the movies that are accessible through the application
   NumberOfSeats.xhtml: This jsf page allows the user to choose the number of seats they wish to purchase
   Reservation.xhtml: This jsf page displays the information the user has already chosen then asks for a name and a credit card number.
   ReservationConfirmed.xhtml: This jsf page is displayed once the user has confirmed the reservation and the data has been persisted to the DB
   Search[noResults].xhtml: This jsf page allows the user to enter a zipcode to search for theaters.
   Search[withResults].xhtml: This jsf page displays the results for the first zipcode search and give the option to search other zipcodes.
 
Java Files:
   MovieTheaterBean.java: This is the bean that all of the above web files use to display data and perform basic calcualtions. This bean will 
                       access the EJB when database information is needed.
   MovieTheaterEJB.java: This is the EJB used to access the database containing information about the movie theaters. Its methods are called
                            by the java bean to get information that needs to be displayed by the web pages
   Movies.java: The entity that represents a movie. It contains things like the time of the movie and the namedescription object.
   Namedescription.java: The entity that contains the name of a movie as well as its description. It is used by Movies.java to provide name/descripiton
                            to a movie.
   Reservation.java: The entity that will be persisted to a database once the user has filled out all the information requested in the web pages
   Theaters.java: The entity that represents a theater. It contains the theater's name, address, and the movies that are being shown there.
   Zips.java: The entity that represents a zipcode. It contains the zipcode, and its id is linked to the theaters that are in its area.