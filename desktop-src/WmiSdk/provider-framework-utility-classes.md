---
description: 不再建議使用屬於 WMI 提供者架構一部分的 WMI c + + 類別。
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: 提供者架構公用程式類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab09c99fe2597cacd81e55a4ed18bd4e286ff16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985376"
---
# <a name="provider-framework-utility-classes"></a><span data-ttu-id="46c10-103">提供者架構公用程式類別</span><span class="sxs-lookup"><span data-stu-id="46c10-103">Provider Framework Utility Classes</span></span>

<span data-ttu-id="46c10-104">\[WMI c + + 類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會有任何進一步的開發、增強功能或更新可用於影響這些程式庫的非安全性相關問題。</span><span class="sxs-lookup"><span data-stu-id="46c10-104">\[WMI C++ classes that are part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="46c10-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="46c10-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="46c10-106">提供者 framework 程式庫 Framedyd.dll (debug 版本) 和 Framedyn.dll (發行版本) 實施數個提供者協助程式類別。</span><span class="sxs-lookup"><span data-stu-id="46c10-106">The provider framework libraries Framedyd.dll (debug version) and Framedyn.dll (release version) implement several provider helper classes.</span></span> <span data-ttu-id="46c10-107">某些 Framedyn.dll 中的函式已從標頭檔中移除。</span><span class="sxs-lookup"><span data-stu-id="46c10-107">Some functions in Framedyn.dll have been removed from the header files.</span></span> <span data-ttu-id="46c10-108">若要繼續使用這些函式，請 `#define FRAMEWORK_ALLOW_DEPRECATED` 先加入至您的程式碼，再加入 Fwcommon .h。</span><span class="sxs-lookup"><span data-stu-id="46c10-108">To continue to use these functions, add `#define FRAMEWORK_ALLOW_DEPRECATED` to your code before including Fwcommon.h.</span></span>

<span data-ttu-id="46c10-109">您可以卸載不再需要的個別提供者。</span><span class="sxs-lookup"><span data-stu-id="46c10-109">You can unload individual providers that are no longer required.</span></span>

<span data-ttu-id="46c10-110">若要使用此功能，您必須對 MainDll 中的提供者進行下列三項變更：</span><span class="sxs-lookup"><span data-stu-id="46c10-110">To use this capability, you must make the three following changes to your provider in MainDll.cpp:</span></span>

-   <span data-ttu-id="46c10-111">在您呼叫 [**CWbemProviderGlue：： FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))的函數 **DllMain** 中，您必須新增第二個參數，也就是 long 的指標。</span><span class="sxs-lookup"><span data-stu-id="46c10-111">In the function **DllMain** where you call [**CWbemProviderGlue::FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), you must add a second parameter which is a pointer to a long.</span></span>
-   <span data-ttu-id="46c10-112">在呼叫 [**CWbemProviderGlue：： FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))的函式 **DllCanUnloadNow** 中，您必須新增第二個參數，也就是 long 的指標。</span><span class="sxs-lookup"><span data-stu-id="46c10-112">In the function **DllCanUnloadNow** where you call [**CWbemProviderGlue::FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), you must add a second parameter which is a pointer to a long.</span></span>
-   <span data-ttu-id="46c10-113">在您建立 **CWbemGlueFactory** 實例的函式 **DllGetClassObject** 中，您必須加入一個指向 long 指標的參數。</span><span class="sxs-lookup"><span data-stu-id="46c10-113">In the function **DllGetClassObject** where you create an instance of **CWbemGlueFactory**, you must add a parameter which is a pointer to a long.</span></span>

<span data-ttu-id="46c10-114">在這三種情況下，long 的指標必須是相同的指標。</span><span class="sxs-lookup"><span data-stu-id="46c10-114">In all three cases, the pointer to a long must be the same pointer.</span></span>

> [!Note]  
> <span data-ttu-id="46c10-115">在 Maindll .cpp 中， **DllGetClassObject**、 **DllCanUnloadNow**、 **DllRegisterServer**、 **DllUnregisterServer** 和 **DllMain** 常式必須包裝在 try/catch 區塊中。</span><span class="sxs-lookup"><span data-stu-id="46c10-115">In Maindll.cpp, **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** and **DllMain** routines must be wrapped in a try/catch block.</span></span>

 

