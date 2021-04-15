---
title: 遷移至 Windows 功能區架構
description: 依賴傳統功能表、工具列和對話方塊的應用程式可以遷移至 Windows 功能區架構命令系統的豐富、動態和內容導向的 UI。
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows 功能區，遷移至
- 功能區，遷移至
- 遷移至 Windows 功能區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463384"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="ece19-106">遷移至 Windows 功能區架構</span><span class="sxs-lookup"><span data-stu-id="ece19-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="ece19-107">依賴傳統功能表、工具列和對話方塊的應用程式可以遷移至 Windows 功能區架構命令系統的豐富、動態和內容導向的 UI。</span><span class="sxs-lookup"><span data-stu-id="ece19-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="ece19-108">這是將應用程式現代化和讓起死回生的簡單且有效的方式，同時也改善了其功能的協助工具、可用性及可探索性。</span><span class="sxs-lookup"><span data-stu-id="ece19-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="ece19-109">簡介</span><span class="sxs-lookup"><span data-stu-id="ece19-109">Introduction</span></span>

<span data-ttu-id="ece19-110">一般情況下，將現有的應用程式遷移至功能區架構包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="ece19-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="ece19-111">設計功能區配置和控制組織來公開現有應用程式的功能，並有足夠的彈性可支援新的功能。</span><span class="sxs-lookup"><span data-stu-id="ece19-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="ece19-112">調整現有應用程式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ece19-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="ece19-113">將現有的應用程式資源遷移 (的字串和影像) 至功能區架構。</span><span class="sxs-lookup"><span data-stu-id="ece19-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="ece19-114">應檢查 [功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx) ，以判斷應用程式是否適合功能區 UI。</span><span class="sxs-lookup"><span data-stu-id="ece19-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="ece19-115">設計功能區版面配置</span><span class="sxs-lookup"><span data-stu-id="ece19-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="ece19-116">您可以藉由執行下列步驟來識別可能的功能區 UI 設計和控制項版面配置：</span><span class="sxs-lookup"><span data-stu-id="ece19-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="ece19-117">取得所有現有功能的清查。</span><span class="sxs-lookup"><span data-stu-id="ece19-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="ece19-118">將此功能轉譯成功能區命令。</span><span class="sxs-lookup"><span data-stu-id="ece19-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="ece19-119">將命令組織成邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="ece19-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="ece19-120">進行清查</span><span class="sxs-lookup"><span data-stu-id="ece19-120">Take Inventory</span></span>

