---
title: 流程行走
description: 包含進程清單的快照集包含每個目前執行之進程的相關資訊。
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- 列舉
- 列舉，進程
- 處理程序
- 進程，列舉進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6efa129182da256a6ce62b3754ea422df908248f7b0ecc30d3b690c29ffaf9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419658"
---
# <a name="process-walking"></a>流程行走

包含進程清單的快照集包含每個目前執行之進程的相關資訊。 您可以使用 [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) 函式，在清單中取得第一個進程的資訊。 在取得清單中的第一個程式之後，您可以使用 [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) 函式來進行後續專案的進程清單。 **Process32First** 和 **Process32Next** 會以快照中進程的相關資訊來填滿 [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) 結構。 如需範例，請參閱 [拍攝快照集和查看進程](taking-a-snapshot-and-viewing-processes.md)。

您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)和 [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)的擴充錯誤狀態碼。

您可以使用 [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) 函數 (或 [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) 函數) ，將特定進程中的記憶體讀入緩衝區。

> [!Note]  
> [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32)的 **th32ProcessID** 和 **th32ParentProcessID** 成員的內容是處理序識別碼，並且可供任何需要處理序識別碼的函式使用。

 

 

 