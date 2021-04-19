---
description: 線清單是隔離、直線段的清單。
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: 行清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970505"
---
# <a name="line-lists"></a><span data-ttu-id="d2da2-103">行清單</span><span class="sxs-lookup"><span data-stu-id="d2da2-103">Line Lists</span></span>

<span data-ttu-id="d2da2-104">線清單是隔離、直線段的清單。</span><span class="sxs-lookup"><span data-stu-id="d2da2-104">A line list is a list of isolated, straight line segments.</span></span> <span data-ttu-id="d2da2-105">在 3D 場景中加入冰雹或暴雨的這類工作適合使用線清單。</span><span class="sxs-lookup"><span data-stu-id="d2da2-105">Line lists are useful for such tasks as adding sleet or heavy rain to a 3D scene.</span></span> <span data-ttu-id="d2da2-106">應用程式藉由填入頂點陣列來建立線清單。</span><span class="sxs-lookup"><span data-stu-id="d2da2-106">Applications create a line list by filling an array of vertices.</span></span> <span data-ttu-id="d2da2-107">請注意，線清單中的頂點數必須是大於或等於二的偶數。</span><span class="sxs-lookup"><span data-stu-id="d2da2-107">Note that the number of vertices in a line list must be an even number greater than or equal to two.</span></span>

<span data-ttu-id="d2da2-108">下圖顯示呈現的線清單。</span><span class="sxs-lookup"><span data-stu-id="d2da2-108">The following illustration shows a rendered line list.</span></span>

![線清單的圖例](images/linelst.png)

<span data-ttu-id="d2da2-110">您可以將資料和紋理套用到線清單。</span><span class="sxs-lookup"><span data-stu-id="d2da2-110">You can apply materials and textures to a line list.</span></span> <span data-ttu-id="d2da2-111">資料或紋理中的的色彩只會隨繪製線條出現，不會出現在線之間的任何點。</span><span class="sxs-lookup"><span data-stu-id="d2da2-111">The colors in the material or texture appear only along the lines drawn, not at any point in between the lines.</span></span>

<span data-ttu-id="d2da2-112">下列程式碼顯示如何建立這個線段的頂點。</span><span class="sxs-lookup"><span data-stu-id="d2da2-112">The following code shows how to create vertices for this line list.</span></span>


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



<span data-ttu-id="d2da2-113">下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)在 Direct3D 9 中轉譯行清單。</span><span class="sxs-lookup"><span data-stu-id="d2da2-113">The code example below shows how to render a line list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a><span data-ttu-id="d2da2-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2da2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2da2-115">基本</span><span class="sxs-lookup"><span data-stu-id="d2da2-115">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