<span data-ttu-id="ece19-121">在功能區架構中，操作工作區或檔之狀態的應用程式所公開的功能會被視為命令。</span><span class="sxs-lookup"><span data-stu-id="ece19-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="ece19-122">什麼構成命令可能會有所不同，並取決於現有應用程式的本質和網域。</span><span class="sxs-lookup"><span data-stu-id="ece19-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="ece19-123">下表列出假設文字編輯應用程式的一組基本命令：</span><span class="sxs-lookup"><span data-stu-id="ece19-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="ece19-124">符號</span><span class="sxs-lookup"><span data-stu-id="ece19-124">Symbol</span></span>           | <span data-ttu-id="ece19-125">ID</span><span class="sxs-lookup"><span data-stu-id="ece19-125">ID</span></span>     | <span data-ttu-id="ece19-126">描述</span><span class="sxs-lookup"><span data-stu-id="ece19-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="ece19-127">新增識別碼檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ece19-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="ece19-128">0xE100</span><span class="sxs-lookup"><span data-stu-id="ece19-128">0xE100</span></span> | <span data-ttu-id="ece19-129">新檔</span><span class="sxs-lookup"><span data-stu-id="ece19-129">New document</span></span>              |
| <span data-ttu-id="ece19-130">儲存識別碼檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ece19-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="ece19-131">0xE103</span><span class="sxs-lookup"><span data-stu-id="ece19-131">0xE103</span></span> | <span data-ttu-id="ece19-132">儲存檔</span><span class="sxs-lookup"><span data-stu-id="ece19-132">Save document</span></span>             |
| <span data-ttu-id="ece19-133">識別碼檔案的 \_ \_ SAVEAS</span><span class="sxs-lookup"><span data-stu-id="ece19-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="ece19-134">0xE104</span><span class="sxs-lookup"><span data-stu-id="ece19-134">0xE104</span></span> | <span data-ttu-id="ece19-135">另存新檔 .。。 (對話方塊) </span><span class="sxs-lookup"><span data-stu-id="ece19-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="ece19-136">識別碼 \_ 檔案 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="ece19-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="ece19-137">0xE101</span><span class="sxs-lookup"><span data-stu-id="ece19-137">0xE101</span></span> | <span data-ttu-id="ece19-138">開啟 ... (] 對話方塊) </span><span class="sxs-lookup"><span data-stu-id="ece19-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="ece19-139">識別碼 \_ 檔案 \_ 結束</span><span class="sxs-lookup"><span data-stu-id="ece19-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="ece19-140">0xE102</span><span class="sxs-lookup"><span data-stu-id="ece19-140">0xE102</span></span> | <span data-ttu-id="ece19-141">結束應用程式</span><span class="sxs-lookup"><span data-stu-id="ece19-141">Exit the application</span></span>      |
| <span data-ttu-id="ece19-142">識別碼 \_ 編輯 \_ 復原</span><span class="sxs-lookup"><span data-stu-id="ece19-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="ece19-143">0xE12B</span><span class="sxs-lookup"><span data-stu-id="ece19-143">0xE12B</span></span> | <span data-ttu-id="ece19-144">復原</span><span class="sxs-lookup"><span data-stu-id="ece19-144">Undo</span></span>                      |
| <span data-ttu-id="ece19-145">識別碼 \_ 編輯 \_ 剪下</span><span class="sxs-lookup"><span data-stu-id="ece19-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="ece19-146">0xE123</span><span class="sxs-lookup"><span data-stu-id="ece19-146">0xE123</span></span> | <span data-ttu-id="ece19-147">剪下選取的文字</span><span class="sxs-lookup"><span data-stu-id="ece19-147">Cut selected text</span></span>         |
| <span data-ttu-id="ece19-148">識別碼 \_ 編輯 \_ 複本</span><span class="sxs-lookup"><span data-stu-id="ece19-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="ece19-149">0xE122</span><span class="sxs-lookup"><span data-stu-id="ece19-149">0xE122</span></span> | <span data-ttu-id="ece19-150">複製選取的文字</span><span class="sxs-lookup"><span data-stu-id="ece19-150">Copy selected text</span></span>        |
| <span data-ttu-id="ece19-151">識別碼 \_ 編輯 \_ 貼上</span><span class="sxs-lookup"><span data-stu-id="ece19-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="ece19-152">0xE125</span><span class="sxs-lookup"><span data-stu-id="ece19-152">0xE125</span></span> | <span data-ttu-id="ece19-153">貼上剪貼簿中的文字</span><span class="sxs-lookup"><span data-stu-id="ece19-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="ece19-154">識別碼 \_ 編輯 \_ 清除</span><span class="sxs-lookup"><span data-stu-id="ece19-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="ece19-155">0xE120</span><span class="sxs-lookup"><span data-stu-id="ece19-155">0xE120</span></span> | <span data-ttu-id="ece19-156">刪除選取的文字</span><span class="sxs-lookup"><span data-stu-id="ece19-156">Delete selected text</span></span>      |
| <span data-ttu-id="ece19-157">識別碼 \_ 視圖 \_ 縮放</span><span class="sxs-lookup"><span data-stu-id="ece19-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="ece19-158">1242</span><span class="sxs-lookup"><span data-stu-id="ece19-158">1242</span></span>   | <span data-ttu-id="ece19-159">縮放 ... (] 對話方塊) </span><span class="sxs-lookup"><span data-stu-id="ece19-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="ece19-160">在建立命令的清查時，查看現有的功能表和工具列。</span><span class="sxs-lookup"><span data-stu-id="ece19-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="ece19-161">請考慮使用者可以與工作區互動的所有方法。</span><span class="sxs-lookup"><span data-stu-id="ece19-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="ece19-162">雖然並非每個命令都適合包含在功能區中，但此練習可能很容易公開先前以 UI 層級遮蔽的命令。</span><span class="sxs-lookup"><span data-stu-id="ece19-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="ece19-163">翻譯</span><span class="sxs-lookup"><span data-stu-id="ece19-163">Translate</span></span>

