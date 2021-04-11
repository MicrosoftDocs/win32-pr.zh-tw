---
description: 當 CreateProcess 函數建立新的進程時，會傳回新進程的控制碼及其主要執行緒。
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: 進程控制碼和識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319155"
---
# <a name="process-handles-and-identifiers"></a>進程控制碼和識別碼

當 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數建立新的進程時，會傳回新進程的控制碼及其主要執行緒。 這些控制碼是使用完整存取權限所建立，且受限於安全性存取檢查，可用於任何接受執行緒或進程控制碼的函式。 這些控制碼可由子進程繼承，視建立時指定的繼承旗標而定。 控制碼在關閉之前都是有效的，即使它們所代表的進程或執行緒已經終止也是一樣。

[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式也會傳回可在整個系統中唯一識別進程的識別碼。 進程可以使用 [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) 函式來取得自己的處理序識別碼 (也稱為處理序識別碼或 PID) 。 從建立程式到進程終止之前，識別碼是有效的。 進程可以使用 [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) 函式來取得其父進程的處理序識別碼。

如果您有進程識別碼，您可以藉由呼叫 [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) 函式來取得處理控制碼。 **OpenProcess** 可讓您指定控制碼的存取權限，以及是否可以繼承。

處理常式可以使用 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 函式，將虛擬控制碼取出至它自己的處理常式物件。 這個虛擬控制碼只對呼叫進程有效;它無法被繼承或複製以供其他進程使用。 若要取得進程的實際控制碼，請呼叫 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函數。

 

 
