---
title: UI 自動化概觀
description: Microsoft 消費者介面自動化是適用于 Windows 的協助工具架構。
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- 消費者介面自動化，關於
- 消費者介面自動化，協助工具
- 消費者介面自動化，元件
- 消費者介面自動化，提供者 API
- 消費者介面自動化，用戶端 API
- 消費者介面自動化，標頭檔
- 消費者介面自動化，模型
- components
- 協助工具
- 提供者 API
- 用戶端 API
- 標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374331"
---
# <a name="ui-automation-overview"></a><span data-ttu-id="57eb5-115">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="57eb5-115">UI Automation Overview</span></span>

<span data-ttu-id="57eb5-116">Microsoft 消費者介面自動化是適用于 Windows 的協助工具架構。</span><span class="sxs-lookup"><span data-stu-id="57eb5-116">Microsoft UI Automation is an accessibility framework for Windows.</span></span> <span data-ttu-id="57eb5-117">它可讓您以程式設計方式存取桌面上大部分的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="57eb5-117">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="57eb5-118">它可讓輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊給使用者，以及透過標準輸入以外的方式操作 UI。</span><span class="sxs-lookup"><span data-stu-id="57eb5-118">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="57eb5-119">消費者介面自動化也可讓自動化測試腳本與 UI 互動。</span><span class="sxs-lookup"><span data-stu-id="57eb5-119">UI Automation also allows automated test scripts to interact with the UI.</span></span>

<span data-ttu-id="57eb5-120">在 Windows XP 中，消費者介面自動化是 Microsoft .NET Framework 的第一次提供。</span><span class="sxs-lookup"><span data-stu-id="57eb5-120">UI Automation was first available in Windows XP as part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="57eb5-121">雖然非受控 c + + API 也會在當時發佈，但因為互通性問題，所以用戶端函式的實用性受到限制。</span><span class="sxs-lookup"><span data-stu-id="57eb5-121">Although an unmanaged C++ API was also published at that time, the usefulness of client functions was limited because of interoperability issues.</span></span> <span data-ttu-id="57eb5-122">針對 Windows 7，API 已在元件物件模型中重寫 (COM) 。</span><span class="sxs-lookup"><span data-stu-id="57eb5-122">For Windows 7, the API has been rewritten in the Component Object Model (COM).</span></span>

> [!Note]  
> <span data-ttu-id="57eb5-123">雖然在舊版消費者介面自動化引進的程式庫函式仍會記載，但不應該用於新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="57eb5-123">Although the library functions introduced in the earlier version of UI Automation are still documented, they should not be used in new applications.</span></span>

 

<span data-ttu-id="57eb5-124">您可以撰寫消費者介面自動化的用戶端應用程式，以確保這些應用程式可在多個 Microsoft Windows 控制項架構上運作。</span><span class="sxs-lookup"><span data-stu-id="57eb5-124">UI Automation client applications can be written with the assurance that they will work on multiple Microsoft Windows control frameworks.</span></span> <span data-ttu-id="57eb5-125">消費者介面自動化 core 會遮罩架構中各種不同部分的架構差異。</span><span class="sxs-lookup"><span data-stu-id="57eb5-125">The UI Automation core masks any differences in the frameworks that underlie various pieces of the UI.</span></span> <span data-ttu-id="57eb5-126">例如，Windows Presentation Foundation (WPF) 按鈕的 [ **內容** ] 屬性、[Microsoft Win32] 按鈕的 [ **標題** ] 屬性，以及 HTML 影像的 **ALT** 屬性，都會對應到消費者介面自動化視圖中的單一屬性 [ **名稱**]。</span><span class="sxs-lookup"><span data-stu-id="57eb5-126">For example, the **Content** property of a Windows Presentation Foundation (WPF) button, the **Caption** property of a Microsoft Win32 button, and the **ALT** property of an HTML image are all mapped to a single property, **Name**, in the UI Automation view.</span></span>

<span data-ttu-id="57eb5-127">消費者介面自動化在 Windows XP、Windows Server 2003 和更新版本的作業系統中提供完整功能。</span><span class="sxs-lookup"><span data-stu-id="57eb5-127">UI Automation provides full functionality in Windows XP, Windows Server 2003, and later operating systems.</span></span>