<span data-ttu-id="ece19-164">並非每個命令都必須在功能區 UI 中表示。</span><span class="sxs-lookup"><span data-stu-id="ece19-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="ece19-165">例如，輸入文字、變更選取範圍、捲軸，或使用滑鼠來移動插入點都符合假設的文字編輯器中的命令，不過，它們不適合在命令列中公開，因為每一個都牽涉到與應用程式 UI 的直接互動。</span><span class="sxs-lookup"><span data-stu-id="ece19-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="ece19-166">相反地，某些功能可能不會被視為傳統上的命令。</span><span class="sxs-lookup"><span data-stu-id="ece19-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="ece19-167">例如，您可以在內容區或 [應用程式模式](ribbon-applicationmodes.md)中，以一組微調控制項的形式呈現印表機頁面邊界調整，而不是隱藏在對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="ece19-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="ece19-168">記下每個命令可能指派的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="ece19-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="ece19-169">某些 UI 架構（例如，Microsoft Foundation class (MFC) ）會定義命令的識別碼，例如 [檔案] 和 [編輯] 功能表， (0xE100 至 0xE200) 。</span><span class="sxs-lookup"><span data-stu-id="ece19-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="ece19-170">組織</span><span class="sxs-lookup"><span data-stu-id="ece19-170">Organize</span></span>

<span data-ttu-id="ece19-171">在嘗試組織命令清查之前，您應該先檢查 [功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx) ，以瞭解執行功能區 UI 時的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="ece19-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="ece19-172">一般情況下，下列規則可套用至功能區命令組織：</span><span class="sxs-lookup"><span data-stu-id="ece19-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="ece19-173">在檔案或整體應用程式上操作的命令，最有可能屬於 [應用程式功能表](windowsribbon-controls-applicationmenu.md)。</span><span class="sxs-lookup"><span data-stu-id="ece19-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="ece19-174">常用) 的命令（例如 [剪下]、[複製] 和 [貼上] (）通常會放在預設的 [首頁] 索引標籤上。在更複雜的應用程式中，它們可能會在功能區 UI 中的其他位置重複。</span><span class="sxs-lookup"><span data-stu-id="ece19-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="ece19-175">重要或經常使用的命令可能會在 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)中包含預設值。</span><span class="sxs-lookup"><span data-stu-id="ece19-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="ece19-176">功能區架構也透過 CoNtextPopup 視圖提供 CoNtextMenu 和浮動工具列控制項。</span><span class="sxs-lookup"><span data-stu-id="ece19-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="ece19-177">這些功能並非強制性的，但如果您的應用程式有一或多個現有的內容功能表，則遷移它們所包含的命令可能會允許重複使用現有的程式碼基底，並自動系結至現有的資源。</span><span class="sxs-lookup"><span data-stu-id="ece19-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="ece19-178">因為每個應用程式都不同，請閱讀指導方針，並嘗試將它們套用到最大限度的範圍。</span><span class="sxs-lookup"><span data-stu-id="ece19-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="ece19-179">功能區架構的其中一個目標是要提供熟悉且一致的使用者體驗，如果新的應用程式設計盡可能地鏡像現有的功能區應用程式，此目標將更能實現。</span><span class="sxs-lookup"><span data-stu-id="ece19-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="ece19-180">調整您的程式碼</span><span class="sxs-lookup"><span data-stu-id="ece19-180">Adapt Your Code</span></span>

