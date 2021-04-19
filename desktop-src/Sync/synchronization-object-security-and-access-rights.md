---
description: Windows 安全性模型可讓您控制事件、mutex、信號和可等候計時器物件的存取。 計時器佇列、連鎖變數和重要區段物件都不是安全的。 如需詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: 同步處理物件安全性和存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c4bfdb17a6e1c4d99a3e9722e67a3b48a3c788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989436"
---
# <a name="synchronization-object-security-and-access-rights"></a>同步處理物件安全性和存取權限

Windows 安全性模型可讓您控制事件、mutex、信號和可等候計時器物件的存取。 計時器佇列、連鎖變數和重要區段物件都不是安全的。 如需詳細資訊，請參閱 [存取控制模型](../secauthz/access-control-model.md)。

當您呼叫 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)、 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)、 [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)或 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)函式時，可以指定進程同步處理物件的 [安全描述項](../secauthz/security-descriptors.md)。 如果您指定 **Null**，則物件會取得預設安全描述項。 在同步處理物件的預設安全描述項中， [ (acl) 的存取控制清單 ](../secauthz/access-control-lists.md) ，是來自建立者的主要或模擬權杖。

若要取得或設定事件、mutex、信號或可等候計時器物件的安全描述項，請呼叫 [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)或 [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)、 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)、 [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)和 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)傳回的控制碼具有新物件的完整存取權。 當您呼叫 [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa)、 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw)、 [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)和 [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) 函式時，系統會針對物件的安全描述項，檢查要求的存取權限。

進程間同步處理物件的有效存取權限包括 [標準存取權限](../secauthz/standard-access-rights.md) ，以及某些特定物件的存取權限。 下表列出所有物件使用的標準存取權限。

| 值                           | 意義                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **刪除** (0x00010000L)         | 刪除物件的必要參數。                                                                                                                                                                                                                                                           |
| **讀取 \_控制** (0x00020000L)  | 需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。 若要讀取或寫入 SACL，您必須要求 **存取 \_ 系統 \_ 安全性** 存取權限。 如需詳細資訊，請參閱 [SACL 訪問](../secauthz/sacl-access-right.md)許可權。 |
| **同步處理** (0x00100000L)    | 使用同步物件的權限。 這可讓執行緒等候，直到物件處於已發出信號的狀態。                                                                                                                                                                |
| **寫入 \_DAC** (0x00040000L)     | 修改物件安全描述項中的 DACL 時需要。                                                                                                                                                                                                                   |
| **寫入 \_擁有** 者 (0x00080000L)   | 需要變更物件之安全描述項中的擁有者。                                                                                                                                                                                                                  |



 

下表列出事件物件的特定物件存取權限。 除了標準存取權限之外，還支援這些權利。



| 值                             | 意義                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_所有 \_ 存取** (0x1F0003)  | 事件物件的所有可能存取權限。 只有當您的應用程式需要存取超過標準存取權限和 **事件 \_ 修改 \_ 狀態** 所授與的存取權時，才使用此許可權。 使用此存取權限可增加您的應用程式必須由系統管理員執行的可能性。 |
| **活動 \_修改 \_ 狀態** (0x0002)  | 修改 [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent)、 [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) 和 [**PulseEvent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) 函數所需的狀態存取。                                                                                                                                    |



 

下表列出 mutex 物件的物件特定存取權限。 除了標準存取權限之外，還支援這些權利。



| 值                             | 意義                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MUTEX \_所有 \_ 存取** (0x1F0001)  | Mutex 物件的所有可能存取權限。 只有在您的應用程式需要存取標準存取權限所授與的存取權之後，才使用此許可權。 使用此存取權限可增加您的應用程式必須由系統管理員執行的可能性。 |
| **MUTEX \_修改 \_ 狀態** (0x0001)  | 保留供未來使用。                                                                                                                                                                                                                                           |



 

下表列出信號物件的物件特定存取權限。 除了標準存取權限之外，還支援這些權利。



| 值                                 | 意義                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **信號 \_所有 \_ 存取** (0x1F0003)  | 信號物件的所有可能存取權限。 只有當您的應用程式需要存取超過標準存取權限和 **信號 \_ 修改 \_ 狀態** 所授與的存取權時，才使用此許可權。 使用此存取權限可增加您的應用程式必須由系統管理員執行的可能性。 |
| **信號 \_修改 \_ 狀態** (0x0002)  | 修改 [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) 函數所需的狀態存取。                                                                                                                                                                                                   |



 

下表列出可等候計時器物件的物件特定存取權限。 除了標準存取權限之外，還支援這些權利。



| 值                             | 意義                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **計時器 \_所有 \_ 存取** (0x1F0003)  | 可等候計時器物件的所有可能存取權限。 只有在您的應用程式需要存取超過標準存取權限和 **計時器 \_ 修改 \_ 狀態** 所授與的存取權時，才使用此許可權。 使用此存取權限可增加您的應用程式必須由系統管理員執行的可能性。 |
| **計時器 \_修改 \_ 狀態** (0x0002)  | 修改 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 和 [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) 函數所需的狀態存取。                                                                                                                                            |
| **計時器 \_查詢 \_ 狀態** (0x0001)   | 保留供未來使用。                                                                                                                                                                                                                                                                                 |



 

若要讀取或寫入進程進程同步處理物件的 SACL，您必須要求 **存取 \_ 系統 \_ 安全性** 存取權限。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](../secauthz/sacl-access-right.md)許可權[的存取控制清單](../secauthz/access-control-lists.md)。

 

 
