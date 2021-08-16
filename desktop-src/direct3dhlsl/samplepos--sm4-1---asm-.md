---
title: 'samplepos (sm 4.1-asm) '
description: 查詢指定之著色器資源檢視或轉譯器中範例的位置。
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2457ca682adacf5daa274b3efbe6c76eb37523df4267cdb20131576815c2b6f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510162"
---
# <a name="samplepos-sm41---asm"></a>samplepos (sm 4.1-asm) 

查詢指定之著色器資源檢視或轉譯器中範例的位置。



| samplepos dest \[ . mask \] ，srcResource \[ . swizzle \] ，sampleIndex (純量運算元)  |
|--------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在 \] 著色器資源中。<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[在 \] 範例的索引中。<br/>                     |



 

## <a name="remarks"></a>備註

此指令會針對指定的資源傳回範例 *sampleIndex* 的2d 樣本位置。 它只適用于可以使用 [**ld2dms**](ld2dms--sm4-1---asm-.md) 載入的資源，除非轉譯器已指定為 *srcResource*。

*srcResource* 可以是 \# (著色器資源檢視) 或轉譯器註冊的 t 註冊。

指令會計算浮點數向量 (Xposition、Yposition、0、0) 。

*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。 樣本位置是相對於圖元的中心（以圖元座標系統為基礎）。

如果 *sampleIndex* 超出範圍，則會傳回零向量。 如果沒有任何資源系結至指定的位置，則會傳回0。

**samplepos** 可用於自訂程式碼中所解析的自訂專案。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





