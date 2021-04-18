---
description: 帶狀線是包含連接的帶狀線的基本類型。
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: 行條紋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510149"
---
# <a name="line-strips"></a><span data-ttu-id="8d1ad-103">行條紋</span><span class="sxs-lookup"><span data-stu-id="8d1ad-103">Line Strips</span></span>

<span data-ttu-id="8d1ad-104">帶狀線是包含連接的帶狀線的基本類型。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="8d1ad-105">您的應用程式可使用帶狀線建立未閉合之多邊形。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="8d1ad-106">封閉的多邊形是用線段將其最後一個頂點連接到第一個頂點的多邊形。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="8d1ad-107">如果您的應用程式讓多邊形以帶狀線為主，不保證頂點為共面。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="8d1ad-108">下圖顯示呈現的帶狀線。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-108">The following illustration shows a rendered line strip.</span></span>

![帶狀線的圖例](images/linstrip.gif)

<span data-ttu-id="8d1ad-110">下列程式碼顯示如何建立這個帶狀線的頂點。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-110">The following code shows how to create vertices for this line strip.</span></span>


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



<span data-ttu-id="8d1ad-111">下列程式碼範例示範如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 在 Direct3D 9 中轉譯行帶。</span><span class="sxs-lookup"><span data-stu-id="8d1ad-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="8d1ad-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d1ad-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d1ad-113">基本</span><span class="sxs-lookup"><span data-stu-id="8d1ad-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
