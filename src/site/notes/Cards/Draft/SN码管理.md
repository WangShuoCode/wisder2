---
{"dg-publish":true,"permalink":"/Cards/Draft/SN码管理/","tags":["江淮毅昌/蝶创I-MES/MES"]}
---


### 列表页面

![Pasted image 20250820134731.png](/img/user/Extras/Attachments/Pasted%20image%2020250820134731.png)


> [!abstract] 页面信息
> - 展示表：[[Cards/Draft/SN码最新状态表\|SN码最新状态表]]、[[Cards/Draft/SN码日志表\|SN码日志表]]、[[Cards/Draft/SN码单据关联表\|SN码单据关联表]]
> - 接口列表
> 	- 生成
> 		- 按照`SN`+七位字符+校验位生成
> 		- 校验位生成
> 			- 将 36 个字符映射到数字
> 			- 给每个位置一个固定权重2, 3, 5, 7, 11, 13, 17（用质数）
> 			- 把每一位字符映射成数字，再乘以对应权重，加总起来。
> 			- 用 36 取模
> 			- 把这个整数再转回 0–9 / A–Z，对应第八位校验位。
> 	- 校验
> 		- 先看传入的字符串是不是 8 位，不是就直接判 False
> 		- 分离数据与校验位
> 			- 调用计算校验的函数，得到期望值
> 			- 做对比
> 	- 物料绑定接口（通用接口）
> 		- 传入单据类型、单据id、物料id


---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/Extras/Excalidraw/测试画布文件/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





==⚠ Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'

# Excalidraw Data

## Text Elements


</div></div>
