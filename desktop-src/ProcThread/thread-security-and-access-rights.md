---
description: Microsoft Windows 可讓您控制對執行緒物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 72709446-5c59-4fac-8dc8-7912906ecc85
title: 執行緒安全性和存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5e14b634b9e41f592df4911211c3374a67166e36fc4735f4a90009275b5da1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427707"
---
# <a name="thread-security-and-access-rights"></a>執行緒安全性和存取權限

Microsoft Windows 可讓您控制對執行緒物件的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](../secauthz/access-control-model.md)。

當您呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)、 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)、 [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)、 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)或 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)函數時，可以指定執行緒的 [安全描述項](../secauthz/security-descriptors.md)。 如果您指定 **Null**，執行緒會取得預設安全描述項。 執行緒之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。

若要取得執行緒的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) 函數。 若要變更執行緒的安全描述項，請呼叫 [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式所傳回的控制碼具有線程物件的 **\_ 所有 \_ 存取** 權。 當您呼叫 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 函式時，系統會傳回 pseudohandle，其中包含執行緒的安全描述項允許呼叫端的最大存取權。

執行緒物件的有效存取權限包括 [標準存取權限](../secauthz/standard-access-rights.md) ，以及某些執行緒特定的存取權限。 下表列出所有物件使用的標準存取權限。

| 值                           | 意義                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **刪除** (0x00010000L)         | 刪除物件的必要參數。                                                                                                                                                                                                                                                           |
| **讀取 \_控制** (0x00020000L)  | 需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。 若要讀取或寫入 SACL，您必須要求 **存取 \_ 系統 \_ 安全性** 存取權限。 如需詳細資訊，請參閱 [SACL 訪問](../secauthz/sacl-access-right.md)許可權。 |
| **同步處理** (0x00100000L)    | 使用同步物件的權限。 這可讓執行緒等候，直到物件處於已發出信號的狀態。                                                                                                                                                                |
| **寫入 \_DAC** (0x00040000L)     | 修改物件安全描述項中的 DACL 時需要。                                                                                                                                                                                                                   |
| **寫入 \_擁有** 者 (0x00080000L)   | 需要變更物件之安全描述項中的擁有者。                                                                                                                                                                                                                  |



 

下表列出執行緒特定的存取權限。



| 值                                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **同步處理** (0x00100000L)                     | 允許在任何 [等候](../sync/wait-functions.md)函式中使用執行緒控制碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **執行緒 \_ 所有 \_ 存取**                          | 執行緒物件的所有可能存取權限。**Windows Server 2003 和 Windows XP：**[**執行緒 \_ 所有 \_ 存取**] 旗標的值 Windows Server 2008 和 Windows Vista 增加。 如果針對 Windows server 2008 和 Windows Vista 編譯的應用程式在 Windows Server 2003 或 Windows XP 上執行，則「**執行緒 \_ 所有 \_ 存取**」旗標會包含不支援的存取位，而且指定此旗標的函式會失敗，並 **\_ \_ 拒絕錯誤存取**。 若要避免這個問題，請指定作業所需的最小存取權限集合。 如果必須使用 **執行緒的 \_ 所有 \_ 存取權**，請將 **\_ WIN32 \_ WINNT** 設定為您的應用程式設為目標的最小作業系統 (例如 `#define _WIN32_WINNT _WIN32_WINNT_WINXP`) 。 如需詳細資訊，請參閱[使用 Windows 標頭](../winprog/using-the-windows-headers.md)。 <br/> |
| **執行緒 \_直接 \_** 模擬 (0x0200)        | 模擬用戶端的伺服器執行緒所需。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **執行緒 \_取得 \_ 內容** (0x0008)                 | 使用 [**GetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)讀取執行緒內容的必要項。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **執行緒 \_模擬 (0x0100**)                  | 需要直接使用執行緒的安全性資訊，而不需要使用提供模擬服務的通訊機制來呼叫它。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **執行緒 \_ (\_** 0x0040) 的查詢資訊          | 從執行緒物件讀取特定資訊（例如結束代碼 (）的必要資訊，請參閱 [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)) 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **執行緒 \_查詢 \_ 有限 \_ 資訊** (0x0800)  | 從執行緒物件讀取特定資訊的必要 (參閱 [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)) 。 具有 [**執行緒 \_ 查詢 \_ 資訊**] 許可權的控制碼會自動授與 **執行緒 \_ 查詢的 \_ 有限 \_ 資訊**。**Windows伺服器2003和 Windows XP：** 不支援此存取權。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **執行緒 \_設定 \_** 0x0010) 內容 (                | 需要使用 [**SetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)撰寫執行緒的內容。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **執行緒 \_將 \_ 資訊設定** (0x0020)             | 在 thread 物件中設定某些資訊的必要項。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **執行緒 \_ (0x0400 設定 \_ 有限的 \_ 資訊**)    | 在 thread 物件中設定某些資訊的必要項。 具有 **執行緒 \_ 集 \_ 資訊** 存取權的控制碼會自動授與 **執行緒 \_ 設定 \_ 有限的 \_ 資訊**。**Windows伺服器2003和 Windows XP：** 不支援此存取權。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **執行緒 \_ (0x0080 設定 \_ 執行緒 \_ TOKEN**)           | 需要使用 [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)來設定執行緒的模擬權杖。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **執行緒 \_暫停 \_ 繼續** (0x0002)              | 暫停或繼續執行緒的必要 (參閱 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) 和 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)) 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **執行緒 \_終止** (0x0001)                    | 使用 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)終止執行緒的必要參數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

如果您想要讀取或寫入物件的 SACL，您可以向執行緒物件要求 **存取 \_ 系統 \_ 安全性** 存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](../secauthz/sacl-access-right.md)許可權[的存取控制清單](../secauthz/access-control-lists.md)。

## <a name="protected-processes"></a>受保護的處理程序

*受保護的進程* 可增強對數位 Rights Management 的支援。 系統會限制受保護進程的存取，以及受保護進程的執行緒。

**Windows Server 2003 和 Windows XP：** 從 Windows Vista 開始加入受保護的進程。

下列特定存取權限不允許來自受保護進程之執行緒的進程：

**執行緒 \_ 所有 \_ 存取**  
**執行緒 \_ 直接 \_ 模擬**  
**執行緒 \_ 取得 \_ 內容**  
**執行緒 \_ 模擬**  
**執行緒 \_ 查詢 \_ 資訊**  
**執行緒 \_ 集 \_ 內容**  
**執行緒 \_ 集 \_ 資訊**  
**執行緒 \_ 集 \_ 權杖**  
**執行緒 \_ 終止**  


已引進 **執行緒 \_ 查詢 \_ 限制 \_ 資訊** ，以提供可透過 **執行緒 \_ 查詢 \_ 資訊** 取得之資訊子集的存取權。

 

 
