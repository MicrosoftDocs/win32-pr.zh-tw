---
description: 多個進程可以有相同事件、mutex、信號或計時器物件的控制碼，因此可以使用這些物件來完成進程間的同步處理。
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: 進程進程同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886348"
---
# <a name="interprocess-synchronization"></a>進程進程同步處理

多個進程可以有相同事件、mutex、信號或計時器物件的控制碼，因此可以使用這些物件來完成進程間的同步處理。 建立物件的程式可以使用建立函數所傳回的控制碼 ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)、 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)、 [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)或 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)) 。 其他處理常式可以使用其名稱或透過繼承或重複來開啟物件的控制碼。 如需詳細資訊，請參閱下列主題：

-   [物件名稱](object-names.md)
-   [物件繼承](object-inheritance.md)
-   [物件重複](object-duplication.md)

 

 
