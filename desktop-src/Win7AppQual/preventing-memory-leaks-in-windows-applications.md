---
description: 瞭解如何在 windows 7 和 Windows Server 2008 R2 平臺的 Windows 應用程式中避免記憶體流失。
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: 防止 Windows 應用程式中的記憶體流失
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104555028"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>防止 Windows 應用程式中的記憶體流失

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  

## <a name="description"></a>Description

記憶體流失是指應用程式無法在不再需要時釋放記憶體的錯誤類別。 經過一段時間後，記憶體流失會影響特定應用程式和作業系統的效能。 由於過度分頁，大量流失可能會導致無法接受的回應時間。 最後，應用程式和作業系統的其他部分將會發生失敗。

Windows 將會在進程終止時釋出應用程式所配置的所有記憶體，因此短時間執行的應用程式不會大幅影響整體系統效能。 不過，長時間執行的進程（例如服務或甚至是 Explorer 外掛程式）可能會大幅影響系統的可靠性，並且可能會強制使用者重新開機 Windows，以便讓系統再次可供使用。

應用程式可以使用多個方法來代表其配置記憶體。 如果未在使用後釋出，每種配置類型可能會導致流失。 以下是一些常見配置模式的範例：

-   透過 [**HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)函式或其 C/c + + 執行時間對等專案 **malloc** 或 **new** 的堆積記憶體
-   經由 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 函式從作業系統直接配置。
-   透過 Kernel32.dll Api （例如 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)、 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)或 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)）建立的核心控制碼，代表應用程式保留核心記憶體
-   根據預設，透過 User32 和 Gdi32 Api 建立的 GDI 和使用者控制碼 (，每個進程都有10000控制碼的配額) 

## <a name="best-practices"></a>最佳做法

監視應用程式在一段時間內的資源耗用量，是偵測及診斷記憶體流失的第一步。 使用 Windows 工作管理員並新增下列資料行：「認可大小」、「處理」、「使用者物件」和「GDI 物件」。 這可讓您建立應用程式的基準，並監視一段時間的資源使用量。

![顯示 Windows 工作管理員中 [進程] 頁面的螢幕擷取畫面。](images/preventingmemoryleaks-windowstaskmanager.gif)

下列 Microsoft 工具提供更詳細的資訊，可協助偵測及診斷應用程式中各種配置類型的流失：

-   效能監視器和資源監視器是 Windows 7 的一部分，而且可以監視和繪製一段時間的資源使用方式
-   最新版本的應用程式驗證器可以在 Windows 7 上診斷堆積流失
-   UMDH 是適用于 Windows 的偵錯工具的一部分，會分析指定進程的堆積記憶體配置，並有助於找出遺漏和其他不尋常的使用模式
-   Xperf 是精密的效能分析工具，可支援堆積配置追蹤
-   CRT Debug 堆積會追蹤堆積配置，並可協助建立您自己的堆積偵錯工具功能

某些編碼和設計實務可能會限制程式碼中的流失數目。

-   在 c + + 程式碼中，同時針對堆積配置以及 Win32 資源（例如核心 **控制碼** s）使用智慧型指標。 C + + 標準程式庫提供堆積配置的 **自動 \_ ptr** 類別。 針對其他配置類型，您將需要撰寫自己的類別。 ATL 程式庫提供一組豐富的類別來自動管理堆積物件和核心控制碼的資源
-   使用編譯器內建功能（例如 **\_ com \_ ptr \_ t** ）將您的 com 介面指標封裝到「智慧型指標」中，並協助參考計數。 其他 COM 資料類型有類似的類別： **\_ bstr \_ t** 和 **\_ variant \_ t**
-   監視您的 .NET 程式碼不尋常的記憶體使用量。 Managed 程式碼不會受到記憶體流失的漏洞。 請參閱如何尋找 GC 流失的「 [追蹤受控記憶體](/archive/blogs/ricom/) 流失」
-   請留意 web 用戶端程式代碼中的遺漏模式。 COM 物件和 JScript 之類的腳本引擎之間的迴圈參考，可能會造成 web 應用程式的大量洩漏。 「[瞭解和解決 Internet Explorer 流失模式](/previous-versions/ms976398(v=msdn.10))」有關于這類流失的詳細資訊。 您可以使用 JavaScript 記憶體流失偵測器來偵測程式碼中的記憶體流失。 雖然 Windows Internet Explorer 8 （隨附于 Windows 7 的 Windows 7）可減少這些問題，但較舊的瀏覽器仍會受到這些錯誤的影響。
-   避免使用來自函式的多個結束路徑。 在函式範圍中指派給變數的配置應該在函式結尾的一個特定區塊中釋放
-   請勿在您的程式碼中使用例外狀況，而不需要釋放函式中的所有區域變數。 如果您使用原生例外狀況，請釋放 finally 區塊內的所有配置 \_ \_ 。 如果您使用 c + + 例外狀況，則所有堆積和處理配置都必須包裝在智慧型指標中
-   請勿捨棄或重新初始化 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 物件，而不呼叫 [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear) 函數

## <a name="links-to-resources"></a>資源的連結

*常見配置模式：*

-   [**堆積配置函數**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**記憶體配置函數**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**New 運算子 (c + +)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**虛擬配置函數**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [核心物件](../sysinfo/kernel-objects.md)
-   [GDI 物件控制碼](../sysinfo/gdi-objects.md)
-   [消費者介面的物件控制碼](../sysinfo/user-objects.md)

*Microsoft 工具：*

-   [應用程式驗證器](application-verifier.md)
-   [Windows 的偵錯工具](/windows-hardware/drivers/debugger/)
-   [使用者模式傾印堆積](/windows-hardware/drivers/debugger/umdh)
-   [追蹤捕捉、處理和分析工具](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [CRT Debug 堆積](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*其他連結：*

-   [**自動 \_ Ptr 類別**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Active Template Library (ATL) 記憶體類別](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_com \_ ptr \_ t 物件**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_bstr \_ t 類別**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_variant \_ Yt 類別**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   [「追蹤受控記憶體流失」](/archive/blogs/ricom/)
-   [「瞭解和解決 Internet Explorer 流失模式」](/previous-versions/ms976398(v=msdn.10))
-   [「JavaScript 記憶體洩漏偵測器」](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [瀏覽器中的迴圈記憶體流失緩和 () ：](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**try-finally 陳述式**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**PROPVARIANT 結構**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**PropVariantClear 函式**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
