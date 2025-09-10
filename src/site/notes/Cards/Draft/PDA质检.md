---
{"dg-publish":true,"permalink":"/Cards/Draft/PDA质检/","tags":["江淮毅昌/蝶创I-MES/MES"]}
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



---

### 全检页面

![Pasted image 20250910161530.png](/img/user/Extras/Attachments/Pasted%20image%2020250910161530.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/缺陷原因表\|qc_ng]]、[[Cards/Draft/质检类型结果表\|qc_type_result]]、[[Cards/Draft/工艺路线-工序-质量控制表\|pm_route_step_qc]]
> - 相关接口：



---
### 质检单生成接口

生成质检单

- 质检单生成编码
- 记录前端选择的「质检类型」
- 记录前端选择的「班组」
- 「质检类型」为「抽检」「质检数」等于质检时容器数量，「质检类型」为「全检」「质检数」为1
- 「抽检数」为抽检扫描SN码并选择了质检结果的数量

更新SN码状态

- 更新SN码

反写汇报单、作业单

- 