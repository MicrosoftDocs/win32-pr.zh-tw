---
description: 畫面格緩衝區 blender 現在可以混合 Alpha 通道，而不會與呈現目標上的色頻混合。 此控制項已啟用新的轉譯狀態 D3DRS \_ SEPARATEALPHABLENDENABLE。
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: '轉譯目標 Alpha (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5d4701b2d09334d605cf2c90ef0e03b06ea7886ea875ce8ec8ff9cbc428ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797933"
---
# <a name="render-target-alpha-direct3d-9"></a>轉譯目標 Alpha (Direct3D 9) 

畫面格緩衝區 blender 現在可以混合 Alpha 通道，而不會與呈現目標上的色頻混合。 此控制項已啟用新的轉譯狀態 D3DRS \_ SEPARATEALPHABLENDENABLE。

當 D3DRS \_ SEPARATEALPHABLENDENABLE 設定為 **FALSE** (預設條件為) 時，套用至 Alpha 的轉譯目標混色因數和作業與針對混色色頻所定義的不同。 驅動程式必須設定 D3DPMISCCAPS \_ SEPARATEALPHABLEND cap，以指出它可以支援轉譯目標 Alpha 混合。 請務必啟用 D3DRS \_ ALPHABLEND，告知管線需要進行 Alpha 混色。

若要控制轉譯目標 blenders 之 Alpha 通道中的因素，會定義兩個新的轉譯狀態，如下所示：


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



如同 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND，這些都可以設定為 [**D3DBLEND**](./d3dblend.md) 列舉中的其中一個值。 來源和目的地 blend 設定可以用數種方式結合，視 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 SrcBlendCaps 和 DestBlendCaps 成員中的設定而定。

Alpha 混合的完成方式如下：

renderTargetAlpha = 在 srcBlendOp<sub>中</sub> (Alpha \*) BlendOp (Alpha<sub>rt</sub> \* destBlendOp) 

其中：

-   <sub>中</sub>的 Alpha 是輸入 Alpha 值。
-   srcBlendOp 是 [**D3DBLEND**](./d3dblend.md)中的其中一個 blend 因素。
-   BlendOp 是 [**D3DBLENDOP**](./d3dblendop.md)中的其中一個 blend 因素。
-   Alpha<sub>rt</sub> 是呈現目標的 Alpha 值。
-   destBlendOp 是 [**D3DBLEND**](./d3dblend.md)中的其中一個 blend 因素。
-   renderTargetAlpha 是最終的混合 Alpha 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Alpha 混色](alpha-blending.md)
</dt> </dl>

 

 
