---
title: 指定要鑲嵌的多邊形
description: '您可以指定多邊形 (可能包含要使用鑲嵌的漏洞) '
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932531"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a><span data-ttu-id="ffdae-103">指定要鑲嵌的多邊形</span><span class="sxs-lookup"><span data-stu-id="ffdae-103">Specifying the Polygon to Be Tessellated</span></span>

<span data-ttu-id="ffdae-104">您可以使用下列內容指定多邊形 (可能包含要鑲嵌的漏洞) ：</span><span class="sxs-lookup"><span data-stu-id="ffdae-104">You specify a polygon (possibly containing holes) to be tessellated using:</span></span>

-   [<span data-ttu-id="ffdae-105">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="ffdae-105">**gluBeginPolygon**</span></span>](glubeginpolygon.md)
-   [<span data-ttu-id="ffdae-106">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="ffdae-106">**gluTessVertex**</span></span>](glutessvertex.md)
-   [<span data-ttu-id="ffdae-107">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="ffdae-107">**gluNextContour**</span></span>](glunextcontour.md)
-   [<span data-ttu-id="ffdae-108">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="ffdae-108">**gluEndPolygon**</span></span>](gluendpolygon.md)

<span data-ttu-id="ffdae-109">針對沒有孔洞的多邊形，規格程式與 OpenGL 相同：</span><span class="sxs-lookup"><span data-stu-id="ffdae-109">For polygons without holes, the specification process is exactly as in OpenGL:</span></span>

1.  <span data-ttu-id="ffdae-110">從 [**gluBeginPolygon**](glubeginpolygon.md)開始。</span><span class="sxs-lookup"><span data-stu-id="ffdae-110">Start with [**gluBeginPolygon**](glubeginpolygon.md).</span></span>
2.  <span data-ttu-id="ffdae-111">針對界限中的每個頂點呼叫 [**gluTessVertex**](glutessvertex.md) 。</span><span class="sxs-lookup"><span data-stu-id="ffdae-111">Call [**gluTessVertex**](glutessvertex.md) for each vertex in the boundary.</span></span>
3.  <span data-ttu-id="ffdae-112">使用 [**gluEndPolygon**](gluendpolygon.md)的呼叫來結束多邊形。</span><span class="sxs-lookup"><span data-stu-id="ffdae-112">End the polygon with a call to [**gluEndPolygon**](gluendpolygon.md).</span></span>

<span data-ttu-id="ffdae-113">如果多邊形包含多個輪廓（包括孔內的孔和孔），您可以指定一個後面接著 [**gluNextContour**](glunextcontour.md)的輪廓。</span><span class="sxs-lookup"><span data-stu-id="ffdae-113">If a polygon consists of multiple contours, including holes and holes within holes, you specify the contours one after the other, preceding each by [**gluNextContour**](glunextcontour.md).</span></span> <span data-ttu-id="ffdae-114">當您呼叫 [**gluEndPolygon**](gluendpolygon.md)時，它會發出最後輪廓的結尾，並開始鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="ffdae-114">When you call [**gluEndPolygon**](gluendpolygon.md), it signals the end of the final contour and starts the tessellation.</span></span> <span data-ttu-id="ffdae-115">您可以在第一個輪廓之前省略 **gluNextContour** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ffdae-115">You can omit the call to **gluNextContour** before the first contour.</span></span> <span data-ttu-id="ffdae-116">[**GluBeginPolygon**](glubeginpolygon.md)函式會開始鑲嵌多邊形的規格，並將鑲嵌式物件 **tessobj** 與其產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ffdae-116">The [**gluBeginPolygon**](glubeginpolygon.md) function begins the specification of a polygon to be tessellated and associates a tessellation object, **tessobj**, with it.</span></span> <span data-ttu-id="ffdae-117">要使用的回呼函式是您使用 [*gluTessCallback*](glutess.md)系結至鑲嵌式物件的函數。</span><span class="sxs-lookup"><span data-stu-id="ffdae-117">The callback functions to be used are those that you bind to the tessellation object with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="ffdae-118">[**GluTessVertex**](glutessvertex.md)函式會指定要鑲嵌的多邊形頂點。</span><span class="sxs-lookup"><span data-stu-id="ffdae-118">The [**gluTessVertex**](glutessvertex.md) function specifies a vertex in the polygon to be tessellated.</span></span> <span data-ttu-id="ffdae-119">針對多邊形中的每個頂點呼叫 **gluTessVertex** 。</span><span class="sxs-lookup"><span data-stu-id="ffdae-119">Call **gluTessVertex** for each vertex in the polygon.</span></span> <span data-ttu-id="ffdae-120">函式的 *tessobj* 參數是要使用的鑲嵌式物件、 *v* 包含三維頂點座標，而 *資料* 是傳送至與 **x.glu 隊 \_ 頂點** 相關聯之回呼的任意指標。</span><span class="sxs-lookup"><span data-stu-id="ffdae-120">The function's *tessobj* parameter is the tessellation object to use, *v* contains the three-dimensional vertex coordinates, and *data* is an arbitrary pointer that is sent to the callback associated with **GLU\_VERTEX**.</span></span> <span data-ttu-id="ffdae-121">一般而言， *資料* 報含頂點資料、材質座標、色彩資訊，或應用程式可能需要的任何其他內容。</span><span class="sxs-lookup"><span data-stu-id="ffdae-121">Typically, *data* contains vertex data, texture coordinates, color information, or whatever else the application may require.</span></span>