<span data-ttu-id="ece19-181">一旦將功能區命令識別和組織成邏輯群組之後，將功能區架構併入現有的應用程式程式碼時所牽涉到的步驟數目，將視原始應用程式的複雜度而定。</span><span class="sxs-lookup"><span data-stu-id="ece19-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="ece19-182">一般而言，有三個基本步驟：</span><span class="sxs-lookup"><span data-stu-id="ece19-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="ece19-183">根據命令組織和版面配置規格來建立功能區標記。</span><span class="sxs-lookup"><span data-stu-id="ece19-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="ece19-184">以功能區功能取代舊版功能表和工具列功能。</span><span class="sxs-lookup"><span data-stu-id="ece19-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="ece19-185">執行 IUICommandHandler 介面卡。</span><span class="sxs-lookup"><span data-stu-id="ece19-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="ece19-186">建立標記</span><span class="sxs-lookup"><span data-stu-id="ece19-186">Create The Markup</span></span>

<span data-ttu-id="ece19-187">命令清單以及其組織和配置是透過功能 [區標記編譯器](windowsribbon-intentcl.md)所使用的功能區標記檔案來宣告。</span><span class="sxs-lookup"><span data-stu-id="ece19-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="ece19-188">調整現有應用程式所需的許多步驟，類似于啟動新的功能區應用程式所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="ece19-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="ece19-189">如需詳細資訊，請參閱建立新功能區應用程式逐步解說的 [功能區應用程式](windowsribbon-stepbystep.md) 教學課程。</span><span class="sxs-lookup"><span data-stu-id="ece19-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="ece19-190">功能區標記有兩個主要區段。</span><span class="sxs-lookup"><span data-stu-id="ece19-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="ece19-191">第一個區段是命令的資訊清單和其相關聯的資源， (字串和影像) 。</span><span class="sxs-lookup"><span data-stu-id="ece19-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="ece19-192">第二個區段指定功能區上控制項的結構和位置。</span><span class="sxs-lookup"><span data-stu-id="ece19-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="ece19-193">簡單文字編輯器的標記看起來可能如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ece19-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="ece19-194">本文稍後會討論映射和字串資源。</span><span class="sxs-lookup"><span data-stu-id="ece19-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="ece19-195">為了避免重新定義 UI 架構（例如 MFC）所定義的符號，上述範例會針對每個命令使用稍微不同的符號名稱， (識別碼檔案 \_ \_ NEW 與 ID \_ CMD \_ NEW) 。</span><span class="sxs-lookup"><span data-stu-id="ece19-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="ece19-196">不過，指派給每個命令的數值識別碼必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="ece19-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="ece19-197">若要將標記檔案整合至應用程式，請設定自訂的組建步驟來執行功能區標記編譯器，UICC.exe。</span><span class="sxs-lookup"><span data-stu-id="ece19-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="ece19-198">接著會將產生的標頭和資源檔合併到現有的專案中。</span><span class="sxs-lookup"><span data-stu-id="ece19-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="ece19-199">如果範例文字編輯器功能區應用程式命名為 "RibbonPad"，則需要類似如下的自訂群組建命令列：</span><span class="sxs-lookup"><span data-stu-id="ece19-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="ece19-200">標記編譯器會建立二進位檔案、標頭 (H) 檔案和資源 (RC) 檔。</span><span class="sxs-lookup"><span data-stu-id="ece19-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="ece19-201">由於現有的應用程式可能有現有的 RC 檔案，因此請在該 RC 檔案中包含產生的 H 和 RC 檔案，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ece19-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="ece19-202">取代舊版功能表和工具列</span><span class="sxs-lookup"><span data-stu-id="ece19-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="ece19-203">使用繼承應用程式中的功能區來取代標準功能表和工具列需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="ece19-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="ece19-204">從應用程式的資源檔中移除工具列和功能表資源參考。</span><span class="sxs-lookup"><span data-stu-id="ece19-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="ece19-205">刪除所有工具列和功能表列初始化程式碼。</span><span class="sxs-lookup"><span data-stu-id="ece19-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="ece19-206">刪除用來將工具列或功能表列附加至應用程式最上層視窗的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="ece19-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="ece19-207">具現化功能區架構。</span><span class="sxs-lookup"><span data-stu-id="ece19-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="ece19-208">將功能區附加至應用程式的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="ece19-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="ece19-209">載入編譯的標記。</span><span class="sxs-lookup"><span data-stu-id="ece19-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ece19-210">您應保留現有的狀態列和鍵盤快速鍵表，因為功能區架構不會取代這些功能。</span><span class="sxs-lookup"><span data-stu-id="ece19-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="ece19-211">下列範例示範如何使用 [**IUIFramework：： initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)初始化架構：</span><span class="sxs-lookup"><span data-stu-id="ece19-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="ece19-212">下列範例示範如何使用 [**IUIFramework：： LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) 載入已編譯的標記：</span><span class="sxs-lookup"><span data-stu-id="ece19-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="ece19-213">上述的 CApplication 類別，必須將一組元件物件模型 (由功能區架構定義的 COM) 介面： [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 和 [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)。</span><span class="sxs-lookup"><span data-stu-id="ece19-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="ece19-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 會提供架構和應用程式之間的主要回呼介面 (例如，功能區的高度會透過 [**IUIApplication：： OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) 進行通訊，而提供個別命令的回呼以回應 [**IUIApplication：： OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)。</span><span class="sxs-lookup"><span data-stu-id="ece19-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="ece19-215">**秘訣：** 某些應用程式架構（例如 MFC）要求在轉譯應用程式的檔空間時，將功能區列的高度列入考慮。</span><span class="sxs-lookup"><span data-stu-id="ece19-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="ece19-216">在這些情況下，加入隱藏視窗以重迭功能區列，並強制檔空間為所需的高度是必要的。</span><span class="sxs-lookup"><span data-stu-id="ece19-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="ece19-217">如需此方法的範例，其中會根據 [**IUIRibbon：： GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) 方法所傳回的功能區高度來呼叫配置函數，請參閱 [HTMLEditRibbon 範例](windowsribbon-htmleditribbonsample.md)。</span><span class="sxs-lookup"><span data-stu-id="ece19-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="ece19-218">下列程式碼範例示範 [**IUIApplication：： OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) 實作為：</span><span class="sxs-lookup"><span data-stu-id="ece19-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="ece19-219">執行 IUICommandHandler 介面卡</span><span class="sxs-lookup"><span data-stu-id="ece19-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="ece19-220">視原始應用程式的設計而定，您可以更輕鬆地使用多個命令處理常式，或叫用現有應用程式命令邏輯的單一橋接命令處理常式。</span><span class="sxs-lookup"><span data-stu-id="ece19-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="ece19-221">許多應用程式都使用 WM \_ 命令訊息來達到這個目的，因為這樣就足以提供單一的全用途命令處理常式，只需將 WM 的 \_ 命令訊息轉寄到最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="ece19-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="ece19-222">不過，這種方法需要特殊的命令處理，例如 **Exit** 或 **Close**。</span><span class="sxs-lookup"><span data-stu-id="ece19-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="ece19-223">因為功能區在處理視窗訊息時無法終結，所以必須 \_ 將 WM 關閉訊息張貼至應用程式的 UI 執行緒，而且不應該以同步方式處理，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ece19-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="ece19-224">正在遷移資源</span><span class="sxs-lookup"><span data-stu-id="ece19-224">Migrating Resources</span></span>

