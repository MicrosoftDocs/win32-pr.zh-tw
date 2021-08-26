---
description: 當 CreateThread 或 CreateRemoteThread 函數建立新的執行緒時，就會傳回該執行緒的控制碼。
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: 執行緒控制碼和識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6058388f450b4b44c371fc26b132ea785b22c29bc0a2fd86875f563371608512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031628"
---
# <a name="thread-handles-and-identifiers"></a>執行緒控制碼和識別碼

當 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 或 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) 函數建立新的執行緒時，就會傳回該執行緒的控制碼。 根據預設，這個控制碼具有完整存取權限，而且受限於安全性存取檢查，可用於任何接受執行緒控制碼的函式。 這個控制碼可由子進程繼承，視建立時指定的繼承旗標而定。 此控制碼可由 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)複製，可讓您建立具有存取權限子集的執行緒控制碼。 控制碼在關閉之前是有效的，即使在其代表的執行緒終止之後也是如此。

[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)和 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)函式也會傳回可唯一識別整個系統中之執行緒的識別碼。 執行緒可以使用 [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) 函數來取得自己的執行緒識別碼。 線上程終止之前，識別碼會從建立執行緒的時間起有效。 請注意，任何執行緒識別碼都不會是0。

如果您有線程識別碼，您可以藉由呼叫 [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) 函數來取得執行緒控制碼。 **OpenThread** 可讓您指定控制碼的存取權限，以及是否可以繼承。

執行緒可以使用 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 函式，將 *虛擬控制碼* 取出至本身的執行緒物件。 這個虛擬控制碼只對呼叫進程有效;它無法被繼承或複製以供其他進程使用。 若要取得執行緒的實際控制碼，請在給定虛擬控制碼的情況下，使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函數。

若要列舉進程的執行緒，請使用 [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) 和 [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) 函數。

 

 
