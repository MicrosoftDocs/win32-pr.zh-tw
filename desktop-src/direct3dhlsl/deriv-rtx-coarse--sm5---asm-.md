---
title: 'deriv_rtx_coarse (sm5-asm) '
description: '計算元件變更的速率。 |deriv_rtx_coarse (sm5-asm) '
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991922"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>deriv \_ rtx \_ 粗略 (sm5-asm) 

計算元件變更的速率。



| deriv \_ rtx \_ 粗略 \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle \] 、 |
|----------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在作業 \] 的元件中。<br/>             |



 

## <a name="remarks"></a>備註

此指令會計算 *src0* 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向 (請參閱 [deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md)) 。 每個2x2 的圖元戳記都只會計算單一 x、y 衍生配對。

目前圖元著色器調用中的資料不一定會參與要求之衍生的計算，因為每個2x2 四次的衍生只會計算一次。 例如，x 導數可能是最上層資料列的差異，而 y 方向 ([deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md)) 可能是來自圖元左邊資料行的差異。 確切的計算是由硬體廠商所組成。 此外，也不會有任何規格會聽寫2x2 四邊形如何對齊或在基本型別上並排顯示。

衍生會以粗略的層級計算，每個2x2 圖元四次。 這個指令和 [deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md) 是 [deriv \_ rtx \_ 精細](deriv-rtx-fine--sm5---asm-.md) 和 [deriv \_ rty \_ ](deriv-rty-fine--sm5---asm-.md)的替代方案。 這些 \_ 粗略和 \_ 精細的說明，是從先前的著色器模型中 **deriv \_ rtxderiv \_ rty** 的替代方案。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





