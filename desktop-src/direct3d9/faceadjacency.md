---
description: FaceAdjacency-此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090506"
---
# <a name="faceadjacency"></a><span data-ttu-id="9da41-103">FaceAdjacency</span><span class="sxs-lookup"><span data-stu-id="9da41-103">FaceAdjacency</span></span>

<span data-ttu-id="9da41-104">此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9da41-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="9da41-105">當頂點位於平滑群組或材質界限時，會產生重複的結果。</span><span class="sxs-lookup"><span data-stu-id="9da41-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="9da41-106">此範本的目的是要讓載入器判斷哪些頂點的不同周邊參數實際上是模型中的相同頂點。</span><span class="sxs-lookup"><span data-stu-id="9da41-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="9da41-107">某些應用程式 (網狀簡化，例如) 可以利用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="9da41-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="9da41-108">其中：</span><span class="sxs-lookup"><span data-stu-id="9da41-108">Where:</span></span>

-   <span data-ttu-id="9da41-109">nIndices-網格中的索引數目。</span><span class="sxs-lookup"><span data-stu-id="9da41-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="9da41-110">索引 \[ nIndices \] -索引的陣列。</span><span class="sxs-lookup"><span data-stu-id="9da41-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="9da41-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9da41-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da41-112">範本</span><span class="sxs-lookup"><span data-stu-id="9da41-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



