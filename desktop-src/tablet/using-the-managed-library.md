---
description: 管理程式庫的總覽，以及使用 Tablet PC 平臺受管理程式庫的附注。
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: 使用受管理的程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106982788"
---
# <a name="using-the-managed-library"></a><span data-ttu-id="c34fd-103">使用受管理的程式庫</span><span class="sxs-lookup"><span data-stu-id="c34fd-103">Using the Managed Library</span></span>

<span data-ttu-id="c34fd-104">Common language runtime 是 Microsoft .NET Framework 的基礎。</span><span class="sxs-lookup"><span data-stu-id="c34fd-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c34fd-105">您可以將 common language runtime 視為在運行時間管理程式碼的代理程式，提供核心服務，例如記憶體管理、執行緒管理和遠端處理，同時強制執行嚴格的程式碼安全性。</span><span class="sxs-lookup"><span data-stu-id="c34fd-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="c34fd-106">事實上，程式碼管理的概念是 common language runtime 的基本原則。</span><span class="sxs-lookup"><span data-stu-id="c34fd-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="c34fd-107">以 common language runtime 為目標的程式碼稱為 managed 程式碼。</span><span class="sxs-lookup"><span data-stu-id="c34fd-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="c34fd-108">不是以 common language runtime 為目標的程式碼稱為機器碼。</span><span class="sxs-lookup"><span data-stu-id="c34fd-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="c34fd-109">Framework 類別庫是一組完整的物件導向集合，可供您用來開發應用程式，範圍從傳統的命令列或圖形化使用者介面， (GUI) 應用程式到以 ASP.NET 和 Web 服務所提供的最新創新為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c34fd-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="c34fd-110">Tablet PC Managed 程式庫包含一組受管理的物件，可延伸架構，以支援 Tablet PC 的手寫輸入和輸出，以及與其他電腦的資料交換。</span><span class="sxs-lookup"><span data-stu-id="c34fd-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="c34fd-111">例外狀況</span><span class="sxs-lookup"><span data-stu-id="c34fd-111">Exceptions</span></span>

<span data-ttu-id="c34fd-112">Tablet PC API 中的 managed 程式庫物件會包裝 COM 程式庫的實現。</span><span class="sxs-lookup"><span data-stu-id="c34fd-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="c34fd-113">當基礎 COM 程式庫物件或控制項傳回錯誤時，managed API 會擲回 ThrowExceptionForHR 例外狀況，以提供內部 COM 例外狀況的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c34fd-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="c34fd-114">您可以參考 COM 程式庫參考中的 HRESULT 值，以取得可能傳回之可能錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c34fd-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="c34fd-115">物件比較</span><span class="sxs-lookup"><span data-stu-id="c34fd-115">Object Comparison</span></span>

