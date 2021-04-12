---
title: 使用應用程式模式重新設定功能區
description: Windows 功能區架構支援在執行時間以動態方式重新設定和公開功能區 UI 的核心元素，並根據應用程式的狀態 (也稱為內容) 。
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Windows 功能區，以應用程式模式重新設定
- 功能區，以應用程式模式重新設定
- 使用應用程式模式重新設定 Windows 功能區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375349"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a><span data-ttu-id="78eef-106">使用應用程式模式重新設定功能區</span><span class="sxs-lookup"><span data-stu-id="78eef-106">Reconfiguring the Ribbon with Application Modes</span></span>

<span data-ttu-id="78eef-107">Windows 功能區架構支援在執行時間以動態方式重新設定和公開功能區 UI 的核心元素，並根據應用程式的狀態 (也稱為內容) 。</span><span class="sxs-lookup"><span data-stu-id="78eef-107">The Windows Ribbon framework supports the dynamic reconfiguring and exposing of core elements of the Ribbon UI at run time, based on the application's state (also referred to as context).</span></span> <span data-ttu-id="78eef-108">宣告並與標記中的特定元素相關聯時，應用程式支援的各種狀態稱為應用程式模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-108">Declared and associated with specific elements in markup, the various states supported by an application are referred to as application modes.</span></span>

