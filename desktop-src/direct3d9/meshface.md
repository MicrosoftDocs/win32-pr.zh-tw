---
description: 由網狀範本用來定義網格的臉部。 NFaceVertexIndices 陣列的每個元素都會參考用來建立臉部的網格頂點。
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108464"
---
# <a name="meshface"></a><span data-ttu-id="c89f0-104">MeshFace</span><span class="sxs-lookup"><span data-stu-id="c89f0-104">MeshFace</span></span>

<span data-ttu-id="c89f0-105">由 [**網狀**](mesh.md) 範本用來定義網格的臉部。</span><span class="sxs-lookup"><span data-stu-id="c89f0-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="c89f0-106">NFaceVertexIndices 陣列的每個元素都會參考用來建立臉部的網格頂點。</span><span class="sxs-lookup"><span data-stu-id="c89f0-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="c89f0-107">其中：</span><span class="sxs-lookup"><span data-stu-id="c89f0-107">Where:</span></span>

-   <span data-ttu-id="c89f0-108">nFaceVertexIndices-索引的數目。</span><span class="sxs-lookup"><span data-stu-id="c89f0-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="c89f0-109">陣列 DWORD faceVertexIndices \[ nFaceVertexIndices \] -索引的陣列。</span><span class="sxs-lookup"><span data-stu-id="c89f0-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="c89f0-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c89f0-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c89f0-111">範本</span><span class="sxs-lookup"><span data-stu-id="c89f0-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



