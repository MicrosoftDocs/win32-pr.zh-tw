---
title: 'dcl_temps (sm4-asm) '
description: 'dcl \_ 溫度 (sm4-asm) '
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6426caff8ecd347ce8233f15df6b914a53c647ae79fb50a530b531e9207bf1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726806"
---
# <a name="dcl_temps-sm4---asm"></a>dcl \_ 溫度 (sm4-asm) 

宣告暫存暫存器。



| dcl \_ 溫度 N |
|--------------|



 



| 項目                                                   | 描述                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N-1*<br/> | \[暫存登錄的 \] 數目。<br/> |



 

每個註冊程式都有一個32位的四元件值空間。 暫存和可 [編制索引](dcl-indexabletemp.md) 的暫存暫存器總數必須小於或等於4096。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_temps 10; // Declare r0-r9
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

 

 