<span data-ttu-id="57eb5-128">消費者介面自動化提供者是在控制項上執行消費者介面自動化支援的元件，並透過內建的橋接服務提供 Microsoft Active Accessibility 用戶端應用程式的一些支援。</span><span class="sxs-lookup"><span data-stu-id="57eb5-128">UI Automation providers are components that implement UI Automation support on controls and offer some support for Microsoft Active Accessibility client applications, through a built-in bridging service.</span></span>

> [!Note]  
> <span data-ttu-id="57eb5-129">消費者介面自動化不會啟用由不同使用者透過 [ **執行身份** ] 命令啟動的進程之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="57eb5-129">UI Automation does not enable communication between processes that are started by different users through the **Run as** command.</span></span>

 

<span data-ttu-id="57eb5-130">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="57eb5-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="57eb5-131">消費者介面自動化元件</span><span class="sxs-lookup"><span data-stu-id="57eb5-131">UI Automation Components</span></span>](#ui-automation-components)
-   [<span data-ttu-id="57eb5-132">消費者介面自動化標頭檔</span><span class="sxs-lookup"><span data-stu-id="57eb5-132">UI Automation Header Files</span></span>](#ui-automation-header-files)
-   [<span data-ttu-id="57eb5-133">使用者介面自動化模型</span><span class="sxs-lookup"><span data-stu-id="57eb5-133">UI Automation Model</span></span>](#ui-automation-model)
-   [<span data-ttu-id="57eb5-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="57eb5-134">Related topics</span></span>](#related-topics)

## <a name="ui-automation-components"></a><span data-ttu-id="57eb5-135">消費者介面自動化元件</span><span class="sxs-lookup"><span data-stu-id="57eb5-135">UI Automation Components</span></span>

<span data-ttu-id="57eb5-136">消費者介面自動化有四個主要元件，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="57eb5-136">UI Automation has four main components, as shown in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57eb5-137">元件</span><span class="sxs-lookup"><span data-stu-id="57eb5-137">Component</span></span></th>
<th><span data-ttu-id="57eb5-138">描述</span><span class="sxs-lookup"><span data-stu-id="57eb5-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57eb5-139">提供者 API</span><span class="sxs-lookup"><span data-stu-id="57eb5-139">Provider API</span></span></td>
<td><span data-ttu-id="57eb5-140">由消費者介面自動化提供者所執行的一組 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="57eb5-140">A set of COM interfaces that are implemented by UI Automation providers.</span></span> <span data-ttu-id="57eb5-141">消費者介面自動化提供者為物件，可提供 UI 元素的相關資訊，並回應程式設計的輸入。</span><span class="sxs-lookup"><span data-stu-id="57eb5-141">UI Automation providers are objects that provide information about UI elements and respond to programmatic input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57eb5-142">用戶端 API</span><span class="sxs-lookup"><span data-stu-id="57eb5-142">Client API</span></span></td>
<td><span data-ttu-id="57eb5-143">一組 COM 介面，可讓用戶端應用程式取得 UI 的相關資訊，並將輸入傳送給控制項。</span><span class="sxs-lookup"><span data-stu-id="57eb5-143">A set of COM interfaces that enable client applications to obtain information about the UI and to send input to controls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="57eb5-144">已淘汰的 <a href="uiauto-entry-cpfunctions.md">控制項模式函數</a> 和已淘汰的 <a href="uiauto-entry-uianodefunctions.md">節點</a> 函式中所述的函式已被取代。</span><span class="sxs-lookup"><span data-stu-id="57eb5-144">The functions described in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> and <a href="uiauto-entry-uianodefunctions.md">Deprecated Node Functions</a> are deprecated.</span></span> <span data-ttu-id="57eb5-145">相反地，用戶端應用程式應該使用 <a href="uiauto-entry-uiautoclientinterfaces.md">用戶端消費者介面自動化元素介面</a>中所述的消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="57eb5-145">Instead, client applications should use the UI Automation COM interfaces described in <a href="uiauto-entry-uiautoclientinterfaces.md">UI Automation Element Interfaces for Clients</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57eb5-146">UIAutomationCore.dll</span><span class="sxs-lookup"><span data-stu-id="57eb5-146">UIAutomationCore.dll</span></span></td>
<td><span data-ttu-id="57eb5-147">執行時間程式庫（有時稱為消費者介面自動化 core）可處理提供者與用戶端之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="57eb5-147">The run-time library, sometimes called the UI Automation core, that handles communication between providers and clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57eb5-148">Oleacc.dll</span><span class="sxs-lookup"><span data-stu-id="57eb5-148">Oleacc.dll</span></span></td>
<td><span data-ttu-id="57eb5-149">Microsoft Active Accessibility 和 proxy 物件的執行時間程式庫。</span><span class="sxs-lookup"><span data-stu-id="57eb5-149">The run-time library for Microsoft Active Accessibility and the proxy objects.</span></span> <span data-ttu-id="57eb5-150">此程式庫也會提供 Microsoft Microsoft Active Accessibility 用來消費者介面自動化 Proxy 以支援 Win32 控制項的 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="57eb5-150">The library also provides proxy objects used by the Microsoft Microsoft Active Accessibility to UI Automation Proxy to support Win32 controls.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="57eb5-151">使用消費者介面自動化的方式有兩種：使用提供者 API 來建立自訂控制項的支援，以及建立使用消費者介面自動化核心來與進行通訊的用戶端應用程式，並取得 UI 元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="57eb5-151">There are two ways of using UI Automation: to create support for custom controls by using the provider API, and to create client applications that use the UI Automation core to communicate with, and retrieve information about, UI elements.</span></span> <span data-ttu-id="57eb5-152">視您著重的部分而定，您應該參閱本文件的不同部分。</span><span class="sxs-lookup"><span data-stu-id="57eb5-152">Depending on your focus, you should refer to different parts of the documentation.</span></span> <span data-ttu-id="57eb5-153">如果您需要建立自訂控制項的支援，請參閱 [消費者介面自動化提供者程式](uiauto-providerportal.md)設計人員手冊。</span><span class="sxs-lookup"><span data-stu-id="57eb5-153">If you need to create support for custom controls, see [UI Automation Provider Programmer's Guide](uiauto-providerportal.md).</span></span> <span data-ttu-id="57eb5-154">如果您需要與 UI 元素通訊或取得相關資訊，請參閱 [消費者介面自動化用戶端程式設計人員手冊](uiauto-clientportal.md)。</span><span class="sxs-lookup"><span data-stu-id="57eb5-154">If you need to communicate with or retrieve information about UI elements, see [UI Automation Client Programmer's Guide](uiauto-clientportal.md).</span></span>

## <a name="ui-automation-header-files"></a><span data-ttu-id="57eb5-155">消費者介面自動化標頭檔</span><span class="sxs-lookup"><span data-stu-id="57eb5-155">UI Automation Header Files</span></span>

<span data-ttu-id="57eb5-156">消費者介面自動化 API 是在 Windows 軟體開發套件 (SDK) 隨附的數個不同 C/c + + 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="57eb5-156">The UI Automation API is defined in several different C/C++ header files that are included with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="57eb5-157">下表說明消費者介面自動化標頭檔案：</span><span class="sxs-lookup"><span data-stu-id="57eb5-157">The UI Automation header files are described in the following table:</span></span>



| <span data-ttu-id="57eb5-158">標頭檔</span><span class="sxs-lookup"><span data-stu-id="57eb5-158">Header file</span></span>           | <span data-ttu-id="57eb5-159">Description</span><span class="sxs-lookup"><span data-stu-id="57eb5-159">Description</span></span>                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57eb5-160">Uiautomationclient.dll。h</span><span class="sxs-lookup"><span data-stu-id="57eb5-160">UIAutomationClient.h</span></span>  | <span data-ttu-id="57eb5-161">定義消費者介面自動化用戶端所使用的介面和相關的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="57eb5-161">Defines the interfaces and related programming elements used by UI Automation clients.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="57eb5-162">UIAutomationCore。h</span><span class="sxs-lookup"><span data-stu-id="57eb5-162">UIAutomationCore.h</span></span>    | <span data-ttu-id="57eb5-163">定義消費者介面自動化提供者所使用的介面和相關的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="57eb5-163">Defines the interfaces and related programming elements used by UI Automation providers.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="57eb5-164">UIAutomationCoreApi。h</span><span class="sxs-lookup"><span data-stu-id="57eb5-164">UIAutomationCoreApi.h</span></span> | <span data-ttu-id="57eb5-165">定義消費者介面自動化用戶端和提供者所使用的一般常數、Guid、資料類型和結構。</span><span class="sxs-lookup"><span data-stu-id="57eb5-165">Defines general constants, GUIDs, data types, and structures used by UI Automation clients and providers.</span></span> <span data-ttu-id="57eb5-166">它也包含已被取代之節點和控制項模式函數的定義。</span><span class="sxs-lookup"><span data-stu-id="57eb5-166">It also contains definitions for the deprecated node and control pattern functions.</span></span>                                                                                    |
| <span data-ttu-id="57eb5-167">UIAutomation。h</span><span class="sxs-lookup"><span data-stu-id="57eb5-167">UIAutomation.h</span></span>        | <span data-ttu-id="57eb5-168">包含所有其他的消費者介面自動化標頭檔。</span><span class="sxs-lookup"><span data-stu-id="57eb5-168">Includes all of the other UI Automation header files.</span></span> <span data-ttu-id="57eb5-169">由於大部分的消費者介面自動化應用程式都需要所有消費者介面自動化標頭檔中的元素，因此最好將 UIAutomation 包含在消費者介面自動化應用程式專案中，而不是個別包含每個檔案。</span><span class="sxs-lookup"><span data-stu-id="57eb5-169">Because most UI Automation applications require elements from all UI Automation header files, it is best to include UIAutomation.h in your UI Automation application projects instead of including each file individually.</span></span> |



 

<span data-ttu-id="57eb5-170">如果您正在開發使用消費者介面自動化 API 的應用程式，您應該在專案中包含 UIAutomation。</span><span class="sxs-lookup"><span data-stu-id="57eb5-170">If you are developing an application that uses the UI Automation API, you should include UIAutomation.h in your project.</span></span> <span data-ttu-id="57eb5-171">如果您的應用程式支援 Microsoft Active Accessibility，請包含 Oleacc .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="57eb5-171">If your application supports Microsoft Active Accessibility, include the Oleacc.h header file.</span></span> <span data-ttu-id="57eb5-172">使用 Guid 的消費者介面自動化應用程式也需要 Initguid .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="57eb5-172">UI Automation applications that use GUIDs also require the Initguid.h header file.</span></span> <span data-ttu-id="57eb5-173">如有需要，Initguid 應該包含在 UIAutomation 之前。</span><span class="sxs-lookup"><span data-stu-id="57eb5-173">If needed, Initguid.h should be included before UIAutomation.h.</span></span>

## <a name="ui-automation-model"></a><span data-ttu-id="57eb5-174">使用者介面自動化模型</span><span class="sxs-lookup"><span data-stu-id="57eb5-174">UI Automation Model</span></span>

<span data-ttu-id="57eb5-175">消費者介面自動化會將 UI 的每個元素公開給用戶端應用程式，以做為 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面所代表的物件。</span><span class="sxs-lookup"><span data-stu-id="57eb5-175">UI Automation exposes every element of the UI to client applications as an object represented by the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="57eb5-176">項目包含於樹狀結構中，且桌面是根項目。</span><span class="sxs-lookup"><span data-stu-id="57eb5-176">Elements are contained in a tree structure, with the desktop as the root element.</span></span> <span data-ttu-id="57eb5-177">用戶端可將樹狀結構之未經處理的檢視篩選為控制項檢視或內容檢視。</span><span class="sxs-lookup"><span data-stu-id="57eb5-177">Clients can filter the raw view of the tree as a control view or a content view.</span></span> <span data-ttu-id="57eb5-178">使用 Windows SDK 隨附的 [檢查](inspect-objects.md) 應用程式，即可輕鬆地查看結構的這些標準觀點。</span><span class="sxs-lookup"><span data-stu-id="57eb5-178">These standard views of the structure can easily be seen by using the [Inspect](inspect-objects.md) application that is included with the Windows SDK.</span></span> <span data-ttu-id="57eb5-179">應用程式也可以建立自訂檢視。</span><span class="sxs-lookup"><span data-stu-id="57eb5-179">Applications can also create custom views.</span></span>

<span data-ttu-id="57eb5-180">消費者介面自動化專案會公開其所代表之控制項或 UI 專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="57eb5-180">A UI Automation element exposes properties of the control or UI element that it represents.</span></span> <span data-ttu-id="57eb5-181">其中一個屬性是控制項類型，它會將控制項或 UI 元素的基本外觀和功能定義為單一可辨識的實體，例如按鈕或核取方塊。</span><span class="sxs-lookup"><span data-stu-id="57eb5-181">One of these properties is the control type, which defines the basic appearance and functionality of the control or UI element as a single recognizable entity, for example, a button or check box.</span></span> <span data-ttu-id="57eb5-182">如需控制項類型的詳細資訊，請參閱 [消費者介面自動化控制項類型總覽](uiauto-controltypesoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="57eb5-182">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="57eb5-183">此外，消費者介面自動化元素會公開一或多個控制項模式。</span><span class="sxs-lookup"><span data-stu-id="57eb5-183">In addition, a UI Automation element exposes one or more control patterns.</span></span> <span data-ttu-id="57eb5-184">控制項模式提供特定控制項類型專屬的一組屬性。</span><span class="sxs-lookup"><span data-stu-id="57eb5-184">A control pattern provides a set of properties that are specific to a particular control type.</span></span> <span data-ttu-id="57eb5-185">控制項模式也會公開方法，讓用戶端應用程式取得專案的詳細資訊，並提供輸入給元素。</span><span class="sxs-lookup"><span data-stu-id="57eb5-185">A control pattern also exposes methods that enable client applications to get more information about the element and to provide input to the element.</span></span> <span data-ttu-id="57eb5-186">如需控制項模式的詳細資訊，請參閱 [F:System.Windows.Automation.ValuePatternIdentifiers.ValueProperty](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="57eb5-186">For more information about control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="57eb5-187">控制項類型和控制項模式之間沒有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="57eb5-187">There is no one-to-one correspondence between control types and control patterns.</span></span> <span data-ttu-id="57eb5-188">控制項模式可由多個控制項類型所支援，且控制項可支援多個控制項模式，每個控制項都會公開其行為的不同層面。</span><span class="sxs-lookup"><span data-stu-id="57eb5-188">A control pattern may be supported by multiple control types, and a control may support multiple control patterns, each of which exposes different aspects of its behavior.</span></span> <span data-ttu-id="57eb5-189">例如，下拉式方塊擁有至少兩個控制項模式：其中一個代表展開和折疊的能力，另一個則代表選取機制。</span><span class="sxs-lookup"><span data-stu-id="57eb5-189">For example, a combo box has at least two control patterns: one that represents its ability to expand and collapse, and another that represents the selection mechanism.</span></span> <span data-ttu-id="57eb5-190">不過，控制項只能展示單一控制項類型。</span><span class="sxs-lookup"><span data-stu-id="57eb5-190">However, a control can exhibit only a single control type.</span></span>

 

<span data-ttu-id="57eb5-191">消費者介面自動化透過事件提供用戶端應用程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="57eb5-191">UI Automation provides information to client applications through events.</span></span> <span data-ttu-id="57eb5-192">不同于 WinEvents，消費者介面自動化事件不是以廣播機制為基礎。</span><span class="sxs-lookup"><span data-stu-id="57eb5-192">Unlike WinEvents, UI Automation events are not based on a broadcast mechanism.</span></span> <span data-ttu-id="57eb5-193">消費者介面自動化用戶端會註冊特定的事件通知，並且可要求將特定屬性和控制項模式資訊傳遞給其事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="57eb5-193">UI Automation clients register for specific event notifications and can request that specific properties and control pattern information be passed to their event handlers.</span></span> <span data-ttu-id="57eb5-194">此外，消費者介面自動化事件包含引發它之專案的參考。</span><span class="sxs-lookup"><span data-stu-id="57eb5-194">In addition, a UI Automation event contains a reference to the element that raised it.</span></span> <span data-ttu-id="57eb5-195">提供者可以選擇引發事件來改善效能，取決於是否有任何用戶端接聽。</span><span class="sxs-lookup"><span data-stu-id="57eb5-195">Providers can improve performance by raising events selectively, depending on whether any clients are listening.</span></span> <span data-ttu-id="57eb5-196">如需事件的詳細資訊，請參閱 [UI Automation Events Overview](uiauto-eventsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="57eb5-196">For more information about events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="57eb5-197">相關主題</span><span class="sxs-lookup"><span data-stu-id="57eb5-197">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57eb5-198">**概念**</span><span class="sxs-lookup"><span data-stu-id="57eb5-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57eb5-199">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="57eb5-199">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="57eb5-200">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="57eb5-200">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="57eb5-201">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="57eb5-201">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 





