# Reproduce vert.x router behaviour

Reproduce a little change in the router behaviour between 3.9.1 and 3.9.2

## check working 3.9.1

1. Run `mvn clean install exec:java`
2. Go to `http://localhost:8888/static`
3. Should display `Static script loaded`
4. Stop it

## check changed behaviour 3.9.2

1. Change Vert.x-web to version 3.9.2 in pom.xml
2. Run `mvn clean install exec:java`
3. Go to `http://localhost:8888/static`
4. Should redirect using a 301 HTTP Code to `http://localhost:8888/static/`
5. Should display `Failed to get script`