<span data-ttu-id="ece19-225">在定義命令的資訊清單之後，就會宣告功能區的結構，並調整應用程式程式碼以裝載功能區架構，最後一個步驟就是每個命令的字串和影像資源規格。</span><span class="sxs-lookup"><span data-stu-id="ece19-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="ece19-226">字串和影像資源通常會在標記檔案中提供。</span><span class="sxs-lookup"><span data-stu-id="ece19-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="ece19-227">不過，您可以藉由執行 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 回呼方法，以程式設計方式產生或取代它們。</span><span class="sxs-lookup"><span data-stu-id="ece19-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="ece19-228">字串資源</span><span class="sxs-lookup"><span data-stu-id="ece19-228">String Resources</span></span>

<span data-ttu-id="ece19-229">[**LabelTitle**](windowsribbon-element-command-labeltitle.md) 是針對命令所定義最常見的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="ece19-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="ece19-230">這些會轉譯為索引標籤、群組和個別控制項的文字標籤。</span><span class="sxs-lookup"><span data-stu-id="ece19-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="ece19-231">舊版功能表項目中的標籤字串通常可以重複使用於 **LabelTitle** ，而不需要太多編輯。</span><span class="sxs-lookup"><span data-stu-id="ece19-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="ece19-232">但是，下列慣例在功能區的出現時已經變更：</span><span class="sxs-lookup"><span data-stu-id="ece19-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="ece19-233">您不再需要省略號 ( ... ) 尾碼（用來指出對話方塊啟動命令）。</span><span class="sxs-lookup"><span data-stu-id="ece19-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="ece19-234">[& 符號 (&]) 仍可用來指出出現在功能表中之命令的鍵盤快速鍵，但架構所支援的 [**命令提示**](windowsribbon-element-command-keytip.md) 字元屬性滿足類似的目的。</span><span class="sxs-lookup"><span data-stu-id="ece19-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="ece19-235">回頭參考文字編輯器範例，可以指定下列 LabelTitle 和快速鍵的字串：</span><span class="sxs-lookup"><span data-stu-id="ece19-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="ece19-236">符號</span><span class="sxs-lookup"><span data-stu-id="ece19-236">Symbol</span></span>           | <span data-ttu-id="ece19-237">原始字串</span><span class="sxs-lookup"><span data-stu-id="ece19-237">Original string</span></span> | <span data-ttu-id="ece19-238">LabelTitle 字串</span><span class="sxs-lookup"><span data-stu-id="ece19-238">LabelTitle string</span></span> | <span data-ttu-id="ece19-239">Keytip 字串</span><span class="sxs-lookup"><span data-stu-id="ece19-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="ece19-240">新增識別碼檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ece19-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="ece19-241">&新的</span><span class="sxs-lookup"><span data-stu-id="ece19-241">&New</span></span>            | <span data-ttu-id="ece19-242">&新的</span><span class="sxs-lookup"><span data-stu-id="ece19-242">&New</span></span>              | <span data-ttu-id="ece19-243">N</span><span class="sxs-lookup"><span data-stu-id="ece19-243">N</span></span>             |
| <span data-ttu-id="ece19-244">儲存識別碼檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ece19-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="ece19-245">&儲存</span><span class="sxs-lookup"><span data-stu-id="ece19-245">&Save</span></span>           | <span data-ttu-id="ece19-246">&儲存</span><span class="sxs-lookup"><span data-stu-id="ece19-246">&Save</span></span>             | <span data-ttu-id="ece19-247">S</span><span class="sxs-lookup"><span data-stu-id="ece19-247">S</span></span>             |
| <span data-ttu-id="ece19-248">識別碼檔案的 \_ \_ SAVEAS</span><span class="sxs-lookup"><span data-stu-id="ece19-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="ece19-249">將 &另存為 .。。</span><span class="sxs-lookup"><span data-stu-id="ece19-249">Save &As…</span></span>       | <span data-ttu-id="ece19-250">將 &另存為</span><span class="sxs-lookup"><span data-stu-id="ece19-250">Save &as</span></span>          | <span data-ttu-id="ece19-251">A</span><span class="sxs-lookup"><span data-stu-id="ece19-251">A</span></span>             |
| <span data-ttu-id="ece19-252">識別碼 \_ 檔案 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="ece19-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="ece19-253">&開啟 .。。</span><span class="sxs-lookup"><span data-stu-id="ece19-253">&Open…</span></span>          | <span data-ttu-id="ece19-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="ece19-254">&Open</span></span>             | <span data-ttu-id="ece19-255">O</span><span class="sxs-lookup"><span data-stu-id="ece19-255">O</span></span>             |
| <span data-ttu-id="ece19-256">識別碼 \_ 檔案 \_ 結束</span><span class="sxs-lookup"><span data-stu-id="ece19-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="ece19-257">結束(&X)</span><span class="sxs-lookup"><span data-stu-id="ece19-257">E&xit</span></span>           | <span data-ttu-id="ece19-258">結束(&X)</span><span class="sxs-lookup"><span data-stu-id="ece19-258">E&xit</span></span>             | <span data-ttu-id="ece19-259">X</span><span class="sxs-lookup"><span data-stu-id="ece19-259">X</span></span>             |
| <span data-ttu-id="ece19-260">識別碼 \_ 編輯 \_ 復原</span><span class="sxs-lookup"><span data-stu-id="ece19-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="ece19-261">&復原</span><span class="sxs-lookup"><span data-stu-id="ece19-261">&Undo</span></span>           | <span data-ttu-id="ece19-262">復原</span><span class="sxs-lookup"><span data-stu-id="ece19-262">Undo</span></span>              | <span data-ttu-id="ece19-263">Z</span><span class="sxs-lookup"><span data-stu-id="ece19-263">Z</span></span>             |
| <span data-ttu-id="ece19-264">識別碼 \_ 編輯 \_ 剪下</span><span class="sxs-lookup"><span data-stu-id="ece19-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="ece19-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="ece19-265">Cu&t</span></span>            | <span data-ttu-id="ece19-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="ece19-266">Cu&t</span></span>              | <span data-ttu-id="ece19-267">X</span><span class="sxs-lookup"><span data-stu-id="ece19-267">X</span></span>             |
| <span data-ttu-id="ece19-268">識別碼 \_ 編輯 \_ 複本</span><span class="sxs-lookup"><span data-stu-id="ece19-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="ece19-269">&複製</span><span class="sxs-lookup"><span data-stu-id="ece19-269">&Copy</span></span>           | <span data-ttu-id="ece19-270">&複製</span><span class="sxs-lookup"><span data-stu-id="ece19-270">&Copy</span></span>             | <span data-ttu-id="ece19-271">C</span><span class="sxs-lookup"><span data-stu-id="ece19-271">C</span></span>             |
| <span data-ttu-id="ece19-272">識別碼 \_ 編輯 \_ 貼上</span><span class="sxs-lookup"><span data-stu-id="ece19-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="ece19-273">&貼上</span><span class="sxs-lookup"><span data-stu-id="ece19-273">&Paste</span></span>          | <span data-ttu-id="ece19-274">&貼上</span><span class="sxs-lookup"><span data-stu-id="ece19-274">&Paste</span></span>            | <span data-ttu-id="ece19-275">V</span><span class="sxs-lookup"><span data-stu-id="ece19-275">V</span></span>             |
| <span data-ttu-id="ece19-276">識別碼 \_ 編輯 \_ 清除</span><span class="sxs-lookup"><span data-stu-id="ece19-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="ece19-277">&刪除</span><span class="sxs-lookup"><span data-stu-id="ece19-277">&Delete</span></span>         | <span data-ttu-id="ece19-278">&刪除</span><span class="sxs-lookup"><span data-stu-id="ece19-278">&Delete</span></span>           | <span data-ttu-id="ece19-279">D</span><span class="sxs-lookup"><span data-stu-id="ece19-279">D</span></span>             |
| <span data-ttu-id="ece19-280">識別碼 \_ 視圖 \_ 縮放</span><span class="sxs-lookup"><span data-stu-id="ece19-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="ece19-281">&縮放 .。。</span><span class="sxs-lookup"><span data-stu-id="ece19-281">&Zoom…</span></span>          | <span data-ttu-id="ece19-282">Zoom</span><span class="sxs-lookup"><span data-stu-id="ece19-282">Zoom</span></span>              | <span data-ttu-id="ece19-283">Z</span><span class="sxs-lookup"><span data-stu-id="ece19-283">Z</span></span>             |



 

