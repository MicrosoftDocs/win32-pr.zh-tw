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
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="6da4d-103">TraceLogging C/c + + 快速入門</span><span class="sxs-lookup"><span data-stu-id="6da4d-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="6da4d-104">下一節說明將 TraceLogging 新增至原生使用者模式程式碼所需的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="6da4d-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6da4d-105">必要條件</span><span class="sxs-lookup"><span data-stu-id="6da4d-105">Prerequisites</span></span>

-   <span data-ttu-id="6da4d-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6da4d-106">Windows 10</span></span>
-   <span data-ttu-id="6da4d-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="6da4d-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="6da4d-108">需要 Windows 10 軟體發展工具組 (SDK) 才能撰寫使用者模式提供者</span><span class="sxs-lookup"><span data-stu-id="6da4d-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="6da4d-109">需要 Windows 10 的 Windows 驅動程式套件 (WDK) 才能撰寫核心模式提供者</span><span class="sxs-lookup"><span data-stu-id="6da4d-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6da4d-110">連結 advapi32.dll，以便編譯這些範例。</span><span class="sxs-lookup"><span data-stu-id="6da4d-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="6da4d-111">SimpleTraceLoggingExample。h</span><span class="sxs-lookup"><span data-stu-id="6da4d-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="6da4d-112">此範例標頭包含 TraceLogging Api，而 forward 會宣告將用來記錄事件的提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="6da4d-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="6da4d-113">任何想要使用 TraceLogging 的類別都會包含此標頭，然後可以開始記錄。</span><span class="sxs-lookup"><span data-stu-id="6da4d-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="6da4d-114">標頭檔包含定義原生 TraceLogging API 的 TraceLoggingProvider。</span><span class="sxs-lookup"><span data-stu-id="6da4d-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="6da4d-115">您必須先包含 Windows .h，因為它會定義 TraceLoggingProvider 所使用的常數。</span><span class="sxs-lookup"><span data-stu-id="6da4d-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="6da4d-116">標頭檔轉送會宣告您要傳遞給 TraceLogging Api 的提供者控制碼， `g_hMyComponentProvider` 以記錄事件。</span><span class="sxs-lookup"><span data-stu-id="6da4d-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="6da4d-117">需要使用 TraceLogging 的任何程式碼都必須能夠存取這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="6da4d-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="6da4d-118">[**TRACELOGGING \_DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) 是 `extern const TraceLoggingHProvider` 使用您提供的名稱（在上述範例中為）來建立控制碼的宏 `g_hMyComponentProvider` 。</span><span class="sxs-lookup"><span data-stu-id="6da4d-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="6da4d-119">您將在程式碼檔案中配置實際的提供者控制碼變數。</span><span class="sxs-lookup"><span data-stu-id="6da4d-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="6da4d-120">SimpleTraceLoggingExample .cpp</span><span class="sxs-lookup"><span data-stu-id="6da4d-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="6da4d-121">下列範例會註冊提供者、記錄事件和取消註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="6da4d-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

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

<span data-ttu-id="6da4d-122">上述範例包含 SimpleTraceLoggingExample，其中包含您的程式碼將用來記錄事件的全域提供者變數。</span><span class="sxs-lookup"><span data-stu-id="6da4d-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="6da4d-123">[**TRACELOGGING \_ 定義 \_ 提供者**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider)宏會配置儲存體並定義提供者控制碼變數。</span><span class="sxs-lookup"><span data-stu-id="6da4d-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="6da4d-124">您提供給這個宏的變數名稱必須符合您在標頭檔中 [**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) 宏所使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="6da4d-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="6da4d-125">只要該控制碼在範圍內，就會保持有效。</span><span class="sxs-lookup"><span data-stu-id="6da4d-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="6da4d-126">註冊提供者控制碼</span><span class="sxs-lookup"><span data-stu-id="6da4d-126">Register the provider handle</span></span>

<span data-ttu-id="6da4d-127">在您可以使用提供者控制碼來記錄事件之前，您必須先呼叫 [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) 來註冊您的提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="6da4d-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="6da4d-128">這通常是在主要 () 或 DLLMain () 中完成，但是只要在任何記錄事件的嘗試之前都可以完成。</span><span class="sxs-lookup"><span data-stu-id="6da4d-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="6da4d-129">如果您在註冊提供者控制碼之前記錄事件，將不會發生任何錯誤，但不會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="6da4d-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="6da4d-130">上述範例中的下列程式碼會註冊提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="6da4d-130">The following code from the example above registers the provider handle.</span></span>

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

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="6da4d-131">記錄 Tracelogging 事件</span><span class="sxs-lookup"><span data-stu-id="6da4d-131">Log a Tracelogging event</span></span>

