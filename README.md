# benchmark
speed comparison of MySQL &amp; MongoDB in GOLANG1.6 &amp; PHP5

system used for benchmark:
  DELL cpu i5 4th gen 1.70Ghz * 4
       ram 4GB
       GPU ram 2GB
       
Speed comparison of RDBMS vs NoSQL 
for INSERT, SELECT, UPDATE, DELETE
executing different number of rows
10,100,1000,10000,100000,1000000

Language used to execute is:
  PHP5 & Google fastest language GO 1.6
  
The Results are here.

________________________________________________
GOLANG with MySQL (engine = MyISAM)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
			INSERT
------------------------------------------------
num of rows				time taken
------------------------------------------------
10      				1.195444ms
100     				6.075053ms
1000    				47.439699ms
10000   				483.999809ms
100000  				4.707089053s
1000000 				49.067407174s


			SELECT
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				872.709µs


		SELECT & DISPLAY
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				20.717354746s


			UPDATE
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				2.309209968s
100000  				257.411502ms
10000   				26.73954ms
1000    				3.483926ms
100     				915.17µs
10      				650.166µs


			DELETE
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				6.065949ms
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


________________________________________________
GOLANG with MongoDB
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
			INSERT
------------------------------------------------
num of rows				time taken
------------------------------------------------
10						2.067094ms
100 					8.841597ms
1000					106.491732ms
10000					998.225023ms
100000					8.98172825s
1000000					1m 29.63203158s


			SELECT
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000					5.251337439s


		FIND & DISPLAY (with index declared)
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000					21.540603252s


			UPDATE
------------------------------------------------
num of rows				time taken
------------------------------------------------
1						1.330954ms
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

________________________________________________
PHP5 with MySQL	(engine = MyISAM)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
			INSERT
------------------------------------------------
num of rows				time taken
------------------------------------------------
 10 					0.0040680000000001s
 100 					0.011595s
 1000 					0.049718s
 10000 					0.457164s
 100000 				4s
 1000000 				42s
 
 
 			SELECT
------------------------------------------------
num of rows				time taken
------------------------------------------------
 1000000 				<1s
 
 
 			SELECT & DISPLAY
------------------------------------------------
num of rows				time taken
------------------------------------------------
  1000000 				20s
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

________________________________________________
PHP5 with MongoDB 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
			INSERT
------------------------------------------------
num of rows				time taken
------------------------------------------------
10 						0.065744s
100 					0.190966s
1000					0.2163s
10000					1s
100000					8s
1000000					78s


			FIND
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				<1s


			FIND & DISPLAY
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				7s


			UPDATE
------------------------------------------------
num of rows				time taken
------------------------------------------------
1000000 				9s
       
