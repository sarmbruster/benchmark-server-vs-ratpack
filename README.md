This repo contains performance tests for Neo4j Server vs. neo4j-ratpack.

Example:

for i in 10 50 100 500 100; do jmeter -n -t loadtest19.jmx -Jthreads=$i -Jhost=localhost -Jport=5050 -Jpath=/cypher; done

for each run a csv file with naming convention $threads-$port-overall-summary.csv is generated

Building diagram:

* install matplot: `sudo apt-get install python-matplotlib`
* generate diagram: `diagram *-$port-overall-summary.csv




