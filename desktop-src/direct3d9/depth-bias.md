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
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="d9531-103"> (Direct3D 9) 的深度偏差</span><span class="sxs-lookup"><span data-stu-id="d9531-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="d9531-104">在3D 空間中有共置的多邊形，可以像是在每個多邊形都不是共置的多邊形一樣地顯示。</span><span class="sxs-lookup"><span data-stu-id="d9531-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="d9531-105">這項技術通常用來確保場景中的陰影正確顯示。</span><span class="sxs-lookup"><span data-stu-id="d9531-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="d9531-106">例如，牆上的陰影可能會有與牆相同的深度值。</span><span class="sxs-lookup"><span data-stu-id="d9531-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="d9531-107">如果您先轉譯牆，然後再呈現陰影，則可能看不到陰影，或是可見的深度成品。</span><span class="sxs-lookup"><span data-stu-id="d9531-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="d9531-108">您可以反轉呈現共面對象的順序，以避免反轉效果，但深度成品仍然很有可能。</span><span class="sxs-lookup"><span data-stu-id="d9531-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="d9531-109">應用程式可以藉由在轉譯共置多邊形的集合時，將偏差新增至系統所用的 z 值，以協助確保會正確轉譯共置多邊形。</span><span class="sxs-lookup"><span data-stu-id="d9531-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="d9531-110">若要將 z 偏差加入至一組多邊形，請在轉譯之前呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，將 *State* 參數設定為 D3DRS \_ DEPTHBIAS，並將 *Value* 參數設定為適當的 float 值 (例如，適當的值可能是從-1.0 到 1.0) ; 若要將此值轉換成 **graphicsdevice**，您也必須將值轉換成 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="d9531-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="d9531-111">較高的 z 偏差值會增加當您顯示的多邊形與其他共置多邊形時，所呈現的多邊形可能會顯示的可能性。</span><span class="sxs-lookup"><span data-stu-id="d9531-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="d9531-112">其中 m 是所呈現三角形的最大深度斜率。</span><span class="sxs-lookup"><span data-stu-id="d9531-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="d9531-113">D3DRS \_ DEPTHBIAS 和 D3DRS SLOPESCALEDEPTHBIAS 轉譯狀態的單位 \_ 取決於是否已啟用 z 緩衝處理或 w 緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="d9531-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="d9531-114">應用程式必須提供適當的值。</span><span class="sxs-lookup"><span data-stu-id="d9531-114">The application must provide suitable values.</span></span>

<span data-ttu-id="d9531-115">偏差不會套用至任何線條和點基本。</span><span class="sxs-lookup"><span data-stu-id="d9531-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="d9531-116">不過，這個偏差必須套用至以線框模式繪製的三角形。</span><span class="sxs-lookup"><span data-stu-id="d9531-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d9531-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9531-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9531-118">圖元管線</span><span class="sxs-lookup"><span data-stu-id="d9531-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
