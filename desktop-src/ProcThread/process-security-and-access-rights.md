---
description: Microsoft Windows 安全性模型可讓您控制處理物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 508a17c4-88cd-431a-a102-00180a7f7ab5
title: 流程安全性和存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668520a6f4e0eb8a81b55418033ff583bce8bddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988788"
---
# <a name="process-security-and-access-rights"></a>流程安全性和存取權限

Microsoft Windows 安全性模型可讓您控制處理物件的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](../secauthz/access-control-model.md)。

當使用者登入時，系統會收集在驗證程式期間可唯一識別使用者的一組資料，並將其儲存在 [存取權杖](../secauthz/access-tokens.md)中。 此存取權杖描述與使用者相關聯之所有進程的安全性內容。 進程的安全性內容是一組提供給處理常式的認證，或建立進程的使用者帳戶。

您可以使用權杖，以使用 [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw) 函式來指定進程的目前安全性內容。 當您呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)、 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)或 [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)函式時，可以指定進程的 [安全描述項](../secauthz/security-descriptors.md)。 如果您指定 **Null**，進程會取得預設安全描述項。 進程之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。

若要取出進程的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) 函數。 若要變更進程的安全描述項，請呼叫 [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

處理常式物件的有效存取權限包括 [標準存取權限](../secauthz/standard-access-rights.md) ，以及某些特定進程的存取權限。 下表列出所有物件使用的標準存取權限。

| 值                           | 意義                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **刪除** (0x00010000L)         | 刪除物件的必要參數。                                                                                                                                                                                                                                                           |
| **讀取 \_控制** (0x00020000L)  | 需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。 若要讀取或寫入 SACL，您必須要求 **存取 \_ 系統 \_ 安全性** 存取權限。 如需詳細資訊，請參閱 [SACL 訪問](../secauthz/sacl-access-right.md)許可權。 |
| **同步處理** (0x00100000L)    | 使用同步物件的權限。 這可讓執行緒等候，直到物件處於已發出信號的狀態。                                                                                                                                                                |
| **寫入 \_DAC** (0x00040000L)     | 修改物件安全描述項中的 DACL 時需要。                                                                                                                                                                                                                   |
| **寫入 \_擁有** 者 (0x00080000L)   | 需要變更物件之安全描述項中的擁有者。                                                                                                                                                                                                                  |



 

下表列出特定進程的存取權限。



| 值                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **處理 \_ 所有 \_ 存取**                          | 處理常式物件的所有可能存取權限。**Windows Server 2003 和 WINDOWS XP：** Windows Server 2008 和 Windows Vista 上的 **進程 \_ 所有 \_ 存取** 旗標增加的大小。 如果針對 Windows Server 2008 和 Windows Vista 編譯的應用程式是在 Windows Server 2003 或 Windows XP 上執行，則「 **處理 \_ 所有 \_ 存取** 」旗標會太大，而指定此旗標的函式會失敗，並出現「 **\_ \_ 拒絕存取」錯誤**。 若要避免這個問題，請指定作業所需的最小存取權限集合。 如果必須使用 [ **處理 \_ 所有 \_ 存取** ]，請將 \_ WIN32 \_ WINNT 設定為您的應用程式設為目標的最小作業系統 (例如 `#define _WIN32_WINNT _WIN32_WINNT_WINXP`) 。 如需詳細資訊，請參閱 [使用 Windows 標頭](../winprog/using-the-windows-headers.md)。 <br/> |
| **進程 \_建立 \_ 進程** (0x0080)              | 建立處理常式所需。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **進程 \_建立 \_ 執行緒** (0x0002)               | 建立執行緒所需。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **進程 \_ (\_** 0x0040) 的 DUP 處理                 | 使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)複製控制碼所需。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **進程 \_ (\_** 0x0400) 的查詢資訊          | 若要取得處理常式的特定資訊（例如其權杖、結束代碼和優先順序類別 (），請參閱 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)) 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **進程 \_查詢 \_ 有限 \_ 資訊** (0x1000)  | 取得處理常式的特定資訊時需要 (參閱 [**>getexitcodeprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)、 [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)、 [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)、 [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)) 。 具有 [ **處理 \_ 查詢 \_ 資訊** ] 許可權的控制碼會自動被授與 **進程 \_ 查詢 \_ 限制 \_ 資訊**。**Windows Server 2003 和 Windows XP：** 不支援此存取權。<br/>                                                                                                                                                                                                                                                                                                                         |
| **進程 \_將 \_ 資訊設定** (0x0200)             | 若要設定處理常式的特定資訊（例如其優先順序類別 (請參閱 [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)) ）。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **進程 \_設定 \_ 配額** (0x0100)                   | 使用 [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize)設定記憶體限制所需。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **進程 \_暫停 \_ 繼續** (0x0800)              | 暫停或繼續進程的必要。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **進程 \_終止** (0x0001)                    | 使用 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)終止進程的必要參數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **進程 \_VM \_ 操作** (0x0008)                | 在處理常式的位址空間上執行作業時需要 (參閱 [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) 和 [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)) 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **進程 \_VM \_ READ** (0x0010)                     | 需要使用 [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)讀取進程中的記憶體。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **進程 \_VM \_ 寫入** (0x0020)                    | 需要使用 [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)寫入進程中的記憶體。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **同步處理** (0x00100000L)                      | 需要使用 [wait](../sync/wait-functions.md)函式來等候進程終止。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