-   [<span data-ttu-id="78eef-109">簡介</span><span class="sxs-lookup"><span data-stu-id="78eef-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="78eef-110">內容相關消費者介面</span><span class="sxs-lookup"><span data-stu-id="78eef-110">Contextual User Interface</span></span>](#contextual-user-interface)
    -   [<span data-ttu-id="78eef-111">簡單的應用程式模式案例</span><span class="sxs-lookup"><span data-stu-id="78eef-111">A Simple Application Mode Scenario</span></span>](#a-simple-application-mode-scenario)
-   [<span data-ttu-id="78eef-112">執行應用程式模式</span><span class="sxs-lookup"><span data-stu-id="78eef-112">Implementing Application Modes</span></span>](#implementing-application-modes)
    -   [<span data-ttu-id="78eef-113">識別模式</span><span class="sxs-lookup"><span data-stu-id="78eef-113">Identify the Modes</span></span>](#identify-the-modes)
    -   [<span data-ttu-id="78eef-114">將控制項指派給應用程式模式</span><span class="sxs-lookup"><span data-stu-id="78eef-114">Assign Controls to Application Modes</span></span>](#assign-controls-to-application-modes)
    -   [<span data-ttu-id="78eef-115">執行時間切換模式</span><span class="sxs-lookup"><span data-stu-id="78eef-115">Switch Modes at Runtime</span></span>](#switch-modes-at-runtime)
-   [<span data-ttu-id="78eef-116">備註</span><span class="sxs-lookup"><span data-stu-id="78eef-116">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="78eef-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="78eef-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="78eef-118">簡介</span><span class="sxs-lookup"><span data-stu-id="78eef-118">Introduction</span></span>

<span data-ttu-id="78eef-119">應用程式模式是由控制項的邏輯群組所組成，這些控制項會公開功能區 UI 中的一些核心應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="78eef-119">Application modes consist of logical groups of controls that expose some core application functionality in the Ribbon UI.</span></span> <span data-ttu-id="78eef-120">這些模式是由應用程式透過呼叫 framework 方法 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)來動態啟用或停用，它會開啟或關閉一或多個應用程式模式的可見度。</span><span class="sxs-lookup"><span data-stu-id="78eef-120">These modes are dynamically enabled or disabled by the application through a call to the framework method [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), which turns the visibility of one or more application modes on or off.</span></span>

## <a name="contextual-user-interface"></a><span data-ttu-id="78eef-121">內容相關消費者介面</span><span class="sxs-lookup"><span data-stu-id="78eef-121">Contextual User Interface</span></span>

<span data-ttu-id="78eef-122">功能區架構藉由併入可順暢地回應使用者互動和應用程式內容的動態控制項，來提供豐富的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="78eef-122">The Ribbon framework provides rich user experience by incorporating dynamic controls that respond seamlessly to user interaction and application context.</span></span> <span data-ttu-id="78eef-123">此豐富的內容 UI 是透過下列機制的組合提供：</span><span class="sxs-lookup"><span data-stu-id="78eef-123">This rich contextual UI is delivered through a combination of the following mechanisms:</span></span>

-   <span data-ttu-id="78eef-124">資源庫-以集合為基礎的控制項，支援其專案集合的動態操作。</span><span class="sxs-lookup"><span data-stu-id="78eef-124">Galleries - collection-based controls that support the dynamic manipulation of their item collections.</span></span>
-   <span data-ttu-id="78eef-125">內容索引標籤-功能區索引標籤，其可見度是由工作區內容的變更所決定，例如檔中的影像選取範圍。</span><span class="sxs-lookup"><span data-stu-id="78eef-125">Contextual tabs - ribbon tabs that have their visibility determined by a change in workspace context, such as the selection of an image in a document.</span></span>
-   <span data-ttu-id="78eef-126">應用程式模式-相依于應用程式內容的核心應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="78eef-126">Application modes - core application functionality that is dependent on application context.</span></span>

<span data-ttu-id="78eef-127">在某些方面，應用程式模式的功能類似于內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="78eef-127">In some respects, application modes appear functionally similar to contextual tabs.</span></span> <span data-ttu-id="78eef-128">不過，基本的差異在於各自的意圖和範圍中。</span><span class="sxs-lookup"><span data-stu-id="78eef-128">However, the fundamental distinction lies in the intent and scope of each.</span></span>

<span data-ttu-id="78eef-129">啟用內容控制項以回應應用程式內的內容變更。</span><span class="sxs-lookup"><span data-stu-id="78eef-129">Contextual controls are activated in response to a change of context within an application.</span></span> <span data-ttu-id="78eef-130">例如，在 Windows 7 的 Microsoft 小畫家中，當使用者將文字區域插入工作區時，會顯示包含文字相關命令群組的內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="78eef-130">For example, in Microsoft Paint for Windows 7, a contextual tab that contains groups of text-related commands is displayed when a user inserts a text area into the workspace.</span></span> <span data-ttu-id="78eef-131">此內容索引標籤不包含應用程式的核心命令，而且只會在 UI 中公開，因為應用程式 *中* 的內容已變更。</span><span class="sxs-lookup"><span data-stu-id="78eef-131">This contextual tab does not contain core commands for the application and is only exposed in the UI because the context *within* the application has changed.</span></span> <span data-ttu-id="78eef-132">應用程式的核心功能 (影像編輯命令) 仍相關且可供使用者使用，即使是可見的內容索引標籤。</span><span class="sxs-lookup"><span data-stu-id="78eef-132">The core functionality of the application (the image editing commands) is still relevant and available to the user, even with the contextual tab visible.</span></span>

<span data-ttu-id="78eef-133">應用程式模式與內容相關的控制項不同之處在于，它們會重新設定功能，以回應應用程式運作的內容變更。</span><span class="sxs-lookup"><span data-stu-id="78eef-133">Application modes differ from contextual controls in that they reconfigure functionality in response to changes in the context that the application is operating in.</span></span> <span data-ttu-id="78eef-134">應用程式模式位於較高層級的抽象層級;它們提供一種方式來重新設定應用程式的核心功能，而不是暫時公開不是 UI 核心元件的功能。</span><span class="sxs-lookup"><span data-stu-id="78eef-134">Application modes sit at a higher level of abstraction; they provide a way to reconfigure the core functionality of an application instead of temporarily exposing functionality that is not a core component of the UI.</span></span> <span data-ttu-id="78eef-135">例如，在 Windows 7 的 Microsoft 小畫家中，當叫用 **預覽列印** 命令時，會在應用程式模式中切換。</span><span class="sxs-lookup"><span data-stu-id="78eef-135">For example, in Microsoft Paint for Windows 7, a switch in application mode occurs when the **Print preview** command is invoked.</span></span> <span data-ttu-id="78eef-136">當 Microsoft 小畫家切換至 [ **預覽列印**] 時，應用程式正在操作的內容會從編輯變更為預覽。</span><span class="sxs-lookup"><span data-stu-id="78eef-136">When Microsoft Paint switches to **Print preview**, the context that the application is operating in changes from editing to previewing.</span></span> <span data-ttu-id="78eef-137">如此一來，應用程式的核心功能就會變更，直到取消 **預覽列印** ，且應用程式再次進入編輯內容為止。</span><span class="sxs-lookup"><span data-stu-id="78eef-137">As a result, the core functionality of the application changes until the **Print preview** is canceled and the application enters the editing context again.</span></span>

### <a name="a-simple-application-mode-scenario"></a><span data-ttu-id="78eef-138">簡單的應用程式模式案例</span><span class="sxs-lookup"><span data-stu-id="78eef-138">A Simple Application Mode Scenario</span></span>

<span data-ttu-id="78eef-139">下列案例示範如何在名為 RibbonApp 的應用程式中使用應用程式模式，以公開核心功能的不同部分。</span><span class="sxs-lookup"><span data-stu-id="78eef-139">The following scenario demonstrates how application modes are used, in an application called RibbonApp, to expose discrete aspects of core functionality.</span></span>

<span data-ttu-id="78eef-140">RibbonApp 中定義了兩個應用程式模式：</span><span class="sxs-lookup"><span data-stu-id="78eef-140">Two application modes are defined in RibbonApp:</span></span>

-   <span data-ttu-id="78eef-141">**簡單** 模式會公開整個功能區 UI 中的基本命令。</span><span class="sxs-lookup"><span data-stu-id="78eef-141">**Simple** mode exposes basic commands throughout the Ribbon UI.</span></span> <span data-ttu-id="78eef-142">無論使用哪一種應用程式模式，這些命令都會出現在任何時候。</span><span class="sxs-lookup"><span data-stu-id="78eef-142">These commands appear at all times, no matter which application mode is active.</span></span>
-   <span data-ttu-id="78eef-143">**Advanced** 模式會公開適用于應用程式專家使用者的複雜命令。</span><span class="sxs-lookup"><span data-stu-id="78eef-143">**Advanced** mode exposes complex commands intended for expert users of the application.</span></span> <span data-ttu-id="78eef-144">除了簡單的命令之外，這些 advanced 命令也會出現在功能區 UI 中。</span><span class="sxs-lookup"><span data-stu-id="78eef-144">These advanced commands appear throughout the Ribbon UI, in addition to the simple commands.</span></span>

<span data-ttu-id="78eef-145">依預設，RibbonApp 會設定為 [在 **簡單** 模式中開啟]，而且會在 [ **應用程式] 功能表** 和 [ **主** 資料夾] 索引標籤中顯示使用者所需的命令。下列螢幕擷取畫面顯示簡單模式下的 [RibbonApp **應用程式] 功能表** 和 [ **首頁** ] 索引 **卷** 標，並醒目提示模式控制項。</span><span class="sxs-lookup"><span data-stu-id="78eef-145">By default, RibbonApp is set to open in **Simple** mode, and the commands required by novice users are displayed in the **Application Menu** and the **Home** tab. The following screen shots show the RibbonApp **Application Menu** and **Home** tab in **Simple** mode, highlighting the modal controls.</span></span>

![顯示簡單應用程式模式索引標籤的螢幕擷取畫面。](images/overviews/appmode-hometab.png)![顯示簡單應用程式模式應用程式功能表的螢幕擷取畫面。](images/overviews/appmode-simpleappmenu.png)

<span data-ttu-id="78eef-148">雖然這些命令對新手使用者而言可能已足夠，但 RibbonApp 也會透過 **Advanced** 模式支援專家使用者，當您按一下 **應用程式功能表** 中的 [**切換到 Advanced mode]** 按鈕來啟動時，就會顯示其他的核心功能。</span><span class="sxs-lookup"><span data-stu-id="78eef-148">While these commands may be sufficient for novice users, the RibbonApp also supports expert users through an **Advanced** mode that, when activated by clicking the **Switch to Advanced Mode** button in the **Application Menu**, displays additional core functionality.</span></span>

<span data-ttu-id="78eef-149">藉由將標記中的各種元素系結至可依需要開啟和關閉的離散應用程式模式，即可輕鬆地執行此案例。</span><span class="sxs-lookup"><span data-stu-id="78eef-149">This scenario is easily implemented by binding various elements in markup to discrete application modes that can be turned on and off as required.</span></span> <span data-ttu-id="78eef-150">下列螢幕擷取畫面顯示 [ **Advanced** ] 模式中的 [RibbonApp **應用程式] 功能表** 和 [**首頁**] 索引標籤，並醒目提示模式控制項。</span><span class="sxs-lookup"><span data-stu-id="78eef-150">The following screen shots show the RibbonApp **Application Menu** and **Home** tab in **Advanced** mode, highlighting the modal controls.</span></span>

![顯示 [advanced] 應用程式模式索引標籤的螢幕擷取畫面。](images/overviews/appmode-advancedtab.png)![顯示 [advanced application] 模式的 [應用程式] 功能表的螢幕擷取畫面。](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a><span data-ttu-id="78eef-153">執行應用程式模式</span><span class="sxs-lookup"><span data-stu-id="78eef-153">Implementing Application Modes</span></span>

<span data-ttu-id="78eef-154">本節將概述功能區架構應用程式模式的執行通常需要的三個步驟。</span><span class="sxs-lookup"><span data-stu-id="78eef-154">This section outlines the three steps typically required for the implementation of Ribbon framework application modes.</span></span> <span data-ttu-id="78eef-155">RibbonApp 是用來提供每個步驟的範例。</span><span class="sxs-lookup"><span data-stu-id="78eef-155">RibbonApp is used to provide an example for each step.</span></span>

### <a name="identify-the-modes"></a><span data-ttu-id="78eef-156">識別模式</span><span class="sxs-lookup"><span data-stu-id="78eef-156">Identify the Modes</span></span>

<span data-ttu-id="78eef-157">應用程式中的每個模式都應該代表一組邏輯功能，這取決於應用程式能夠操作的內容。</span><span class="sxs-lookup"><span data-stu-id="78eef-157">Each mode in an application should represent a logical set of functionality that depends on the context an application is able to operate in.</span></span> <span data-ttu-id="78eef-158">例如，如果應用程式顯示的控制項只有在偵測到網路連接時才有關聯，這些控制項就會在網路內容中運作，而這可能會讓 **網路** 模式的建立。</span><span class="sxs-lookup"><span data-stu-id="78eef-158">For example, if an application displays controls that are only relevant when a network connection is detected, those controls operate within a networking context that might justify the creation of a **Network** mode.</span></span>

<span data-ttu-id="78eef-159">RibbonApp 有兩個在任何指定時間都可以處於作用中的內容： **Simple** 和 **Advanced**。</span><span class="sxs-lookup"><span data-stu-id="78eef-159">RibbonApp has two contexts that can be active at any given time: **Simple** and **Advanced**.</span></span> <span data-ttu-id="78eef-160">因此，RibbonApp 需要兩種模式： **Simple** 和 **Advanced**。</span><span class="sxs-lookup"><span data-stu-id="78eef-160">Therefore, RibbonApp requires two modes: **Simple** and **Advanced**.</span></span>

### <a name="assign-controls-to-application-modes"></a><span data-ttu-id="78eef-161">將控制項指派給應用程式模式</span><span class="sxs-lookup"><span data-stu-id="78eef-161">Assign Controls to Application Modes</span></span>

<span data-ttu-id="78eef-162">一旦識別出應用程式模式之後，請在支援應用程式模式的控制項元素的標記中宣告 *ApplicationModes* 屬性，將每個功能區控制項指派給模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-162">Once the application modes have been identified, assign each Ribbon control to a mode by declaring an *ApplicationModes* attribute in markup for those control elements that support application modes.</span></span>

<span data-ttu-id="78eef-163">功能區視圖可讓您在下列控制項元素上指定模式：</span><span class="sxs-lookup"><span data-stu-id="78eef-163">The Ribbon View allows modes to be specified on the following control elements:</span></span>

-   <span data-ttu-id="78eef-164">核心 [**選項卡**](windowsribbon-element-tab.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="78eef-164">Core [**Tab**](windowsribbon-element-tab.md) elements.</span></span>
-   <span data-ttu-id="78eef-165">[**群組**](windowsribbon-element-group.md) 專案 [**是核心索引**](windowsribbon-element-tab.md) 標籤元素的子項目。</span><span class="sxs-lookup"><span data-stu-id="78eef-165">[**Group**](windowsribbon-element-group.md) elements that are child elements of a core [**Tab**](windowsribbon-element-tab.md) element.</span></span>
-   <span data-ttu-id="78eef-166">指派給 [應用程式功能表](windowsribbon-controls-applicationmenu.md)內 [**MenuGroup**](windowsribbon-element-menugroup.md)的 [**按鈕**](windowsribbon-element-button.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)和 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)元素。</span><span class="sxs-lookup"><span data-stu-id="78eef-166">[**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md), and [**DropDownButton**](windowsribbon-element-dropdownbutton.md) elements assigned to a [**MenuGroup**](windowsribbon-element-menugroup.md) within the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="78eef-167">除非裝載于 [[應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中，否則無法將 [**Button**](windowsribbon-element-button.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)和 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)元素指派給模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-167">[**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md), and [**DropDownButton**](windowsribbon-element-dropdownbutton.md) elements cannot be assigned to a mode unless hosted in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

     

<span data-ttu-id="78eef-168">在功能區架構中，這些控制項元素稱為強制回應控制項。</span><span class="sxs-lookup"><span data-stu-id="78eef-168">In the Ribbon framework, these control elements are referred to as modal controls.</span></span> <span data-ttu-id="78eef-169">只有當其系結的模式在 UI 中為作用中時，才會顯示它們。</span><span class="sxs-lookup"><span data-stu-id="78eef-169">They appear only if a mode to which they are bound is active in the UI.</span></span>

<span data-ttu-id="78eef-170">包含在強制回應控制項內的控制項元素，會繼承應用程式模式的行為。</span><span class="sxs-lookup"><span data-stu-id="78eef-170">Control elements that are contained within a modal control inherit the application mode behavior.</span></span> <span data-ttu-id="78eef-171">例如，如果將 [**群組**](windowsribbon-element-group.md) 強制回應控制項指派給 **advanced** 模式，而 [ **advanced** ] 模式不是作用中，則在功能區 UI 中將不會顯示該 **群組** 以及其中的任何控制項（強制回應或其他）。</span><span class="sxs-lookup"><span data-stu-id="78eef-171">For example, if a [**Group**](windowsribbon-element-group.md) modal control is assigned to an **Advanced** mode and the **Advanced** mode is not active, then that **Group** and any controls in it, modal or otherwise, will not be visible in the Ribbon UI.</span></span>

<span data-ttu-id="78eef-172">使用 *ApplicationModes* 屬性時，模式會指派給1： N (一對多) 關聯性中的強制回應控制項，其中單一模式控制項可以與數個模式相關聯。</span><span class="sxs-lookup"><span data-stu-id="78eef-172">With the use of the *ApplicationModes* attribute, modes are assigned to modal controls in a 1:N (one-to-many) relationship, where a single modal control can be associated with several modes.</span></span>

<span data-ttu-id="78eef-173">功能區架構指的是數位的模式，從0到31，而模式0則是在功能區應用程式啟動時自動啟動的預設模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-173">The Ribbon framework refers to modes numerically, from 0 to 31, with mode 0 considered the default mode that is automatically activated when a Ribbon application starts.</span></span> <span data-ttu-id="78eef-174">未指定 *ApplicationModes* 屬性的任何模式控制項都會被視為預設模式的成員。</span><span class="sxs-lookup"><span data-stu-id="78eef-174">Any modal control that does not specify an *ApplicationModes* attribute is considered to be a member of the default mode.</span></span>

<span data-ttu-id="78eef-175">在 RibbonApp 中， **Simple** 是預設模式，只有在使用者啟動時才會顯示 [ **Advanced** mode] 功能。</span><span class="sxs-lookup"><span data-stu-id="78eef-175">In RibbonApp, **Simple** is the default mode, with **Advanced** mode functionality displayed only when it is initiated by the user.</span></span>

<span data-ttu-id="78eef-176">下列範例示範 RibbonApp 所需的標記。</span><span class="sxs-lookup"><span data-stu-id="78eef-176">The following example demonstrates the markup required for RibbonApp.</span></span>


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



<span data-ttu-id="78eef-177">此範例示範下列各項：</span><span class="sxs-lookup"><span data-stu-id="78eef-177">This example demonstrates the following:</span></span>

-   <span data-ttu-id="78eef-178">不需要明確宣告預設模式0。</span><span class="sxs-lookup"><span data-stu-id="78eef-178">Default mode 0 does not need to be explicitly declared.</span></span> <span data-ttu-id="78eef-179">因為未指定 *ApplicationModes* 屬性的強制回應控制項會自動系結至) RibbonApp 範例中的模式 0 (**簡單** 模式，所以不需要明確宣告預設強制回應控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="78eef-179">Because modal controls that do not specify the *ApplicationModes* attribute are automatically bound to mode 0 (**Simple** mode in the RibbonApp example), there is no need to explicitly declare the attribute for default modal controls.</span></span>
-   <span data-ttu-id="78eef-180">控制項可以系結至多個模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-180">Controls can be bound to multiple modes.</span></span> <span data-ttu-id="78eef-181">針對 RibbonApp，**簡單** 模式控制項中 *ApplicationModes* 屬性的唯一需求是 `cmdSwitchModes` 按鈕，因為它是 **簡單** 和 **先進** 模式的一部分。</span><span class="sxs-lookup"><span data-stu-id="78eef-181">For RibbonApp, the only need for the *ApplicationModes* attribute in a **Simple** mode control is the `cmdSwitchModes` button , since it is a part of both **Simple** and **Advanced** modes.</span></span> <span data-ttu-id="78eef-182">如果其中一個模式為使用中，此控制項將會出現在 [ [應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中。</span><span class="sxs-lookup"><span data-stu-id="78eef-182">If either mode is active, this control will appear in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="78eef-183">強制回應控制項不會繼承自其父代。</span><span class="sxs-lookup"><span data-stu-id="78eef-183">Modal controls do not inherit from their parents.</span></span> <span data-ttu-id="78eef-184">RibbonApp 的 [ **Advanced** ] 索引標籤包含 **中繼資料** 群組;這兩個模式控制項都指派給模式 1 (**Advanced** 模式) 。</span><span class="sxs-lookup"><span data-stu-id="78eef-184">The **Advanced** tab of RibbonApp contains a **Metadata** group; both of these modal controls are assigned to mode 1 (**Advanced** mode).</span></span> <span data-ttu-id="78eef-185">將 [ **Advanced** ] 索引標籤指派給模式1，並不會自動將子控制項（例如 **中繼資料** 群組）指派給模式1。</span><span class="sxs-lookup"><span data-stu-id="78eef-185">Assigning the **Advanced** tab to mode 1 does not automatically assign child controls, such as the **Metadata** group, to mode 1.</span></span> <span data-ttu-id="78eef-186">這可讓索引標籤內的任何群組在執行時間獨立啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="78eef-186">This allows any group within a tab to be independently enabled or disabled at runtime.</span></span>
-   <span data-ttu-id="78eef-187">非強制回應控制項仍然可以依賴模式切換。</span><span class="sxs-lookup"><span data-stu-id="78eef-187">Non-modal controls can still rely on mode switches.</span></span> <span data-ttu-id="78eef-188">RibbonApp 的 [ **編輯中繼資料** ] 和 [ **檢查錯誤** ] 按鈕是否適用于 advanced users，而且只有在使用者切換至 **advanced** 模式時才可使用。</span><span class="sxs-lookup"><span data-stu-id="78eef-188">The **Edit Metadata** and **Check for Errors** buttons of RibbonApp are for advanced users and available only when the user switches to **Advanced** mode.</span></span> <span data-ttu-id="78eef-189">未裝載在 [應用程式功能表](windowsribbon-controls-applicationmenu.md) 內的按鈕控制項為非強制回應;不過，由於這些按鈕是裝載在 (**中繼資料** 群組) 的強制回應控制項內，因此當群組為可見時，就會顯示這些按鈕。</span><span class="sxs-lookup"><span data-stu-id="78eef-189">Button controls that are not hosted inside the [Application Menu](windowsribbon-controls-applicationmenu.md) are non-modal; however, because these buttons are hosted inside a modal control (the **Metadata** group), they are visible when the group is visible.</span></span> <span data-ttu-id="78eef-190">因此，當啟動 advanced 模式並在功能區 UI 中公開 **中繼資料** 群組時，就會出現這些按鈕。</span><span class="sxs-lookup"><span data-stu-id="78eef-190">Therefore, these buttons appear when the advanced mode is activated and the **Metadata** group is exposed in the Ribbon UI.</span></span>

### <a name="switch-modes-at-runtime"></a><span data-ttu-id="78eef-191">執行時間切換模式</span><span class="sxs-lookup"><span data-stu-id="78eef-191">Switch Modes at Runtime</span></span>

<span data-ttu-id="78eef-192">在標記中定義模式之後，您可以輕鬆地啟用或停用這些模式，以回應內容相關事件。</span><span class="sxs-lookup"><span data-stu-id="78eef-192">After modes are defined in markup, they can be easily enabled or disabled in response to contextual events.</span></span> <span data-ttu-id="78eef-193">如先前所述，功能區應用程式一律會以預設模式0開始。</span><span class="sxs-lookup"><span data-stu-id="78eef-193">As mentioned previously, Ribbon applications always start in the default mode 0.</span></span> <span data-ttu-id="78eef-194">在應用程式初始化且模式0為使用中之後，即可藉由呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) 函式來變更現用模式的集合。</span><span class="sxs-lookup"><span data-stu-id="78eef-194">After the application has initialized and mode 0 is active, the set of active modes can be changed by calling the [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) function.</span></span> <span data-ttu-id="78eef-195">此函式會採用32位整數作為應為作用中之模式的位標記法;最不重要的位代表模式0，而最大的位代表模式31。</span><span class="sxs-lookup"><span data-stu-id="78eef-195">This function takes a 32-bit integer as a bitwise representation of the modes that should be active; the least significant bit represents mode 0 and the most significant bit represents mode 31.</span></span> <span data-ttu-id="78eef-196">如果位設定為零，則在功能區 UI 中不會使用此模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-196">If a bit is set to zero, the mode is not active in the Ribbon UI.</span></span>

<span data-ttu-id="78eef-197">在 RibbonApp 中，當使用者啟用 **advanced** 模式時，Advanced 命令會與簡單的命令一起顯示。</span><span class="sxs-lookup"><span data-stu-id="78eef-197">In RibbonApp, when a user enables **Advanced** mode, the advanced commands are displayed alongside the simple commands.</span></span> <span data-ttu-id="78eef-198">**切換至 [切換至 Advanced 模式]** 按鈕的命令處理常式會呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) ，以將模式 0 (**簡單** 的) 和 1 (**Advanced**) 在 UI 中為作用中。</span><span class="sxs-lookup"><span data-stu-id="78eef-198">The command handler for the **Switch to Advanced Mode** button calls [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) in order to set modes 0 (**Simple**) and 1 (**Advanced**) as active in the UI.</span></span> <span data-ttu-id="78eef-199">下列範例是此函式呼叫的 RibbonApp 程式碼：</span><span class="sxs-lookup"><span data-stu-id="78eef-199">The following example is the RibbonApp code for this function call :</span></span>


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> <span data-ttu-id="78eef-200">功能區架構 UI \_ MAKEAPPMODE 宏可簡化正確設定這些位的工作，以準備呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)。</span><span class="sxs-lookup"><span data-stu-id="78eef-200">The Ribbon framework UI\_MAKEAPPMODE macro simplifies the task of setting these bits correctly in preparation for the call to [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).</span></span>

 

<span data-ttu-id="78eef-201">此範例示範下列各項：</span><span class="sxs-lookup"><span data-stu-id="78eef-201">This example demonstrates the following:</span></span>

-   <span data-ttu-id="78eef-202">使用 UI \_ MAKEAPPMODE 宏來建立模式設定。</span><span class="sxs-lookup"><span data-stu-id="78eef-202">Use the UI\_MAKEAPPMODE macro to build a mode set.</span></span>
-   <span data-ttu-id="78eef-203">模式會以明確且明確的方式設定。</span><span class="sxs-lookup"><span data-stu-id="78eef-203">Modes are set explicitly and atomically.</span></span> <span data-ttu-id="78eef-204">傳遞給 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) 的整數值代表在函式傳回之後將會作用的模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-204">The integer value that is passed to [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) represents the modes that will be active after the function returns.</span></span> <span data-ttu-id="78eef-205">雖然 **簡單** 模式先前為使用中，但 **IUIFramework：： SetModes** 必須指出當啟動 **Advanced** 模式時，**簡單** 模式仍保持作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="78eef-205">Although the **Simple** mode was previously active, **IUIFramework::SetModes** must indicate that the **Simple** mode remain active when the **Advanced** mode is activated.</span></span>
-   <span data-ttu-id="78eef-206">可以移除預設模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-206">The default mode can be removed.</span></span> <span data-ttu-id="78eef-207">雖然在 RibbonApp 中，預設模式 (模式 0) 不會被移除，但您可以使用下列呼叫來移除它： `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` ，只會在 UI 中公開 advanced 命令。</span><span class="sxs-lookup"><span data-stu-id="78eef-207">Although in RibbonApp the default mode (mode 0) is never removed, it can be removed with the following call: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))`, exposing only the advanced commands in the UI.</span></span>

> [!Note]  
> <span data-ttu-id="78eef-208">重新設定應用程式的模式時，功能區會嘗試保留 UI 中先前選取的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="78eef-208">When the modes of an application are reconfigured, the Ribbon will attempt to preserve the previously selected tab in the UI.</span></span> <span data-ttu-id="78eef-209">如果新的一組模式不再包含呼叫之前選取的索引標籤，功能區將會在其配置中選取最接近 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="78eef-209">If the new set of modes no longer contains the tab that was selected before the call, the Ribbon will select the tab in its layout that is closest to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="78eef-210">此索引標籤的目的是要包含與使用者最相關的命令。</span><span class="sxs-lookup"><span data-stu-id="78eef-210">This tab is meant to contain the commands that are most relevant to the user.</span></span> <span data-ttu-id="78eef-211">如需詳細資訊，請參閱 [功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)。</span><span class="sxs-lookup"><span data-stu-id="78eef-211">For more information, see [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="78eef-212">備註</span><span class="sxs-lookup"><span data-stu-id="78eef-212">Remarks</span></span>

<span data-ttu-id="78eef-213">功能區隨時都必須有一個主動模式。</span><span class="sxs-lookup"><span data-stu-id="78eef-213">The Ribbon must have at least one active mode at all times.</span></span> <span data-ttu-id="78eef-214">如果應用程式透過呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) （其模式值為0）來嘗試停用所有模式， \_ 則會傳回 E 失敗，而且主動模式設定會維持不變。</span><span class="sxs-lookup"><span data-stu-id="78eef-214">If an application attempts to deactivate all modes by calling [**IUIFramework::SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) with a mode value of 0, E\_FAIL is returned and the active mode set remains unchanged.</span></span>

<span data-ttu-id="78eef-215">此架構要求功能區 UI 中必須至少有一個索引標籤存在。</span><span class="sxs-lookup"><span data-stu-id="78eef-215">The framework requires that at least one tab exist in the Ribbon UI at all times.</span></span> <span data-ttu-id="78eef-216">如此一來，預設模式至少必須有一個索引標籤 (模式 0) 和每個模式切換之後。</span><span class="sxs-lookup"><span data-stu-id="78eef-216">As a result, there must be at least one tab exposed by the default mode (mode 0) and after each mode switch.</span></span>

<span data-ttu-id="78eef-217">功能區 UI 的所有區域都不會受到應用程式模式的影響。</span><span class="sxs-lookup"><span data-stu-id="78eef-217">Not all areas of the Ribbon UI are affected by application modes.</span></span> <span data-ttu-id="78eef-218">例如，如果停用模式導致從先前新增至 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)的功能區消失按鈕，這些按鈕會保留在快速存取工具列中，讓使用者可以執行系結至按鈕的命令。</span><span class="sxs-lookup"><span data-stu-id="78eef-218">For example, if disabling a mode causes the disappearance of buttons from the Ribbon that were previously added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), those buttons remain in the Quick Access Toolbar, allowing users to execute the Commands bound to the buttons.</span></span> <span data-ttu-id="78eef-219">一般來說，如果某個命令屬於一或多個非使用中的模式，則該命令也應該停用，方法是將 [ [UI \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) ] 屬性設定為 0 (VARIANT \_ FALSE) 。</span><span class="sxs-lookup"><span data-stu-id="78eef-219">As a general rule, if a Command belongs to one or more inactive modes, then that Command should also be disabled by setting the [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) property to 0 (VARIANT\_FALSE) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="78eef-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="78eef-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78eef-221">功能區使用者體驗指導方針</span><span class="sxs-lookup"><span data-stu-id="78eef-221">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="78eef-222">顯示內容索引標籤</span><span class="sxs-lookup"><span data-stu-id="78eef-222">Displaying Contextual Tabs</span></span>](ribbon-contextualtabs.md)
</dt> </dl>

 

 