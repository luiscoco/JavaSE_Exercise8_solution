# JavaSE_Exercise8_solution

## How to create the Github actions build.yml file

![Github actions image 1](https://github.com/luiscoco/JavaSE_Exercise8_solution/assets/32194879/7a4e1211-2ef6-4ff9-a91a-d5a1f05b2f22)


![Github actions image 2](https://github.com/luiscoco/JavaSE_Exercise8_solution/assets/32194879/b731c0b4-3da8-4245-a795-9c3eb725ce80)


![Github actions image 3](https://github.com/luiscoco/JavaSE_Exercise8_solution/assets/32194879/51d033a2-3bc8-4098-80bb-997305d51d44)


![Github actions image 4](https://github.com/luiscoco/JavaSE_Exercise8_solution/assets/32194879/ef4b5721-c406-4e93-bd48-fdf7401639ab)


## build.yml file

```yml
name: Java Build

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Set up JDK
        uses: actions/setup-java@v1
        with:
          java-version: '11'

      - name: Check out code
        uses: actions/checkout@v2

      - name: Compile Java
        run: javac -d . *.java
```


