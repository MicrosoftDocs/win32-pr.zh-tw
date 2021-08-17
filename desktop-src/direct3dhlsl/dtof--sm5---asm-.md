---
title: 'dtof (sm5-asm) '
description: 從雙精確度浮點數轉換成單精確度浮點數據的元件取向轉換。
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d16ddf79b1a201bf78e0b45d1206169576bee4193b8c8158469055131768efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792325"
---
# <a name="dtof-sm5---asm"></a>dtof (sm5-asm) 

從雙精確度浮點數轉換成單精確度浮點數據的元件取向轉換。



| dtof dest \[ . mask \] 、 \[ - \] src \[ . swizzle \] 、 |
|-------------------------------------------|



 



| 項目                                                            | 描述                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[已 \] 轉換資料的位址。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要轉換的資料中。<br/>          |



 

## <a name="remarks"></a>備註

來源的每個元件都會使用四捨五入到最接近的舍入，從雙精確度表示轉換成單精確度標記法。

來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。

有效的 *目的地* 遮罩是任何一或兩個元件。 亦即：. x、. y、. z、w、xy、. xw、. yz、. yw、. zw 第一個轉換的結果會移至遮罩中的第一個元件，而第二個元件的結果會移至遮罩中的第二個元件（如果有的話）。

*dest* 元件是 float32。

*src* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) post swizzle 的雙 vec2。

針對 float32<->雙精度浮點數轉換，執行可能會接受 denorms 或清除它們。

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

 

 





