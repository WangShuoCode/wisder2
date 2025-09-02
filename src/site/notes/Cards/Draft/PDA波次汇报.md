---
{"dg-publish":true,"permalink":"/Cards/Draft/PDA波次汇报/","tags":["江淮毅昌/蝶创I-MES/MES"]}
---


### 波次汇报列表页面

![Pasted image 20250901180937.png](/img/user/Extras/Attachments/Pasted%20image%2020250901180937.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/作业波次表\|作业波次表]]
> - 相关接口：

显示当前登录人的工序且「开工日期」大于「今日」的波次单。

点击波次单卡片，进入波次单子设备序号为1的作业单详情。

---

### 波次汇报界面

![Pasted image 20250901182223.png](/img/user/Extras/Attachments/Pasted%20image%2020250901182223.png)

> [!abstract] 页面信息
> - 相关表：[[Cards/Draft/SN码最新状态表\|bd_sn_base]]

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

#### 汇报单保存接口



- 更改SN码的物料为作业单物料
- 变更SN码的「合格状态」为待质检
- 清空SN码的「质检结果」
- 清空SN码的所属容器
- 变更SN码的「库位」为工序的汇报库位
- 变更绑定单据类型为汇报单、绑定单据编码
- 反写作业单、计划单、生产工单的已生产数量
- 将汇报人的班组与设备写入汇报单中
- 若此工序的检验控制为免检，则汇报单的合格数量等于汇报数量
	- 更改sn码的合格结果为合格状态

---

### 波次切换设备子项页面

图片

> [!abstract] 页面信息
> - 相关表：
> - 相关接口：

按照设备子项编码

---
<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="Drawing_2025-09-02_1358.34.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.15.1","elements":[{"id":"HzQZhgQ_YgP-Vd9p9joio","type":"rectangle","x":476.6144505739212,"y":222.59443664550784,"width":104.28640747070312,"height":103.41001892089841,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":"xGkrUzHwHDO7J0tADpvL_","index":"Zzl","roundness":null,"seed":427009766,"version":22,"versionNonce":1302389434,"isDeleted":false,"boundElements":null,"updated":1756792748696,"link":null,"locked":false},{"id":"xGkrUzHwHDO7J0tADpvL_","type":"frame","x":362.6881810426712,"y":178.77664184570312,"width":344.4079284667969,"height":247.1324462890625,"angle":0,"strokeColor":"#bbb","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a0","roundness":null,"seed":2137643558,"version":24,"versionNonce":56573414,"isDeleted":false,"boundElements":null,"updated":1756792748696,"link":null,"locked":false,"customData":{"frameColor":{"stroke":"#D4D4D4","fill":"#ADADAD","nameColor":"#7A7A7A"}},"name":null},{"id":"Jg6rdrL4NSMf_1Si1O7PX","type":"diamond","x":513.4214268922806,"y":559.9915161132812,"width":76.24298095703125,"height":105.1627197265625,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":"IPz033UV5GLuf_Ekqufda","index":"a0V","roundness":null,"seed":112698726,"version":27,"versionNonce":1403550586,"isDeleted":false,"boundElements":null,"updated":1756792748696,"link":null,"locked":false},{"id":"IPz033UV5GLuf_Ekqufda","type":"frame","x":388.97886097431183,"y":524.0609130859375,"width":332.138916015625,"height":202.43829345703125,"angle":0,"strokeColor":"#bbb","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a1","roundness":null,"seed":1353320614,"version":19,"versionNonce":1976209702,"isDeleted":false,"boundElements":null,"updated":1756792748696,"link":null,"locked":false,"customData":{"frameColor":{"stroke":"#D4D4D4","fill":"#ADADAD","nameColor":"#7A7A7A"}},"name":null},{"id":"SLXeuF88B3OLtblvCxjk0","type":"frame","x":408.25867664813995,"y":787.8440768879226,"width":291.8265686035156,"height":237.49249267578136,"angle":0,"strokeColor":"#bbb","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a2","roundness":null,"seed":1290666982,"version":29,"versionNonce":247397434,"isDeleted":false,"boundElements":null,"updated":1756792748696,"link":null,"locked":false,"customData":{"frameColor":{"stroke":"#D4D4D4","fill":"#ADADAD","nameColor":"#7A7A7A"}},"name":null},{"id":"WlxEKtTta1qUaZtBmklIY","type":"frame","x":416.1459141969681,"y":1153.2845805172835,"width":301.46649169921875,"height":388.2257385253906,"angle":0,"strokeColor":"#bbb","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":0,"opacity":100,"groupIds":[],"frameId":null,"index":"a3","roundness":null,"seed":1838192422,"version":19,"versionNonce":2112453734,"isDeleted":false,"boundElements":null,"updated":1756792748696,"link":null,"locked":false,"customData":{"frameColor":{"stroke":"#D4D4D4","fill":"#ADADAD","nameColor":"#7A7A7A"}},"name":null},{"id":"3Pk0okEJ","type":"text","x":529.0004063844681,"y":349,"width":8,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":"xGkrUzHwHDO7J0tADpvL_","index":"Zz","roundness":null,"seed":2003706790,"version":3,"versionNonce":1615458854,"isDeleted":true,"boundElements":null,"updated":1756792736766,"link":null,"locked":false,"text":"","rawText":"","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"","autoResize":true,"lineHeight":1.25},{"id":"buBTPrrb","type":"text","x":504.0004063844681,"y":256,"width":8,"height":25,"angle":0,"strokeColor":"#1e1e1e","backgroundColor":"transparent","fillStyle":"solid","strokeWidth":2,"strokeStyle":"solid","roughness":1,"opacity":100,"groupIds":[],"frameId":"xGkrUzHwHDO7J0tADpvL_","index":"ZzV","roundness":null,"seed":99099834,"version":3,"versionNonce":731758138,"isDeleted":true,"boundElements":null,"updated":1756792737613,"link":null,"locked":false,"text":"","rawText":"","fontSize":20,"fontFamily":5,"textAlign":"left","verticalAlign":"top","containerId":null,"originalText":"","autoResize":true,"lineHeight":1.25}],"appState":{"theme":"light","viewBackgroundColor":"#ffffff","currentItemStrokeColor":"#1e1e1e","currentItemBackgroundColor":"transparent","currentItemFillStyle":"solid","currentItemStrokeWidth":2,"currentItemStrokeStyle":"solid","currentItemRoughness":0,"currentItemOpacity":100,"currentItemFontFamily":5,"currentItemFontSize":20,"currentItemTextAlign":"left","currentItemStartArrowhead":null,"currentItemEndArrowhead":"arrow","currentItemArrowType":"round","currentItemFrameRole":null,"scrollX":0,"scrollY":-2.842170943040401e-14,"zoom":{"value":1},"currentItemRoundness":"sharp","gridSize":20,"gridStep":5,"gridModeEnabled":false,"gridColor":{"Bold":"rgba(217, 217, 217, 0.5)","Regular":"rgba(230, 230, 230, 0.5)"},"currentStrokeOptions":null,"frameRendering":{"enabled":true,"clip":true,"name":true,"outline":true,"markerName":true,"markerEnabled":true},"objectsSnapModeEnabled":false,"activeTool":{"type":"selection","customType":null,"locked":false,"fromSelection":false,"lastActiveTool":null}},"files":{}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("Drawing_2025-09-02_1358.34.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>