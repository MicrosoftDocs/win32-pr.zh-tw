---
description: 當處理常式完成檔案對應物件時，應該使用每個檔案視圖的 UnmapViewOfFile 函式，以終結其位址空間中的所有檔案視圖。
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: 關閉檔案對應物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49734a8cf0b2d4fce2025196fc867926840e89c48b352c3dc1f096da9363ac0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992956"
---
# <a name="closing-a-file-mapping-object"></a>關閉檔案對應物件

當處理常式完成檔案對應物件時，應該使用每個檔案視圖的 [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) 函式，以終結其位址空間中的所有檔案視圖。

取消對應檔案的對應視圖會使此進程的位址空間中的視圖所佔用的範圍失效，並讓範圍可供其他配置使用。 它會移除每個未對應的虛擬頁面的工作集專案，這是處理常式的工作集一部分，並減少進程的工作集大小。 它也會減少對應實體頁面的共用計數。

未對應的視圖中修改過的頁面不會寫入至磁片，直到其共用計數到達零為止，或者也就是從共用頁面的所有進程的工作集取消對應或修剪為止。 就算如此，修改過的頁面也會「延遲」寫入磁片;也就是說，修改可能會快取在記憶體中，並于稍後寫入磁片。 為了將發生電源中斷或系統損毀時資料遺失的風險降至最低，應用程式應該使用 [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) 函式明確地排清修改過的頁面。

當每個程式使用檔案對應物件完成，而且已將所有視圖都未對應時，它必須藉由呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)來關閉檔案對應物件的控制碼和磁片上的檔案。 即使有檔案視圖仍處於開啟狀態，這些 **CloseHandle** 的呼叫還是會成功。 不過，保留檔案視圖會導致記憶體流失。

 

 
