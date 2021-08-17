---
title: 'dmin (sm5-asm) '
description: 元件的雙精確度最小值。
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20977a24113db111e85bc644ed68eccaa7e75db91c18bf71d80ac89f5ee19547
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855118"
---
# <a name="dmin-sm5---asm"></a>dmin (sm5-asm) 

元件的雙精確度最小值。



| dmin \[ \_ sat \] dest \[ . mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> *目的地*  = *src0*  < *src1* 嗎？ *src0* ： *src1*<br/> < 是用來取代 <=，因此，如果 min (x，y) = x， (x，y) = y。 <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要與 *src1* 比較的元件中。<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要與 *src0* 比較的元件中。<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>備註

NaN 具有特殊處理。 如果一個來源運算元為 NaN，則會傳回另一個來源運算元。 選擇是依元件進行。 如果兩者都是 NaN，則會傳回任何 NaN 表示。

來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。 有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。 以下是 swizzle 後的 *src* 對應：

-   *dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。
-   *src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。
-   *src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 否        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





