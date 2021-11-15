# LogFlash_G
## 进入entrance包下，下面有如下5个文件：
  - StreamBuildTCFG.java 
  - StreamErrorDiagnosis.java
  - StreamErrorFeedback.java
  - StreamSourceToKafka.java
  - StreamTemplating.java
  ### StreamSourceToKafka.java
  从日志源处读取日志数据，发送到kafka队列中
  ### StreamTemplating.java
  通过drain算法，将日志流解析成日志模板流，可以通过高并行来增加效率，最后将它发送到三个kafka队列中
  ### StreamBuildTCFG.java 
  对已有的模板流，进行构建和更新TCFG矩阵
  ### StreamErrorDiagnosis.java
  通过TCFG矩阵进行异常日志的诊断
  ### StreamErrorFeedback.java
  通过TCFG矩阵进行异常日志的反馈
## 使用方法，在out/artifacts/ReferenceNew_jar下存在ReferenceNew.jar，将它提交到Flink集群，入口类为上面的五个文件。