> [!Caution]  
> <span data-ttu-id="46c10-116">Framedyd.dll 的提供者 debug 與 Framedyd 程式庫連結。</span><span class="sxs-lookup"><span data-stu-id="46c10-116">Provider debug builds link with Framedyd.lib for Framedyd.dll.</span></span> <span data-ttu-id="46c10-117">Framedyd.dll 位於 \\ 不包含在系統路徑中的 Microsoft Windows 軟體開發套件 (SDK) bin 目錄。</span><span class="sxs-lookup"><span data-stu-id="46c10-117">Framedyd.dll is in the Microsoft Windows Software Development Kit (SDK) \\bin directory which is not included in the system path.</span></span> <span data-ttu-id="46c10-118">當提供者的偵錯工具組建經過 Windows 管理服務測試時，架構提供者將無法載入，因為不會有 Framedyd.dll 或其中一個相依性。</span><span class="sxs-lookup"><span data-stu-id="46c10-118">When a debug build of a provider is tested with the Windows Management service, the framework provider will fail to load because Framedyd.dll or one of its dependencies will not be located.</span></span> <span data-ttu-id="46c10-119">因此，您必須將 Framedyd.dll 從 Windows SDK \\ bin 目錄複寫到 \\ system32 \\ wbem 目錄，或將 Windows SDK \\ bin 目錄新增至系統搜尋路徑。</span><span class="sxs-lookup"><span data-stu-id="46c10-119">Therefore, you must either copy Framedyd.dll from the Windows SDK \\bin directory to the \\system32\\wbem directory or add the Windows SDK \\bin directory to the system search path.</span></span>

 

<span data-ttu-id="46c10-120">下表列出提供者 framework 公用程式類別。</span><span class="sxs-lookup"><span data-stu-id="46c10-120">The following table lists the provider framework utility classes.</span></span>



