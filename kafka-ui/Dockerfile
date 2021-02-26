FROM provectuslabs/kafka-ui:0.0.9 as kafkauiimage

FROM amazoncorretto:15-alpine-jdk

RUN addgroup -S bocusers && adduser -S bocuser -G bocusers -s /bin/sh -h /home/bocuser

COPY --from=kafkauiimage /kafka-ui-api.jar /kafka-ui-api.jar

USER bocuser

WORKDIR /home/bocuser

EXPOSE 8080

CMD ["java", "-jar", "/kafka-ui-api.jar"]
