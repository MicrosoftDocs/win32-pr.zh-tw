---
description: Mutex 物件是一種同步處理物件，其狀態會設定為當執行緒不是任何執行緒所擁有時的信號，而未收到信號則是擁有時。
ms.assetid: eca0795a-1fd0-4034-9d61-9416670919cf
title: Mutex 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84c17ba3e99e888f7d1e9137a7f24a4d78ce2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850500"
---
# <a name="mutex-objects"></a>Mutex 物件

*Mutex 物件* 是一種同步處理物件，其狀態會設定為當執行緒不是任何執行緒所擁有時的信號，而未收到信號則是擁有時。 一次只能有一個執行緒可以擁有 mutex 物件，其名稱來自于協調共用資源的互斥存取。 例如，為了防止兩個執行緒同時寫入至共用記憶體，每個執行緒會在執行存取記憶體的程式碼之前，先等候 mutex 物件的擁有權。 寫入至共用記憶體之後，執行緒會釋放 mutex 物件。

執行緒使用 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) 或 [**CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) 函數來建立 mutex 物件。 建立執行緒可以要求 mutex 物件的立即擁有權，也可以指定 mutex 物件的名稱。 它也可以建立未命名的 mutex。 如需 mutex、事件、信號和計時器物件之名稱的詳細資訊，請參閱 [進程間同步](interprocess-synchronization.md)處理。

其他進程中的執行緒可以藉由在 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) 函式的呼叫中指定其名稱，來開啟現有已命名 mutex 物件的控制碼。 若要將控制碼傳遞給未命名的 mutex 至另一個進程，請使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函數或父子式控制碼繼承。

任何具有 mutex 物件之控制碼的執行緒都可以使用其中一個 [等候](wait-functions.md) 函式來要求 mutex 物件的擁有權。 如果 mutex 物件是由另一個執行緒所擁有，等候函式會封鎖發出要求的執行緒，直到擁有線程使用 [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) 函式釋放 mutex 物件為止。 Wait 函式的傳回值會指出函式是否因為 mutex 狀態以外的某個原因而傳回。

如果有一個以上的執行緒正在等候 mutex，則會選取等候中的執行緒。 請勿採用先進先出 (FIFO) 順序。 外來事件（例如核心模式 Apc）可以變更等候順序。

當執行緒取得 mutex 的擁有權之後，它可以在重複呼叫 [等候函式](wait-functions.md) 時指定相同的 mutex，而不會封鎖其執行。 這可防止在等候已擁有的 mutex 時，死結本身的執行緒。 若要在這種情況下釋放其擁有權，執行緒必須在每次 mutex 滿足 wait 函式的條件時，呼叫 [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) 一次。

如果執行緒在未釋放 mutex 物件的擁有權的情況下終止，則會將 mutex 物件視為被放棄。 等候中的執行緒可以取得已放棄之 mutex 物件的擁有權，但 wait 函式會傳回 Wait，表示已放棄 mutex 物件。 **\_** 已放棄的 mutex 物件表示發生錯誤，且受 mutex 物件保護的任何共用資源都處於未定義狀態。 如果執行緒依照 mutex 物件的方式繼續進行，則線上程釋出其擁有權後，就不會再被視為已放棄。 如果後續在等候函式中指定了 mutex 物件的控制碼，就會還原正常行為。

請注意， [重要區段物件](critical-section-objects.md) 提供的同步處理與 mutex 物件所提供的類似，不同之處在于，只有單一進程的執行緒可以使用重要區段物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Mutex 物件](using-mutex-objects.md)
</dt> </dl>

 

 
