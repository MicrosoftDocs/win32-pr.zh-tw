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
# <a name="shading-state-direct3d-9"></a><span data-ttu-id="9dc69-105"> (Direct3D 9) 的陰影狀態</span><span class="sxs-lookup"><span data-stu-id="9dc69-105">Shading State (Direct3D 9)</span></span>

<span data-ttu-id="9dc69-106">Direct3D 同時支援平面和 Gouraud 陰影。</span><span class="sxs-lookup"><span data-stu-id="9dc69-106">Direct3D supports both flat and Gouraud shading.</span></span> <span data-ttu-id="9dc69-107">預設值為 Gouraud 網底。</span><span class="sxs-lookup"><span data-stu-id="9dc69-107">The default is Gouraud shading.</span></span> <span data-ttu-id="9dc69-108">若要控制目前的陰影模式，您的 c + + 應用程式會為 D3DRS SHADEMODE 轉譯狀態指定 [**D3DSHADEMODE**](./d3dshademode.md) 列舉類型的成員 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9dc69-108">To control the current shading mode, your C++ application specifies a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type for the D3DRS\_SHADEMODE render state.</span></span>

<span data-ttu-id="9dc69-109">下列 c + + 程式碼範例示範將陰影狀態設定為平面陰影模式的程式。</span><span class="sxs-lookup"><span data-stu-id="9dc69-109">The following C++ code example demonstrates the process of setting the shading state to flat shading mode.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a><span data-ttu-id="9dc69-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="9dc69-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dc69-111">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="9dc69-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
