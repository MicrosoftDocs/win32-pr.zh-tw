---
title: 關於 TraceLogging
description: TraceLogging 是使用者模式應用程式和核心模式驅動程式的新 Windows 10 事件追蹤。
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842412"
---
# <a name="about-tracelogging"></a>關於 TraceLogging

TraceLogging 是使用者模式應用程式和核心模式驅動程式的新 Windows 10 事件追蹤。 TraceLogging 是適用于 Windows (ETW) 之自我描述事件追蹤的格式。 TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。

TraceLogging 為 Windows 軟體追蹤預處理器 (的 WPP) 提供簡單的增強功能，可讓您將具有事件的結構化資料包括在內、使事件相互關聯的功能，以及全都不需要個別的檢測資訊清單 XML 檔案。 事件是自我描述的，表示包含檢測資訊清單的二進位檔不需要在系統上註冊，就能使用追蹤資料協助程式 (TDH) Api 來解碼和顯示事件。

Windows 的事件追蹤 (ETW) 是在 windows 2000 中引進，並在 Windows Vista 中更新。 Tracelogging 建置於 Windows Vista ETW Api 之上。 提供者可以使用 TraceLogging 技術，但仍可在 Windows Vista 上運作。 使用 Windows VistaAPIs) 的現有控制器 (可以用來控制 TraceLogging 提供者。

TraceLogging 也與現有的工具相容。 仍支援使用以資訊清單為基礎之 ETW 的提供者。 除非您想要利用 TraceLogging 提供的簡易性，否則您不需要將資訊清單型 ETW 提供者轉換為 TraceLogging 提供者。 也支援 WPP 追蹤。

TraceLogging 是以 ETW 為基礎，但引進了幾項重要的改進：

-   追蹤事件就像 API 呼叫一樣簡單。
-   事件是自我描述的，且不需要包含已編譯事件資訊清單的任何其他二進位檔來解讀事件。 事件中會記錄有關事件的所有中繼資料。
-   您可以透過開始和停止事件輕鬆地表示單一進程內的活動。
-   TraceLogging 與現有的檢測支援相容。 新的 ETW Api 會繼續支援舊的提供者。 您可以針對策略性案例投資新的 ETW Api，同時保留舊的檢測點。
-   TraceLogging 為 Windows 10、Xbox One 和 Windows 10 行動裝置版提供相同的事件追蹤 API。
-   您可以從 C、c + +、.NET 和 Windows 執行階段存取 TraceLogging Api。

## <a name="api-high-level-overview"></a>API 高層級總覽

有三個不同的 TraceLogging Api，以不同開發人員的物件為目標。 每個 API 的設計目的是為了符合該 API 目標物件的不同需求集合。

適用于 WinRT 開發人員：

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) 已在 Windows 10 中擴充，可記錄自我描述 WINDOWS (ETW) 事件的事件追蹤，而不需要資訊清單。
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) 已在 Windows 10 中擴充，以提供活動開始和停止方法，這些方法可讓您控制開始和停止事件的格式和內容。 此外，也可以嵌套活動。

針對 C/c + + 開發人員：

-   TraceLoggingProvider 包含最有效率的 API，不過，此 API 並不適合用於動態 (腳本) 案例（例如 JAVAscript）。 此 API 可用於使用者模式和核心模式程式碼。

針對 managed 程式碼 (Microsoft .NET Framework) 開發人員：

-   舊版 .NET Framework 隨附的 [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) 類別已支援寫入 ETW 事件-自動產生資訊清單，並將資訊清單內嵌至事件資料流程。 不過，開發人員仍必須追蹤資訊清單以將事件解碼 (除非是在支援內嵌資訊清單) 的情況下運作。 TraceLogging 可讓您完全刪除資訊清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於事件追蹤](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 