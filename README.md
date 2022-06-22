### TakingSpringBoot application Heap and Thread dump

In this tutorial, we will explore ways to capture Heap and Thread dump from a spring boot application running inside the Kubernetes cluster.

A Heap Dump is a snapshot of all the objects that are in memory in the JVM at a certain moment. They are very useful to troubleshoot memory-leak problems and optimize memory usage in Java applications.

A Thread Dump is a snapshot of the state of all the threads of a Java process. The state of each thread is presented with a stack trace, showing the content of a thread's stack. A thread dump is useful for diagnosing problems, as it displays the thread's activity.



In this manifest we are passing command “kill -3 1” as prestop (“Note in this command, 1 represents the process id of the springboot application running inside the pod”) . This command will print the “threaddump” and “GC.heap_info” in the logs. To check the output of this command run the below mentioned command:- 

kubectl logs < pod-name > -n namespace