<span data-ttu-id="ffdae-122">當多個輪廓組成要鑲嵌的多邊形界限時， [**gluNextContour**](glunextcontour.md) 函式會標示下一個輪廓的開頭。</span><span class="sxs-lookup"><span data-stu-id="ffdae-122">The [**gluNextContour**](glunextcontour.md) function marks the beginning of the next contour when multiple contours make up the boundary of the polygon to be tessellated.</span></span> <span data-ttu-id="ffdae-123">函數的 *型* 別參數可以是 **X.glu 隊 \_ 外部**、 **X.glu 隊 \_ 內部**、 **x.glu 隊 \_ CCW**、 **x.glu 隊 \_ CW** 或 **x.glu 隊 \_ 未知**。</span><span class="sxs-lookup"><span data-stu-id="ffdae-123">The function's *type* parameter can be **GLU\_EXTERIOR**, **GLU\_INTERIOR**, **GLU\_CCW**, **GLU\_CW**, or **GLU\_UNKNOWN**.</span></span> <span data-ttu-id="ffdae-124">這些常數僅作為鑲嵌式的提示。</span><span class="sxs-lookup"><span data-stu-id="ffdae-124">These constants serve only as hints to the tessellation.</span></span> <span data-ttu-id="ffdae-125">如果您得到適當的方式，鑲嵌可能會更快。</span><span class="sxs-lookup"><span data-stu-id="ffdae-125">If you get them right, the tessellation might go faster.</span></span> <span data-ttu-id="ffdae-126">如果您遇到錯誤，這些錯誤會被忽略，而且鑲嵌仍能運作。</span><span class="sxs-lookup"><span data-stu-id="ffdae-126">If you get them wrong, they're ignored, and the tessellation still works.</span></span>

<span data-ttu-id="ffdae-127">對於具有孔洞的多邊形，有一個輪廓是外部輪廓，其他則是內部。</span><span class="sxs-lookup"><span data-stu-id="ffdae-127">For a polygon with holes, one contour is the exterior contour, and the others are interior.</span></span> <span data-ttu-id="ffdae-128">如果您未在 [**gluBeginPolygon**](glubeginpolygon.md)後立即呼叫 **gluNextContour** ，則會假設第一個輪廓的類型為 **x.glu 隊 \_ 外部**。</span><span class="sxs-lookup"><span data-stu-id="ffdae-128">If you don't call **gluNextContour** immediately after [**gluBeginPolygon**](glubeginpolygon.md), the first contour is assumed to be of type **GLU\_EXTERIOR**.</span></span>

<span data-ttu-id="ffdae-129">**X.glu 隊 \_CW** 和 **x.glu 隊 \_ CCW** 指出順時針和逆時針方向的多邊形。</span><span class="sxs-lookup"><span data-stu-id="ffdae-129">**GLU\_CW** and **GLU\_CCW** indicate clockwise- and counterclockwise-oriented polygons.</span></span> <span data-ttu-id="ffdae-130">選擇的是順時針的，而這些是逆時針的，但在任何平面中，都有兩種不同的方向：以一致的方式使用 **x.glu 隊的 \_ CW** 和 **x.glu 隊 \_ CCW** 類型。</span><span class="sxs-lookup"><span data-stu-id="ffdae-130">Choosing which are clockwise and which are counterclockwise is arbitrary in three dimensions, but in any plane, there are two different orientations; use the **GLU\_CW** and **GLU\_CCW** types consistently.</span></span> <span data-ttu-id="ffdae-131">如果您不知道要使用哪一個，請使用 **X.glu 隊 \_ UNKNOWN** 。</span><span class="sxs-lookup"><span data-stu-id="ffdae-131">Use **GLU\_UNKNOWN** if you don't know which to use.</span></span>

<span data-ttu-id="ffdae-132">[**GluEndPolygon**](gluendpolygon.md)函數表示多邊形規格的結尾。</span><span class="sxs-lookup"><span data-stu-id="ffdae-132">The [**gluEndPolygon**](gluendpolygon.md) function indicates the end of the polygon specification.</span></span> <span data-ttu-id="ffdae-133">這也表示鑲嵌可以開始使用鑲嵌式物件 *tessobj*。</span><span class="sxs-lookup"><span data-stu-id="ffdae-133">It also indicates that the tessellation can begin using the tessellation object *tessobj*.</span></span>

 

 




