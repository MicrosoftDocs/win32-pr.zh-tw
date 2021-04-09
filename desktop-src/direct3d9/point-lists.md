---
description: 點清單是轉譯為隔離點的頂點集合。 您的應用程式可以在3D 場景中使用它們來表示星星欄位，或是多邊形表面的虛線。
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: 點清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688067"
---
# <a name="point-lists"></a><span data-ttu-id="1c6c9-104">點清單</span><span class="sxs-lookup"><span data-stu-id="1c6c9-104">Point Lists</span></span>

<span data-ttu-id="1c6c9-105">點清單是轉譯為隔離點的頂點集合。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="1c6c9-106">您的應用程式可以在3D 場景中使用它們來表示星星欄位，或是多邊形表面的虛線。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="1c6c9-107">下圖描述轉譯的點清單。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-107">The following illustration depicts a rendered point list.</span></span>

![點清單的圖例](images/pointlst.png)

<span data-ttu-id="1c6c9-109">您的應用程式可以套用資料和紋理到點清單。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="1c6c9-110">資料或紋理中的色彩只出現在繪製的點，而不是點之間的任何位置。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="1c6c9-111">下列程式碼顯示如何建立這個點清單的頂點。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-111">The following code shows how to create vertices for this point list.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



<span data-ttu-id="1c6c9-112">下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)，在 Direct3D 9 中轉譯此點清單。</span><span class="sxs-lookup"><span data-stu-id="1c6c9-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="1c6c9-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c6c9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6c9-114">基本</span><span class="sxs-lookup"><span data-stu-id="1c6c9-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
