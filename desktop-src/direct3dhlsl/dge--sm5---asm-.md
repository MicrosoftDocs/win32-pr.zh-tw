---
title: 'dge (sm5-asm) '
description: 元件的雙精確度雙精確度大於或等於比較。
ms.assetid: 2E769077-E861-4EFA-817F-7D1AE998746C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508354affbabe1ebab70be31ab45f0e7f80d0765
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022802"
---
# <a name="dge-sm5---asm"></a>dge (sm5-asm) 

元件的雙精確度雙精確度大於或等於比較。



| dge \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | 要與 *src1* 比較的元件。<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | 要與 *src0* 比較的元件。<br/>                |



 

## <a name="remarks"></a>備註

此指令會針對每個元件執行雙精確度浮點數比較 (*src0*  >=  *src1*) ，然後將結果寫入至 *目的地*。

如果比較結果為 true，則會傳回該元件的32位0xFFFFFFFF。 否則會傳回32位0x00000000。

與 NaN 的比較會傳回 false。

有效的 *目的地* 遮罩是任何一或兩個元件。 亦即：. x、. y、. z、w、xy、xw、. yz、. yw、. zw 遮罩中的第一個 *目的地* 元件會收到第一個雙重比較的32位結果。 遮罩中的第二個元件（如果有的話）會接收第二個雙重比較的32位結果。

來源參數的有效 swizzles 為. xyzw、. xyxy、. zwxy、. zwzw。 以下是 swizzle 後的 *src* 對應：

-   *src0* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。
-   *src1* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙重 vec2。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





