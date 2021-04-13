---
description: 網格中的每個臉部都有垂直的單元法線向量，如下圖所示。
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: " (Direct3D 9) 的臉部和頂點一般向量"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0ef6fd8eba85b770cbfe71477655ddbafd8ee7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559562"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a><span data-ttu-id="45399-103"> (Direct3D 9) 的臉部和頂點一般向量</span><span class="sxs-lookup"><span data-stu-id="45399-103">Face and Vertex Normal Vectors (Direct3D 9)</span></span>

<span data-ttu-id="45399-104">網格中的每個臉部都有垂直的單元法線向量，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="45399-104">Each face in a mesh has a perpendicular unit normal vector, as shown in the following illustration.</span></span> <span data-ttu-id="45399-105">向量的方向是由定義頂點的順序，和座標系統是否為右手系或左手系而決定的。</span><span class="sxs-lookup"><span data-stu-id="45399-105">The vector's direction is determined by the order in which the vertices are defined and by whether the coordinate system is right- or left-handed.</span></span> <span data-ttu-id="45399-106">面標準點偏離面的正面。</span><span class="sxs-lookup"><span data-stu-id="45399-106">The face normal points away from the front side of the face.</span></span> <span data-ttu-id="45399-107">在 Direct3D 中，只會看見正面。</span><span class="sxs-lookup"><span data-stu-id="45399-107">In Direct3D, only the front of a face is visible.</span></span> <span data-ttu-id="45399-108">正面上的頂點是依順時針方向定義。</span><span class="sxs-lookup"><span data-stu-id="45399-108">A front face is one in which vertices are defined in clockwise order.</span></span>

![正面臉部的一般向量圖例](images/nrmlvect.png)

