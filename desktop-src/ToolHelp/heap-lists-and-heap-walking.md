---
title: 堆積清單和堆積行走
description: 包含指定進程之堆積清單的快照集包含每個與指定進程相關聯之堆積的識別資訊，以及每個堆積的詳細資訊。
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cc1eaa2093715e3f42fd52cc5191bedf5a0ac137cf93df57daa5ef590e2471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058225"
---
# <a name="heap-lists-and-heap-walking"></a>堆積清單和堆積行走

包含指定進程之堆積清單的快照集包含每個與指定進程相關聯之堆積的識別資訊，以及每個堆積的詳細資訊。 您可以使用 [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) 函式，來抓取堆積清單的第一個堆積的識別碼。 在抓取清單中的第一個堆積之後，您可以使用 [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) 函式，針對與進程相關聯的後續堆積來進行堆積清單。 **Heap32ListFirst** 和 **Heap32ListNext** 會以處理常式識別碼、堆積識別碼和描述堆積的旗標來填滿 [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) 結構。

您可以使用 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) 函數來取得堆積第一個區塊的相關資訊。 在抓取堆積的第一個區塊之後，您可以使用 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) 函數來取得相同堆積之後續區塊的相關資訊。 **Heap32First** 和 **Heap32Next** 會在 [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) 結構中填入適當堆積區塊的資訊。

您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)、 [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)、 [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)和 [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)的擴充錯誤狀態碼。

> [!Note]  
> 在 [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32)結構的 **th32HeapID** 成員中指定的堆積識別碼，只有工具說明函式的意義。 它不是控制碼，也不能供其他函式使用。

 

 

 