<span data-ttu-id="ece19-284">以下是應該在大部分命令上設定的其他字串屬性清單：</span><span class="sxs-lookup"><span data-stu-id="ece19-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="ece19-285">**LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="ece19-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="ece19-286">**TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="ece19-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="ece19-287">**TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="ece19-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="ece19-288">您現在可以使用指定的所有字串和影像資源來宣告索引標籤、群組和其他功能區 UI 功能。</span><span class="sxs-lookup"><span data-stu-id="ece19-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="ece19-289">下列功能區標記範例示範各種字串資源：</span><span class="sxs-lookup"><span data-stu-id="ece19-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="ece19-290">影像資源</span><span class="sxs-lookup"><span data-stu-id="ece19-290">Image Resources</span></span>

<span data-ttu-id="ece19-291">功能區架構支援影像格式，可提供比上一個功能表和工具列元件所支援的影像格式更豐富的外觀和風格。</span><span class="sxs-lookup"><span data-stu-id="ece19-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="ece19-292">針對 Windows 8 和更新版本，功能區架構支援下列圖形格式：32位 ARGB 點陣圖 (BMP) 檔和可移植網狀圖形 (PNG) 具有透明度的檔。</span><span class="sxs-lookup"><span data-stu-id="ece19-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="ece19-293">針對 Windows 7 及更早版本，映射資源必須符合 Windows 中所使用的標準 BMP 圖形格式。</span><span class="sxs-lookup"><span data-stu-id="ece19-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="ece19-294">現有的影像檔案可以轉換成任何格式。</span><span class="sxs-lookup"><span data-stu-id="ece19-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="ece19-295">但是，如果影像檔案不支援消除鋸齒和透明度，結果可能會小於滿意。</span><span class="sxs-lookup"><span data-stu-id="ece19-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="ece19-296">在功能區架構中，無法指定影像資源的單一預設大小。</span><span class="sxs-lookup"><span data-stu-id="ece19-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="ece19-297">不過，若要 [支援控制項](windowsribbon-templates.md) 的調適型配置，可 (大型和小型) 以兩種大小來指定影像。</span><span class="sxs-lookup"><span data-stu-id="ece19-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="ece19-298">功能區架構中的所有影像都會根據每英寸的點來調整， (DPI) 解析度解析度的顯示，以及與此 DPI 設定相依的精確呈現大小。</span><span class="sxs-lookup"><span data-stu-id="ece19-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="ece19-299">如需詳細資訊，請參閱 [指定功能區影像資源](windowsribbon-imageformats.md) 。</span><span class="sxs-lookup"><span data-stu-id="ece19-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="ece19-300">下列範例示範如何在標記中參考一組 DPI 特定的影像：</span><span class="sxs-lookup"><span data-stu-id="ece19-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="ece19-301">相關主題</span><span class="sxs-lookup"><span data-stu-id="ece19-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ece19-302">指定功能區影像資源</span><span class="sxs-lookup"><span data-stu-id="ece19-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 