<span data-ttu-id="45399-110">只要不是正面，都稱為背面。</span><span class="sxs-lookup"><span data-stu-id="45399-110">Any face that is not a front face is a back face.</span></span> <span data-ttu-id="45399-111">Direct3D 不一定會轉譯回臉部;因此，背面的臉部稱為挑選。</span><span class="sxs-lookup"><span data-stu-id="45399-111">Direct3D does not always render back faces; therefore, back faces are said to be culled.</span></span> <span data-ttu-id="45399-112">如果您想要的話，可以變更消除模式以轉譯背面。</span><span class="sxs-lookup"><span data-stu-id="45399-112">You can change the culling mode to render back faces if you want.</span></span> <span data-ttu-id="45399-113">如需詳細資訊，請參閱 [ (Direct3D 9) 的挑選狀態 ](culling-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="45399-113">See [Culling State (Direct3D 9)](culling-state.md) for more information.</span></span>

<span data-ttu-id="45399-114">Direct3D 使用頂點單位法向量呈現 Gouraud Shading、光源及紋理效果。</span><span class="sxs-lookup"><span data-stu-id="45399-114">Direct3D uses the vertex unit normals for Gouraud shading, lighting, and texturing effects.</span></span> <span data-ttu-id="45399-115">下圖顯示法線範例。</span><span class="sxs-lookup"><span data-stu-id="45399-115">The following illustration shows example normals.</span></span>

![頂點法線的圖例](images/vertnrml.png)

<span data-ttu-id="45399-117">對多邊形套用 Gouraud Shading 時，Direct3D 會使用頂點法向量計算光源與表面之間的角度。</span><span class="sxs-lookup"><span data-stu-id="45399-117">When applying Gouraud shading to a polygon, Direct3D uses the vertex normals to calculate the angle between the light source and the surface.</span></span> <span data-ttu-id="45399-118">它會計算頂點的色彩和濃度值，並針對所有基本類型表面上的每一個點插入它們。</span><span class="sxs-lookup"><span data-stu-id="45399-118">It calculates the color and intensity values for the vertices and interpolates them for every point across all the primitive's surfaces.</span></span> <span data-ttu-id="45399-119">Direct3D 會使用角度計算光線強度值。</span><span class="sxs-lookup"><span data-stu-id="45399-119">Direct3D calculates the light intensity value by using the angle.</span></span> <span data-ttu-id="45399-120">角度越大，照射在表面上的光線就越弱。</span><span class="sxs-lookup"><span data-stu-id="45399-120">The greater the angle, the less light is shining on the surface.</span></span>

<span data-ttu-id="45399-121">如果您要建立一個平面物件，請將頂點法線設定為與介面垂直的點，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="45399-121">If you are creating an object that is flat, set the vertex normals to point perpendicular to the surface, as shown in the following illustration.</span></span>

![由兩個三角形組成頂點法線的平坦表面圖例](images/flatvert.png)

<span data-ttu-id="45399-123">不過，您的物件比較有可能是由三角形的條紋組成，而且三角形不是共面。</span><span class="sxs-lookup"><span data-stu-id="45399-123">It is more likely, however, that your object is made up of triangle strips and the triangles are not coplanar.</span></span> <span data-ttu-id="45399-124">有一種簡單的方式可在連環中所有三角形上達到平滑著色，那就是先計算與頂點相關聯的每個多邊形面的表面法向量。</span><span class="sxs-lookup"><span data-stu-id="45399-124">One simple way to achieve smooth shading across all the triangles in the strip is to first calculate the surface normal vector for each polygonal face with which the vertex is associated.</span></span> <span data-ttu-id="45399-125">表面法向量可設定為與每個表面法向量等角。</span><span class="sxs-lookup"><span data-stu-id="45399-125">The vertex normal can be set to make an equal angle with each surface normal.</span></span> <span data-ttu-id="45399-126">不過，這個方法對於複雜的基本類型可能不夠有效率。</span><span class="sxs-lookup"><span data-stu-id="45399-126">However, this method might not be efficient enough for complex primitives.</span></span>

<span data-ttu-id="45399-127">下圖顯示此方法，當中顯示的兩個表面 S1 和 S2 從上方看起來邊緣朝上。</span><span class="sxs-lookup"><span data-stu-id="45399-127">This method is illustrated by the following diagram, which shows two surfaces, S1 and S2 seen edge-on from above.</span></span> <span data-ttu-id="45399-128">S1 及 S2 的法向量以藍色顯示。</span><span class="sxs-lookup"><span data-stu-id="45399-128">The normal vectors for S1 and S2 are shown in blue.</span></span> <span data-ttu-id="45399-129">頂點法向量是以紅色顯示。</span><span class="sxs-lookup"><span data-stu-id="45399-129">The vertex normal vector is shown in red.</span></span> <span data-ttu-id="45399-130">頂點法向量與 S1 表面法向量所呈現的角度，與 S2 的頂點法向量和表面法向量相同。</span><span class="sxs-lookup"><span data-stu-id="45399-130">The angle that the vertex normal vector makes with the surface normal of S1 is the same as the angle between the vertex normal and the surface normal of S2.</span></span> <span data-ttu-id="45399-131">當這兩個表面亮起並採用 Gouraud Shading 時，結果會是兩者之間有平滑著色、平滑圓邊。</span><span class="sxs-lookup"><span data-stu-id="45399-131">When these two surfaces are lit and shaded with Gouraud shading, the result is a smoothly shaded, smoothly rounded edge between them.</span></span>

![兩個表面 (s1 和 s2) 及其一般向量和頂點一般向量的圖表](images/gvert.png)

<span data-ttu-id="45399-133">如果頂點法向量朝向相關聯的其中一個面傾斜，會造成該表面上的點的亮度增加或減少，取決於它與光源形成的角度。</span><span class="sxs-lookup"><span data-stu-id="45399-133">If the vertex normal leans toward one of the faces with which it is associated, it causes the light intensity to increase or decrease for points on that surface, depending on the angle it makes with the light source.</span></span> <span data-ttu-id="45399-134">如下圖範例所示。</span><span class="sxs-lookup"><span data-stu-id="45399-134">The following diagram shows an example.</span></span> <span data-ttu-id="45399-135">同樣地，這些表面會顯示為 edge。</span><span class="sxs-lookup"><span data-stu-id="45399-135">Again, these surfaces are seen edge-on.</span></span> <span data-ttu-id="45399-136">頂點法向量朝向 S1，使其與光源之間形成的角度較小，如果頂點法向量與表面法向量呈等角的話。</span><span class="sxs-lookup"><span data-stu-id="45399-136">The vertex normal leans toward S1, causing it to have a smaller angle with the light source than if the vertex normal had equal angles with the surface normals.</span></span>

![兩個表面的圖表 (s1 和 s2) 具有仰賴朝一面的頂點一般向量](images/gvert2.png)

<span data-ttu-id="45399-138">您可以使用 Gouraud Shading 在 3D 場景中顯示一些物件的銳利邊緣。</span><span class="sxs-lookup"><span data-stu-id="45399-138">You can use Gouraud shading to display some objects in a 3D scene with sharp edges.</span></span> <span data-ttu-id="45399-139">若要這樣做，請將頂點一般向量複製到需要尖邊緣的任何臉部交集，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="45399-139">To do so, duplicate the vertex normal vectors at any intersection of faces where a sharp edge is required, as shown in the following illustration.</span></span>

![在尖邊的重複頂點一般向量圖例](images/shade1.png)

<span data-ttu-id="45399-141">如果您使用 DrawPrimitive 方法轉譯場景，請將有銳利邊緣的物件定義為三角形清單，而非三角形連環。</span><span class="sxs-lookup"><span data-stu-id="45399-141">If you use the DrawPrimitive methods to render your scene, define the object with sharp edges as a triangle list, rather than a triangle strip.</span></span> <span data-ttu-id="45399-142">當您將物件定義為三角形連環時，Direct3D 會將它視為單一多邊形，由多個三角形面所組成。</span><span class="sxs-lookup"><span data-stu-id="45399-142">When you define an object as a triangle strip, Direct3D treats it as a single polygon composed of multiple triangular faces.</span></span> <span data-ttu-id="45399-143">Gouraud Shading 同時套用在多邊形的每個面以及相鄰的面之間。</span><span class="sxs-lookup"><span data-stu-id="45399-143">Gouraud shading is applied both across each face of the polygon and between adjacent faces.</span></span> <span data-ttu-id="45399-144">結果物件會在面與面之間平滑著色。</span><span class="sxs-lookup"><span data-stu-id="45399-144">The result is an object that is smoothly shaded from face to face.</span></span> <span data-ttu-id="45399-145">由於三角形清單是由一系列不相鄰的三角面所組成的多邊形，因此 Direct3D 會在多邊形的每個面上套用 Gouraud Shading。</span><span class="sxs-lookup"><span data-stu-id="45399-145">Because a triangle list is a polygon composed of a series of disjoint triangular faces, Direct3D applies Gouraud shading across each face of the polygon.</span></span> <span data-ttu-id="45399-146">不過，它不會從一個面套用至另一個面。</span><span class="sxs-lookup"><span data-stu-id="45399-146">However, it is not applied from face to face.</span></span> <span data-ttu-id="45399-147">如果三角形清單中有兩個以上相鄰的三角形，這些三角形之間會顯示銳利邊緣。</span><span class="sxs-lookup"><span data-stu-id="45399-147">If two or more triangles of a triangle list are adjacent, they appear to have a sharp edge between them.</span></span>

<span data-ttu-id="45399-148">另一個替代方法是在轉譯有銳利邊緣的物件時改變為平面著色。</span><span class="sxs-lookup"><span data-stu-id="45399-148">Another alternative is to change to flat shading when rendering objects with sharp edges.</span></span> <span data-ttu-id="45399-149">運算上來說，這是最有效率的方法，但可能會導致場景中的物件不會進行點陣化轉譯，就像套用 Gouraud 著色的物件一樣。</span><span class="sxs-lookup"><span data-stu-id="45399-149">This is computationally the most efficient method, but it may result in objects in the scene that are not rendered as realistically as the objects that are Gouraud-shaded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45399-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="45399-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45399-151">座標系統和幾何</span><span class="sxs-lookup"><span data-stu-id="45399-151">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



