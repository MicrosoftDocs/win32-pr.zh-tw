---
title: 設定壓縮機和 Decompressors
description: 設定壓縮機和 Decompressors
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，設定壓縮機
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，設定壓縮機
- ICQueryConfigure 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372113"
---
# <a name="configuring-compressors-and-decompressors"></a><span data-ttu-id="49fb5-106">設定壓縮機和 Decompressors</span><span class="sxs-lookup"><span data-stu-id="49fb5-106">Configuring Compressors and Decompressors</span></span>

<span data-ttu-id="49fb5-107">下列範例會使用 [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) 宏來示範如何測試「壓縮箱」是否支援 [設定] 對話方塊，並在執行時顯示。</span><span class="sxs-lookup"><span data-stu-id="49fb5-107">The following example uses the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro to demonstrate how to test whether a compressor supports the configuration dialog box and to display it if it does.</span></span>


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



<span data-ttu-id="49fb5-108">下列範例顯示如何使用 [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) 宏取得狀態資料。</span><span class="sxs-lookup"><span data-stu-id="49fb5-108">The following example shows how to obtain the state data using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



<span data-ttu-id="49fb5-109">下列範例顯示如何使用 [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) 宏還原狀態資料。</span><span class="sxs-lookup"><span data-stu-id="49fb5-109">The following example shows how to restore state data using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span> <span data-ttu-id="49fb5-110">應用程式還原的狀態資料不應包含從驅動程式取得之狀態資料的任何變更。</span><span class="sxs-lookup"><span data-stu-id="49fb5-110">State data restored by applications should not contain any changes to the state data obtained from a driver.</span></span>


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




