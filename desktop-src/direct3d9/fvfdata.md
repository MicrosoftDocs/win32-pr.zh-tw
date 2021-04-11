---
description: 指定網格資料減去位置資料。
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108737"
---
# <a name="fvfdata"></a><span data-ttu-id="ad22c-103">FVFData</span><span class="sxs-lookup"><span data-stu-id="ad22c-103">FVFData</span></span>

<span data-ttu-id="ad22c-104">指定網格資料減去位置資料。</span><span class="sxs-lookup"><span data-stu-id="ad22c-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="ad22c-105">其中：</span><span class="sxs-lookup"><span data-stu-id="ad22c-105">Where:</span></span>

-   <span data-ttu-id="ad22c-106">dwFVF-FVF 程式碼。</span><span class="sxs-lookup"><span data-stu-id="ad22c-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="ad22c-107">nDWords-二進位資料。</span><span class="sxs-lookup"><span data-stu-id="ad22c-107">nDWords - Binary data.</span></span> <span data-ttu-id="ad22c-108">DWORD 的數目。</span><span class="sxs-lookup"><span data-stu-id="ad22c-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="ad22c-109">資料 \[ nDWords \] -dword 的陣列，其中包含每個頂點元素中的資料。</span><span class="sxs-lookup"><span data-stu-id="ad22c-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad22c-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad22c-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad22c-111">範本</span><span class="sxs-lookup"><span data-stu-id="ad22c-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



