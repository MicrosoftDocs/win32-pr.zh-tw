---
title: 判斷驅動程式是否可以處理輸入格式
description: 判斷驅動程式是否可以處理輸入格式
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，輸入格式
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，輸入格式
- ICDrawQuery 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b3e2da69f8c061a7d0aefe847f40113d5104d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021431"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a><span data-ttu-id="5ba6f-106">判斷驅動程式是否可以處理輸入格式</span><span class="sxs-lookup"><span data-stu-id="5ba6f-106">Determining If a Driver Can Handle the Input Format</span></span>

<span data-ttu-id="5ba6f-107">下列範例顯示如何使用 [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) 宏來檢查輸入格式。</span><span class="sxs-lookup"><span data-stu-id="5ba6f-107">The following example shows how to check the input format with the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




