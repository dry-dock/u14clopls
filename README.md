u14clopls
===================

Shippable CI image for clojure on Ubuntu 14.04. Lein2 version is available in this image.
Available clojure versions:

1. 1.3.0
2. 1.4.0
3. 1.5.1
4. 1.6.0


**Services:**

1. elasticsearch 1.5
2. memcached 1.4
3. mongodb 3.0
4. mysql 5.6
5. postgres 9.4
6. rabbitmq 3.5
7. redis 3.0
8. selenium 2.45
9. sqllite 3

## How to use
You can use this image to run clojure builds on Shippable. Just update your
`shippable.yml` file and add the `build_image` directive. Here's a sample YML file to get you going:

````````
language: clojure

lein:
  - lein2

services:
  - elasticsearch
  - memcached
  - mongodb
  - mysql
  - postgres
  - rabbitmq
  - redis
  - selenium
  - sqllite

build_image: drydock/u14clopls:prod

# Running the test with Leiningen
script:
  - lein test

`````````
