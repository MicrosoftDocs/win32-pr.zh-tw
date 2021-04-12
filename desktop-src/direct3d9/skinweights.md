---
description: 此範本會以每個網狀架構為基礎來具現化。
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509882"
---
# <a name="skinweights"></a><span data-ttu-id="8da86-103">SkinWeights</span><span class="sxs-lookup"><span data-stu-id="8da86-103">SkinWeights</span></span>

<span data-ttu-id="8da86-104">此範本會以每個網狀架構為基礎來具現化。</span><span class="sxs-lookup"><span data-stu-id="8da86-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="8da86-105">在網狀架構中，會顯示此範本的 n 個實例序列，其中 n 是 (X 檔案框架的數目，這是影響網格中頂點的) 。</span><span class="sxs-lookup"><span data-stu-id="8da86-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="8da86-106">範本的每個實例基本上會定義特定骨骼在網格上的影響。</span><span class="sxs-lookup"><span data-stu-id="8da86-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="8da86-107">其中有一個頂點索引清單，以及一個相對應的加權清單。</span><span class="sxs-lookup"><span data-stu-id="8da86-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="8da86-108">其中：</span><span class="sxs-lookup"><span data-stu-id="8da86-108">Where:</span></span>

-   <span data-ttu-id="8da86-109">要定義其影響的骨骼名稱是 transformNodeName，而 nWeights 是受此骨骼影響的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="8da86-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="8da86-110">此骨骼受影響的頂點會包含在 vertexIndices 中，而且此骨骼所影響之每個頂點的權數都會包含在加權中。</span><span class="sxs-lookup"><span data-stu-id="8da86-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="8da86-111">矩陣 matrixOffset 會將網格頂點轉換成骨骼的空間。</span><span class="sxs-lookup"><span data-stu-id="8da86-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="8da86-112">當串連至骨骼的轉換時，這會提供與骨骼所影響之網格的世界空間座標。</span><span class="sxs-lookup"><span data-stu-id="8da86-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="8da86-113">請參閱 [**Matrix4x4**](matrix4x4.md)。</span><span class="sxs-lookup"><span data-stu-id="8da86-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8da86-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8da86-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da86-115">範本</span><span class="sxs-lookup"><span data-stu-id="8da86-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



