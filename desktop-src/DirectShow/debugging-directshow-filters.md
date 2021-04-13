---
description: 本主題中所述的許多偵錯工具都是在 DirectShow 基礎類別庫中執行。 如需詳細資訊，請參閱 DirectShow 基類。
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: 偵測 DirectShow 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510300"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="4432b-104">偵測 DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="4432b-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="4432b-105">本主題中所述的許多偵錯工具都是在 DirectShow 基礎類別庫中執行。</span><span class="sxs-lookup"><span data-stu-id="4432b-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="4432b-106">如需詳細資訊，請參閱 [DirectShow 基類](directshow-base-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="4432b-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="4432b-107">判斷提示檢查</span><span class="sxs-lookup"><span data-stu-id="4432b-107">Assertion Checking</span></span>

<span data-ttu-id="4432b-108">使用判斷提示檢查壓縮。</span><span class="sxs-lookup"><span data-stu-id="4432b-108">Use assertion checking liberally.</span></span> <span data-ttu-id="4432b-109">判斷提示可以驗證您在程式碼中針對前置條件與後置條件進行的假設。</span><span class="sxs-lookup"><span data-stu-id="4432b-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="4432b-110">DirectShow 提供數個判斷提示宏。</span><span class="sxs-lookup"><span data-stu-id="4432b-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="4432b-111">如需詳細資訊，請參閱 [Assert 和中斷點宏](assert-and-breakpoint-macros.md)。</span><span class="sxs-lookup"><span data-stu-id="4432b-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="4432b-112">物件名稱</span><span class="sxs-lookup"><span data-stu-id="4432b-112">Object Names</span></span>

<span data-ttu-id="4432b-113">在 debug 組建中，有一個從 [**CBaseObject**](cbaseobject.md) 類別衍生的全域物件清單。</span><span class="sxs-lookup"><span data-stu-id="4432b-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="4432b-114">建立物件時，會將它們新增至清單。</span><span class="sxs-lookup"><span data-stu-id="4432b-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="4432b-115">當它們損毀時，就會從清單中移除它們。</span><span class="sxs-lookup"><span data-stu-id="4432b-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="4432b-116">若要顯示這些物件的清單，請呼叫 [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="4432b-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="4432b-117">[**CBaseObject**](cbaseobject.md)基類的函式方法（和其衍生的大部分類別）包含物件名稱的參數。</span><span class="sxs-lookup"><span data-stu-id="4432b-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="4432b-118">提供物件的唯一名稱來識別它們。</span><span class="sxs-lookup"><span data-stu-id="4432b-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="4432b-119">當您宣告名稱時，請使用 [**name**](name.md) 宏，如此就只會在 debug 組建中配置此名稱。</span><span class="sxs-lookup"><span data-stu-id="4432b-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="4432b-120">在零售組建中，名稱會變成 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4432b-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="4432b-121">偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="4432b-121">Debug Logging</span></span>

<span data-ttu-id="4432b-122">當程式執行時， [**DbgLog**](dbglog.md) 函式會顯示偵錯工具的訊息。</span><span class="sxs-lookup"><span data-stu-id="4432b-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="4432b-123">您可以使用此函式來追蹤應用程式或篩選的執行。</span><span class="sxs-lookup"><span data-stu-id="4432b-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="4432b-124">您可以記錄傳回碼、變數值，以及任何其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4432b-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="4432b-125">每個偵錯工具訊息都有一種類型，例如記錄 \_ 追蹤或記錄檔 \_ 錯誤，以及表示訊息重要性的調試層級。</span><span class="sxs-lookup"><span data-stu-id="4432b-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="4432b-126">具有較低 debug 層級的訊息比較高層級的訊息更重要。</span><span class="sxs-lookup"><span data-stu-id="4432b-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="4432b-127">在下列範例中，假設的篩選會將 pin 與 pin 陣列中斷連線。</span><span class="sxs-lookup"><span data-stu-id="4432b-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="4432b-128">如果中斷連接嘗試成功，則篩選會顯示記錄 \_ 追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="4432b-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="4432b-129">如果嘗試失敗，則會顯示記錄 \_ 錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="4432b-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="4432b-130">當您正在進行偵錯工具時，您可以設定每個訊息類型的 debug 層級。</span><span class="sxs-lookup"><span data-stu-id="4432b-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="4432b-131">此外，每個模組 (DLL 或可執行檔) 都會維護它自己的調試層級。</span><span class="sxs-lookup"><span data-stu-id="4432b-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="4432b-132">如果您要測試篩選，請針對包含篩選的 DLL，引發偵錯工具層級。</span><span class="sxs-lookup"><span data-stu-id="4432b-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="4432b-133">如需詳細資訊，請參閱 [Debug Output 函數](debug-output-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="4432b-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="4432b-134">重要區段</span><span class="sxs-lookup"><span data-stu-id="4432b-134">Critical Sections</span></span>

<span data-ttu-id="4432b-135">為了讓您更容易追蹤鎖死，請包含判斷呼叫程式碼是否擁有指定的重要區段的判斷提示。</span><span class="sxs-lookup"><span data-stu-id="4432b-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="4432b-136">[**CritCheckIn**](critcheckin.md)和 [**CritCheckOut**](critcheckout.md)函數會指出呼叫執行緒是否擁有重要區段。</span><span class="sxs-lookup"><span data-stu-id="4432b-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="4432b-137">一般來說，您會從 assert 宏內部呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="4432b-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="4432b-138">您也可以使用 [**DbgLockTrace**](dbglocktrace.md) 函式來追蹤何時保留或釋放重要區段。</span><span class="sxs-lookup"><span data-stu-id="4432b-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4432b-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="4432b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4432b-140">在 DirectShow 中進行調試</span><span class="sxs-lookup"><span data-stu-id="4432b-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



