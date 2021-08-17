---
title: TraceLogging 參考
description: 下列主題提供有關原生 TraceLogging API 的資訊。TraceLogging 是針對 Windows (ETW) 的事件追蹤所建立，並提供簡單的方式來檢測程式碼。
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6563186411ace599f249220b9fd44b9ee4c682fdebd1391b4a3027a87c3482e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349988"
---
# <a name="tracelogging-reference"></a>TraceLogging 參考

下列主題提供有關原生 TraceLogging API 的資訊。

TraceLogging 是針對 Windows (ETW) 的事件追蹤所建立，並提供簡單的方式來檢測程式碼。 TraceLogging 可讓您包含事件的結構化資料、使事件相互關聯，而且不需要個別的檢測資訊清單 XML 檔案。

<span class="underline">適用于 WinRT 開發人員</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel)已在 Windows 10 中擴充，可記錄 Windows (ETW) 事件的自我描述事件追蹤，而不需要資訊清單。
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity)已在 Windows 10 中擴充，以提供活動開始和停止方法，這些方法可讓您控制開始和停止事件的格式和內容。 此外，也可以嵌套活動。

<span class="underline">針對 managed 程式碼 (Microsoft .NET Framework) 開發人員</span>

-   舊版 .NET Framework 隨附的[EventSource](/dotnet/api/system.diagnostics.tracing.eventsource)類別已支援寫入 ETW 事件，而不需要資訊清單。 不過，開發人員必須使用 EventSource 作為基類，並將屬性和方法新增至已自動轉換成 ETW 資訊清單的衍生類別。 現在，開發人員不需要從 EventSource 衍生，而可以改為直接使用 EventSource 來記錄不需要資訊清單的自我描述事件。

<span class="underline">適用于 C/c + + 開發人員</span>

-   TraceLoggingProvider 是在使用者或核心模式中，適用于 C/c + + 開發人員的建議 API。 這個 API 並不適合用於動態 (腳本) 案例（例如 JAVAscript）。 下列連結說明 C/c + + API。

<!-- -->

-   [類別](trace-logging-classes.md)
-   [函數](trace-logging-functions.md)
-   [巨集](trace-logging-macros.md)

請注意，WINVER 的值會影響 TraceLoggingProvider 的運作方式。

-   如果在包含 <的> 之前未設定 WINVER，則 <windows .h> 會將 WINVER 設定為對應至 SDK 版本的預設值。
-   使用 TraceLoggingProvider 將 WINVER 設為 0x0602 (Windows 8) 或更高版本，程式將無法在 Windows Vista 或 Windows 7 上執行。
-   使用 TraceLoggingProvider 將 WINVER 設定為 0x0600 (Windows Vista) 或 0x0601 (Windows 7) ，程式將會針對相容性進行設定，並可在指定的 Windows 版本上運作。

 

 