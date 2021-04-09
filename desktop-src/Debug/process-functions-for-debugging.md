---
description: CreateProcess 函式可讓偵錯工具啟動處理常式並進行調試。
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: 用於偵錯工具的進程函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936208"
---
# <a name="process-functions-for-debugging"></a>用於偵錯工具的進程函式

[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式可讓偵錯工具啟動處理常式並進行調試。 **CreateProcess** 的 *fdwCreate* 參數是用來指定偵錯工具的類型。 如果為 \_ 參數指定了 DEBUG PROCESS 旗標，則偵錯工具會將新的進程以及所有進程的下階，都在不使用 DEBUG PROCESS 旗標的情況下建立 \_ 。

如果 \_ \_ 只 \_ 針對 fdwCreate 指定 DEBUG 程式和 debug debug 這個 \_ 進程旗標，偵錯工具就會將新的進程（而非其子系）進行偵錯工具。

有一個偵錯工具可以使用 DEBUG 流程旗標建立進程，以進行另一個偵錯工具的偵錯工具 \_ 。  (偵錯工具的新進程) 必須使用 DEBUG process 旗標建立處理常式 \_ 。

[**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)函式可讓偵錯工具取得現有進程的識別碼。  ([**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) 函式會使用這個識別碼，將偵錯工具附加至進程。通常 ) ，偵錯工具會使用進程 \_ VM \_ 讀取和處理 \_ vm \_ 寫入旗標來開啟進程。 使用這些旗標，可讓偵錯工具使用 [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) 和 [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) 函式來讀取和寫入進程的虛擬記憶體。 如需詳細資訊，請參閱 [**進程和執行緒**](../procthread/processes-and-threads.md)。

 

 
