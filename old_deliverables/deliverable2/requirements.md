## CitySim9000 Requirements

FUN-CITY-LOCS. The program shall simulate a city with four locations: Mall, Bookstore, Coffee Shop, and University.

FUN-OUTSIDE-CITY. A fifth location, Outside City, shall stand for a driver outside the city limits.

FUN-AVENUES. The city shall have two one-way avenues, Fourth Ave and Fifth Ave.  Fourth Ave shall connect, in order, Outside City -> Mall -> Bookstore -> Outside City.  Fifth Ave shall connect, in order, Outside City -> University -> Coffee Shop -> Outside City.

FUN-STREETS. The city shall have two two-way streets, Meow St. and Chirp St.  Meow St. shall connect Coffee Shop and Mall.  Chirp St. shall connect Bookstore and University.

FUN-FIVE-DRIVERS. Five drivers, numbered 0 through 4, shall traverse the city, one after the other.

FUN-START-LOC. A driver may start in any of the five locations listed in FUN-CITY-LOCS or FUN-OUTSIDE-CITY.

FUN-ITERATION. At each iteration, a Driver will drive from the current Location to one of the possible Locations that can be reached from the original Location.  The decision shall be made pseudorandomly based on a seed passed in from the command line, as covered by FUN-ARGS.

FUN-END. The simulation shall end if a Driver encounters the Outside City Location and it is not the first iteration of the simulation.  If it is the first iteration of the simulation, behavior is covered by FUN-FIRST-LOC.

FUN-FIRST-LOC. If the Location the Driver starts is Outside City, the Driver will pseudorandomly choose to go to University (via Fifth Ave) or Mall (via Fourth Ave).

FUN-ARGS. The system shall accept an integer seed from the command line for the pseudorandom number generator.  No other arguments shall be accepted.  If no arguments are provided,  more than one argument is provided, or the single argument is not an integer, the system shall inform the user and exit.

It may be easier to understand the map of the city visually.

```
	 City Map
	
	   ---> [Mall] ----> [Bookstore] ----> Fourth Ave.
	         A  |         A   |
	 Meow St.|  |         |   | Chirp St.
 	         |  V         |   V
	   <--- [Coffee] <-- [University] <--- Fifth Ave.
```	
