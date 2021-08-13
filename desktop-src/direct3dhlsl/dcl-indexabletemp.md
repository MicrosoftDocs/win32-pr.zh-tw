---
title: 'dcl_indexableTemp (sm4-asm) '
description: 'dcl \_ indexableTemp (sm4-asm) '
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f1d6e02b36daef0643910d69404adc0973ebbcf6370ae5f5c11ad2aa7bd3480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793444"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>dcl \_ indexableTemp (sm4-asm) 

宣告可編制索引的臨時暫存器。



| dcl \_ indexableTemp x *N \[ 大小 \] ，ComponentCount* |
|-------------------------------------------------|



 



| Item                                                                                                                           | 描述                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N-1*<br/>                                                                         | \[\]代表註冊編號的整數。<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[大小\]*<br/>                                                        | \[在 \] 選擇性的整數值中。 暫存器陣列中的元素數目。<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[在 \] 選擇性的整數值中。暫存器陣列中的元件數目。<br/> |



 

暫存器包含足夠的空間來容納32位的四個元件值;臨時暫存器陣列中的元素數目 (可編制索引和 [不可索引](dcl-temps.md) 的) 不能超過4096。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

以下是針對可編制索引的暫存器所產生之程式碼的一些範例。


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





