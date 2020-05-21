# -信息化平台需求分析
一、	需求概述
1.	编写目的
编写文档有两个目的，一个是便于和用户的需求达成共识；另一个是让开发人员更好的了解需求情况
2.	需求更新记录
1	需求描述	上线时间
2	展示项目进度，付款进度，项目重要程度	2020.05.11
3	项目全周期管理，多部门无纸化信息化办公	待开发

二、	项目综述
1.	技术平台
使用了.NET CORE 3.1平台中的Razor Page模式，数据库使用了SQL Server 2014，ORM工具使用了EF CORE，UI框架使用了Bootstarp
2.	用例图
 
3.	对象设计
1)	Department（枚举）

字段	DepartmentId	DepartName
类型	Int	string
备注	部门ID	部门名

2)	Role（枚举）
字段	RoleId	RoleName
类型	Int	String
备注	角色ID	角色名

3)	User（用户表）
字段	UserId	LoginName	Name	Password	Role	Department
类型	Int	String	String	String	Role	Depatrment
备注	用户ID	登录名	名字	Password	角色	部门

4)	Stage（枚举）
字段	StageId	StageName
类型	Int	String
备注	阶段ID	阶段名

5)	Work（项目表）
序号	字段	类型	备注
1	WorkId	Int	项目ID
2	Name	String	项目名
3	Responsibler	String	负责人
4	Department	Department	生产所室
5	Client	String	委托单位
6	Type	String	类型
7	Scale	String	规模
8	IfHaveContract	Boolen	是否签合同
9	ContractNum	Int	合同编号
10	Amount	Int	金额
11	Level	Level	重要程度
12	Stage	Stage	项目阶段
13	Days	Int	天数
14	FirstTime	Datetime	进场时间
15	TechnicalReviewTime	Datetime	技术大纲时间
16	FirstScheme	Datetime	初案编制时间
17	Scheme	Datetime	成果编制时间
18	OutAchievement	Datetime	归档时间
6)	Level（枚举）
字段	LevelId	LevelName
类型	Int	String
备注	重要程度	重要程度

7)	Payment（收款计划表）
字段	PaimentId	Work	约定时间	开票人	开票时间	实践时间
类型	Int	Work				string
备注	ID	项目				部门名

4.	项目管理流程图
 
