---
title: Windows 功能區架構簡介
description: 查看 Windows 功能區架構的登陸頁面，這是傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的替代方案。
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，關於
- 功能區，關於
- Windows 功能區，元件
- 功能區、元件
- Windows 功能區，views
- 功能區、視圖
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，Api
- 功能區，Api
- Windows 功能區，安全性
- 功能區，安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db15165b91708a85e5ae6237b66a15bf733e80a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404391"
---
# <a name="introducing-the-windows-ribbon-framework"></a><span data-ttu-id="8636b-117">Windows 功能區架構簡介</span><span class="sxs-lookup"><span data-stu-id="8636b-117">Introducing the Windows Ribbon Framework</span></span>

<span data-ttu-id="8636b-118">Windows 功能區架構是一種豐富的命令呈現系統，提供了傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。</span><span class="sxs-lookup"><span data-stu-id="8636b-118">The Windows Ribbon framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

-   [<span data-ttu-id="8636b-119">新的命令範例</span><span class="sxs-lookup"><span data-stu-id="8636b-119">A New Command Paradigm</span></span>](#a-new-command-paradigm)
-   [<span data-ttu-id="8636b-120">檢視</span><span class="sxs-lookup"><span data-stu-id="8636b-120">Views</span></span>](#views)
    -   [<span data-ttu-id="8636b-121">功能區視圖</span><span class="sxs-lookup"><span data-stu-id="8636b-121">The Ribbon View</span></span>](#the-ribbon-view)
    -   [<span data-ttu-id="8636b-122">CoNtextPopup 視圖</span><span class="sxs-lookup"><span data-stu-id="8636b-122">The ContextPopup View</span></span>](#the-contextpopup-view)
-   [<span data-ttu-id="8636b-123">功能區架構</span><span class="sxs-lookup"><span data-stu-id="8636b-123">Ribbon Architecture</span></span>](#ribbon-architecture)
    -   [<span data-ttu-id="8636b-124">功能區 Api</span><span class="sxs-lookup"><span data-stu-id="8636b-124">The Ribbon APIs</span></span>](#the-ribbon-apis)
    -   [<span data-ttu-id="8636b-125">安全性和隱私權</span><span class="sxs-lookup"><span data-stu-id="8636b-125">Security and Privacy</span></span>](#security-and-privacy)
    -   [<span data-ttu-id="8636b-126">存取範圍和當地語系化</span><span class="sxs-lookup"><span data-stu-id="8636b-126">Accessibility and Localization</span></span>](#accessibility-and-localization)
-   [<span data-ttu-id="8636b-127">結論</span><span class="sxs-lookup"><span data-stu-id="8636b-127">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="8636b-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="8636b-128">Related topics</span></span>](#related-topics)

## <a name="a-new-command-paradigm"></a><span data-ttu-id="8636b-129">新的命令範例</span><span class="sxs-lookup"><span data-stu-id="8636b-129">A New Command Paradigm</span></span>

<span data-ttu-id="8636b-130">功能區架構是 Microsoft Win32 Api 的集合，可支援 Windows 開發人員的新 UI 功能。</span><span class="sxs-lookup"><span data-stu-id="8636b-130">The Ribbon framework is a collection of Microsoft Win32 APIs that support a host of new UI capabilities for Windows developers.</span></span>

<span data-ttu-id="8636b-131">這種豐富的新式 UI 命令架構提供：</span><span class="sxs-lookup"><span data-stu-id="8636b-131">This rich, modern UI command framework offers:</span></span>

-   <span data-ttu-id="8636b-132">輕鬆地為新的功能區架構應用程式，並直接遷移現有的 Win32 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8636b-132">Easy implementation for brand new Ribbon framework applications and straightforward migration of existing Win32 applications.</span></span>
-   <span data-ttu-id="8636b-133">跨功能區應用程式一致的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="8636b-133">Consistent appearance and behavior across Ribbon applications.</span></span>
-   <span data-ttu-id="8636b-134">遵循適用于透過協助工具標準的第一層 Windows 體驗的 Windows UI 指導方針、視覺化樣式 (主題) 支援、自動高對比調整，以及每英寸的高點 (DPI) 認知。</span><span class="sxs-lookup"><span data-stu-id="8636b-134">Adherence to Windows UI guidelines for a first-class Windows experience through accessibility standards, visual style (theming) support, automatic high contrast adjustments, and high dots per inch (dpi) awareness.</span></span>

<span data-ttu-id="8636b-135">功能區架構是由兩個主要的 UI 元件所組成：</span><span class="sxs-lookup"><span data-stu-id="8636b-135">The Ribbon framework consists of two primary UI components:</span></span>

-   <span data-ttu-id="8636b-136">功能區命令列是由快速存取工具列 (QAT) ，它會公開和醒目顯示使用者或應用程式所指定的各種功能區命令，以及包含應用程式功能表、標準或內容索引標籤的索引標籤列，以及 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="8636b-136">The ribbon command bar, which is composed of the Quick Access Toolbar (QAT) that exposes and highlights various ribbon commands as specified by the user or the application, and a tab row that contains the application menu, standard or contextual tabs, and a help button.</span></span>
-   <span data-ttu-id="8636b-137">豐富的內容功能表系統。</span><span class="sxs-lookup"><span data-stu-id="8636b-137">A rich context menu system.</span></span>

<span data-ttu-id="8636b-138">宣告式 XML 和原生 COM 介面的組合是用來分離這些元件的呈現和功能。</span><span class="sxs-lookup"><span data-stu-id="8636b-138">A combination of declarative XML and native COM interfaces is used to decouple the presentation and functionality of these components.</span></span>

## <a name="views"></a><span data-ttu-id="8636b-139">檢視</span><span class="sxs-lookup"><span data-stu-id="8636b-139">Views</span></span>

<span data-ttu-id="8636b-140">功能區架構、功能區命令列和內容功能表系統的主要 UI 元件，在結構上是透過 *視圖* 來區分。</span><span class="sxs-lookup"><span data-stu-id="8636b-140">The primary UI components of the Ribbon framework, the ribbon command bar and the context menu system, are differentiated structurally through *Views*.</span></span> <span data-ttu-id="8636b-141">架構支援兩種視圖： [**功能區**](windowsribbon-element-ribbon.md) 視圖和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖。</span><span class="sxs-lookup"><span data-stu-id="8636b-141">The framework supports two Views: the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

### <a name="the-ribbon-view"></a><span data-ttu-id="8636b-142">功能區視圖</span><span class="sxs-lookup"><span data-stu-id="8636b-142">The Ribbon View</span></span>

<span data-ttu-id="8636b-143">[**功能區**](windowsribbon-element-ribbon.md)視圖的 UI 是功能區架構的主要功能，並提供在 Windows 應用程式中呈現命令的下一代使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="8636b-143">The UI of the [**Ribbon**](windowsribbon-element-ribbon.md) View is the primary feature of the Ribbon framework and provides the next-generation user experience for presenting commands in Windows applications.</span></span>

<span data-ttu-id="8636b-144">功能區是一個命令列，可透過應用程式視窗頂端的一系列索引標籤，來公開應用程式的主要功能。</span><span class="sxs-lookup"><span data-stu-id="8636b-144">The ribbon is a command bar that exposes the major features of an application through a series of tabs at the top of an application window.</span></span> <span data-ttu-id="8636b-145">它類似于 Microsoft Office 2007 流暢 UI 的功能和外觀。</span><span class="sxs-lookup"><span data-stu-id="8636b-145">It is similar in functionality and appearance to the Microsoft Office 2007 Fluent UI.</span></span> <span data-ttu-id="8636b-146">功能區提供以直覺的對應，說明通常是標準 Windows 功能表系統的命令探索的試驗和錯誤程式。</span><span class="sxs-lookup"><span data-stu-id="8636b-146">The ribbon provides an intuitive counterpoint to the trial-and-error process of command discovery that is typical of standard Windows menu systems.</span></span> <span data-ttu-id="8636b-147">功能區已針對效率和可搜尋性進行優化，可透過標準控制項、資源庫和即時預覽的系統，以最少的滑鼠點擊和按鍵來加速尋找、瞭解及使用命令。</span><span class="sxs-lookup"><span data-stu-id="8636b-147">Optimized for efficiency and discoverability, the ribbon facilitates finding, understanding, and using commands with minimum mouse clicks and keystrokes through a system of standard controls, galleries, and live previewing.</span></span>

<span data-ttu-id="8636b-148">下圖說明適用于 Windows 7 的 Paint 中的功能區架構執行。</span><span class="sxs-lookup"><span data-stu-id="8636b-148">The following image illustrates the Ribbon framework implementation in Paint for Windows 7.</span></span>

![螢幕擷取畫面，顯示 windows 7 的 [油漆] 中的功能區執行。](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a><span data-ttu-id="8636b-150">CoNtextPopup 視圖</span><span class="sxs-lookup"><span data-stu-id="8636b-150">The ContextPopup View</span></span>

<span data-ttu-id="8636b-151">[**CoNtextPopup**](windowsribbon-element-contextpopup.md) View （透過 [內容](windowsribbon-controls-contextpopup.md)快顯控制項）提供的內容功能表系統，比舊版 Windows 應用程式所提供的更豐富。</span><span class="sxs-lookup"><span data-stu-id="8636b-151">The [**ContextPopup**](windowsribbon-element-contextpopup.md) View, through the [Context Popup](windowsribbon-controls-contextpopup.md) control, provides a richer context menu system than is available with earlier Windows applications.</span></span> <span data-ttu-id="8636b-152">您只能部署內容快顯視窗，以支援功能區，功能區架構不支援獨立的內容快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="8636b-152">A Context Popup can only be deployed in support of a ribbon, a standalone Context Popup is not supported by the Ribbon framework.</span></span>

## <a name="ribbon-architecture"></a><span data-ttu-id="8636b-153">功能區架構</span><span class="sxs-lookup"><span data-stu-id="8636b-153">Ribbon Architecture</span></span>

<span data-ttu-id="8636b-154">相較于傳統以控制項為基礎的 Windows UI 開發模型，Windows 功能區架構 UI 開發是以更抽象的命令概念為基礎。</span><span class="sxs-lookup"><span data-stu-id="8636b-154">In contrast to the traditional control-based Windows UI development model, Windows Ribbon framework UI development is based on the more abstract concept of Commands.</span></span> <span data-ttu-id="8636b-155">藉由將焦點放在與控制項相關聯的命令（而不是控制項本身），架構就能夠視需要自動調整 UI，以回應從功能區主機應用程式取出的命令執行狀態。</span><span class="sxs-lookup"><span data-stu-id="8636b-155">By focusing on the Commands that are associated with controls, rather than the controls themselves, the framework is able to automatically adjust the UI as required in response to Command execution state retrieved from the Ribbon host application.</span></span>

<span data-ttu-id="8636b-156">使用功能區架構的應用程式會公開命令，而不會在 UI 中呈現該命令的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8636b-156">An application that uses the Ribbon framework exposes Commands without being encumbered with the details of how that Command is represented in the UI.</span></span> <span data-ttu-id="8636b-157">這有時稱為以意圖為基礎的 UI 模型。</span><span class="sxs-lookup"><span data-stu-id="8636b-157">This is sometimes referred to as an intent-based UI model.</span></span> <span data-ttu-id="8636b-158">[**命令類型**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)、其屬性和其資源會定義應用程式命令的意圖。</span><span class="sxs-lookup"><span data-stu-id="8636b-158">The [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), its properties, and its resources define the intent of the Command for the application.</span></span> <span data-ttu-id="8636b-159">例如，滑鼠輸入、鍵盤輸入或甚至是搖動 gyroscopic 裝置可能會導致執行相同的命令，而應用程式只在意執行命令，而不是叫用該命令的方式。</span><span class="sxs-lookup"><span data-stu-id="8636b-159">For example, mouse input, keyboard input, or even shaking a gyroscopic device can result in the execution of the same Command the application is only concerned with executing the Command, not with how it was invoked.</span></span>

<span data-ttu-id="8636b-160">功能區架構可讓您以兩種不同的開發結構分隔功能，以提供這種彈性： Extensible Application Markup Language (XAML) 型標記語言來宣告控制項和功能區實的視覺化配置，以及 c + + COM 型介面，可在執行時間初始化架構和處理事件。</span><span class="sxs-lookup"><span data-stu-id="8636b-160">The Ribbon framework provides this flexibility by separating functionality from presentation with two distinct development structures: an Extensible Application Markup Language (XAML)-based markup language to declare controls and the visual layout of a Ribbon implementation, and C++ COM-based interfaces to initialize the framework and handle events at run time.</span></span> <span data-ttu-id="8636b-161">這項區別可讓 UI 開發人員和設計人員單獨負責功能區應用程式的外觀，而核心功能仍然是軟體工程師的領域。</span><span class="sxs-lookup"><span data-stu-id="8636b-161">This distinction enables UI developers and designers to be solely responsible for the appearance of a Ribbon application, while core functionality remains the domain of software engineers.</span></span>

<span data-ttu-id="8636b-162">如需詳細資訊，請參閱 [瞭解命令和控制項](windowsribbon-commandscontrols.md)。</span><span class="sxs-lookup"><span data-stu-id="8636b-162">For more information, see [Understanding Commands and Controls](windowsribbon-commandscontrols.md).</span></span>

### <a name="the-ribbon-apis"></a><span data-ttu-id="8636b-163">功能區 Api</span><span class="sxs-lookup"><span data-stu-id="8636b-163">The Ribbon APIs</span></span>

<span data-ttu-id="8636b-164">功能區 Api 會在 View 和功能區主應用程式之間提供必要的連接。</span><span class="sxs-lookup"><span data-stu-id="8636b-164">The Ribbon APIs provide the necessary connections between a View and the Ribbon host application.</span></span> <span data-ttu-id="8636b-165">這些 Api 包含下列介面和屬性索引鍵：</span><span class="sxs-lookup"><span data-stu-id="8636b-165">These APIs consist of the following interfaces and property keys:</span></span>

-   <span data-ttu-id="8636b-166">功能區架構所執行的一組 COM 介面，用來執行 UI 服務。</span><span class="sxs-lookup"><span data-stu-id="8636b-166">A set of COM interfaces implemented by the Ribbon framework to perform UI services.</span></span>

    

    | <span data-ttu-id="8636b-167">介面</span><span class="sxs-lookup"><span data-stu-id="8636b-167">Interface</span></span>                                                                        | <span data-ttu-id="8636b-168">描述</span><span class="sxs-lookup"><span data-stu-id="8636b-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="8636b-169">IUICoNtextualUI\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-169">\*\*\*\*IUIContextualUI\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | <span data-ttu-id="8636b-170">定義 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖核心功能的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-170">Defines the methods for the core functionality of the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [<span data-ttu-id="8636b-171">IUIFramework\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-171">\*\*\*\*IUIFramework\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | <span data-ttu-id="8636b-172">定義支援 [**功能區**](windowsribbon-element-ribbon.md) 和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖核心功能的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-172">Defines the methods that support the core functionality of the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md) Views.</span></span>                                                                                                                                                                                                                                                                                                                                                     |
    | [<span data-ttu-id="8636b-173">IUIRibbon\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-173">\*\*\*\*IUIRibbon\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | <span data-ttu-id="8636b-174">定義用於指定 [**功能區**](windowsribbon-element-ribbon.md) 視圖之設定和屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-174">Defines the methods for specifying settings and properties for a [**Ribbon**](windowsribbon-element-ribbon.md) View.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [<span data-ttu-id="8636b-175">IUISimplePropertySet\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-175">\*\*\*\*IUISimplePropertySet\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | <span data-ttu-id="8636b-176">定義方法，以抓取屬性索引鍵所識別的值。</span><span class="sxs-lookup"><span data-stu-id="8636b-176">Defines a method for retrieving the value identified by a property key.</span></span> <span data-ttu-id="8636b-177">這個介面是由功能區架構所執行，而且也會由主應用程式針對專案資源庫的 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件中的每個專案執行。</span><span class="sxs-lookup"><span data-stu-id="8636b-177">This interface is implemented by the Ribbon framework and is also implemented by the host application for each item in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object of an item gallery.</span></span><br/> <span data-ttu-id="8636b-178">由主應用程式執行時，這個介面所定義的方法會用來在 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)中取得所選取專案的屬性索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="8636b-178">When implemented by the host application, the method defined by this interface is used to retrieve a property key value for the selected item in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span><br/> |
    | [<span data-ttu-id="8636b-179">IUICollection\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-179">\*\*\*\*IUICollection\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | <span data-ttu-id="8636b-180">定義在執行時間動態操作集合型控制項（例如功能區 QAT 和以集合為基礎的資源 [庫](ribbon-controls-galleries.md)）的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-180">Defines the methods for dynamically manipulating collection-based controls, such as the Ribbon QAT and collection-based [galleries](ribbon-controls-galleries.md), at run time.</span></span>                                                                                                                                                                                                                                                                                                                                                        |
    | [<span data-ttu-id="8636b-181">IUIImage\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-181">\*\*\*\*IUIImage\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | <span data-ttu-id="8636b-182">定義用來抓取影像以顯示在功能區 UI 中的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-182">Defines the method for retrieving an image for display in the Ribbon UI.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [<span data-ttu-id="8636b-183">IUIImageFromBitmap\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-183">\*\*\*\*IUIImageFromBitmap\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | <span data-ttu-id="8636b-184">定義用來建立 [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) 物件的 factory 方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-184">Defines the factory method for creating an [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   <span data-ttu-id="8636b-185">功能區主機應用程式所執行的一組 COM 介面，架構會呼叫這些介面來回應 UI 變更。</span><span class="sxs-lookup"><span data-stu-id="8636b-185">A set of COM interfaces implemented by the Ribbon host application that the framework calls in response to UI changes.</span></span>

    

    | <span data-ttu-id="8636b-186">介面</span><span class="sxs-lookup"><span data-stu-id="8636b-186">Interface</span></span>                                                                                  | <span data-ttu-id="8636b-187">描述</span><span class="sxs-lookup"><span data-stu-id="8636b-187">Description</span></span>                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="8636b-188">IUIApplication\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-188">\*\*\*\*IUIApplication\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | <span data-ttu-id="8636b-189">定義功能區架構的應用程式回呼進入點方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-189">Defines the application callback entry-point methods for the Ribbon framework.</span></span>                               |
    | [<span data-ttu-id="8636b-190">IUICommandHandler\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-190">\*\*\*\*IUICommandHandler\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | <span data-ttu-id="8636b-191">定義用來從功能區架構收集命令資訊和處理命令事件的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-191">Defines the methods for gathering Command information and handling Command events from the Ribbon framework.</span></span> |
    | [<span data-ttu-id="8636b-192">IUICollectionChangedEvent\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8636b-192">\*\*\*\*IUICollectionChangedEvent\*\*\*\*</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | <span data-ttu-id="8636b-193">定義在執行時間處理集合變更所需的方法。</span><span class="sxs-lookup"><span data-stu-id="8636b-193">Defines the method required to handle changes to a collection at run time.</span></span>                                   |

    

     

-   <span data-ttu-id="8636b-194">一組屬性索引鍵，定義應用程式以程式設計方式控制的 UI 屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-194">A set of property keys that define which UI properties the application has programmatic control over.</span></span>

    

    | <span data-ttu-id="8636b-195">屬性索引鍵類型</span><span class="sxs-lookup"><span data-stu-id="8636b-195">Property Key Type</span></span>                                                  | <span data-ttu-id="8636b-196">描述</span><span class="sxs-lookup"><span data-stu-id="8636b-196">Description</span></span>                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [<span data-ttu-id="8636b-197">集合</span><span class="sxs-lookup"><span data-stu-id="8636b-197">Collection</span></span>](windowsribbon-reference-properties-collection.md)    | <span data-ttu-id="8636b-198">定義以功能區集合為基礎之控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-198">Defines properties for Ribbon collection-based controls.</span></span> |
    | [<span data-ttu-id="8636b-199">色彩選擇器</span><span class="sxs-lookup"><span data-stu-id="8636b-199">Color Picker</span></span>](windowsribbon-reference-properties-colorpicker.md) | <span data-ttu-id="8636b-200">定義功能區色彩選擇器控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-200">Defines properties for Ribbon color picker controls.</span></span>     |
    | [<span data-ttu-id="8636b-201">字型</span><span class="sxs-lookup"><span data-stu-id="8636b-201">Font</span></span>](windowsribbon-reference-properties-fontcontrol.md)         | <span data-ttu-id="8636b-202">定義功能區 FontControl 的屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-202">Defines properties for the Ribbon FontControl.</span></span>           |
    | [<span data-ttu-id="8636b-203">全球</span><span class="sxs-lookup"><span data-stu-id="8636b-203">Global</span></span>](windowsribbon-reference-properties-framework.md)         | <span data-ttu-id="8636b-204">定義功能區架構的全域屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-204">Defines global properties for the Ribbon framework.</span></span>      |
    | [<span data-ttu-id="8636b-205">Resource</span><span class="sxs-lookup"><span data-stu-id="8636b-205">Resource</span></span>](windowsribbon-reference-properties-resource.md)        | <span data-ttu-id="8636b-206">定義功能區資源屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-206">Defines Ribbon resource properties.</span></span>                      |
    | [<span data-ttu-id="8636b-207">功能區</span><span class="sxs-lookup"><span data-stu-id="8636b-207">Ribbon</span></span>](windowsribbon-reference-properties-ribbon.md)            | <span data-ttu-id="8636b-208">定義功能區視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-208">Defines Ribbon View properties.</span></span>                          |
    | [<span data-ttu-id="8636b-209">State</span><span class="sxs-lookup"><span data-stu-id="8636b-209">State</span></span>](windowsribbon-reference-properties-state.md)              | <span data-ttu-id="8636b-210">定義功能區控制項狀態或內容的屬性。</span><span class="sxs-lookup"><span data-stu-id="8636b-210">Defines properties for Ribbon control state or context.</span></span>  |

    

     

### <a name="security-and-privacy"></a><span data-ttu-id="8636b-211">安全性和隱私權</span><span class="sxs-lookup"><span data-stu-id="8636b-211">Security and Privacy</span></span>

<span data-ttu-id="8636b-212">功能區架構 DLL (uiribbon.dll) 在同進程中執行，而且具有與主應用程式相同的許可權。</span><span class="sxs-lookup"><span data-stu-id="8636b-212">The Ribbon framework DLL (uiribbon.dll) runs in-process and has the same privileges as the host application.</span></span> <span data-ttu-id="8636b-213">功能區只接受主機應用程式做為輸入或使用者輸入（來自嚴格限制的控制項），例如微調和可編輯的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="8636b-213">The Ribbon accepts only what the host application provides as input or user input from tightly constrained controls such as the spinner and editable combo box.</span></span>

<span data-ttu-id="8636b-214">此外，除了由主應用程式提供的資訊之外，架構也不會永久儲存任何資訊，或是由使用者透過「加入宣告 Windows 客戶經驗計畫」所授權) 收集 (。</span><span class="sxs-lookup"><span data-stu-id="8636b-214">In addition, the framework does not permanently store any information except what is provided by the host application or collected (as authorized by the end user) through the opt-in Windows Customer Experience Program.</span></span>

### <a name="accessibility-and-localization"></a><span data-ttu-id="8636b-215">存取範圍和當地語系化</span><span class="sxs-lookup"><span data-stu-id="8636b-215">Accessibility and Localization</span></span>

<span data-ttu-id="8636b-216">功能區架構會執行 Microsoft Active Accessibility，以提供可高度存取的 UI。</span><span class="sxs-lookup"><span data-stu-id="8636b-216">To provide a highly accessible UI, the Ribbon framework implements Microsoft Active Accessibility.</span></span> <span data-ttu-id="8636b-217">架構會自動以有效且有用的資訊來填入相關的 Microsoft Active Accessibility 屬性，以大幅降低開發人員為所有使用者提供內含體驗的負擔。</span><span class="sxs-lookup"><span data-stu-id="8636b-217">By automatically populating relevant Microsoft Active Accessibility properties with valid and helpful information, the framework significantly reduces the burden on developers to provide an inclusive experience for all users.</span></span>

<span data-ttu-id="8636b-218">如需功能區架構中協助工具的詳細資訊，請參閱 [使用 2007 Office 流暢消費者介面中的 Active Accessibility](/previous-versions/office/developer/office-2007/bb404170(v=office.12))。</span><span class="sxs-lookup"><span data-stu-id="8636b-218">For more information on accessibility in the Ribbon framework, see [Working with Active Accessibility in the 2007 Office Fluent User Interface](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).</span></span>

<span data-ttu-id="8636b-219">此外，功能區架構也是 Windows 功能，因此會針對 Windows 支援的所有語言進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="8636b-219">In addition, the Ribbon framework is a Windows feature and, as such, is localized for all languages that Windows supports.</span></span> <span data-ttu-id="8636b-220">不過，開發人員必須負責當地語系化自己的特定應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="8636b-220">Developers, however, are responsible for localizing their own specific application resources.</span></span>

## <a name="conclusion"></a><span data-ttu-id="8636b-221">結論</span><span class="sxs-lookup"><span data-stu-id="8636b-221">Conclusion</span></span>

<span data-ttu-id="8636b-222">功能區是一種全新且吸引人的命令展示，應用程式開發人員、架構設計人員和設計人員在設計和建立新的應用程式或更新現有的應用程式時，應該考慮到。</span><span class="sxs-lookup"><span data-stu-id="8636b-222">The Ribbon is a new and engaging form of command presentation that application developers, architects, and designers should consider when designing and building new applications or updating existing ones.</span></span>

<span data-ttu-id="8636b-223">[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可討論主題，並詢問與開發執行 Windows 功能區架構的應用程式有關的問題。</span><span class="sxs-lookup"><span data-stu-id="8636b-223">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing applications that implement the Windows Ribbon framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8636b-224">相關主題</span><span class="sxs-lookup"><span data-stu-id="8636b-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8636b-225">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="8636b-225">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="8636b-226">功能區使用者體驗指導方針</span><span class="sxs-lookup"><span data-stu-id="8636b-226">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="8636b-227">功能區設計流程</span><span class="sxs-lookup"><span data-stu-id="8636b-227">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

