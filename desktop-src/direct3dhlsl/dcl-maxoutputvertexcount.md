---
title: 'dcl_maxOutputVertexCount (sm4-asm) '
description: 'dcl \_ maxOutputVertexCount (sm4-asm) '
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba7783575ac5782c63bc1ec3ca5f56f6ffe9a1bc7483f3f01ccbcf8adac5e23f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068518"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>dcl \_ maxOutputVertexCount (sm4-asm) 

宣告幾何著色器可以輸出的最大頂點數目。



| dcl \_ maxOutputVertexCount *計數* |
|-----------------------------------|



 



| 項目                                                               | 描述                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*計數*<br/> | \[在 \] 1 到 n （含）之間的32位不帶正負號的整數。<br/> |



 

幾何著色器最多可以輸出 1024 32 位值。 此最大值包含輸入資料的大小，以及著色器所建立之資料的大小。

以下是一些限制：

-   如果在幾何著色器完成執行之前已到達頂點數目，著色器就會終止。
-   幾何著色器在輸出任何頂點之前，可以到達其程式的結尾;這是完全合法的。
-   如果您正在進行幾何著色器的偵錯工具，您可以藉由計算產生的發出指令數目來判斷所產生的頂點數目。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

以下是一些範例。

假設輸入資料是由 position ( xyzw) 和 color ( rgb) 。 每個元件都會耗用一個位元組;如果有7個位元組，著色器可以產生的最大頂點數目是 1024/ (4 + 3) = 146。


```
dcl_maxOutputVertexCount 146
```



假設您的幾何著色器會建立 32 4 元件向量。 著色器可以產生的最大頂點數目是 1024/ (32 \* 4) = 8。


```
dcl_maxOutputVertexCount 8
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

 

 





