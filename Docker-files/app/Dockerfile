# Stage 1: Build stage
FROM openjdk:11 AS build_stage
RUN apt-get update && apt-get install -y maven git
RUN git clone --branch docker https://github.com/omniacommuniasunt/vprofile-project.git
RUN cd vprofile-project && mvn install

# Stage 2: Production stage
FROM tomcat:9-jre11
LABEL "Project"="Vprofile"
LABEL "Author"="Nixx"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=build_stage /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
