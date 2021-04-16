---
description: 同步處理物件是一種物件，可在其中一個等候函式中指定其控制碼，以協調多個執行緒的執行。
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: 同步處理物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299cbd6225b3cc7629378f5fe500fc36ccbe8e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513480"
---
# <a name="synchronization-objects"></a>同步處理物件

*同步處理物件* 是一種物件，可在其中一個 [等候](wait-functions.md)函式中指定其控制碼，以協調多個執行緒的執行。 有一個以上的進程可以有相同同步處理物件的控制碼，因此可以進行進程間同步處理。

以下是專為同步處理提供的物件類型。



| 類型           | Description                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 事件          | 告知一個以上的等候中執行緒已發生事件。 如需詳細資訊，請參閱 [事件物件](event-objects.md)。                                                                                   |
| Mutex          | 一次只能有一個執行緒擁有，可讓執行緒協調對共用資源的互斥存取。 如需詳細資訊，請參閱 [Mutex 物件](mutex-objects.md)。                          |
| Semaphore      | 會維護介於零和某個最大值之間的計數，以限制同時存取共用資源的執行緒數目。 如需詳細資訊，請參閱 [信號物件](semaphore-objects.md)。 |
| 可等候計時器 | 通知一或多個等候中的執行緒已到達指定的時間。 如需詳細資訊，請參閱 [可等候計時器物件](waitable-timer-objects.md)。                                                          |



 

雖然可供其他用途使用，但下列物件也可以用於同步處理。



| Object                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 變更通知          | 在指定的目錄或目錄樹狀結構內發生指定的變更類型時， [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) 函式所建立的狀態會設定為 [已發出信號]。 如需詳細資訊，請參閱 [取得目錄變更通知](../fileio/obtaining-directory-change-notifications.md)。                                                                                                                                   |
| 主控台輸入                | 建立主控台時建立。 當指定 CONIN $ 或 [**GetStdHandle**](/windows/console/getstdhandle)函式時， [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)函數會傳回主控台輸入的控制碼。 當主控台的輸入緩衝區中有未讀取的輸入時，它的狀態會設為 [已發出信號]，當輸入緩衝區是空的時，它會設為未收到信號。 如需有關主控台的詳細資訊，請參閱[字元模式應用程式](/windows/console/character-mode-applications)。 |
| 工作 (Job)                          | 藉由呼叫 [**CreateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) 函數來建立。 工作物件的狀態會在其所有處理常式終止時設定為已終止，因為已超過指定的工作時間限制。 如需工作物件的詳細資訊，請參閱 [工作物件](../procthread/job-objects.md)。                                                                                                                                                             |
| 記憶體資源通知 | 由 [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) 函數所建立。 在實體記憶體內發生指定的變更類型時，其狀態會設定為「已發出信號」。 如需記憶體的詳細資訊，請參閱 [記憶體管理](../memory/memory-management.md)。                                                                                                                                                                                  |
| 處理序                      | 藉由呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數所建立。 當程式正在執行時，其狀態會設為未收到信號，並在進程終止時設為已發出信號。 如需處理常式的詳細資訊，請參閱 [進程和執行緒](../procthread/processes-and-threads.md)。                                                                                                                                                                                  |
| Thread                       | 當透過呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)、 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)或 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) 函式來建立新的執行緒時建立。 當執行緒正在執行時，其狀態會設為未收到信號，並線上程終止時設為已發出信號。 如需執行緒的詳細資訊，請參閱 [進程和執行緒](../procthread/processes-and-threads.md)。                                                            |



 

在某些情況下，您也可以使用檔案、具名管道或通訊裝置作為同步處理物件;但是，不建議使用這些用途。 相反地，請使用非同步 i/o，並等候重 [**迭結構中的事件**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 物件集。 使用事件物件會比較安全，因為在相同的檔案、具名管道或通訊裝置上執行多個同時重迭的作業時可能會發生混淆。 在此情況下，無法得知哪一個作業導致物件的狀態被告知。

如需有關檔案、具名管道或通訊之 i/o 作業的詳細資訊，請參閱 [同步處理和重迭的輸入和輸出](synchronization-and-overlapped-input-and-output.md)。

 

 