<span data-ttu-id="c34fd-116">針對 Tablet PC 平臺 Managed 程式庫中的所有物件，不會覆寫 [**Equals**](/previous-versions/windows/) 以正確地比較兩個相同的物件。</span><span class="sxs-lookup"><span data-stu-id="c34fd-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="c34fd-117">Managed 應用程式開發介面 (API) 不支援透過 **equals** 函式或 equals (= =) 運算子來比較物件是否相等。</span><span class="sxs-lookup"><span data-stu-id="c34fd-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="c34fd-118">系結至最新的 Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="c34fd-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="c34fd-119">最新的 Microsoft.Ink.dll 元件是 Microsoft.Ink.dll 1.0 版和 Microsoft.Ink.15.dll 的相容取代。</span><span class="sxs-lookup"><span data-stu-id="c34fd-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="c34fd-120">在大部分情況下，您不需要對使用舊版元件所散發的應用程式進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="c34fd-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="c34fd-121">不過，在某些情況下，您需要指示 common language runtime 載入器使用較新的動態連結程式庫， (DLL) 參考較舊的 Dll 的任何地方。</span><span class="sxs-lookup"><span data-stu-id="c34fd-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="c34fd-122">您必須使用下列技巧明確地系結至新元件的唯一時機，就是您的應用程式所使用的 1.5 1.0 元件，與參考較新版本元件的元件（例如1.7）以及這些元件可能交換資料的元件組合使用。</span><span class="sxs-lookup"><span data-stu-id="c34fd-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="c34fd-123">指示 common language runtime 載入器使用較新 DLL 的最佳方式，就是在應用層級重新導向元件版本。</span><span class="sxs-lookup"><span data-stu-id="c34fd-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="c34fd-124">您可以藉由將元件系結資訊放在應用程式的設定檔中，指定您的應用程式使用較新版本的元件。</span><span class="sxs-lookup"><span data-stu-id="c34fd-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="c34fd-125">如需在應用層級重新導向元件版本的詳細資訊，請參閱重新導向 [元件版本](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)，尤其是「在設定檔中指定元件系結」一節。</span><span class="sxs-lookup"><span data-stu-id="c34fd-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="c34fd-126">您將需要在與可執行檔相同的目錄中建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="c34fd-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="c34fd-127">設定檔的名稱必須與可執行檔的名稱相同，後面接著 .config 副檔名。</span><span class="sxs-lookup"><span data-stu-id="c34fd-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="c34fd-128">例如，MyApp.exe 的應用程式中，設定檔必須是 MyApp.exe.config 的檔案。</span><span class="sxs-lookup"><span data-stu-id="c34fd-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="c34fd-129">設定檔會使用 [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) 專案來強制所有先前的版本對應至最新版本，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="c34fd-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="c34fd-130">如需設定檔的詳細資訊，包括如何為設定檔建立可延伸標記語言 (XML)  (XML) 的範例，請參閱 [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) 和重新導向 [元件版本](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)。</span><span class="sxs-lookup"><span data-stu-id="c34fd-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="c34fd-131">使用 Microsoft Windows XP Tablet PC Edition 開發工具組1.7 和更新版本所建立的應用程式，會自動系結至新版的 Microsoft Ink 元件。</span><span class="sxs-lookup"><span data-stu-id="c34fd-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="c34fd-132">如需元件系結的詳細資訊，請參閱 [執行時間如何找出元件](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp)。</span><span class="sxs-lookup"><span data-stu-id="c34fd-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="c34fd-133">使用 [分割](/previous-versions/ms583616(v=vs.100)) 類別或 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 類別的應用程式無法使用應用程式原則系結至更新的元件。</span><span class="sxs-lookup"><span data-stu-id="c34fd-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="c34fd-134">使用其中一種類別的應用程式必須繼續使用 Microsoft.Ink.15.dll 或在參考更新的元件之後重新編譯。</span><span class="sxs-lookup"><span data-stu-id="c34fd-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="c34fd-135">使用事件</span><span class="sxs-lookup"><span data-stu-id="c34fd-135">Working with Events</span></span>

<span data-ttu-id="c34fd-136">如果任何 managed 物件的事件處理常式中的程式碼擲回例外狀況，則不會將例外狀況傳遞給使用者。</span><span class="sxs-lookup"><span data-stu-id="c34fd-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="c34fd-137">若要確保傳遞例外狀況，請在事件處理常式中針對 managed 事件使用 try-catch 區塊。</span><span class="sxs-lookup"><span data-stu-id="c34fd-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="c34fd-138">管理表單</span><span class="sxs-lookup"><span data-stu-id="c34fd-138">Managing Forms</span></span>

