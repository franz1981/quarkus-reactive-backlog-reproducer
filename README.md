To hit the bug:

$ mvn clean package

$ java -Dquarkus.vertx.prefer-native-transport=true -jar ./target/quarkus-app/quarkus-run.jar

$ siege -c 512 -r 1 http://localhost:8080/hello -v -R .siegerc 

If `-Dquarkus.vertx.prefer-native-transport=false` the issue won't happen anymore.