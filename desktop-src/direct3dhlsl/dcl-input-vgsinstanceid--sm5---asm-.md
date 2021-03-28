---
title: 'dcl_input vGSInstanceID (sm5-asm) '
description: 啟用幾何著色器實例。
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313761"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>dcl \_ 輸入 vGSInstanceID (sm5-asm) 

啟用幾何著色器實例。



| dcl \_ 輸入 vGSInstanceID、instanceCount |
|-----------------------------------------|



 



| 項目                                                                                                                       | 描述                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*<br/> | \[在 \] 實例識別碼中。<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[在 \] 實例計數中。<br/> |



 

## <a name="remarks"></a>備註

宣告的 *instanceCount* 參數會指定幾何著色器應該針對每個輸入基本類型執行多少個實例。 *InstanceCount* 的最大值是32。

透過 [**dcl \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md)針對輸出宣告的最大頂點數目，會個別套用至每個實例。

此宣告中的實例計數（乘以透過 [**\_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md)的每個實例最大頂點計數）必須是 <= 1024。

給定幾何著色器實例可以發出的資料量是1024的最大值，並藉由計算針對輸入所宣告的所有純量，並乘以宣告的輸出頂點計數來進行驗證。

使用幾何著色器實例，可有效地增加每個輸入基本資料可發出的總數據量。 針對單一實例的1024純量，會產生 \* 單一輸入基本的所有幾何著色器實例之輸出資料的最高 1024 32 純量。 不過，實例越多，每個實例可以發出的頂點就越少。 單一實例 (沒有可發出1024頂點的實例) 。 如果您宣告 \* 32 實例，表示每個實例只能輸出 1024/32 = 32 頂點。

幾何著色器實例宣告可讓程式使用獨立的32位整數輸入暫存器 *vGSInstanceID*。 每個幾何著色器實例都是以 *vGSInstanceID* \[ 0，1，2中包含的值來 \] 識別。

*vGSInstanceID* 不是幾何著色器輸入頂點陣列的一部分 (例如，在輸入三角形) 時，會有3個頂點。 *VGSInstanceID* 註冊本身會有其本身，例如 vPrimitiveID。

當每個幾何著色器實例結束時，輸出拓撲中會有隱含的剪下，因此連續的實例不會彼此相依。

雖然硬體可能會以平行方式執行每個幾何著色器實例，但最後的所有實例的輸出會序列化，就像是將 *vGSInstanceID* 從0逐一查看到 *instanceCount*-1 的迴圈中，會在每個實例結束時，將隱含的輸出拓朴剪下。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