<span data-ttu-id="c34fd-139">[Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1)類別和其基類並未定義完成項。</span><span class="sxs-lookup"><span data-stu-id="c34fd-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="c34fd-140">若要清除表單上的資源，請撰寫提供完成項的子類別 (例如， \# 使用 ~) 呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1)的 C 函式。</span><span class="sxs-lookup"><span data-stu-id="c34fd-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="c34fd-141">若要進行清除，完成項會覆寫 Dispose，然後呼叫基類處置。</span><span class="sxs-lookup"><span data-stu-id="c34fd-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="c34fd-142">當布林值參數為 **FALSE** 時，請不要在 Dispose 方法中參考需要 [Finalize](/previous-versions/windows/)方法的其他物件，因為這些物件可能已經完成。</span><span class="sxs-lookup"><span data-stu-id="c34fd-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="c34fd-143">如需釋放資源的詳細資訊 [，請參閱 Finalize 方法和析構函數](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp)。</span><span class="sxs-lookup"><span data-stu-id="c34fd-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="c34fd-144">表單和 RecognizerCoNtext</span><span class="sxs-lookup"><span data-stu-id="c34fd-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="c34fd-145">[RecognizerCoNtext](/previous-versions/ms552546(v=vs.100)) 事件會在與表單所線上程不同的執行緒中執行。</span><span class="sxs-lookup"><span data-stu-id="c34fd-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="c34fd-146">Windows Forms 中的控制項系結至特定的執行緒，而且不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="c34fd-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="c34fd-147">因此，您必須使用其中一個控制項的 invoke 方法，將呼叫封送處理至適當的執行緒。</span><span class="sxs-lookup"><span data-stu-id="c34fd-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="c34fd-148">控制項上的四個方法都是安全線程： [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)、 [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1)、 [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)和 [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) 方法。</span><span class="sxs-lookup"><span data-stu-id="c34fd-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="c34fd-149">針對其他所有方法呼叫，請在從不同的執行緒呼叫時，使用其中一個 invoke 方法。</span><span class="sxs-lookup"><span data-stu-id="c34fd-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="c34fd-150">如需使用這些方法的詳細資訊，請參閱 [從執行緒操作控制項](/previous-versions/757y83z4(v=vs.140))。</span><span class="sxs-lookup"><span data-stu-id="c34fd-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="c34fd-151">等候事件</span><span class="sxs-lookup"><span data-stu-id="c34fd-151">Waiting for Events</span></span>

<span data-ttu-id="c34fd-152">Tablet PC 環境為多執行緒。</span><span class="sxs-lookup"><span data-stu-id="c34fd-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="c34fd-153">使用 [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) 函式，而不是其他等候方法，以允許可重複使用的元件物件模型 (COM) 呼叫，以在應用程式等候事件時輸入您的多執行緒單元 (MTA) 。</span><span class="sxs-lookup"><span data-stu-id="c34fd-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="c34fd-154">使用筆墨筆劃集合</span><span class="sxs-lookup"><span data-stu-id="c34fd-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="c34fd-155">從[筆墨](/previous-versions/aa515768(v=msdn.10))物件取得之[筆劃](/previous-versions/ms552701(v=vs.100))集合的實例不會進行垃圾收集。</span><span class="sxs-lookup"><span data-stu-id="c34fd-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="c34fd-156">為了避免記憶體流失，每當您使用這些集合的其中一個時，請使用如下所示的 "using" 語句。</span><span class="sxs-lookup"><span data-stu-id="c34fd-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="c34fd-157">處置 Managed 物件和控制項</span><span class="sxs-lookup"><span data-stu-id="c34fd-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="c34fd-158">若要避免記憶體流失，您必須在物件或控制項超出範圍之前，于已附加事件處理常式的任何 Tablet PC 物件或控制項上明確呼叫 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法。</span><span class="sxs-lookup"><span data-stu-id="c34fd-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="c34fd-159">若要改善應用程式的效能，請在不再需要下列物件、控制項和集合時，手動處置這些物件、控制項和集合。</span><span class="sxs-lookup"><span data-stu-id="c34fd-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="c34fd-160">[分](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c34fd-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="c34fd-161">[筆跡](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c34fd-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="c34fd-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c34fd-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="c34fd-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c34fd-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="c34fd-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c34fd-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="c34fd-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c34fd-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="c34fd-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c34fd-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="c34fd-167">[RecognizerCoNtext](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c34fd-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="c34fd-168">[中風](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c34fd-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="c34fd-169">下列 C \# 範例示範使用 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法的某些案例。</span><span class="sxs-lookup"><span data-stu-id="c34fd-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 