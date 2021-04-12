---
description: 3D 基本類型是形成單一 3D 實體的頂點集合。 最簡單的基本物件是3D 座標系統中的點集合，稱為點清單。
ms.assetid: vs|directx_sdk|~\primitives.htm
title: " (Direct3D 9 圖形) 的基本專案"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108456"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="65434-104"> (Direct3D 9 圖形) 的基本專案</span><span class="sxs-lookup"><span data-stu-id="65434-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="65434-105">3D 基本類型是形成單一 3D 實體的頂點集合。</span><span class="sxs-lookup"><span data-stu-id="65434-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="65434-106">最簡單的基本物件是3D 座標系統中的點集合，稱為點清單。</span><span class="sxs-lookup"><span data-stu-id="65434-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="65434-107">3D 基本專案通常是多邊形。</span><span class="sxs-lookup"><span data-stu-id="65434-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="65434-108">多邊形是由至少三個頂點來描繪的 3D 封閉圖形。</span><span class="sxs-lookup"><span data-stu-id="65434-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="65434-109">最簡單的多邊形為三角形。</span><span class="sxs-lookup"><span data-stu-id="65434-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="65434-110">Microsoft Direct3D 使用三角形來組合大部分的多邊形，因為這保證三角形中的所有三個頂點為共面。</span><span class="sxs-lookup"><span data-stu-id="65434-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="65434-111">轉譯非平面頂端沒有效率。</span><span class="sxs-lookup"><span data-stu-id="65434-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="65434-112">您可以結合三角形來形成大型且複雜的多邊形和網格。</span><span class="sxs-lookup"><span data-stu-id="65434-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="65434-113">下圖顯示立方體。</span><span class="sxs-lookup"><span data-stu-id="65434-113">The following illustration shows a cube.</span></span> <span data-ttu-id="65434-114">兩個三角形形成立方體的每個面。</span><span class="sxs-lookup"><span data-stu-id="65434-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="65434-115">整組三角形形成一個立方體基本類型。</span><span class="sxs-lookup"><span data-stu-id="65434-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="65434-116">您可以將材質和材質套用至基本專案的表面，讓它們看起來就像是單一穩固的表單。</span><span class="sxs-lookup"><span data-stu-id="65434-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="65434-117">如需詳細資訊，請參閱 [ (direct3d 9) ](materials.md) 和 [Direct3D 材質 (direct3d 9) ](direct3d-textures.md)的材質。</span><span class="sxs-lookup"><span data-stu-id="65434-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![每個面有兩個三角形的立方體的圖例](images/cube3d.png)

<span data-ttu-id="65434-119">您也可以使用三角形。建立表面看起來像是平滑曲線的基本類型。</span><span class="sxs-lookup"><span data-stu-id="65434-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="65434-120">下圖顯示使用三角形模擬球體的方式。</span><span class="sxs-lookup"><span data-stu-id="65434-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="65434-121">在套用材質之後，球體會在呈現時顯示為曲線。</span><span class="sxs-lookup"><span data-stu-id="65434-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="65434-122">尤其是當您使用 Gouraud 陰影時更是如此。</span><span class="sxs-lookup"><span data-stu-id="65434-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="65434-123">如需詳細資訊，請參閱 [Gouraud 陰影](shading-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="65434-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![使用三角形模擬球體的圖例](images/sphere3d.png)

<span data-ttu-id="65434-125">Direct3D 裝置可以建立和操作下列類型的基本類型。</span><span class="sxs-lookup"><span data-stu-id="65434-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="65434-126">點清單</span><span class="sxs-lookup"><span data-stu-id="65434-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="65434-127">行清單</span><span class="sxs-lookup"><span data-stu-id="65434-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="65434-128">行條紋</span><span class="sxs-lookup"><span data-stu-id="65434-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="65434-129">三角形清單</span><span class="sxs-lookup"><span data-stu-id="65434-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="65434-130">三角形條紋</span><span class="sxs-lookup"><span data-stu-id="65434-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="65434-131"> (Direct3D 9) 的三角形風扇 </span><span class="sxs-lookup"><span data-stu-id="65434-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="65434-132">您可以使用 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面的任何轉譯方法，從 c + + 應用程式呈現基本類型。</span><span class="sxs-lookup"><span data-stu-id="65434-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65434-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="65434-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65434-134">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="65434-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
