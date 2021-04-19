---
description: 所有使用者都具有系統中處理常式清單的讀取權限，而且有許多不同的函式會列舉使用中的進程。 您應使用的函式將取決於所需平臺支援等因素。
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: 進程列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979783"
---
# <a name="process-enumeration"></a>進程列舉

所有使用者都具有系統中處理常式清單的讀取權限，而且有許多不同的函式會列舉使用中的進程。 您應使用的函式將取決於所需平臺支援等因素。

下列函數用來列舉進程。



| 函式                                                    | 描述                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | 抓取系統中每個處理常式物件的處理序識別碼。            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | 抓取系統快照中所發生第一個進程的相關資訊。    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | 抓取系統快照中所記錄之下一個進程的相關資訊。        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | 抓取指定終端機伺服器上使用中進程的相關資訊。 |



 

Toolhelp 函數和 [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) 列舉所有進程。 若要列出在特定使用者帳戶中執行的處理常式，請使用 [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) 並篩選使用者 SID。 您可以篩選會話識別碼，以隱藏在其他終端機伺服器會話中執行的進程。

您也可以藉由呼叫 [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)、 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)和 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 與 **TokenUser**，依使用者帳戶篩選進程（不論列舉函數為何）。 不過，除非您已授與存取權，否則無法開啟受安全描述項保護的進程。

 

 
