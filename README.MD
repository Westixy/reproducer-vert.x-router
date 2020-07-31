# Reproduce vert.x router behaviour

## check working 3.9.1

1. Run `mvn clean install exec:java`
2. Go to `http://localhost/static`
3. Should display `Static script loaded`
4. Stop it

## check changed behaviour 3.9.2

1. Change Vert.x-web to version 3.9.2
2. Run `mvn clean install exec:java`
3. Go to `http://localhost/static`
4. Should redirect using a 301 HTTP Code to `http://localhost/static/`
5. Should display `Failed to get script`
