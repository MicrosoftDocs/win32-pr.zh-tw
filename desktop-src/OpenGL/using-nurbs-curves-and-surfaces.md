---
title: 使用 NURBS 曲線和表面
description: 非統一的有理 B 曲線 (NURBS) 函數提供兩個和三個維度中曲線和表面的一般和強大描述，並將曲線和曲面轉換為 OpenGL 評估工具。
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- 'OpenGL 公用程式 (X.GLU 隊) 、非統一的有理 B 曲線 (NURBS) '
- 'X.GLU 隊 (OpenGL 公用程式) 、非統一的有理 B 曲線 (NURBS) '
- 非統一的有理 B 曲線 (NURBS) OpenGL
- NURBS (非統一有理數 B 曲線) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300479"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="b727d-107">使用 NURBS 曲線和表面</span><span class="sxs-lookup"><span data-stu-id="b727d-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="b727d-108">非統一的有理 B 曲線 (NURBS) 函數提供兩個和三個維度中曲線和表面的一般和強大描述，並將曲線和曲面轉換為 OpenGL 評估工具。</span><span class="sxs-lookup"><span data-stu-id="b727d-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="b727d-109">NURBS 函數可以表示許多電腦輔助機械設計系統中的幾何。</span><span class="sxs-lookup"><span data-stu-id="b727d-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="b727d-110">它們可以在各種不同的樣式中轉譯曲線和表面，並可自動處理將 tessellates 至較高曲率區域中較小三角形和接近側面裝訂邊的自我調整細分。</span><span class="sxs-lookup"><span data-stu-id="b727d-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="b727d-111">NURBS 函數分為下列類別。</span><span class="sxs-lookup"><span data-stu-id="b727d-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="b727d-112">若要管理 NURBS 物件，請使用：</span><span class="sxs-lookup"><span data-stu-id="b727d-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="b727d-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (建立 NURBS 物件) </span><span class="sxs-lookup"><span data-stu-id="b727d-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="b727d-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (會刪除 NURBS 物件) </span><span class="sxs-lookup"><span data-stu-id="b727d-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="b727d-115">[*gluNurbsCallback*](glunurbs.md) (會建立錯誤處理函式) </span><span class="sxs-lookup"><span data-stu-id="b727d-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="b727d-116">若要指定所需的曲線，請使用：</span><span class="sxs-lookup"><span data-stu-id="b727d-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="b727d-117">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="b727d-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="b727d-118">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="b727d-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="b727d-119">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="b727d-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="b727d-120">若要指定所需的表面，請使用：</span><span class="sxs-lookup"><span data-stu-id="b727d-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="b727d-121">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="b727d-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="b727d-122">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="b727d-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="b727d-123">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="b727d-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="b727d-124">您也可以指定修剪區域，此區域會定義要評估之 NURBS 介面網域的子集，如此您就可以建立具有平滑界限或包含孔洞的表面。</span><span class="sxs-lookup"><span data-stu-id="b727d-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="b727d-125">若要指定修剪區域，請使用：</span><span class="sxs-lookup"><span data-stu-id="b727d-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="b727d-126">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="b727d-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="b727d-127">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="b727d-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="b727d-128">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="b727d-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="b727d-129">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="b727d-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="b727d-130">如同 quadric 物件，您可以控制如何轉譯的 NURBS 曲線和表面。</span><span class="sxs-lookup"><span data-stu-id="b727d-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="b727d-131">您可以判斷：</span><span class="sxs-lookup"><span data-stu-id="b727d-131">You can determine:</span></span>

-   <span data-ttu-id="b727d-132">是否要捨棄其控制項多面體位於目前視窗之外的曲線或表面。</span><span class="sxs-lookup"><span data-stu-id="b727d-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="b727d-133">用來呈現曲線和表面的多邊形邊緣的最大長度 (以圖元為單位) 。</span><span class="sxs-lookup"><span data-stu-id="b727d-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="b727d-134">您是否將採用 OpenGL 伺服器的投射矩陣、模型矩陣和視口，或提供它們明確與 [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)。</span><span class="sxs-lookup"><span data-stu-id="b727d-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="b727d-135">使用 [**gluNurbsProperty**](glunurbsproperty.md) 來設定這些屬性，或使用預設值。</span><span class="sxs-lookup"><span data-stu-id="b727d-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="b727d-136">您可以使用 [**gluGetNurbsProperty**](glugetnurbsproperty.md)查詢其轉譯樣式的 NURBS 物件。</span><span class="sxs-lookup"><span data-stu-id="b727d-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




