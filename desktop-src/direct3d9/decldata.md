---
description: 描述頂點宣告。
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467540"
---
# <a name="decldata"></a><span data-ttu-id="01776-103">DeclData</span><span class="sxs-lookup"><span data-stu-id="01776-103">DeclData</span></span>

<span data-ttu-id="01776-104">描述頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="01776-104">Describes a vertex declaration.</span></span>

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="01776-105">其中：</span><span class="sxs-lookup"><span data-stu-id="01776-105">Where:</span></span>

-   <span data-ttu-id="01776-106">nElements：頂點宣告元素的數目。</span><span class="sxs-lookup"><span data-stu-id="01776-106">nElements - Number of vertex declaration elements.</span></span>
-   <span data-ttu-id="01776-107">Elements \[ nElements \] -頂點宣告元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="01776-107">Elements\[nElements\] - Array of vertex declaration elements.</span></span>
-   <span data-ttu-id="01776-108">nDWords-DWORD 的數目。</span><span class="sxs-lookup"><span data-stu-id="01776-108">nDWords - Number of DWORDS.</span></span>
-   <span data-ttu-id="01776-109">資料 \[ nDWords \] -dword 的陣列，其中包含每個頂點元素中的資料。</span><span class="sxs-lookup"><span data-stu-id="01776-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="01776-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01776-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01776-111">範本</span><span class="sxs-lookup"><span data-stu-id="01776-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



