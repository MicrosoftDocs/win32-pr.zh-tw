---
description: 核心物件控制碼是進程特定的。
ms.assetid: 3e3288dd-155a-41d0-9d43-5f49ed4c4a9d
title: 核心物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7cf8c46e4754c46e81cfd959f62de052332594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561915"
---
# <a name="kernel-objects"></a>核心物件

核心物件控制碼是進程特定的。 也就是說，處理常式必須建立物件或開啟現有的物件，才能取得核心物件控制碼。 核心控制碼的每個處理常式限制為 2 ^ 24。 不過，處理常式會儲存在分頁集區中，因此您可以建立的實際控制碼數目是以可用的記憶體為基礎。 您可以在32位 Windows 上建立的控制碼數目明顯低於 2 ^ 24。

任何程式都可以為現有的核心物件建立新的控制碼， (即使該進程知道物件的名稱，而且具有該物件的安全性存取權，也是由另一個進程) 所建立。 核心物件控制碼包括存取權限，指出可授與或拒絕處理常式的動作。 應用程式會在建立物件時指定存取權限，或取得現有的物件控制碼。 每種類型的核心物件都支援其本身的存取權限集。 例如，事件控制碼可以設定或等候存取 (或兩個) ，檔案控制代碼可以有 (或) 等的讀取或寫入存取權。 如需詳細資訊，請參閱 [安全物件](/windows/desktop/SecAuthZ/securable-objects)。

在下圖中，應用程式會建立事件物件。 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)函數會建立事件物件，並傳回物件控制碼。

![建立事件物件的應用程式](images/cshob-03.png)

建立事件物件之後，應用程式可以使用事件控制碼來設定或等候事件。 控制碼會維持有效，直到應用程式關閉控制碼或終止為止。

大部分的核心物件都支援單一物件的多個控制碼。 例如，上圖中的應用程式可以使用 [**OpenEvent**](/windows/desktop/api/synchapi/nf-synchapi-openeventa) 函式來取得額外的事件物件控制碼，如下圖所示。

![建立具有多個控制碼之事件物件的應用程式](images/cshob-04.png)

這個方法可讓應用程式擁有具有不同存取權限的控制碼。 例如，控制碼1可能已設定並等候事件的存取，而處理2可能只會有等候存取權。

如果另一個進程知道事件名稱，而且具有物件的安全性存取權，則可以使用 [**OpenEvent**](/windows/desktop/api/synchapi/nf-synchapi-openeventa)來建立自己的事件物件控制碼。 建立應用程式也可以使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函式，將其中一個控制碼複製到相同的進程或另一個進程中。

只要至少有一個物件控制碼存在，物件就會保留在記憶體中。 在下圖中，應用程式會使用 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式來關閉其事件物件控制碼。 如果沒有任何事件控制碼，系統就會從記憶體中移除物件，如下圖所示。

![應用程式關閉事件物件控制碼，以從記憶體中移除物件](images/cshob-08.png)

系統管理檔案物件的方式與其他核心物件稍有不同。 檔案物件包含檔案指標，也就是要在檔案中讀取或寫入下一個位元組的指標。 只要應用程式建立新的檔案控制代碼，系統就會建立新的檔案物件。 因此，有一個以上的檔案物件可以參考磁片上的單一檔案，如下圖所示。

![多個檔案物件參考磁片上的檔案](images/cshob-09.png)

只有透過重複或繼承才能有一個以上的檔案控制代碼參考相同的檔案物件，如下圖所示。

![兩個檔案控制代碼參考相同的檔案物件](images/cshob-10.png)

下表列出每個核心物件，以及每個物件的建立者和 destroyer 函數。 建立者函式會建立物件和物件控制碼，或建立新的現有物件控制碼。 Destroyer 函式會關閉物件控制碼。 當應用程式關閉核心物件的最後一個控制碼時，系統就會從記憶體中移除該物件。



