# Twitter-Project
Twitter Project for Spark Streaming

Step 1: Create a Project called Stream-Proj in your workspace

Step 2: Create below folder hierarchy and put the two Scala API's Streaming - "StreamingExamples.scala" & "TwitterPopularTags.scala"  inside myPackage folder at this path: ~/stream-proj/src/main/scala/myPackage.

Step 3: Copy build.sbt in root project folder: /home/edureka/workspace/stream-proj

Step 4: Create Project folder and inside that save assembly.sbt

Step 5: goto terminal and cd into project root folder Stream-Proj in your workspace, and run sbt assembly

Step 7: Make sure you update the master url on spark-defaults.conf to your master localhost before you submit this application in cluster mode.

Step 6: Once you do sbt assembly cd into spark-1.5.2 and run below command with consumer key, consumer token, access token and access token secret like: 

Local Mode:
----------
~/spark-1.5.2/bin/spark-submit --class TwitterPopularTags ./target/scala-2.10/TwitterPopularTags-assembly-1.0.jar rXSczW0WTtxkR18sPzd1rYdQa PdH5FDr67bmIhS30B6A16tACUZVWCuhqjmBolY3eWI6TbfT4d2 829554074076864512-w0BotN8CHsOFpTGn38erPu3r3TeA6DZ Plby2GaSZcGvD8a1yfuPjc9wnIxHyb5nGztdAcd9fg3MC

With filterred tweets in cluster mode:
-------------------------------------
~/spark-1.5.2/bin/spark-submit --deploy-mode cluster --class TwitterPopularTags ./target/scala-2.10/TwitterPopularTags-assembly-1.0.jar rXSczW0WTtxkR18sPzd1rYdQa PdH5FDr67bmIhS30B6A16tACUZVWCuhqjmBolY3eWI6TbfT4d2 829554074076864512-w0BotN8CHsOFpTGn38erPu3r3TeA6DZ Plby2GaSZcGvD8a1yfuPjc9wnIxHyb5nGztdAcd9fg3MC India,Modi


Step 7: 
To view the results in local mode run: 
-------------------------------------
Once you see some results, ctrl-z to pause the streaming, and check the top tweets for last 10 sec and last 60 secs printed on the terminal.

To view the results in lcuster mode run:
---------------------------------------
Goto spark master url, you should see your application as driver app
click on the driver, and checkout stdout and stderr




