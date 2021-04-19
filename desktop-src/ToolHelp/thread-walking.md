---
title: 執行緒走
description: 包含執行緒清單的快照集包含每個目前正在執行之進程的每個執行緒的相關資訊。
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- 列舉
- 列舉，執行緒
- 執行緒
- 執行緒，列舉執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967683"
---
# <a name="thread-walking"></a>執行緒走

包含執行緒清單的快照集包含每個目前正在執行之進程的每個執行緒的相關資訊。 您可以使用 [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) 函式，來取得清單中第一個執行緒的資訊。 在取得清單中的第一個執行緒之後，您可以使用 [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) 函式來抓取後續執行緒的資訊。 **Thread32First** 和 **Thread32Next** 會以快照集中個別執行緒的相關資訊來填滿 [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) 結構。

您可以取得包含執行緒的快照集，然後藉由追蹤執行緒清單來列舉特定進程的執行緒，並保留與指定進程具有相同處理序識別碼之執行緒的相關資訊。

您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)和 [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)的擴充錯誤狀態碼。

> [!Note]  
> [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)的 **th32ThreadID** 成員內容是執行緒識別碼，可供任何需要執行緒識別碼的函式使用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遍歷執行緒清單](traversing-the-thread-list.md)
</dt> </dl>

 

 