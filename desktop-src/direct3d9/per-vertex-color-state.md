---
description: 如果您告訴執行時間有資料，Direct3D 光源引擎可以在執行光源時使用每個頂點的色彩資料。
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: 'Per-Vertex 色彩狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385529"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="0ae80-103">Per-Vertex 色彩狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="0ae80-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="0ae80-104">如果您告訴執行時間有資料，Direct3D 光源引擎可以在執行光源時使用每個頂點的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="0ae80-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="0ae80-105">這是藉由開啟下列呈現狀態來完成的：</span><span class="sxs-lookup"><span data-stu-id="0ae80-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="0ae80-106">如果啟用了每個頂點的色彩，則應用程式可以設定來源，讓系統從中抓取頂點的色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="0ae80-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="0ae80-107">D3DRS \_ AMBIENTMATERIALSOURCE、D3DRS \_ DIFFUSEMATERIALSOURCE、D3DRS \_ EMISSIVEMATERIALSOURCE 和 D3DRS SPECULARMATERIALSOURCE 轉譯 \_ 狀態分別會控制環境、擴散、放射和反射色彩元件的來源。</span><span class="sxs-lookup"><span data-stu-id="0ae80-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="0ae80-108">每個狀態都可以設定為 [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) 列舉型別的成員，它會定義常數以指示系統使用目前的材質、漫射色彩或反射色彩做為指定之色彩元件的來源。</span><span class="sxs-lookup"><span data-stu-id="0ae80-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ae80-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ae80-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ae80-110">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="0ae80-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
