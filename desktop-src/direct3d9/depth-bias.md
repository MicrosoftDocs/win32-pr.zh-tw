---
description: 在3D 空間中有共置的多邊形，可以像是在每個多邊形都不是共置的多邊形一樣地顯示。
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: " (Direct3D 9) 的深度偏差"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467652"
---
# <a name="depth-bias-direct3d-9"></a> (Direct3D 9) 的深度偏差

在3D 空間中有共置的多邊形，可以像是在每個多邊形都不是共置的多邊形一樣地顯示。 這項技術通常用來確保場景中的陰影正確顯示。 例如，牆上的陰影可能會有與牆相同的深度值。 如果您先轉譯牆，然後再呈現陰影，則可能看不到陰影，或是可見的深度成品。 您可以反轉呈現共面對象的順序，以避免反轉效果，但深度成品仍然很有可能。

應用程式可以藉由在轉譯共置多邊形的集合時，將偏差新增至系統所用的 z 值，以協助確保會正確轉譯共置多邊形。 若要將 z 偏差加入至一組多邊形，請在轉譯之前呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，將 *State* 參數設定為 D3DRS \_ DEPTHBIAS，並將 *Value* 參數設定為適當的 float 值 (例如，適當的值可能是從-1.0 到 1.0) ; 若要將此值轉換成 **graphicsdevice**，您也必須將值轉換成 **DWORD**。 較高的 z 偏差值會增加當您顯示的多邊形與其他共置多邊形時，所呈現的多邊形可能會顯示的可能性。


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



其中 m 是所呈現三角形的最大深度斜率。


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



D3DRS \_ DEPTHBIAS 和 D3DRS SLOPESCALEDEPTHBIAS 轉譯狀態的單位 \_ 取決於是否已啟用 z 緩衝處理或 w 緩衝處理。 應用程式必須提供適當的值。

偏差不會套用至任何線條和點基本。 不過，這個偏差必須套用至以線框模式繪製的三角形。


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 
