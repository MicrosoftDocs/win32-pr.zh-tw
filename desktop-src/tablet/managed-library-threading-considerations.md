---
description: 下列 Tablet PC 執行緒的考慮是受管理的程式庫所特有。
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Managed 程式庫執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996840"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="04cdf-103">Managed 程式庫執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="04cdf-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="04cdf-104">下列 Tablet PC 執行緒的考慮是受管理的程式庫所特有。</span><span class="sxs-lookup"><span data-stu-id="04cdf-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="04cdf-105">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="04cdf-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="04cdf-106">STA 和 MTA 應用程式</span><span class="sxs-lookup"><span data-stu-id="04cdf-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="04cdf-107">Windows Forms 執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="04cdf-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="04cdf-108">剪貼簿考慮</span><span class="sxs-lookup"><span data-stu-id="04cdf-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="04cdf-109">事件處理常式內的例外狀況</span><span class="sxs-lookup"><span data-stu-id="04cdf-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="04cdf-110">處置物件和控制項</span><span class="sxs-lookup"><span data-stu-id="04cdf-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="04cdf-111">StylusInput Api</span><span class="sxs-lookup"><span data-stu-id="04cdf-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="04cdf-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="04cdf-112">Thread-Safety</span></span>

<span data-ttu-id="04cdf-113">Tablet PC 平臺的 Managed 程式庫類別通常不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="04cdf-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="04cdf-114">下列集合是成員層級上的安全線程;但是，如果另一個執行緒同時在集合上操作，則這些集合不保證會保護列舉值：</span><span class="sxs-lookup"><span data-stu-id="04cdf-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="04cdf-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="04cdf-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="04cdf-116">[資料指標](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="04cdf-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="04cdf-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="04cdf-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="04cdf-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="04cdf-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="04cdf-119">[辨識器](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="04cdf-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="04cdf-120">[平板電腦](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="04cdf-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="04cdf-121">STA 和 MTA 應用程式</span><span class="sxs-lookup"><span data-stu-id="04cdf-121">STA and MTA Applications</span></span>

<span data-ttu-id="04cdf-122">使用 Microsoft Visual Studio .NET 中包含的嚮導所建立的受控應用程式，預設是單一執行緒的單元 (STA) 。</span><span class="sxs-lookup"><span data-stu-id="04cdf-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="04cdf-123">您可以藉由在應用程式的進入點上設定 STA 執行緒或多執行緒單元 (MTA) thread 屬性，來變更應用程式的單元。</span><span class="sxs-lookup"><span data-stu-id="04cdf-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="04cdf-124">如果您的應用程式是在 MTA 中執行，您必須撰寫安全線程的程式碼;不過，藉由這麼做，您就可以改善某些事件處理效能問題。</span><span class="sxs-lookup"><span data-stu-id="04cdf-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="04cdf-125">如需 STA 執行緒和 MTA 執行緒屬性的詳細資訊，請參閱 [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) 類別和 [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) 類別。</span><span class="sxs-lookup"><span data-stu-id="04cdf-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="04cdf-126">Windows Forms 執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="04cdf-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="04cdf-127">[InkPicture](/previous-versions/aa514604(v=msdn.10))和[InkEdit](/previous-versions/ms552265(v=vs.100))控制項會擴充 Windows Forms 控制項。</span><span class="sxs-lookup"><span data-stu-id="04cdf-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="04cdf-128">Windows Forms 控制項使用單一執行緒的單元 (STA) 模型，因為 Windows Forms 是以原本就是單一執行緒的原生 Win32 視窗為基礎。</span><span class="sxs-lookup"><span data-stu-id="04cdf-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="04cdf-129">在 managed 程式碼中，筆墨控制項應該在與表單主執行緒相同的執行緒中建立。</span><span class="sxs-lookup"><span data-stu-id="04cdf-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="04cdf-130">在 STA 應用程式中，某些事件會發生在應用程式的使用者介面以外的執行緒上， (UI) 執行緒。</span><span class="sxs-lookup"><span data-stu-id="04cdf-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="04cdf-131">從 Tablet PC 事件處理常式內呼叫任何 Windows Forms 物件或控制項（包括 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 和 [InkEdit](/previous-versions/ms552265(v=vs.100)) 控制項）時，請使用物件或控制項的繼承 [控制項。 Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) 方法。</span><span class="sxs-lookup"><span data-stu-id="04cdf-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="04cdf-132">[System.windows.forms.control.invokerequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1)屬性（繼承自 Control 類別）可以用來判斷是否需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="04cdf-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="04cdf-133">例如 [，在下列辨識事件的](/previous-versions/ms829424(v=msdn.10)) 事件處理常式中，會測試 [system.windows.forms.control.invokerequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) 屬性，如果是 **TRUE**，就會從使用者介面執行緒重新叫用事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="04cdf-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="04cdf-134">如果您將 [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) 放到 awebpagein 瀏覽器 (查看) 的 [Web 控制項](web-controls.md) ，則會以 STA 應用程式的形式執行。</span><span class="sxs-lookup"><span data-stu-id="04cdf-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="04cdf-135">針對智慧型用戶端應用程式 (看 [不到任何 Touch 部署](no-touch-deployment.md)) ，開發人員可以完全掌控 [system.threading.thread.apartmentstate](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1)。</span><span class="sxs-lookup"><span data-stu-id="04cdf-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="04cdf-136"> (預設值通常是 STA，但可以是 MTA （視您的 CLR 版本而定）。 ) 涉及 [**RealTimeStylus**](realtimestylus-class.md)的執行緒問題，請參閱 [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="04cdf-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="04cdf-137">如需從 MTA 應用程式呼叫 Windows Forms 的詳細資訊，請參閱 [多執行緒 Windows Forms 控制項範例](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71))。</span><span class="sxs-lookup"><span data-stu-id="04cdf-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="04cdf-138">剪貼簿考慮</span><span class="sxs-lookup"><span data-stu-id="04cdf-138">Clipboard Considerations</span></span>

<span data-ttu-id="04cdf-139">[剪貼](../dataxchg/clipboard.md)簿物件僅適用于 STA 執行緒。</span><span class="sxs-lookup"><span data-stu-id="04cdf-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="04cdf-140">嘗試從不是 STA 的執行緒複製或貼上剪貼簿時，您會收到 [system.threading.threadstateexception](/previous-versions/windows/)。</span><span class="sxs-lookup"><span data-stu-id="04cdf-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="04cdf-141">如果您的應用程式是 MTA，請建立 STA 執行緒來處理剪貼簿的方法呼叫，以及您應用程式的一些其他 UI 層面。</span><span class="sxs-lookup"><span data-stu-id="04cdf-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="04cdf-142">事件處理常式內的例外狀況</span><span class="sxs-lookup"><span data-stu-id="04cdf-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="04cdf-143">無法從 Tablet PC 事件處理常式中擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="04cdf-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="04cdf-144">例如，如果 Tablet PC 物件或集合的事件處理常式委派有三個已註冊的處理常式，而第一個處理常式擲回例外狀況，則會發生下列順序：</span><span class="sxs-lookup"><span data-stu-id="04cdf-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="04cdf-145">第一個處理常式會結束。</span><span class="sxs-lookup"><span data-stu-id="04cdf-145">The first handler exits.</span></span>
2.  <span data-ttu-id="04cdf-146">例外狀況會遺失。</span><span class="sxs-lookup"><span data-stu-id="04cdf-146">The exception is lost.</span></span>
3.  <span data-ttu-id="04cdf-147">不會叫用剩餘的處理常式。</span><span class="sxs-lookup"><span data-stu-id="04cdf-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="04cdf-148">處置物件和控制項</span><span class="sxs-lookup"><span data-stu-id="04cdf-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="04cdf-149">若要避免記憶體流失，您必須在物件或控制項超出範圍之前，于已附加事件處理常式的任何 Tablet PC 物件或控制項上明確呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法。</span><span class="sxs-lookup"><span data-stu-id="04cdf-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="04cdf-150">若要改善應用程式的效能，請在不再需要物件或控制項時，手動處置任何執行 [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法的 Tablet PC 物件或控制項。</span><span class="sxs-lookup"><span data-stu-id="04cdf-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="04cdf-151">StylusInput Api</span><span class="sxs-lookup"><span data-stu-id="04cdf-151">StylusInput APIs</span></span>

<span data-ttu-id="04cdf-152">如需有關 [**RealTimeStylus**](realtimestylus-class.md) 物件的執行緒考慮和 StylusInput 應用程式設計介面 (api 的詳細資訊) 參閱 [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="04cdf-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
