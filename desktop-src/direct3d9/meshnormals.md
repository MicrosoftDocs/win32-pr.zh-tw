---
description: 定義網格的法線。
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187498"
---
# <a name="meshnormals"></a><span data-ttu-id="7e496-103">MeshNormals</span><span class="sxs-lookup"><span data-stu-id="7e496-103">MeshNormals</span></span>

<span data-ttu-id="7e496-104">定義網格的法線。</span><span class="sxs-lookup"><span data-stu-id="7e496-104">Defines normals for a mesh.</span></span> <span data-ttu-id="7e496-105">向量的第一個陣列是一般向量本身，而第二個數組是索引的陣列，用來指定要套用至指定臉部的法線。</span><span class="sxs-lookup"><span data-stu-id="7e496-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="7e496-106">NFaceNormals 成員的值應等於網格中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="7e496-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

<span data-ttu-id="7e496-107">其中：</span><span class="sxs-lookup"><span data-stu-id="7e496-107">Where:</span></span>

-   <span data-ttu-id="7e496-108">nNormals：法線數目。</span><span class="sxs-lookup"><span data-stu-id="7e496-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="7e496-109">陣列向量法線 \[ nNormals \] -法線的陣列。</span><span class="sxs-lookup"><span data-stu-id="7e496-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="7e496-110">請參閱 [**Vector**](vector.md)。</span><span class="sxs-lookup"><span data-stu-id="7e496-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="7e496-111">nFaceNormals-臉部法線的數目。</span><span class="sxs-lookup"><span data-stu-id="7e496-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="7e496-112">陣列 MeshFace faceNormals \[ nFaceNormals \] -網狀臉部法線的陣列。</span><span class="sxs-lookup"><span data-stu-id="7e496-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="7e496-113">請參閱 [**MeshFace**](meshface.md)。</span><span class="sxs-lookup"><span data-stu-id="7e496-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7e496-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e496-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e496-115">範本</span><span class="sxs-lookup"><span data-stu-id="7e496-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



