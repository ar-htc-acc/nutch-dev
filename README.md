# nutch-dev
Nutch 2.3.1 + Gora/MongoDB + Elasticsearch

# version info
Nutch: 2.3.1  
MongoDB: 2.6.x (2.6.12)  
Elasticsearch: 1.4.1 (used 1.7.6)  
Kibana: 4.1.x  

# Ant: include the missing JAR
Trying to override old definition of task javac  
  [taskdef] Could not load definitions from resource org/sonar/ant/antlib.xml. It could not be found.  
  
Download sonar-ant-task-2.1.jar   
Modify build.xml  

`<!-- Define the Sonar task if this hasn't been done in a common script -->`  
`<taskdef uri="antlib:org.sonar.ant" resource="org/sonar/ant/antlib.xml">`  
`<classpath path="${ant.library.dir}" />`  
`    <classpath path="${mysql.library.dir}" />`  
`    <classpath>`  
`	    <fileset dir="your_directory" includes="sonar*.jar" />`  
`	</classpath>`  
`</taskdef>`  

# Result
Successfully built a demo. 
