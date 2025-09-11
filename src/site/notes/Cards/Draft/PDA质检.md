---
{"dg-publish":true,"permalink":"/Cards/Draft/PDA质检/","tags":["蝶创I-MES/MES/江淮毅昌"]}
---


### 质检单列表

![Pasted image 20250910161411.png](/img/user/Extras/Attachments/Pasted%20image%2020250910161411.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/质检单表\|质检单表]]、[[Cards/Draft/SN码单据关联表\|SN码单据关联表、bd_sn_link\_{qc_bill/pm_bill/ww_bill}]]
> - 相关接口：

---

### 选择质检类型页面

![Pasted image 20250910161422.png](/img/user/Extras/Attachments/Pasted%20image%2020250910161422.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/质检类型表\|质检类型表]]
> - 相关接口：

---

### 抽检页面

![Pasted image 20250910161952.png](/img/user/Extras/Attachments/Pasted%20image%2020250910161952.png)

> [!abstract] 页面信息
> - 相关表：
> - 相关接口：

扫描容器码

- 获取此容器物料个数

扫描SN码

- 扫描后跳转到SN码详情页面

选择单个SN码质检结果

- 选择质检结果，选择缺陷原因

选择整容器质检结果

- 若已提交SN码的质检结果存在有「不合格」，则整容器质检结果限制只能选择「不合格的」

提交

---

### 全检页面

![Pasted image 20250910161530.png](/img/user/Extras/Attachments/Pasted%20image%2020250910161530.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/缺陷原因表\|qc_ng]]、[[Cards/Draft/质检类型结果表\|qc_type_result]]、[[Cards/Draft/工艺路线-工序-质量控制表\|pm_route_step_qc]]

扫描SN码进行校验

- 校验SN码
- 若SN码「合格状态」不为「待质检」，进行提醒
- 若上一SN码未提交，用户扫描新的SN码，进行拦截

选择质检结果

- 「质检结果」为「不合格」的，必须选择「缺陷原因」（多选）

提交

- 生成【质检单】
- 刷新页面

---

### 质检单生成接口

生成质检单

- 质检单生成编码
- 记录前端选择的「质检类型」
- 记录前端选择的「班组」
- 「质检类型」为「抽检」「质检数」等于质检时容器数量，「质检类型」为「全检」「质检数」为1
- 「抽检数」为抽检扫描SN码并选择了质检结果的数量

更新SN码状态

- 更新SN码的「质检结果」等于质检单选择的「质检结果」
- 更新SN码「合格状态」
	- 如「质检类型」的结果是最终合格，则「合格状态」为合格，如非最终合格，合格状态依旧为待质检

反写上游单据

- 待确定：是否需要反写生产「合格数量」与「不合格数量」