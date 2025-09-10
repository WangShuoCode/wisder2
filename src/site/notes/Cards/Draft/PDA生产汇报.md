---
{"dg-publish":true,"permalink":"/Cards/Draft/PDA生产汇报/","tags":["江淮毅昌/蝶创I-MES/MES"]}
---



### 作业单界面
![Pasted image 20250910133956.png](/img/user/Extras/Attachments/Pasted%20image%2020250910133956.png)
![Pasted image 20250910134004.png](/img/user/Extras/Attachments/Pasted%20image%2020250910134004.png)


> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/生产作业单表\|生产作业单表]]、[[Cards/Draft/作业汇报单表\|作业汇报单表]]
> - 相关接口：

---

### 汇报页面

![Pasted image 20250910134154.png](/img/user/Extras/Attachments/Pasted%20image%2020250910134154.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/生产作业单表\|生产作业单表]]、[[Cards/Draft/作业汇报单表\|作业汇报单表]]
> - 相关接口：开始汇报(WorkReport.Start)、汇报单保存(WorkReport.Save)、SN/容器码 校验(WorkReport.NumberValidate)


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/Cards/Draft/PDA波次汇报/#sn" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### 扫描SN码校验接口

进入扫码界面后，用户开始扫码，每扫一次码，对SN码绑定物料进行校验。

- 获取SN码绑定的物料，及约束校验
	- 若无SN码未绑定物料，不进行任何约束
	- 校验位错误，拦截
	- 检测合格状态是否为合格
	- 检验库存状态为线边库
- 检测此SN码的库存是否处于线边仓
- 查询此物料是否在此作业单的生产订单明细行的生产用料清单的物料中，且此物料需为启用SN码管理
- 查询此作业单工序的类型，如为拆卸类型或组装类型，则需要扫描物料清单中所有启用SN码管理的物料，扫描后「已扫数量」+1

---

用户点击「上一项」/「下一项」按钮，保存当前扫描结果，生成「作业汇报单」。


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/Cards/Draft/PDA波次汇报/#" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### 波次汇报列表页面

![Pasted image 20250901180937.png](/img/user/Extras/Attachments/Pasted%20image%2020250901180937.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/作业波次表\|作业波次表]]
> - 相关接口：

显示当前登录人的工序且「开工日期」大于「今日」的波次单。

点击波次单卡片，进入波次单子设备序号为1的作业单详情。

---


</div></div>



---