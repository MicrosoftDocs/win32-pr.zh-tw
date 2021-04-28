---
description: VertexDuplicationIndices-此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090175"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="a2fe8-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="a2fe8-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="a2fe8-104">此範本會以每個網狀架構為基礎來具現化，並保留網格中哪些頂點與彼此重複的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="a2fe8-105">當頂點位於平滑群組或材質界限時，會產生重複的結果。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="a2fe8-106">此範本的目的是要讓載入器判斷哪些頂點的不同周邊參數實際上是模型中的相同頂點。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="a2fe8-107">某些應用程式 (網狀簡化，例如) 可以利用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="a2fe8-108">其中：</span><span class="sxs-lookup"><span data-stu-id="a2fe8-108">Where:</span></span>

-   <span data-ttu-id="a2fe8-109">nIndices-頂點索引的數目。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="a2fe8-110">這是網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="a2fe8-111">nOriginalVertices：發生任何重複之前，網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="a2fe8-112">\[如果未發生重複，值索引 n 會保存頂點的頂點 \] \[ n \] 在網格的頂點陣列中的頂點。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="a2fe8-113">因此，這個陣列中的索引是相同的，因此會指出重複的頂點。</span><span class="sxs-lookup"><span data-stu-id="a2fe8-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2fe8-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2fe8-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fe8-115">範本</span><span class="sxs-lookup"><span data-stu-id="a2fe8-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



