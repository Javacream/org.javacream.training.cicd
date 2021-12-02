FROM h2908727.stratoserver.net:8083/javacream/javabase:1.0
ADD jolokia-jvm-1.3.7-agent.jar ./jolokia-agent.jar
ENV JAVA_OPTS ${JAVA_OPTS} -javaagent:jolokia-agent.jar=port=7654,host=0.0.0.0
EXPOSE 7654
