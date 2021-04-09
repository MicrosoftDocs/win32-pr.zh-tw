---
title: 正在抓取目錄資訊
description: 正在抓取目錄資訊
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player 線上商店，正在抓取目錄資訊
- 線上商店，正在抓取目錄資訊
- 輸入1個線上商店，正在抓取目錄資訊
- Windows Media Player 線上商店、目錄的診斷資訊
- 線上商店、目錄的診斷資訊
- 輸入1個線上商店、目錄的診斷資訊
- Windows Media Player 線上商店，catcomp.exe
- 線上商店、catcomp.exe
- 輸入1個線上商店，catcomp.exe
- catcomp.exe
- 目錄的診斷資訊
- 正在抓取目錄資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674684"
---
# <a name="retrieving-catalog-information"></a><span data-ttu-id="55f7d-115">正在抓取目錄資訊</span><span class="sxs-lookup"><span data-stu-id="55f7d-115">Retrieving Catalog Information</span></span>

<span data-ttu-id="55f7d-116">您可以使用下列語法來執行 catcomp，以顯示目錄的診斷資訊：</span><span class="sxs-lookup"><span data-stu-id="55f7d-116">You can display diagnostic information on a catalog by running catcomp with the following syntax:</span></span>


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



<span data-ttu-id="55f7d-117">例如，下列命令會顯示整個類別目錄的相關資訊，包括版本、地區設定以及類別目錄專案的內部資訊：</span><span class="sxs-lookup"><span data-stu-id="55f7d-117">For example, the following command displays information on an entire catalog, including the version, locale, and internal information on catalog items:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



<span data-ttu-id="55f7d-118">以下顯示識別碼為3256的追蹤資訊：</span><span class="sxs-lookup"><span data-stu-id="55f7d-118">The following displays information for the track with ID 3256:</span></span>


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




