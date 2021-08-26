---
description: 每個新的執行緒或光纖都會收到自己的堆疊空間，其中包含保留和最初認可的記憶體。
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: 執行緒堆疊大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff392577d529ab03a3859a0c6b0a94057ff8d8e0dc3c09fef86176d5c8950ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031408"
---
# <a name="thread-stack-size"></a>執行緒堆疊大小

每個新的執行緒或光纖都會收到自己的堆疊空間，其中包含保留和最初認可的記憶體。 保留的記憶體大小代表虛擬記憶體中的總堆疊配置。 因此，保留的大小會限制為虛擬位址範圍。 初始認可的頁面不會使用實體記憶體，直到被參考為止;不過，它們會從系統的認可限制總計移除頁面，也就是分頁檔的大小加上實體記憶體的大小。 系統會視需要從保留的堆疊記憶體認可額外的頁面，直到堆疊到達保留大小減去一頁 (這會用來做為防護頁面，以防止堆疊溢位) 或系統在記憶體中的記憶體不足而導致作業失敗。

最好選擇盡可能小的堆疊大小，並認可執行緒或光纖所需的堆疊以可靠地執行。 保留給堆疊的每個頁面都不能用於任何其他用途。

堆疊會在其執行緒結束時釋放。 如果執行緒由另一個執行緒終止，則不會釋放它。

保留和初始認可的堆疊記憶體預設大小是在可執行檔標頭中指定。 如果沒有足夠的記憶體可保留或認可要求的位元組數目，執行緒或光纖建立將會失敗。 連結器所使用的預設堆疊保留大小是 1 MB。 若要為所有線程和纖維指定不同的預設堆疊保留大小，請在模組定義中使用 STACKSIZE 語句 ( .def) 檔。 作業系統會將指定的大小四捨五入到最接近系統組態細微性的倍數 (通常是 64 KB) 。 若要取出目前系統的配置資料細微性，請使用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。

若要變更最初認可的堆疊空間，請使用 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)、 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)或 [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)函數的 *dwStackSize* 參數。 此值會無條件進位到最接近的頁面。 一般而言，保留大小是在可執行檔標頭中指定的預設保留大小。 但是，如果 *dwStackSize* 所指定的最初認可大小大於或等於預設的保留大小，則保留大小為最接近 1 MB 倍數的新認可大小。

若要變更保留的堆疊大小，請將 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)或 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)的 *dwCreationFlags* 參數設定為 stack \_ 大小 PARAM 的 \_ \_ \_ \_ 保留，並使用 *dwStackSize* 參數。 在此情況下，最初認可的大小是在可執行檔標頭中指定的預設大小。 若為纖維，請使用 [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)的 *dwStackReserveSize* 參數。 認可的大小是在 *dwStackCommitSize* 參數中指定。

[**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)函式會設定與呼叫執行緒或光纖相關聯之堆疊的最小大小，在任何堆疊溢位例外狀況期間都可以使用。

 

 
