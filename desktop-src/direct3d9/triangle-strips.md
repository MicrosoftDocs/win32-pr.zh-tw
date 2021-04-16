---
description: 三角形連環是一系列的連接三角形。
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: 三角形條紋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567450"
---
# <a name="triangle-strips"></a><span data-ttu-id="082c6-103">三角形條紋</span><span class="sxs-lookup"><span data-stu-id="082c6-103">Triangle Strips</span></span>

<span data-ttu-id="082c6-104">三角形連環是一系列的連接三角形。</span><span class="sxs-lookup"><span data-stu-id="082c6-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="082c6-105">因為是連接三角形，應用程式不需要重複指定每個三角形的所有三個頂點。</span><span class="sxs-lookup"><span data-stu-id="082c6-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="082c6-106">例如，您只需要七個頂點即可定義下列三角形連環。</span><span class="sxs-lookup"><span data-stu-id="082c6-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![使用七個頂點的三角形連環的圖例](images/tristrip.png)

<span data-ttu-id="082c6-108">系統會使用頂點 v1、v2 及 v3 繪製第一個三角形；v2、v4 及 v3 繪製第二個三角形；v3、v4 及 v5 繪製第三個；v4、v6 及 v5 繪製第四個，以此類推。</span><span class="sxs-lookup"><span data-stu-id="082c6-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="082c6-109">請注意，第二個和第四個三角形的頂點失序，這是確保所有三角形都是以順時針方向繪製。</span><span class="sxs-lookup"><span data-stu-id="082c6-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="082c6-110">3D 場景中的大多數物件都是由三角形連環組成。</span><span class="sxs-lookup"><span data-stu-id="082c6-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="082c6-111">這是因為三角形連環可用於以有效率使用記憶體和處理時間的方式指定複雜物件。</span><span class="sxs-lookup"><span data-stu-id="082c6-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="082c6-112">下圖描述轉譯的三角形連環。</span><span class="sxs-lookup"><span data-stu-id="082c6-112">The following illustration depicts a rendered triangle strip.</span></span>

![轉譯三角形連環的圖例](images/tstrip2.png)

<span data-ttu-id="082c6-114">下列程式碼顯示如何建立這個三角形連環的頂點。</span><span class="sxs-lookup"><span data-stu-id="082c6-114">The following code shows how to create vertices for this triangle strip.</span></span>


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



<span data-ttu-id="082c6-115">下列程式碼範例示範如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)，在 Direct3D 9 中轉譯這個三角形的條紋。</span><span class="sxs-lookup"><span data-stu-id="082c6-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="082c6-116">使用三角形帶狀轉譯未彼此連接的三角形。</span><span class="sxs-lookup"><span data-stu-id="082c6-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="082c6-117">若要這樣做，請指定退化三角形 (也就是在三角形清單中，其區域為零) 的三角形。</span><span class="sxs-lookup"><span data-stu-id="082c6-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="082c6-118">這會在兩個不會轉譯的三角形之間建立線條。</span><span class="sxs-lookup"><span data-stu-id="082c6-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="082c6-119">若只要轉譯前一個範例中的第一個和最後一個三角形，請修改頂點緩衝區，如下所示：</span><span class="sxs-lookup"><span data-stu-id="082c6-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="082c6-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="082c6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="082c6-121">基本</span><span class="sxs-lookup"><span data-stu-id="082c6-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
