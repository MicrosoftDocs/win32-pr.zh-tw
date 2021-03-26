---
title: 'dcl_tgsm_structured (sm5-asm) '
description: 宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。 記憶體會被視為結構的陣列。
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990743"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>dcl \_ tgsm \_ 結構化 (sm5-asm) 

宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。 記憶體會被視為結構的陣列。



| dcl \_ tgsm \_ 結構化 g \# 、structByteStride、structCount |
|----------------------------------------------------------|



 



| 項目                                                                                                                                   | 描述                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                                             | \[在 \] *structByteStride* \* *structCount* 位元組大小之共用記憶體區塊的參考中。 <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[在 \] 結構 stride 中。 這個值是以位元組為單位的單位，而且必須是4的倍數。 <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[\]結構的數目。<br/>                                                                   |



 

## <a name="remarks"></a>備註

所有 g 的總儲存空間 \# 必須 <= 每個執行緒群組可用的共用記憶體量（32kB）或 8192 32 位的純量。

在極端情況下， \# 如果每個 g s 的 *structByteStride* 為4，而 *structCount* 為1，則您可以宣告 8192 total g s。

相反地，您可以 \# 使用32kB 的結構 stride 和結構計數1來宣告單一 g。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





