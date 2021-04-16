---
description: 定義可以在其他範本中使用的 GUID。
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: " (DirectX 9) 的 Guid"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510019"
---
# <a name="guid-directx-9"></a><span data-ttu-id="bfcd1-103"> (DirectX 9) 的 Guid</span><span class="sxs-lookup"><span data-stu-id="bfcd1-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="bfcd1-104">定義可以在其他範本中使用的 GUID。</span><span class="sxs-lookup"><span data-stu-id="bfcd1-104">Defines a GUID that can be used in other templates.</span></span>

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

<span data-ttu-id="bfcd1-105">這些參數會形成 GUID 的二進位儲存格式：</span><span class="sxs-lookup"><span data-stu-id="bfcd1-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="bfcd1-106">data1-32-位不帶正負號整數資料值</span><span class="sxs-lookup"><span data-stu-id="bfcd1-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="bfcd1-107">data2-16 位不帶正負號整數資料值</span><span class="sxs-lookup"><span data-stu-id="bfcd1-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="bfcd1-108">data3-16 位不帶正負號整數資料值</span><span class="sxs-lookup"><span data-stu-id="bfcd1-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="bfcd1-109">data4-不帶正負號字元的陣列</span><span class="sxs-lookup"><span data-stu-id="bfcd1-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="bfcd1-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfcd1-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcd1-111">範本</span><span class="sxs-lookup"><span data-stu-id="bfcd1-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



