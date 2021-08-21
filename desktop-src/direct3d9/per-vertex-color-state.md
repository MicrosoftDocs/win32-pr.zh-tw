---
description: 如果您告訴執行時間有資料，Direct3D 光源引擎可以在執行光源時使用每個頂點的色彩資料。
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: 'Per-Vertex 色彩狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6efd227c64785f7399ae3ba56d4623342c0910d901c3cfc404fc4a37f0d233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727981"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Per-Vertex 色彩狀態 (Direct3D 9) 

如果您告訴執行時間有資料，Direct3D 光源引擎可以在執行光源時使用每個頂點的色彩資料。 這是藉由開啟下列呈現狀態來完成的：


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



如果啟用了每個頂點的色彩，則應用程式可以設定來源，讓系統從中抓取頂點的色彩資訊。 D3DRS \_ AMBIENTMATERIALSOURCE、D3DRS \_ DIFFUSEMATERIALSOURCE、D3DRS \_ EMISSIVEMATERIALSOURCE 和 D3DRS SPECULARMATERIALSOURCE 轉譯 \_ 狀態分別會控制環境、擴散、放射和反射色彩元件的來源。 每個狀態都可以設定為 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員，它會定義常數以指示系統使用目前的材質、漫射色彩或反射色彩做為指定之色彩元件的來源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
