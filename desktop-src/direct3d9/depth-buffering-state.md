---
description: 深度緩衝是移除隱藏行和表面的方法。 根據預設，Direct3D 不會使用深度緩衝。
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: ) 的深度緩衝狀態 (Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467650"
---
# <a name="depth-buffering-state-direct3d-9"></a>) 的深度緩衝狀態 (Direct3D 9

深度緩衝是移除隱藏行和表面的方法。 根據預設，Direct3D 不會使用深度緩衝。

如需深度緩衝區的概念總覽，請參閱 [ (Direct3D 9) 的深度緩衝區 ](depth-buffers.md)。

C + + 應用程式會 \_ 使用 [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) 列舉的成員指定新的狀態值，以 D3DRS ZENABLE 轉譯狀態來更新深度緩衝狀態。

如果您的應用程式需要防止 Direct3D 寫入深度緩衝區，它可以使用 D3DRS \_ ZWRITEENABLE 列舉值，指定 D3DZB \_ FALSE 做為呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)的第二個參數。

下列程式碼範例示範如何將深度緩衝區狀態設定為啟用 z 緩衝。


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



您的應用程式也可以使用 D3DRS \_ ZFUNC 轉譯狀態，來控制 Direct3D 在執行深度緩衝時所使用的比較函數。

Z-偏差是在另一個表面上顯示一個表面的方法，即使它們的深度值相同也一樣。 您可以將這項技術用於各種效果。 常見的範例是在牆上呈現陰影。 陰影和牆都有相同的深度值。 不過，您想要讓應用程式顯示牆上的陰影。 對陰影提供 z 偏差，讓 Direct3D 適當地顯示 (請參閱 D3DRS \_ DEPTHBIAS) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
