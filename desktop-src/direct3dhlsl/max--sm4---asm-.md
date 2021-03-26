---
title: 'max (sm4-asm) '
description: 元件的最大浮點數。
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373722"
---
# <a name="max-sm4---asm"></a>max (sm4-asm) 

元件的最大浮點數。



| 最大 \[ \_ sat \] 目的地 \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、 |
|---------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。 <br/> *目的地*  = *src0*  >= *src1* 嗎？ *src0* ： *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] [要與 *src1* 比較的元件] 中。<br/>                                                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] [要與 *src0* 比較的元件] 中。<br/>                                                    |



 

## <a name="remarks"></a>備註

>= 會用來取代 >，因此，如果 min (x、y) = x，則 (x，y) = y 的上限。

NaN 具有特殊處理。 如果一個來源運算元為 NaN，則會傳回另一個來源運算元，並依元件進行選擇。 如果兩者都是 NaN，則會傳回任何 NaN 表示。

在進行比較之前，會先將 Denorms 排清並保留正負號。 不過，寫入至 *目的地* 的結果不一定會 denorm 排清。

下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。 F 表示有限的實數。



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| **src0 src1->** | **-inf** | **F**        | **+ inf** | **NaN** |
| **-inf**           | -inf     | src1         | +inf     | -inf    |
| **F**              | src0     | src0 或 src1 | +inf     | src0    |
| **+ inf**           | +inf     | +inf         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