| <span data-ttu-id="46c10-121">公用程式類別</span><span class="sxs-lookup"><span data-stu-id="46c10-121">Utility class</span></span>                                          | <span data-ttu-id="46c10-122">Description</span><span class="sxs-lookup"><span data-stu-id="46c10-122">Description</span></span>                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46c10-123">**CHString**</span><span class="sxs-lookup"><span data-stu-id="46c10-123">**CHString**</span></span>](chstring.md)                           | <span data-ttu-id="46c10-124">提供 WMI 的字串比較和操作函數。</span><span class="sxs-lookup"><span data-stu-id="46c10-124">Provides string comparison and manipulation functions for WMI.</span></span>                                                                  |
| [<span data-ttu-id="46c10-125">**CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="46c10-125">**CHStringArray**</span></span>](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | <span data-ttu-id="46c10-126">包含用於建立及操作 CHString 的陣列。</span><span class="sxs-lookup"><span data-stu-id="46c10-126">Contains for creating and manipulating arrays of CHString.</span></span>                                                                      |
| [<span data-ttu-id="46c10-127">**TRefPointerCollection**</span><span class="sxs-lookup"><span data-stu-id="46c10-127">**TRefPointerCollection**</span></span>](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | <span data-ttu-id="46c10-128">針對指標授與容器類別的存取權。</span><span class="sxs-lookup"><span data-stu-id="46c10-128">Grants access to a container class for pointers.</span></span>                                                                                |
| [<span data-ttu-id="46c10-129">**WBEMTime**</span><span class="sxs-lookup"><span data-stu-id="46c10-129">**WBEMTime**</span></span>](wbemtime.md)                           | <span data-ttu-id="46c10-130">促進各種 Windows 和 ANSI C 執行時間時間格式之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="46c10-130">Facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>                                               |
| [<span data-ttu-id="46c10-131">**WBEMTimeSpan**</span><span class="sxs-lookup"><span data-stu-id="46c10-131">**WBEMTimeSpan**</span></span>](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | <span data-ttu-id="46c10-132">包含 helper 函式，用來計算和保存兩個 [**WBEMTime**](wbemtime.md) 物件之間的時間範圍差異。</span><span class="sxs-lookup"><span data-stu-id="46c10-132">Contains helper functions used to calculate and hold the time span difference between two [**WBEMTime**](wbemtime.md) objects.</span></span> |



 

> [!Note]  
> <span data-ttu-id="46c10-133">[**CHString**](chstring.md)和 [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)類別類似于 (MFC) **CString** 和 **CStringArray** 的 Microsoft Foundation 類別。</span><span class="sxs-lookup"><span data-stu-id="46c10-133">The [**CHString**](chstring.md) and [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) classes are similar to the Microsoft Foundation Classes (MFC) **CString** and **CStringArray**.</span></span> <span data-ttu-id="46c10-134">WMI 版本存在，讓開發人員可以存取字串操作和比較方法，而不需要存取 MFC。</span><span class="sxs-lookup"><span data-stu-id="46c10-134">The WMI versions exist so that developers can access to string manipulation and comparison methods without having to access MFC.</span></span> <span data-ttu-id="46c10-135">[**WBEMTime**](wbemtime.md)和 [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)類別也類似于 MFC **CTime** 和 **CTimeSpan** 類別。</span><span class="sxs-lookup"><span data-stu-id="46c10-135">The [**WBEMTime**](wbemtime.md) and [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) classes are also similar to the MFC **CTime** and **CTimeSpan** classes.</span></span> <span data-ttu-id="46c10-136">WMI 版本能夠儲存時間到毫微秒的精確度，也可以在 **BSTR** 之間轉換。</span><span class="sxs-lookup"><span data-stu-id="46c10-136">The WMI versions are capable of storing time to nanosecond accuracy, and can also convert to and from **BSTR**.</span></span> <span data-ttu-id="46c10-137">如需 CString、CStringArray、CTime 和 CTimeSpan 類別的詳細資訊，請參閱 MSDN 上的 [Microsoft Foundation 類別](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) 。</span><span class="sxs-lookup"><span data-stu-id="46c10-137">For more information about the CString, CStringArray, CTime, and CTimeSpan classes, see the [Microsoft Foundation Classes](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) on MSDN.</span></span>

 

<span data-ttu-id="46c10-138">[**WBEMTime**](wbemtime.md)方法所傳回的 **BSTR** 值為 [日期和時間格式](date-and-time-format.md)： "yyyymmddhhmmss.ffffff. mmmmmmsUUU"</span><span class="sxs-lookup"><span data-stu-id="46c10-138">**BSTR** values returned by [**WBEMTime**](wbemtime.md) methods are in [Date and Time Format](date-and-time-format.md): "yyyymmddHHMMSS.mmmmmmsUUU"</span></span>

<span data-ttu-id="46c10-139">[**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)方法所傳回的 **BSTR** 值採用 [間隔格式](interval-format.md)： "ddddddddHHMMSS. mmmmmm： 000"</span><span class="sxs-lookup"><span data-stu-id="46c10-139">**BSTR** values returned by [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) methods are in [Interval Format](interval-format.md): "ddddddddHHMMSS.mmmmmm:000"</span></span>

<span data-ttu-id="46c10-140">雖然時間和時間範圍會在內部儲存為毫微秒，但不一定會以毫微秒精確度進行儲存。</span><span class="sxs-lookup"><span data-stu-id="46c10-140">Although times and time spans are stored internally as nanoseconds, they are not necessarily stored with nanosecond accuracy.</span></span> <span data-ttu-id="46c10-141">這是因為 [**WBEMTime**](wbemtime.md) 物件可以使用精確至第二個 (**結構 tm** 和 **時間 \_ t**) 的時間格式來建立。</span><span class="sxs-lookup"><span data-stu-id="46c10-141">This is because [**WBEMTime**](wbemtime.md) objects can be constructed using time formats that are accurate to a second (**struct tm**, and **time\_t**).</span></span> <span data-ttu-id="46c10-142">新增人工小數位數不會提高精確度。</span><span class="sxs-lookup"><span data-stu-id="46c10-142">Adding artificial decimal places does not increase the accuracy.</span></span>

 

 
