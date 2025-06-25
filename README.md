# WiFi-CSI-indoor-intrusion-detection-dataset
我们在一个3m×2m的区域内对所提出的方案进行了全面的评估。在测试过程中，环境内无非相关人员出现，以保证实验的准确性。在实测场景中，主要收集了三大类数据：1.静态数据，即此时区域内无人情况；2.移动数据，即测试人员在被监视的区域中进行各种动作，包括静止不动、行走、小跑等；3.临界数据，即测试人员靠近区域边界但未进入区域的情况。数据包含五种人类活动，分别为：1.环境中无人存在(envonly) 2.有人靠近房间但并未入侵(approach) 3.房间内有人且人员静止不动(stand) 4.房间内有人且人员慢速行走(walk) 5.房间内有人且人员快速移动(run)
 
实验以Wi-Fi设备为原型，环境中包含电梯、电视和桌椅等物体，以此来模拟低信噪比的室内环境，并对所提出的方案的性能进行了评估。接收端通过利用Linux 802.11n CSI Tool从Intel 5300网卡中获取CSI值。在实验中，测量的天线数量设置为一发三收，并按照均匀线阵的方式分布，相邻的天线之间的距离大约为2.5cm，数据速率约为每秒1500个CSI数据包，每对天线可以获取30个子载波的CSI数据。
 
在感知部署阶段，首先在一个角落布置了装有Intel 5300无线网卡的笔记本电脑作为接收端节点，同时在其对角角落布置了同样的电脑作为发射端节点。接收端和发射端节点的位置固定不变，人员在限制区域内移动。接收端负责采集CSI数据，并将数据传输到服务器端进行处理。在数据采集之前，首先将接收端的操作系统配置为Ubuntu，并安装了CSI-Tools，再将发射端AP的工作模式设置为802.11n，接着在接收端终端运行命令，使接收端与发射端AP进行通信，从而分别采集接收端与AP之间的CSI数据。每种情况共收集了五次大样本测试数据，每次测试收集30000个数据包，即每种情况共采集了150000个数据包。

We conducted a comprehensive evaluation of our proposed intrusion detection framework in a 3m × 2m indoor area. To ensure accuracy and repeatability, no irrelevant personnel were present during the data collection process.

The dataset consists of three major categories of data:
1.Static data: Captured when no person is present in the monitored area.
2.Movement data: Collected while a subject performs various activities inside the target area, including standing still, walking, and running.
3.Boundary data: Recorded when a subject approaches the monitored area but does not enter it.

In total, the dataset includes five types of human activities:
A. envonly: No person present in the environment.
B. approach: A person approaches the area boundary but does not enter.
C. stand: A person remains stationary inside the monitored area.
D. walk: A person walks slowly within the area.
E. run: A person moves quickly (runs) inside the area.

To simulate a realistic low-SNR indoor environment, the testing area contains objects such as elevators, televisions, and furniture. The experiments were conducted using commodity WiFi devices. Channel State Information (CSI) was collected using the Intel 5300 wireless NIC and the Linux 802.11n CSI Tool.

The receiver node was equipped with three antennas arranged in a uniform linear array with approximately 2.5 cm spacing. A single transmitter and three receivers were used. The receiver captured CSI packets at a rate of approximately 1500 packets per second, with 30 subcarriers per antenna pair.

For deployment, a laptop with an Intel 5300 NIC was placed in one corner of the area as the receiver, and another identical laptop was positioned diagonally across as the transmitter. Both nodes remained stationary throughout the experiment, while the subject moved within the defined area. The receiver node ran Ubuntu and CSI-Tool, while the transmitter operated in 802.11n AP mode. CSI data was collected using terminal commands that enabled real-time communication between the transmitter and receiver.

Each activity type was recorded five times, with 30,000 CSI packets collected per trial, resulting in a total of 150,000 packets per activity.
