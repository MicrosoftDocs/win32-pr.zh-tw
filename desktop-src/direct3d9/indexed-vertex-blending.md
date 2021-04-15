---
description: 已編制索引的頂點混色可延伸 Direct3D 中的頂點混合支援，以允許使用矩陣進行混合。
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: " (Direct3D 9) 的索引頂點混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467440"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="aaac0-103"> (Direct3D 9) 的索引頂點混合</span><span class="sxs-lookup"><span data-stu-id="aaac0-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="aaac0-104">已編制索引的頂點混色可延伸 Direct3D 中的頂點混合支援，以允許使用矩陣進行混合。</span><span class="sxs-lookup"><span data-stu-id="aaac0-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="aaac0-105">這些矩陣是使用矩陣索引來參考的。</span><span class="sxs-lookup"><span data-stu-id="aaac0-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="aaac0-106">這些索引是以每個頂點為基礎提供，並參考最多256個矩陣的調色板。</span><span class="sxs-lookup"><span data-stu-id="aaac0-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="aaac0-107">每個索引都是8位，而且每個頂點最多可有四個索引，以允許每個頂點混合四個矩陣。</span><span class="sxs-lookup"><span data-stu-id="aaac0-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="aaac0-108">索引會封裝成 DWORD。</span><span class="sxs-lookup"><span data-stu-id="aaac0-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="aaac0-109">因為索引是以每個頂點為基礎來指定，最多12個矩陣可能會影響單一三角形，而調色板中的任何矩陣都可能影響一個繪製呼叫的頂點。</span><span class="sxs-lookup"><span data-stu-id="aaac0-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="aaac0-110">這種方法有下列優點。</span><span class="sxs-lookup"><span data-stu-id="aaac0-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="aaac0-111">它可讓更多的矩陣影響單一三角形。</span><span class="sxs-lookup"><span data-stu-id="aaac0-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="aaac0-112">它可讓您在相同的繪製呼叫中傳遞更多混合的三角形。</span><span class="sxs-lookup"><span data-stu-id="aaac0-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="aaac0-113">它讓頂點與三角形索引無關。</span><span class="sxs-lookup"><span data-stu-id="aaac0-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="aaac0-114">這可讓漸進式網格與頂點混色一起使用。</span><span class="sxs-lookup"><span data-stu-id="aaac0-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="aaac0-115">這種方法的其中一個缺點是，它無法在頂點處理之前進行鑲嵌式時，與曲線表面的基本專案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="aaac0-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="aaac0-116">下圖會示範四個矩陣如何影響頂點。</span><span class="sxs-lookup"><span data-stu-id="aaac0-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="aaac0-117">每個頂點最多可有4個索引，因此四個矩陣可依頂點進行混合。</span><span class="sxs-lookup"><span data-stu-id="aaac0-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="aaac0-118">此圖表會使用以0、2、5和6為索引的矩陣。</span><span class="sxs-lookup"><span data-stu-id="aaac0-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![使用256可用矩陣的4個索引頂點混合圖](images/dword1.png)

<span data-ttu-id="aaac0-120">下圖會示範最多12個矩陣如何影響三角形。</span><span class="sxs-lookup"><span data-stu-id="aaac0-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="aaac0-121">使用以每個頂點指定的索引，最多12個矩陣可能會影響三角形。</span><span class="sxs-lookup"><span data-stu-id="aaac0-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![使用 12 256 可用矩陣的索引頂點混合圖](images/dword2.png)

<span data-ttu-id="aaac0-123">下列方程式會決定矩陣如何影響頂點的一般案例。</span><span class="sxs-lookup"><span data-stu-id="aaac0-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![索引頂點混合的方程式](images/indexedvblend.png)

<span data-ttu-id="aaac0-125">V <sub>模型</sub> 是輸入模型空間頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="aaac0-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="aaac0-126">Index0..Index3 是封裝成 DWORD 的每個頂點矩陣索引。</span><span class="sxs-lookup"><span data-stu-id="aaac0-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="aaac0-127">M \[ \] 是取得索引的世界矩陣陣列。</span><span class="sxs-lookup"><span data-stu-id="aaac0-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="aaac0-128">b ₀ .。。b ₂是 blend 加權。</span><span class="sxs-lookup"><span data-stu-id="aaac0-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="aaac0-129">V<sub>世界</sub> 是輸出世界空間頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="aaac0-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="aaac0-130">如需索引頂點混合的詳細資訊，請參閱 [使用索引頂點混合 (Direct3D 9) ](using-indexed-vertex-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="aaac0-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaac0-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="aaac0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaac0-132">幾何混合</span><span class="sxs-lookup"><span data-stu-id="aaac0-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



