---
description: PatchMesh 會定義貝塞爾修補程式所定義的網格，包括頂點清單以及網格的補充程式，方法是在頂點陣列中編制索引。
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404711"
---
# <a name="patchmesh"></a><span data-ttu-id="ca0aa-103">PatchMesh</span><span class="sxs-lookup"><span data-stu-id="ca0aa-103">PatchMesh</span></span>

<span data-ttu-id="ca0aa-104">定義貝塞爾修補程式所定義的網格。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-104">Defines a mesh defined by Bézier patches.</span></span> <span data-ttu-id="ca0aa-105">第一個陣列是頂點的清單，而第二個數組會透過索引至頂點陣列來定義網格的修補程式。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-105">The first array is a list of vertices, and the second array defines the patches for the mesh by indexing into the vertex array.</span></span>

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

<span data-ttu-id="ca0aa-106">其中：</span><span class="sxs-lookup"><span data-stu-id="ca0aa-106">Where:</span></span>

-   <span data-ttu-id="ca0aa-107">nVertices-頂點數目。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-107">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="ca0aa-108">頂點 \[ nVertices \] -頂點的陣列。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-108">vertices\[nVertices\] - Array of vertices.</span></span> <span data-ttu-id="ca0aa-109">請參閱 [**Vector**](vector.md)。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-109">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="ca0aa-110">nPatches-修補程式的數目。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-110">nPatches - Number of patches.</span></span>
-   <span data-ttu-id="ca0aa-111">修補程式 \[ nPatches \] -修補程式陣列。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-111">patches\[nPatches\] - Array of patches.</span></span> <span data-ttu-id="ca0aa-112">請參閱 [**Patch**](patch.md)。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-112">See [**Patch**](patch.md).</span></span>
-   <span data-ttu-id="ca0aa-113">\[ ... \] -您可以在這裡使用任何的. x 檔案範本。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-113">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="ca0aa-114">這可讓架構成為可擴充的。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-114">This makes the architecture extensible.</span></span>

<span data-ttu-id="ca0aa-115">修補程式會使用頂點陣列中的頂點做為每個修補程式的控制點。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-115">The patches use the vertices in the array of vertices as the control points for each patch.</span></span> <span data-ttu-id="ca0aa-116">這是舊版的範本。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-116">This is a legacy template.</span></span> <span data-ttu-id="ca0aa-117">最新的修補程式網狀範本是 [**PatchMesh9**](patchmesh9.md)。</span><span class="sxs-lookup"><span data-stu-id="ca0aa-117">The latest patch mesh template is [**PatchMesh9**](patchmesh9.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ca0aa-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca0aa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0aa-119">範本</span><span class="sxs-lookup"><span data-stu-id="ca0aa-119">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



