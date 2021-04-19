---
description: Direct3D 同時支援平面和 Gouraud 陰影。 預設值為 Gouraud 網底。 若要控制目前的陰影模式，您的 c + + 應用程式會為 D3DRS SHADEMODE 轉譯狀態指定 D3DSHADEMODE 列舉類型的成員 \_ 。
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: " (Direct3D 9) 的陰影狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991599"
---
# <a name="shading-state-direct3d-9"></a> (Direct3D 9) 的陰影狀態

Direct3D 同時支援平面和 Gouraud 陰影。 預設值為 Gouraud 網底。 若要控制目前的陰影模式，您的 c + + 應用程式會為 D3DRS SHADEMODE 轉譯狀態指定 [**D3DSHADEMODE**](./d3dshademode.md) 列舉類型的成員 \_ 。

下列 c + + 程式碼範例示範將陰影狀態設定為平面陰影模式的程式。


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
