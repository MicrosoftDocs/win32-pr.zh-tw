---
description: Debug Output 函數
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Debug Output 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973360"
---
# <a name="debug-output-functions"></a><span data-ttu-id="ba709-103">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="ba709-103">Debug Output Functions</span></span>

<span data-ttu-id="ba709-104">[DirectShow 基類](directshow-base-classes.md)提供數個宏來顯示偵錯工具資訊。</span><span class="sxs-lookup"><span data-stu-id="ba709-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="ba709-105">函式</span><span class="sxs-lookup"><span data-stu-id="ba709-105">Function</span></span>                                               | <span data-ttu-id="ba709-106">描述</span><span class="sxs-lookup"><span data-stu-id="ba709-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba709-107">**DbgCheckModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="ba709-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="ba709-108">檢查是否已針對指定的訊息類型和層級啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="ba709-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="ba709-109">**DbgDumpObjectRegister**</span><span class="sxs-lookup"><span data-stu-id="ba709-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="ba709-110">顯示作用中物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba709-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="ba709-111">**DbgInitialise**</span><span class="sxs-lookup"><span data-stu-id="ba709-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="ba709-112">初始化 debug 程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba709-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="ba709-113">**DbgLog**</span><span class="sxs-lookup"><span data-stu-id="ba709-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="ba709-114">如果已啟用指定類型和層級的記錄，則會將字串傳送至偵錯工具輸出位置。</span><span class="sxs-lookup"><span data-stu-id="ba709-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="ba709-115">**DbgOutString**</span><span class="sxs-lookup"><span data-stu-id="ba709-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="ba709-116">將字串傳送至調試輸出位置。</span><span class="sxs-lookup"><span data-stu-id="ba709-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="ba709-117">**DbgSetModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="ba709-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="ba709-118">設定一或多個訊息類型的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="ba709-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="ba709-119">**DbgTerminate**</span><span class="sxs-lookup"><span data-stu-id="ba709-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="ba709-120">清除 debug 程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba709-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="ba709-121">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="ba709-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="ba709-122">將媒體類型的相關資訊傳送至調試輸出位置。</span><span class="sxs-lookup"><span data-stu-id="ba709-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="ba709-123">**DumpGraph**</span><span class="sxs-lookup"><span data-stu-id="ba709-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="ba709-124">將篩選圖形的相關資訊傳送至偵錯工具輸出位置。</span><span class="sxs-lookup"><span data-stu-id="ba709-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="ba709-125">**GuidNames**</span><span class="sxs-lookup"><span data-stu-id="ba709-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="ba709-126">全域陣列，包含代表 Uuid 中定義之 Guid 的字串。</span><span class="sxs-lookup"><span data-stu-id="ba709-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="ba709-127">**名字**</span><span class="sxs-lookup"><span data-stu-id="ba709-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="ba709-128">產生僅限 debug 的字串。</span><span class="sxs-lookup"><span data-stu-id="ba709-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="ba709-129">**注意**</span><span class="sxs-lookup"><span data-stu-id="ba709-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="ba709-130">將字串傳送至調試輸出位置。</span><span class="sxs-lookup"><span data-stu-id="ba709-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="ba709-131">**提醒**</span><span class="sxs-lookup"><span data-stu-id="ba709-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="ba709-132">在編譯時期產生提醒。</span><span class="sxs-lookup"><span data-stu-id="ba709-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="ba709-133">**登錄機碼**</span><span class="sxs-lookup"><span data-stu-id="ba709-133">**Registry Keys**</span></span>

<span data-ttu-id="ba709-134">DirectShow 中的 debug output 函數會使用一組登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ba709-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="ba709-135">這些登錄機碼的位置取決於 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="ba709-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="ba709-136">在 *Windows Vista 之前*，調試機碼位於下列路徑底下：</span><span class="sxs-lookup"><span data-stu-id="ba709-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="ba709-137">**HKEY \_本機 \_ 電腦** \\ **軟體** 的 \\ **調試** 程式</span><span class="sxs-lookup"><span data-stu-id="ba709-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="ba709-138">在 Windows Vista 或更新版本中，它們位於下列路徑：</span><span class="sxs-lookup"><span data-stu-id="ba709-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="ba709-139">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **DirectShow** \\ **Debug**</span><span class="sxs-lookup"><span data-stu-id="ba709-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="ba709-140">若為協力廠商篩選，位置取決於用來建立篩選器的 [DirectShow 基類](directshow-base-classes.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="ba709-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="ba709-141">Windows Vista 的 Windows SDK 中包含的版本會使用較新的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba709-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="ba709-142">先前的版本會使用較舊的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba709-142">Previous versions used the older path.</span></span>

<span data-ttu-id="ba709-143">在接下來的備註中，標籤 *<DebugRoot>* 是用來表示這兩個路徑。</span><span class="sxs-lookup"><span data-stu-id="ba709-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="ba709-144">根據 Windows 版本或基類版本，取代正確的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba709-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="ba709-145">**Debug 記錄**</span><span class="sxs-lookup"><span data-stu-id="ba709-145">**Debug Logging**</span></span>