若要開啟另一個進程的控制碼並取得完整存取權限，您必須啟用 **SeDebugPrivilege** 許可權。 如需詳細資訊，請參閱 [變更權杖中的許可權](../secbp/changing-privileges-in-a-token.md)。

[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函數所傳回的控制碼具有處理常式物件的 **\_ 所有 \_ 存取** 權。 當您呼叫 [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) 函式時，系統會針對進程安全描述項中的 DACL 檢查要求的 [存取權限](../secauthz/access-rights-and-access-masks.md) 。 當您呼叫 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 函式時，系統會傳回具有 DACL 允許呼叫端之最大存取權的 pseudohandle。

如果您想要讀取或寫入物件的 SACL，您可以向進程物件要求 **存取 \_ 系統 \_ 安全性** 存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](../secauthz/sacl-access-right.md)許可權[的存取控制清單](../secauthz/access-control-lists.md)。

> [!WARNING]
> 具有此處所述之一些存取權限的程式可以使用它們來取得其他存取權限。 例如，如果進程 A 具有處理常式 B 的控制碼，且進程會重複 **\_ \_ 處理** 存取，它可以複製進程 b 的虛擬控制碼。這會建立一個控制碼，該控制碼具有進程 B 的最大存取權。如需虛擬控制碼的詳細資訊，請參閱 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)。

 

## <a name="protected-processes"></a>受保護的處理程序

Windows Vista 引進了 *受保護的進程* ，以增強對數位 Rights Management 的支援。 系統會限制受保護進程的存取，以及受保護進程的執行緒。

下列標準存取權限不允許從進程到受保護的進程：

- **DELETE**  
- **讀取 \_ 控制**  
- **寫入 \_ DAC**  
- **寫入 \_ 擁有者**  

下列特定存取權限不允許從進程到受保護的進程：

- **處理 \_ 所有 \_ 存取**  
- **進程 \_ 建立 \_ 流程**  
- **進程 \_ 建立 \_ 執行緒**  
- **進程 \_ DUP \_ 控制碼**  
- **處理 \_ 查詢 \_ 資訊**  
- **進程 \_ 集 \_ 資訊**  
- **進程 \_ 集 \_ 配額**  
- **進程 \_ VM \_ 操作**  
- **進程 \_ VM \_ 讀取**  
- **進程 \_ VM \_ 寫入**  

我們引進了「程式 **\_ 查詢 \_ 限制的 \_ 資訊** 」許可權，以提供透過 **流程 \_ 查詢 \_ 資訊** 提供之資訊子集的存取權。
