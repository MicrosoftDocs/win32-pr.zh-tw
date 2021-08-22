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
ms.openlocfilehash: 073a9ac7eb56c0870d7a08d8ed9fd221a2626bb6be83cc4683cd86c4bfa907db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144921"
---
# <a name="configuring-compressors-and-decompressors"></a>設定壓縮機和 Decompressors

下列範例會使用 [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) 宏來示範如何測試「壓縮箱」是否支援 [設定] 對話方塊，並在執行時顯示。


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



下列範例顯示如何使用 [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) 宏取得狀態資料。


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



下列範例顯示如何使用 [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) 宏還原狀態資料。 應用程式還原的狀態資料不應包含從驅動程式取得之狀態資料的任何變更。


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




