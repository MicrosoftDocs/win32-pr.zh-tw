---
title: 對齊錯誤
description: 對齊錯誤
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- 對齊錯誤 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965034"
---
# <a name="alignment-faults"></a>對齊錯誤

根據預設，系統會在 Itanium 型系統上關閉系統對齊-錯誤處理常式。 因此，任何未對齊的資料存取都會產生一個例外狀況，系統將不會自動修正此例外狀況，除非應用程式在以 [框架為基礎的例外狀況處理常式](/windows/desktop/Debug/frame-based-exception-handling)中攔截到例外狀況。 若要啟用系統對齊-錯誤處理函式，請使用 **SEM \_ NOALIGNMENTFAULTEXCEPT** 呼叫 [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode)函數。 不過，請注意，如果系統對齊-錯誤處理常式已啟用，且進程產生對齊錯誤，進程可能會遇到嚴重的效能降低。

如果 WinDbg 偵錯工具已安裝為系統偵錯工具，則如果系統上有任何進程產生未處理的例外狀況，則會自動啟動 WinDbg。 如果您沒有以系統偵錯工具的方式安裝偵錯工具，系統會顯示一個對話方塊，指出您的應用程式發生錯誤，並提供機會向 Microsoft 回報問題。

在 x64 和 ARM64 系統上，任何對齊錯誤都是由硬體和軟體的組合來處理。 為了達到最佳效能，記憶體的所有存取都應該適當對齊。 此外，您應該避免在 ARM64 上使用未對齊的 [連鎖變數存取](/windows/desktop/Sync/interlocked-variable-access) ，因為這些作業不是不可部分完成的安全。

 

 