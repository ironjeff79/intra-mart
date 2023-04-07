#### 1 申请页面
- 参考
![所需语句](pictures/fe45b6ea1cee17972ededaee74397b1.png)

1. 如图操作
![如图](pictures/ce094288c6846aab748e58e0d3ccc93.png)

2. 登录系统 --> Workflow下的一览表 --> 流程 --> 差旅费申请（直线） --> 如图 
![申请](pictures/10aca9bcb73ac5faf0be864c11f43b9.png)

3. 页面相关程序保存在screen下的apply.html 
![screen](pictures/3cf593033db26dbe1ff29b97ad1ff79.png)

4. 如图添加（可以实现申请页面的调用）
![申请页面的调用](pictures/ed055457a0dcf4aaaf1f2476679bc52.png)

5. 登录系统 --> Workflow下的一览表 --> 流程 --> 差旅费申请（直线） --> 脚本开发模式被打开了 

6. 源代码参考
![源代码参考](pictures/433c6fe8ac8a6cd15a7b3ea3bf3656d.png)

7. 申请页面参考
![申请页面参考](pictures/09afedbeea3c12193e4c40b670233c1.png)

8. 申请模态
![申请模态](pictures/dd0e4ff87b8fb2eaf7fe6a1e946d359.png)

9. rebootModel是false的时候，再次打开仍然会显示之前输入的案件名等内容
![rebootModel](pictures/cb2eb459d9517ab54c92eff79ecb0e7.png)

#### 2 Aciton处理
10. action处理
![action处理](pictures/c538cc05f2fd7815d77fe215ac49de0.png)

11. 点击actionProcess1 填入图中内容
![actionProcess1](pictures/d94be00b7189af80cf3c815f2585b50.png)

12. action处理方法名
![action处理方法名](pictures/0b4747f791845513458477477938fc4.png)

13. action处理代码一般有两个参数 
- 第一个是保存有工作流信息的ActionProcessParameterInfo
- 第二个是保存有用户信息的userParameter

获得的用户信息参数 也就是申请内容 将在34-42行被保存到用于保存用户登记信息的对象中去 45会将数据登记到表中去
![获得的用户信息参数](pictures/e2dad8f733d038e7463035129bf669e.png)

14. 两种工作流数据
![两种工作流数据](pictures/2fcbb615f2d8938e95d68f96f901bfb.png)
![两种工作流数据](pictures/aae0ba961087ba615350d0b5d93c15b.png)

15. 在action处理中可以从工作流参数的ActionProcessParameterInfo中获得系统案件ID和用户数据ID（案件ID不会显示在页面上 另！案件编号不是唯一性的编号）

16. 申请案件 --> wrokflow --> 申请一览表 --> 差旅费申请 --> 进入脚本开发模式页面 依次填写 

17. wrokflow --> 案件一览表 --> 点击已处理（未完成）图标 --> 点击第二个详细内容图标

#### 3 临时保存 再申请页面

18. 本次培训已在内容定义中设置完成
![设置完成](pictures/443d4ba19c122bf61ed38fde9579381.png)

19. 被调用的时机
![调用](pictures/71d2570f341f21266dfc19fb50079b0.png)

20. 点击screen下的apply.js --> 代码参考 
![代码参考](pictures/27a2af15623f7b000b9f437c1633345.png)

21. 申请案件 --> wrokflow --> 申请一览表 --> 差旅费申请 --> 撤回并确定 --> 未处理 --> 点击处理 --> 再申请 

#### 4 学习要点
![学习要点](pictures/61f418af1f14c7e9dca132164de32f1.png)
![学习要点](pictures/9fdaea3d9949cf10208ca860ea68e63.png)
