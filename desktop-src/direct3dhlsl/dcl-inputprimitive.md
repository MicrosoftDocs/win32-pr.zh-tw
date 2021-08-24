---
title: 'dcl_inputPrimitive (sm4-asm) '
description: 'dcl \_ inputPrimitive (sm4-asm) '
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479894"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>dcl \_ inputPrimitive (sm4-asm) 

宣告幾何著色器輸入的基本類型。



| dcl \_ inputPrimitive *類型* |
|----------------------------|



 




| 項目 | 描述 | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>類型</em><br /> | 在輸入-資料基本類型，這是下列其中一項： <br /><ul><li><em>點</em> 點清單</li><li><em>行</em> 行清單</li><li><em>三角形</em> -三角形清單</li><li>具有相鄰資料的<em>line_adj</em>行清單</li><li>具有相鄰資料的<em>triangle_adj</em>三角形清單</li></ul> | 




 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_inputPrimitive triangle
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

 

 





