---
description: PatchMesh9 會定義貝塞爾修補程式所定義的網格，包括頂點清單以及網格的補充程式，方法是在頂點陣列中編制索引。
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404701"
---
# <a name="patchmesh9"></a><span data-ttu-id="6c3ec-103">PatchMesh9</span><span class="sxs-lookup"><span data-stu-id="6c3ec-103">PatchMesh9</span></span>

<span data-ttu-id="6c3ec-104">定義貝塞爾修補程式所定義的網格。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="6c3ec-105">第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的修補程式。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

<span data-ttu-id="6c3ec-106">其中：</span><span class="sxs-lookup"><span data-stu-id="6c3ec-106">Where:</span></span>

-   <span data-ttu-id="6c3ec-107">類型-修補程式網格類型：矩形、三角形或 N 修補程式。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-107">Type - Patch mesh type: rectangle, triangle, or N-patch.</span></span>
-   <span data-ttu-id="6c3ec-108">曲線方程式中的變數程度。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-108">Degree - Degree of the variables in the curve equation.</span></span>
-   <span data-ttu-id="6c3ec-109">高序位修補程式介面的基礎型別。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-109">Basis - Basis type of a high-order patch surface.</span></span>
-   <span data-ttu-id="6c3ec-110">nVertices-頂點數目。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-110">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="6c3ec-111">頂點 \[ nVertices \] -頂點的陣列。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-111">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="6c3ec-112">請參閱 [**Vector**](vector.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-112">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="6c3ec-113">nPatches-修補程式的數目。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-113">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="6c3ec-114">修補程式 \[ nPatches \] -修補程式陣列。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-114">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="6c3ec-115">請參閱 [**Patch**](patch.md)。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-115">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="6c3ec-116">\[ ... \] -您可以在這裡使用任何的. x 檔案範本。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-116">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="6c3ec-117">這可讓架構成為可擴充的。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-117">This makes the architecture extensible.</span></span>

<span data-ttu-id="6c3ec-118">修補程式會使用頂點陣列中的頂點做為每個修補程式的控制點。</span><span class="sxs-lookup"><span data-stu-id="6c3ec-118">The patches use the vertices in the array of vertices as the control points for each patch.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c3ec-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c3ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3ec-120">範本</span><span class="sxs-lookup"><span data-stu-id="6c3ec-120">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



