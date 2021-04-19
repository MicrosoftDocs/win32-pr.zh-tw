---
description: 用於網格物件中，以指定要將哪些材質套用至哪些臉部。 NMaterials 成員會指定有多少材質存在，而材質則會指定要套用的材質。
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972917"
---
# <a name="meshmateriallist"></a><span data-ttu-id="c2792-104">MeshMaterialList</span><span class="sxs-lookup"><span data-stu-id="c2792-104">MeshMaterialList</span></span>

<span data-ttu-id="c2792-105">用於網格物件中，以指定要將哪些材質套用至哪些臉部。</span><span class="sxs-lookup"><span data-stu-id="c2792-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="c2792-106">NMaterials 成員會指定有多少材質存在，而材質則會指定要套用的材質。</span><span class="sxs-lookup"><span data-stu-id="c2792-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

<span data-ttu-id="c2792-107">其中：</span><span class="sxs-lookup"><span data-stu-id="c2792-107">Where:</span></span>

-   <span data-ttu-id="c2792-108">nMaterials-DWORD。</span><span class="sxs-lookup"><span data-stu-id="c2792-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="c2792-109">材質數目。</span><span class="sxs-lookup"><span data-stu-id="c2792-109">The number of materials.</span></span>
-   <span data-ttu-id="c2792-110">nFaceIndexes-DWORD。</span><span class="sxs-lookup"><span data-stu-id="c2792-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="c2792-111">索引的數目。</span><span class="sxs-lookup"><span data-stu-id="c2792-111">The number of indices.</span></span>
-   <span data-ttu-id="c2792-112">faceIndexes \[ nFaceIndexes \] -包含臉部索引的 dword 陣列。</span><span class="sxs-lookup"><span data-stu-id="c2792-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2792-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2792-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2792-114">範本</span><span class="sxs-lookup"><span data-stu-id="c2792-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



