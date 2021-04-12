---
description: 指定網格的頂點色彩，而不是套用每個臉部或每個網格的材質。
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385632"
---
# <a name="meshvertexcolors"></a><span data-ttu-id="9f2b4-103">MeshVertexColors</span><span class="sxs-lookup"><span data-stu-id="9f2b4-103">MeshVertexColors</span></span>

<span data-ttu-id="9f2b4-104">指定網格的頂點色彩，而不是套用每個臉部或每個網格的材質。</span><span class="sxs-lookup"><span data-stu-id="9f2b4-104">Specifies vertex colors for a mesh, instead of applying a material per face or per mesh.</span></span>

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

<span data-ttu-id="9f2b4-105">其中：</span><span class="sxs-lookup"><span data-stu-id="9f2b4-105">Where:</span></span>

-   <span data-ttu-id="9f2b4-106">nVertexColors-色彩數目。</span><span class="sxs-lookup"><span data-stu-id="9f2b4-106">nVertexColors - Number of colors.</span></span> <span data-ttu-id="9f2b4-107">這符合網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="9f2b4-107">This matches the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="9f2b4-108">陣列 IndexColor vertexColors \[ nVertexColors \] -索引色彩的陣列。</span><span class="sxs-lookup"><span data-stu-id="9f2b4-108">array IndexColor vertexColors\[nVertexColors\] - Array of indexed colors.</span></span> <span data-ttu-id="9f2b4-109">請參閱 [**IndexedColor**](indexedcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="9f2b4-109">See [**IndexedColor**](indexedcolor.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9f2b4-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f2b4-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2b4-111">範本</span><span class="sxs-lookup"><span data-stu-id="9f2b4-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