<span data-ttu-id="ba709-146">DirectShow 定義了數種訊息類型，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ba709-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="ba709-147">值</span><span class="sxs-lookup"><span data-stu-id="ba709-147">Value</span></span>                   | <span data-ttu-id="ba709-148">描述</span><span class="sxs-lookup"><span data-stu-id="ba709-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="ba709-149">記錄 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="ba709-149">LOG\_ERROR</span></span>              | <span data-ttu-id="ba709-150">錯誤通知。</span><span class="sxs-lookup"><span data-stu-id="ba709-150">Error notification.</span></span>                                     |
| <span data-ttu-id="ba709-151">記錄 \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba709-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="ba709-152">鎖定和解除鎖定重要區段。</span><span class="sxs-lookup"><span data-stu-id="ba709-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="ba709-153">記錄檔 \_ 記憶體</span><span class="sxs-lookup"><span data-stu-id="ba709-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="ba709-154">記憶體配置，以及物件建立和終結。</span><span class="sxs-lookup"><span data-stu-id="ba709-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="ba709-155">記錄 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="ba709-155">LOG\_TIMING</span></span>             | <span data-ttu-id="ba709-156">計時和效能度量。</span><span class="sxs-lookup"><span data-stu-id="ba709-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="ba709-157">記錄 \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="ba709-157">LOG\_TRACE</span></span>              | <span data-ttu-id="ba709-158">一般呼叫追蹤。</span><span class="sxs-lookup"><span data-stu-id="ba709-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="ba709-159">CUSTOM1 至 CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="ba709-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="ba709-160">適用于自訂的偵錯工具訊息</span><span class="sxs-lookup"><span data-stu-id="ba709-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="ba709-161">每個 DirectShow debug 記錄函式都會指定訊息類型和記錄層級。</span><span class="sxs-lookup"><span data-stu-id="ba709-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="ba709-162">只有當該訊息類型目前的調試層級等於或大於記錄函式中指定的層級時，才會顯示此偵錯工具訊息。</span><span class="sxs-lookup"><span data-stu-id="ba709-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="ba709-163">否則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="ba709-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="ba709-164">例如，如果記錄 \_ 追蹤層級為3或更高，則下列程式碼會輸出字串 "This a debug message"：</span><span class="sxs-lookup"><span data-stu-id="ba709-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="ba709-165">每個模組都可以針對每個訊息類型設定自己的調試層級。</span><span class="sxs-lookup"><span data-stu-id="ba709-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="ba709-166"> (*模組* 是可使用 **LoadLibrary** 函式載入的 DLL 或可執行檔。 ) 模組的調試層級會出現在登錄的下列機碼底下：</span><span class="sxs-lookup"><span data-stu-id="ba709-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="ba709-167">**HKEY \_ 本機 \_ 電腦**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="ba709-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="ba709-168">其中 *<Message Type>* 是訊息類型減去初始 "LOG \_ "; 例如， **鎖定** 記錄 \_ 鎖定訊息。</span><span class="sxs-lookup"><span data-stu-id="ba709-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="ba709-169">載入模組時，debug 程式庫會在登錄中尋找模組的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="ba709-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="ba709-170">如果登錄機碼不存在，則偵錯工具程式庫會建立它們。</span><span class="sxs-lookup"><span data-stu-id="ba709-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="ba709-171">模組也可以在執行時間使用 [**DbgSetModuleLevel**](dbgsetmodulelevel.md) 函式來設定它自己的層級。</span><span class="sxs-lookup"><span data-stu-id="ba709-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="ba709-172">若要將訊息傳送至調試輸出，請呼叫 [**DbgLog**](dbglog.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="ba709-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="ba709-173">下列範例會建立類型記錄追蹤的層級3訊息 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ba709-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="ba709-174">您也可以使用下列登錄機碼來指定全域記錄層級：</span><span class="sxs-lookup"><span data-stu-id="ba709-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="ba709-175">Debug 程式庫會使用較大的層級，也就是全域層級或模組層級。</span><span class="sxs-lookup"><span data-stu-id="ba709-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="ba709-176">**調試輸出位置**</span><span class="sxs-lookup"><span data-stu-id="ba709-176">**Debug Output Location**</span></span>

<span data-ttu-id="ba709-177">偵錯工具輸出位置取決於另一個登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="ba709-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="ba709-178">**HKEY \_本機 \_ 電腦** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**</span><span class="sxs-lookup"><span data-stu-id="ba709-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="ba709-179">如果此索引鍵的值為 `Console` ，則輸出會移至主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="ba709-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="ba709-180">如果值為 `Deb` 、 `Debug` 、 `Debugger` 或空字串，則輸出會移至偵錯工具視窗。</span><span class="sxs-lookup"><span data-stu-id="ba709-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="ba709-181">否則，輸出會寫入登錄機碼所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="ba709-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="ba709-182">在可執行檔使用 DirectShow debug 程式庫之前，必須先呼叫 [**DbgInitialise**](dbginitialise.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="ba709-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="ba709-183">之後，它必須呼叫 [**DbgTerminate**](dbgterminate.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="ba709-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="ba709-184">Dll 不需要呼叫這些函式，因為在基類庫中 (定義 DLL 進入點) 會自動呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="ba709-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba709-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba709-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba709-186">偵錯工具</span><span class="sxs-lookup"><span data-stu-id="ba709-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



