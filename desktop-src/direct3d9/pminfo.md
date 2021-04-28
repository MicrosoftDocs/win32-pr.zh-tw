---
description: PMInfo-不支援。 由 DirectX 在內部使用。
ms.assetid: 8a07357f-d4e8-4104-9d21-51c3e8b8d6d2
title: PMInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cfc0edb59d22a14ca5ffefbded3a8c830161c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090166"
---
# <a name="pminfo"></a><span data-ttu-id="5155c-104">PMInfo</span><span class="sxs-lookup"><span data-stu-id="5155c-104">PMInfo</span></span>

<span data-ttu-id="5155c-105">不支援。</span><span class="sxs-lookup"><span data-stu-id="5155c-105">Not supported.</span></span> <span data-ttu-id="5155c-106">由 DirectX 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="5155c-106">Used internally by DirectX.</span></span>

``` syntax
template PMInfo 
{ 
    < B6C3E656-EC8B-4b92-9B62-681659522947 > 
    DWORD nAttributes; 
    array PMAttributeRange attributeRanges[nAttributes]; 
    DWORD nMaxValence; 
    DWORD nMinLogicalVertices; 
    DWORD nMaxLogicalVertices; 
    DWORD nVSplits; 
    array PMVSplitRecord splitRecords[nVSplits]; 
    DWORD nAttributeMispredicts; 
    array DWORD attributeMispredicts[nAttributeMispredicts]; 
}
```

## <a name="see-also"></a><span data-ttu-id="5155c-107">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5155c-107">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5155c-108">範本</span><span class="sxs-lookup"><span data-stu-id="5155c-108">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