<span data-ttu-id="6da4d-132">註冊提供者之後，下列程式碼會記錄簡單事件。</span><span class="sxs-lookup"><span data-stu-id="6da4d-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="6da4d-133">[**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite)宏最多會使用99個引數，並以數個語句的形式執行。</span><span class="sxs-lookup"><span data-stu-id="6da4d-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="6da4d-134">這表示所要記錄的值不應該是 c + + 暫存物件。</span><span class="sxs-lookup"><span data-stu-id="6da4d-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="6da4d-135">事件名稱是以 UTF-8 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="6da4d-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="6da4d-136">您不得 `null` 在事件或其他功能變數名稱中使用內嵌字元。</span><span class="sxs-lookup"><span data-stu-id="6da4d-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="6da4d-137">允許的字元沒有其他限制。</span><span class="sxs-lookup"><span data-stu-id="6da4d-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="6da4d-138">事件名稱後面的每個引數都必須包裝在 [TraceLogging 包裝](tracelogging-wrapper-macros.md)函式宏內。</span><span class="sxs-lookup"><span data-stu-id="6da4d-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="6da4d-139">如果您使用 c + +，您可以使用 `TraceLoggingValue` 包裝函式宏來自動推斷引數的類型。</span><span class="sxs-lookup"><span data-stu-id="6da4d-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="6da4d-140">如果您是以 C 撰寫驅動程式，則必須使用特定類型的欄位宏，例如 `TraceLoggingInt32` 、 `TraceLoggingUnicodeString` 、等等 `TraceLoggingString` 。TraceLogging 包裝函式巨集定義于 TraceLoggingProvider 中。</span><span class="sxs-lookup"><span data-stu-id="6da4d-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="6da4d-141">除了記錄單一事件之外，您也可以使用 TraceLoggingActivity 中找到的 [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity)或 [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop)宏，依活動將事件分組。</span><span class="sxs-lookup"><span data-stu-id="6da4d-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="6da4d-142">活動會將事件相互關聯，而且在具有開頭和結尾的案例中很有用。</span><span class="sxs-lookup"><span data-stu-id="6da4d-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="6da4d-143">例如，您可以使用活動來測量啟動應用程式所需的案例，包括啟動顯示畫面所花費的時間，並在應用程式的初始畫面變成可見時結束。</span><span class="sxs-lookup"><span data-stu-id="6da4d-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="6da4d-144">活動會捕捉單一事件，並將在該活動的開始和結束之間發生的其他活動加以嵌套。</span><span class="sxs-lookup"><span data-stu-id="6da4d-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="6da4d-145">活動具有每個進程的範圍，而且必須從執行緒傳給執行緒，才能正確地將多執行緒事件的嵌套。</span><span class="sxs-lookup"><span data-stu-id="6da4d-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="6da4d-146">提供者控制碼的範圍嚴格限制為其定義所在的模組 (DLL、EXE 或 SYS 檔案) ，而不應將控制碼傳遞至其他 Dll。</span><span class="sxs-lookup"><span data-stu-id="6da4d-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="6da4d-147">如果使用 B.DLL 中定義的提供者控制碼在 A.DLL 中叫用 [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) 宏，可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="6da4d-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="6da4d-148">符合這項需求的最安全且最有效率的方法，就是直接參考全域提供者控制碼，而且永遠不會將提供者控制碼作為參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="6da4d-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="6da4d-149">取消註冊提供者</span><span class="sxs-lookup"><span data-stu-id="6da4d-149">Unregister the provider</span></span>

<span data-ttu-id="6da4d-150">當您完成記錄事件時，您必須取消註冊 TraceLogging 提供者。</span><span class="sxs-lookup"><span data-stu-id="6da4d-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="6da4d-151">下列程式碼會取消註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="6da4d-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="6da4d-152">相容性</span><span class="sxs-lookup"><span data-stu-id="6da4d-152">Compatibility</span></span>

<span data-ttu-id="6da4d-153">根據其設定，TraceLoggingProvider 可以回溯相容 (相容于 Windows Vista 或更新版本的) ，或可針對較新的作業系統版本進行優化。</span><span class="sxs-lookup"><span data-stu-id="6da4d-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="6da4d-154">TraceLoggingProvider 使用 WINVER (使用者模式) 和 NTDDI_VERSION (核心模式) 來判斷它是否應該與舊版作業系統相容，或針對較新的作業系統版本進行優化。</span><span class="sxs-lookup"><span data-stu-id="6da4d-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="6da4d-155">在使用者模式中，如果您在設定 WINVER 之前包含 <的 windows .h>，<windows .h> 將 WINVER 設定為 SDK 的預設目標 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="6da4d-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="6da4d-156">如果 WINVER 設定為0x602 或更高版本，則 TraceLoggingProvider 會為 Windows 8 優化其行為， (您的應用程式將不會在舊版 Windows) 上執行。</span><span class="sxs-lookup"><span data-stu-id="6da4d-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="6da4d-157">如果您的程式需要在 Vista 或 Windows 7 上執行，請務必先將 WINVER 設定為適當的值，然後再包含 <的 windows .h>。</span><span class="sxs-lookup"><span data-stu-id="6da4d-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="6da4d-158">同樣地，如果您在設定 NTDDI_VERSION 之前包含 <的 wdm>，<wdm> 會將 NTDDI_VERSION 設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="6da4d-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="6da4d-159">如果 NTDDI_VERSION 設定為0x06040000 或更高版本，則 TraceLoggingProvider 會針對 Windows 10 優化其行為， (您的驅動程式在舊版 Windows) 上無法運作。</span><span class="sxs-lookup"><span data-stu-id="6da4d-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="6da4d-160">摘要和後續步驟</span><span class="sxs-lookup"><span data-stu-id="6da4d-160">Summary and next steps</span></span>

<span data-ttu-id="6da4d-161">若要瞭解如何使用 Windows 效能工具的最新內部版本 (WPT) 來捕捉和查看 TraceLogging 資料，請參閱 [記錄和顯示 TraceLogging 事件](tracelogging-record-and-display-tracelogging-events.md)。</span><span class="sxs-lookup"><span data-stu-id="6da4d-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="6da4d-162">如需更多 c + + TraceLogging 範例，請參閱 [c/c + + Tracelogging 範例](tracelogging-c-cpp-tracelogging-examples.md) 。</span><span class="sxs-lookup"><span data-stu-id="6da4d-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




