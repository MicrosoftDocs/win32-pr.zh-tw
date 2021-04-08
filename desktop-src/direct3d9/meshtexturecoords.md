---
description: 定義網格的材質座標。
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: MeshTextureCoords
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974ec31f4358578277cfac46dc014f34752df46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687447"
---
# <a name="meshtexturecoords"></a><span data-ttu-id="ac30d-103">MeshTextureCoords</span><span class="sxs-lookup"><span data-stu-id="ac30d-103">MeshTextureCoords</span></span>

<span data-ttu-id="ac30d-104">定義網格的材質座標。</span><span class="sxs-lookup"><span data-stu-id="ac30d-104">Defines a mesh's texture coordinates.</span></span>

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

<span data-ttu-id="ac30d-105">其中：</span><span class="sxs-lookup"><span data-stu-id="ac30d-105">Where:</span></span>

-   <span data-ttu-id="ac30d-106">nTextureCoords-材質座標的數目。</span><span class="sxs-lookup"><span data-stu-id="ac30d-106">nTextureCoords - Number of texture coordinates.</span></span>
-   <span data-ttu-id="ac30d-107">陣列 Coords2d textureCoords \[ nTextureCoords \] -2d 材質座標的陣列。</span><span class="sxs-lookup"><span data-stu-id="ac30d-107">array Coords2d textureCoords\[nTextureCoords\] - Array of 2D texture coordinates.</span></span> <span data-ttu-id="ac30d-108">請參閱 [**Coords2d**](coords2d.md)。</span><span class="sxs-lookup"><span data-stu-id="ac30d-108">See [**Coords2d**](coords2d.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ac30d-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac30d-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac30d-110">範本</span><span class="sxs-lookup"><span data-stu-id="ac30d-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



