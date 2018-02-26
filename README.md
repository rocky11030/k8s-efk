# k8s-efk

安装说明
========

- 此项目主要是使用ansible部署基于k8s的filebeat、logstash、elasticsearch和kibana
- 一、部署filebeat，这部分还没有完成
- 二、部署logstash集群，不同的项目部署不同的集群
- 三、部署elasticsearch集群，3个节点部署
- 四、部署kibana单点
- 五、logstash、es和kibana的镜像太大，放到网盘
- PS: 一定要先部署k8s环境

第三步: 安装es集群
--------------
* 修改hosts的主机变量和groups_vars/all里面的变量
* 执行脚本:ansible-playbook -i hosts es_install.yml


第一步: 安装filebeat
--------------
* 修改hosts的主机变量和groups_vars/all里面的变量
* 执行脚本:ansible-playbook -i hosts filebeat_install.yml


第二步: 安装logstash集群
--------------
* 修改hosts的主机变量和groups_vars/all里面的变量
* 执行脚本:ansible-playbook -i hosts logstash_install.yml

第三步: 安装es集群
--------------
* 修改hosts的主机变量和groups_vars/all里面的变量
* 执行脚本:ansible-playbook -i hosts es_install.yml

第四步: 安装kibana
--------------
* 修改hosts的主机变量和groups_vars/all里面的变量
* 执行脚本:ansible-playbook -i hosts kibana_install.yml
