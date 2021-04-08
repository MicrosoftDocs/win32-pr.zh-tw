---
title: TraceLogging C/c + + 快速入門
description: 下一節說明將 TraceLogging 新增至原生使用者模式程式碼所需的基本步驟。
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2020
ms.locfileid: "103932981"
---
# <a name="tracelogging-cc-quick-start"></a>TraceLogging C/c + + 快速入門

下一節說明將 TraceLogging 新增至原生使用者模式程式碼所需的基本步驟。

## <a name="prerequisites"></a>必要條件

-   Windows 10
-   Microsoft Visual Studio 2013
-   需要 Windows 10 軟體發展工具組 (SDK) 才能撰寫使用者模式提供者
-   需要 Windows 10 的 Windows 驅動程式套件 (WDK) 才能撰寫核心模式提供者

> [!IMPORTANT]
> 連結 advapi32.dll，以便編譯這些範例。

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample。h

此範例標頭包含 TraceLogging Api，而 forward 會宣告將用來記錄事件的提供者控制碼。 任何想要使用 TraceLogging 的類別都會包含此標頭，然後可以開始記錄。

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

標頭檔包含定義原生 TraceLogging API 的 TraceLoggingProvider。 您必須先包含 Windows .h，因為它會定義 TraceLoggingProvider 所使用的常數。

標頭檔轉送會宣告您要傳遞給 TraceLogging Api 的提供者控制碼， `g_hMyComponentProvider` 以記錄事件。 需要使用 TraceLogging 的任何程式碼都必須能夠存取這個控制碼。

[**TRACELOGGING \_DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) 是 `extern const TraceLoggingHProvider` 使用您提供的名稱（在上述範例中為）來建立控制碼的宏 `g_hMyComponentProvider` 。 您將在程式碼檔案中配置實際的提供者控制碼變數。

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample .cpp

下列範例會註冊提供者、記錄事件和取消註冊提供者。

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

上述範例包含 SimpleTraceLoggingExample，其中包含您的程式碼將用來記錄事件的全域提供者變數。

[**TRACELOGGING \_ 定義 \_ 提供者**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider)宏會配置儲存體並定義提供者控制碼變數。 您提供給這個宏的變數名稱必須符合您在標頭檔中 [**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) 宏所使用的名稱。 只要該控制碼在範圍內，就會保持有效。

### <a name="register-the-provider-handle"></a>註冊提供者控制碼

在您可以使用提供者控制碼來記錄事件之前，您必須先呼叫 [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) 來註冊您的提供者控制碼。 這通常是在主要 () 或 DLLMain () 中完成，但是只要在任何記錄事件的嘗試之前都可以完成。 如果您在註冊提供者控制碼之前記錄事件，將不會發生任何錯誤，但不會記錄事件。 上述範例中的下列程式碼會註冊提供者控制碼。

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a>記錄 Tracelogging 事件

註冊提供者之後，下列程式碼會記錄簡單事件。

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

[**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite)宏最多會使用99個引數，並以數個語句的形式執行。 這表示所要記錄的值不應該是 c + + 暫存物件。 事件名稱是以 UTF-8 格式儲存。 您不得 `null` 在事件或其他功能變數名稱中使用內嵌字元。 允許的字元沒有其他限制。

事件名稱後面的每個引數都必須包裝在 [TraceLogging 包裝](tracelogging-wrapper-macros.md)函式宏內。 如果您使用 c + +，您可以使用 `TraceLoggingValue` 包裝函式宏來自動推斷引數的類型。 如果您是以 C 撰寫驅動程式，則必須使用特定類型的欄位宏，例如 `TraceLoggingInt32` 、 `TraceLoggingUnicodeString` 、等等 `TraceLoggingString` 。TraceLogging 包裝函式巨集定義于 TraceLoggingProvider 中。

除了記錄單一事件之外，您也可以使用 TraceLoggingActivity 中找到的 [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity)或 [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop)宏，依活動將事件分組。 活動會將事件相互關聯，而且在具有開頭和結尾的案例中很有用。 例如，您可以使用活動來測量啟動應用程式所需的案例，包括啟動顯示畫面所花費的時間，並在應用程式的初始畫面變成可見時結束。

活動會捕捉單一事件，並將在該活動的開始和結束之間發生的其他活動加以嵌套。 活動具有每個進程的範圍，而且必須從執行緒傳給執行緒，才能正確地將多執行緒事件的嵌套。

提供者控制碼的範圍嚴格限制為其定義所在的模組 (DLL、EXE 或 SYS 檔案) ，而不應將控制碼傳遞至其他 Dll。 如果使用 B.DLL 中定義的提供者控制碼在 A.DLL 中叫用 [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) 宏，可能會造成問題。 符合這項需求的最安全且最有效率的方法，就是直接參考全域提供者控制碼，而且永遠不會將提供者控制碼作為參數傳遞。

### <a name="unregister-the-provider"></a>取消註冊提供者

當您完成記錄事件時，您必須取消註冊 TraceLogging 提供者。 下列程式碼會取消註冊提供者。

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>相容性

根據其設定，TraceLoggingProvider 可以回溯相容 (相容于 Windows Vista 或更新版本的) ，或可針對較新的作業系統版本進行優化。 TraceLoggingProvider 使用 WINVER (使用者模式) 和 NTDDI_VERSION (核心模式) 來判斷它是否應該與舊版作業系統相容，或針對較新的作業系統版本進行優化。

在使用者模式中，如果您在設定 WINVER 之前包含 <的 windows .h>，<windows .h> 將 WINVER 設定為 SDK 的預設目標 OS 版本。 如果 WINVER 設定為0x602 或更高版本，則 TraceLoggingProvider 會為 Windows 8 優化其行為， (您的應用程式將不會在舊版 Windows) 上執行。 如果您的程式需要在 Vista 或 Windows 7 上執行，請務必先將 WINVER 設定為適當的值，然後再包含 <的 windows .h>。

同樣地，如果您在設定 NTDDI_VERSION 之前包含 <的 wdm>，<wdm> 會將 NTDDI_VERSION 設定為預設值。 如果 NTDDI_VERSION 設定為0x06040000 或更高版本，則 TraceLoggingProvider 會針對 Windows 10 優化其行為， (您的驅動程式在舊版 Windows) 上無法運作。

## <a name="summary-and-next-steps"></a>摘要和後續步驟

若要瞭解如何使用 Windows 效能工具的最新內部版本 (WPT) 來捕捉和查看 TraceLogging 資料，請參閱 [記錄和顯示 TraceLogging 事件](tracelogging-record-and-display-tracelogging-events.md)。

如需更多 c + + TraceLogging 範例，請參閱 [c/c + + Tracelogging 範例](tracelogging-c-cpp-tracelogging-examples.md) 。

 

 