| 核心物件                | Creator 函數                                                                                                                                                                                                                                                  | Destroyer 函式                                                                      |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| 存取權杖                 | [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)、 [**DuplicateToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)、 [**DuplicateTokenEx**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)、 [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)、 [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 變更通知          | [**FindFirstChangeNotification**](/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa)                                                                                                                                                                                                 | [**FindCloseChangeNotification**](/windows/desktop/api/fileapi/nf-fileapi-findclosechangenotification)                       |
| 通訊裝置        | [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                                                                                                                                                                                                                   | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 主控台輸入                | [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)，CONIN $                                                                                                                                                                                                                      | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 主控台畫面緩衝區        | [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)，CONOUT $                                                                                                                                                                                                                     | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 桌面                      | [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop)                                                                                                                                                                                                                     | 應用程式無法刪除此物件。                                                 |
| 事件                        | [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)、 [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa)、 [**OpenEvent**](/windows/desktop/api/synchapi/nf-synchapi-openeventa)                                                                                                                                                     | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 事件記錄檔                    | [**OpenEventLog**](/windows/desktop/api/winbase/nf-winbase-openeventloga)、 [**RegisterEventSource**](/windows/desktop/api/winbase/nf-winbase-registereventsourcea)、 [**OpenBackupEventLog**](/windows/desktop/api/winbase/nf-winbase-openbackupeventloga)                                                                                                                     | [**CloseEventLog**](/windows/desktop/api/winbase/nf-winbase-closeeventlog)                                                 |
| 檔案                         | [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                                                                                                                                                                                                                 | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)、 [ **DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)                     |
| 檔案對應                 | [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)、 [ **OpenFileMapping**](/windows/desktop/api/winbase/nf-winbase-openfilemappinga)                                                                                                                                                                          | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 尋找檔案                    | [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea)                                                                                                                                                                                                                             | [**FindClose**](/windows/desktop/api/fileapi/nf-fileapi-findclose)                                                           |
| 堆積                         | [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)                                                                                                                                                                                                                                 | [**HeapDestroy**](/windows/desktop/api/heapapi/nf-heapapi-heapdestroy)                                                     |
| I/o 完成埠          | [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport)                                                                                                                                                                                                           | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 工作 (Job)                          | [**CreateJobObject**](/windows/desktop/api/winbase/nf-winbase-createjobobjecta)                                                                                                                                                                                                                       | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 郵箱                     | [**CreateMailslot**](/windows/desktop/api/winbase/nf-winbase-createmailslota)                                                                                                                                                                                                                         | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 記憶體資源通知 | [**CreateMemoryResourceNotification**](/windows/desktop/api/memoryapi/nf-memoryapi-creatememoryresourcenotification)                                                                                                                                                                                     | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 模組                       | [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)、 [ **GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                                                                                                                                                                                  | [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)                                                     |
| Mutex                        | [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa)、 [**CreateMutexEx**](/windows/desktop/api/synchapi/nf-synchapi-createmutexexa)、 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw)                                                                                                                                                     | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| Pipe                         | [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea)、 [ **CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)                                                                                                                                                                                    | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)、 [ **DisconnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) |
| 處理序                      | [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)、 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)、 [**GetCurrentProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                                                                                                                                     | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)、 [ **TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)       |
| Semaphore                    | [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)、 [**CreateSemaphoreEx**](/windows/desktop/api/winbase/nf-winbase-createsemaphoreexa)、 [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)                                                                                                                             | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 插座                       | [**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket)， [**接受**](/windows/desktop/api/winsock2/nf-winsock2-accept)                                                                                                                                                                                                    | [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)                                                |
| Thread                       | [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)、 [**CreateRemoteThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread)、 [**GetCurrentThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                                                                                                                           | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)、 [ **TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread)         |
| 計時器                        | [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)、 [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw)、 [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)                                                                                                     | [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)                                                      |
| 更新資源              | [**BeginUpdateResource**](/windows/win32/api/winbase/nf-winbase-beginupdateresourcea)                                                                                                                                                                                                         | [**EndUpdateResource**](/windows/win32/api/winbase/nf-winbase-endupdateresourcea)                                   |
| 視窗站               | [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation)                                                                                                                                                                                                       | 應用程式無法刪除此物件。                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心物件命名空間](/windows/desktop/TermServ/kernel-object-namespaces)
</dt> </dl>

 

 
