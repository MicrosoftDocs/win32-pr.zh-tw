---
title: 'deriv_rtx_fine (sm5-asm) '
description: '計算元件變更的速率。 |deriv_rtx_fine (sm5-asm) '
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6666750be76d673ddc6c5f0d66d23131096812c93b71be52eb7e0f6ebb403ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792650"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>deriv \_ rtx \_ 良好 (sm5-asm) 

計算元件變更的速率。



| deriv \_ rtx \_ 精細的 \[ \_ sat： \] \[ mask \] 、 \[ - \] src0 \[ \_ abs \] \[ swizzle \] 、 |
|--------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在作業 \] 的元件中。<br/>             |



 

## <a name="remarks"></a>備註

此指令會計算 *src0* 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向 (請參閱 [deriv \_ rty \_ 精細](deriv-rty-fine--sm5---asm-.md)) 。 2x2 戳記中的每個圖元都會取得一組獨特的 x/y 衍生計算

目前圖元著色器調用中的資料一律會參與所要求之衍生的計算。 在2x2 圖元中，目前的圖元落在四個圖元的範圍內，x 衍生是2圖元的資料列差異，包括目前的圖元。 Y 衍生資料行的差異是2圖元的資料行，包括目前的圖元。 您不會在基本的情況上聽寫2x2 四邊形如何對齊或並排顯示。

衍生的計算方式為精細層級 (2x2 四) 中每個圖元的 x/y 衍生配對的唯一計算。 這個指令和 [deriv \_ rty \_ ](deriv-rty-fine--sm5---asm-.md) 是 [deriv \_ rtx \_ 粗略](deriv-rtx-coarse--sm5---asm-.md) 和 [deriv \_ rty \_ 粗略](deriv-rty-coarse--sm5---asm-.md)的替代方案。 這些 \_ 粗略和 \_ 精細的 **deriv \_ rtx** 取代了這些 \_ 粗略和 \_ 精細的說明，是從先前的著色器模型取代 **deriv \_ rtx** 和 **deriv \_ rty** 。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





