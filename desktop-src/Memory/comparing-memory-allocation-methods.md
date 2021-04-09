---
Description: 以下是各種記憶體配置方法的簡短比較。
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: 比較記憶體配置方法
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "103946031"
---
# <a name="comparing-memory-allocation-methods"></a>比較記憶體配置方法

以下是各種記憶體配置方法的簡短比較：

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **新增功能**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

雖然 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)、 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)和 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 函式最終會配置相同堆積的記憶體，但每個函數都提供稍微不同的功能集。 例如，如果無法配置記憶體，則可指示 **HeapAlloc** 引發例外狀況，這是 **LocalAlloc** 無法使用的功能。 **LocalAlloc** 支援配置控制碼，以允許重新配置來移動基礎記憶體，而不變更控制碼值，也就是 **HeapAlloc** 無法使用的功能。

從32位 Windows 開始， [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) 和 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) 會實作為包裝函式，以使用處理程式預設堆積的控制碼來呼叫 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 。 因此， **GlobalAlloc** 和 **LocalAlloc** 的額外負荷高於 **HeapAlloc**。

因為不同的堆積配置器會使用不同的機制來提供獨特的功能，所以您必須使用正確的函式來釋放記憶體。 例如，使用 [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) 配置的記憶體必須使用 [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) 來釋放，而不是 [**>localfree**](/windows/desktop/api/WinBase/nf-winbase-localfree) 或 [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)。 使用 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) 或 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) 所配置的記憶體必須使用對應的全域或區域函數進行查詢、驗證和發行。

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)函式可讓您指定額外的記憶體配置選項。 不過，其配置會使用頁面細微性，因此使用 **VirtualAlloc** 可能會導致更高的記憶體使用量。

**Malloc** 函數具有與執行時間相依的缺點。 **New** 運算子的缺點是編譯器相依和語言相依。

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)函式的優點是在 c、c + + 或 Visual Basic 中都能正常運作。 它也是在以 COM 為基礎的應用程式中共用記憶體的唯一方式，因為 MIDL 會使用 **CoTaskMemAlloc** 和 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 來封送處理記憶體。


## <a name="examples"></a>範例

* [保留和認可記憶體](./reserving-and-committing-memory.md)

* [AWE 範例](./awe-example.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[全域和區域函數](global-and-local-functions.md)
</dt> <dt>

[堆積函數](heap-functions.md)
</dt> <dt>

[虛擬記憶體函數](virtual-memory-functions.md)
</dt> </dl>

 

 