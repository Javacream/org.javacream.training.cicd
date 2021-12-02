FROM h2908727.stratoserver.net:8083/javacream/javabase_monitored:1.0
ENV JAVA_LOGFILE gc_log
CMD java -jar java_lib/app.jar -javaagent:jolokia-agent.jar=port=7654,host=0.0.0.0 -Xloggc:gc_log
