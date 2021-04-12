---
title: '協助工具工具-AccEvent (可存取的事件監看員) '
description: AccEvent (可存取的事件監看員) 可讓開發人員和測試人員驗證應用程式的 UI 元素是否會在 UI 變更時引發適當的 Microsoft 消費者介面自動化和 Microsoft Active Accessibility 事件。
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e6fa4896c0cfe3155536537099b1c00af8ebe5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376140"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a><span data-ttu-id="7f48a-103">協助工具工具-AccEvent (可存取的事件監看員) </span><span class="sxs-lookup"><span data-stu-id="7f48a-103">Accessibility tools - AccEvent (Accessible Event Watcher)</span></span>

<span data-ttu-id="7f48a-104">**AccEvent (可存取的事件** 監看員) 可讓開發人員和測試人員驗證應用程式的 ui 元素是否會在 ui 變更時引發適當的 Microsoft 消費者介面自動化和 Microsoft Active Accessibility 事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-104">**AccEvent (Accessible Event Watcher)** lets developers and testers to validate that an application's UI elements raise proper Microsoft UI Automation and Microsoft Active Accessibility events when UI changes occur.</span></span> <span data-ttu-id="7f48a-105">當焦點變更時，或叫用、選取或變更狀態或屬性時，就會發生 UI 中的變更。</span><span class="sxs-lookup"><span data-stu-id="7f48a-105">Changes in the UI can occur when focus changes, or when a UI element is invoked, selected, or has a state or property change.</span></span>

<span data-ttu-id="7f48a-106">**AccEvent** 會隨 WINDOWS 軟體開發套件 (SDK) 安裝。</span><span class="sxs-lookup"><span data-stu-id="7f48a-106">**AccEvent** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7f48a-107">它位於 \\ \\ < SDK 安裝路徑的 bin *版本* > \\ < *平臺*> 資料夾 (Accevent.exe) 。</span><span class="sxs-lookup"><span data-stu-id="7f48a-107">It is located in the \\bin\\<*version*>\\<*platform*> folder of the SDK installation path (Accevent.exe).</span></span>

> [!NOTE]
> <span data-ttu-id="7f48a-108">**AccEvent** 是一種舊版工具。</span><span class="sxs-lookup"><span data-stu-id="7f48a-108">**AccEvent** is a legacy tool.</span></span> <span data-ttu-id="7f48a-109">建議您改為使用 [協助工具深入](https://accessibilityinsights.io/) 解析。</span><span class="sxs-lookup"><span data-stu-id="7f48a-109">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f48a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f48a-110">Requirements</span></span>

<span data-ttu-id="7f48a-111">**AccEvent** 可以用來檢查沒有消費者介面自動化的系統上的協助工具資料，其原本是針對 Microsoft Active Accessibility 撰寫。</span><span class="sxs-lookup"><span data-stu-id="7f48a-111">**AccEvent** can be used to examine accessibility data on systems that don't have UI Automation, it was originally written for Microsoft Active Accessibility.</span></span> <span data-ttu-id="7f48a-112">若要檢查消費者介面自動化，消費者介面自動化必須存在於系統上。</span><span class="sxs-lookup"><span data-stu-id="7f48a-112">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="7f48a-113">如需詳細資訊，請參閱 [消費者介面自動化](entry-uiauto-win32.md)的「需求」一節。</span><span class="sxs-lookup"><span data-stu-id="7f48a-113">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="7f48a-114">**AccEvent** 會安裝為 Windows SDK 的整體工具組的一部分，而不是以個別的 exe 下載方式來散發。</span><span class="sxs-lookup"><span data-stu-id="7f48a-114">**AccEvent** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="7f48a-115">Windows SDK 包含本節中記載的所有協助工具相關工具。</span><span class="sxs-lookup"><span data-stu-id="7f48a-115">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="7f48a-116">取得 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="7f48a-116">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="7f48a-117">如果您需要先前的版本， (也有從該頁面連結的 SDK 下載封存。 ) </span><span class="sxs-lookup"><span data-stu-id="7f48a-117">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="7f48a-118">若要執行 **AccEvent**，請在 [ \\ bin \\ < *版本* 平臺>] 資料夾中尋找 AccEvent.exe， > \\ < 然後執行它 (您通常不需要以系統管理員身分執行) 。</span><span class="sxs-lookup"><span data-stu-id="7f48a-118">To run **AccEvent**, find AccEvent.exe in the \\bin\\<*version*>\\<*platform*> folder and run it (you don't typically have to run as administrator).</span></span>

## <a name="the-accessible-event-watcher-window"></a><span data-ttu-id="7f48a-119">可存取的事件監看員視窗</span><span class="sxs-lookup"><span data-stu-id="7f48a-119">The Accessible Event Watcher Window</span></span>

<span data-ttu-id="7f48a-120">當您啟動 **AccEvent** 時，主視窗會隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="7f48a-120">When you launch **AccEvent**, the main window is displayed.</span></span> <span data-ttu-id="7f48a-121">[主要 **AccEvent** ] 視窗會顯示正在執行的應用程式所引發的消費者介面自動化或 Microsoft Active Accessibility 事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-121">The main **AccEvent** window displays the UI Automation or Microsoft Active Accessibility events raised by applications that are running.</span></span> <span data-ttu-id="7f48a-122">主視窗有下列主要部分：</span><span class="sxs-lookup"><span data-stu-id="7f48a-122">The main window has the following major parts:</span></span>

- <span data-ttu-id="7f48a-123">標題列：</span><span class="sxs-lookup"><span data-stu-id="7f48a-123">Title bar.</span></span> <span data-ttu-id="7f48a-124">顯示目前的作業模式和狀態。</span><span class="sxs-lookup"><span data-stu-id="7f48a-124">Displays the current operating mode and state.</span></span>
- <span data-ttu-id="7f48a-125">功能表列：</span><span class="sxs-lookup"><span data-stu-id="7f48a-125">Menu bar.</span></span> <span data-ttu-id="7f48a-126">提供 **AccEvent** 功能的存取權。</span><span class="sxs-lookup"><span data-stu-id="7f48a-126">Provides access to **AccEvent** functionality.</span></span>
- <span data-ttu-id="7f48a-127">資料檢視。</span><span class="sxs-lookup"><span data-stu-id="7f48a-127">Data view.</span></span> <span data-ttu-id="7f48a-128">顯示每個事件的相關資訊，包括事件識別碼和引發事件之 UI 元素的選取屬性。</span><span class="sxs-lookup"><span data-stu-id="7f48a-128">Displays information about each event, including the event ID and selected properties of the UI element that raised the event.</span></span>

<span data-ttu-id="7f48a-129">**AccEvent** 只能有圖形化使用者介面;此工具沒有任何命令列引數，但您可以使用其他工具將輸出記錄檔當作文字來處理。</span><span class="sxs-lookup"><span data-stu-id="7f48a-129">**AccEvent** has a graphical user interface only; there are no command line arguments for this tool, but you could use other tools to process the output log as text.</span></span>

<span data-ttu-id="7f48a-130">下圖顯示主要 **AccEvent** 視窗。</span><span class="sxs-lookup"><span data-stu-id="7f48a-130">The following image shows the main **AccEvent** window.</span></span>

![可存取的事件監看員工具的使用者介面](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a><span data-ttu-id="7f48a-132">可存取的事件監看員工作</span><span class="sxs-lookup"><span data-stu-id="7f48a-132">Accessible Event Watcher Tasks</span></span>

<span data-ttu-id="7f48a-133">本節包含常用 **AccEvent** 工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-133">This section includes information about commonly used **AccEvent** tasks.</span></span>

### <a name="configuring-the-operating-mode"></a><span data-ttu-id="7f48a-134">設定操作模式</span><span class="sxs-lookup"><span data-stu-id="7f48a-134">Configuring the Operating Mode</span></span>

<span data-ttu-id="7f48a-135">您可以使用 [ **模式]** 功能表來設定 **AccEvent** 作業模式，並選取控制工具行為的設定。</span><span class="sxs-lookup"><span data-stu-id="7f48a-135">You use the **Mode** menu to configure the **AccEvent** operating mode and select settings that control the behavior of the tool.</span></span> <span data-ttu-id="7f48a-136">您可以選取下列選項。</span><span class="sxs-lookup"><span data-stu-id="7f48a-136">You can select the following options.</span></span>



| <span data-ttu-id="7f48a-137">選取此選項時</span><span class="sxs-lookup"><span data-stu-id="7f48a-137">When this option is selected</span></span> | <span data-ttu-id="7f48a-138">**AccEvent**</span><span class="sxs-lookup"><span data-stu-id="7f48a-138">**AccEvent** does this</span></span>                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f48a-139">永遠開啟頂端</span><span class="sxs-lookup"><span data-stu-id="7f48a-139">Always on Top</span></span>                | <span data-ttu-id="7f48a-140">顯示在畫面上任何其他使用者介面的上方。</span><span class="sxs-lookup"><span data-stu-id="7f48a-140">Appears on top of any other user interface on the screen.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="7f48a-141">UIA 事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-141">UIA Events</span></span>                   | <span data-ttu-id="7f48a-142">顯示消費者介面自動化事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-142">Displays information about UI Automation events.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="7f48a-143">內容) 中的 WinEvents (</span><span class="sxs-lookup"><span data-stu-id="7f48a-143">WinEvents (In Context)</span></span>       | <span data-ttu-id="7f48a-144">顯示 Microsoft Active Accessibility 事件的相關資訊 (WinEvents) 傳遞給位於伺服器位址空間的攔截函式。</span><span class="sxs-lookup"><span data-stu-id="7f48a-144">Displays information about Microsoft Active Accessibility events (WinEvents) passed to hook functions that reside in the server address space.</span></span> <span data-ttu-id="7f48a-145">如需詳細資訊，請參閱內部內容攔截函 [式](in-context-hook-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="7f48a-145">For more information, see [In-Context Hook Functions](in-context-hook-functions.md).</span></span>         |
| <span data-ttu-id="7f48a-146">WinEvents (出內容) </span><span class="sxs-lookup"><span data-stu-id="7f48a-146">WinEvents (Out of Context)</span></span>   | <span data-ttu-id="7f48a-147">顯示 (WinEvents) 傳遞給位於用戶端位址空間之攔截函式的 Microsoft Active Accessibility 事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-147">Displays information about Microsoft Active Accessibility events (WinEvents) passed to hook functions that reside in the client address space.</span></span> <span data-ttu-id="7f48a-148">如需詳細資訊，請參閱 [跨內容](out-of-context-hook-functions.md)攔截函式。</span><span class="sxs-lookup"><span data-stu-id="7f48a-148">For more information, see [Out-of-Context Hook Functions](out-of-context-hook-functions.md).</span></span> |
| <span data-ttu-id="7f48a-149">顯示反白顯示矩形</span><span class="sxs-lookup"><span data-stu-id="7f48a-149">Show Highlight Rectangle</span></span>     | <span data-ttu-id="7f48a-150">反白顯示引發所選事件之 UI 元素周圍的矩形。</span><span class="sxs-lookup"><span data-stu-id="7f48a-150">Highlights a rectangle around the UI element that raised the selected event.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="7f48a-151">顯示資訊工具提示</span><span class="sxs-lookup"><span data-stu-id="7f48a-151">Show Information Tooltip</span></span>     | <span data-ttu-id="7f48a-152">在工具提示中顯示事件資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-152">Shows event information in a tooltip.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="7f48a-153">設定</span><span class="sxs-lookup"><span data-stu-id="7f48a-153">Settings</span></span>                     | <span data-ttu-id="7f48a-154">顯示 [ **UIA 事件設定** ] 或 [ **new-winevent 設定** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-154">Displays the **UIA Event Settings** or **WinEvent Settings** dialog box.</span></span>                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a><span data-ttu-id="7f48a-155">篩選消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-155">Filtering UI Automation Events</span></span>

<span data-ttu-id="7f48a-156">若要設定 **AccEvent** 視窗中顯示的消費者介面自動化事件和屬性，請按一下 [ **模式]** 功能表，選取 [ **UIA 事件**]，然後選取 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-156">To configure the UI Automation events and properties that are displayed in the **AccEvent** window, click the **Mode** menu, select **UIA Events**, and then select **Settings**.</span></span> <span data-ttu-id="7f48a-157">[ **UIA 事件設定** ] 對話方塊隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="7f48a-157">The **UIA Event Settings** dialog box is displayed.</span></span> <span data-ttu-id="7f48a-158">您也可以使用此對話方塊來篩選事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-158">You can also use this dialog box to filter for events.</span></span>

<span data-ttu-id="7f48a-159">[ **UIA 事件設定** ] 對話方塊包含下列窗格：</span><span class="sxs-lookup"><span data-stu-id="7f48a-159">The **UIA Event Settings** dialog box contains the following panes:</span></span>

- <span data-ttu-id="7f48a-160">**全域活動**</span><span class="sxs-lookup"><span data-stu-id="7f48a-160">**Global Events**</span></span>

    <span data-ttu-id="7f48a-161">選取 [ **FocusChangedEvent** ] 核取方塊，以顯示有關全域焦點變更事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-161">Select the **FocusChangedEvent** check box to display information about global focus-changed events.</span></span>

- <span data-ttu-id="7f48a-162">**事件類型**</span><span class="sxs-lookup"><span data-stu-id="7f48a-162">**Event Type**</span></span>

    <span data-ttu-id="7f48a-163">選取您感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-163">Select the events that you are interested in.</span></span>

- <span data-ttu-id="7f48a-164">**範圍**</span><span class="sxs-lookup"><span data-stu-id="7f48a-164">**Scope**</span></span>

    <span data-ttu-id="7f48a-165">選取您希望 **AccEvent** 接聽事件的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="7f48a-165">Select the UI element that you want **AccEvent** to listen to for events.</span></span>

- <span data-ttu-id="7f48a-166">**包含事件來源**</span><span class="sxs-lookup"><span data-stu-id="7f48a-166">**Include events from**</span></span>

    <span data-ttu-id="7f48a-167">如果您要在 [**領域**] 窗格中選取之 UI 元素的直屬子項目看到事件，請選取 [**直屬子** 系]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-167">Select **Immediate children** if you what to see events from the immediate child elements of the UI element selected in the **Scope** pane.</span></span> <span data-ttu-id="7f48a-168">如果您想要查看所有子系專案的事件，請選取 [ **所有** 子系]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-168">If you want to see events from all descendant elements, select **All Descendants**.</span></span>

- <span data-ttu-id="7f48a-169">**報表屬性**</span><span class="sxs-lookup"><span data-stu-id="7f48a-169">**Report Properties**</span></span>

    <span data-ttu-id="7f48a-170">選取您要在主視窗中的每個事件之後顯示的屬性。</span><span class="sxs-lookup"><span data-stu-id="7f48a-170">Select the properties that you want displayed after each event in the main window.</span></span> <span data-ttu-id="7f48a-171">如果已在 [**模式]** 功能表中選取 [**顯示資訊工具提示**]，則選取的屬性也會顯示在工具提示中。</span><span class="sxs-lookup"><span data-stu-id="7f48a-171">If **Show Information Tooltip** is selected in the **Mode** menu, the selected properties are also displayed in a tooltip.</span></span>

### <a name="filtering-active-accessibility-events"></a><span data-ttu-id="7f48a-172">篩選 Active Accessibility 事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-172">Filtering Active Accessibility Events</span></span>

<span data-ttu-id="7f48a-173">若要設定 [ **AccEvent** ] 視窗中顯示的 Microsoft Active Accessibility 事件和屬性，請按一下 [ **模式]** 功能表，選取 [ **內容) 中** 的 [WinEvents] (或 [WinEvents] **(超出內容)**，然後選取 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-173">To configure the Microsoft Active Accessibility events and properties that are displayed in the **AccEvent** window, click the **Mode** menu, select either **WinEvents (In Context)** or **WinEvents (Out of Context)**, and then select **Settings**.</span></span> <span data-ttu-id="7f48a-174">[ **New-winevent 設定** ] 對話方塊隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="7f48a-174">The **WinEvent Settings** dialog box is displayed.</span></span> <span data-ttu-id="7f48a-175">您也可以使用此對話方塊來篩選事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-175">You can also use this dialog box to filter for events.</span></span>

<span data-ttu-id="7f48a-176">[ **New-winevent 設定** ] 對話方塊包含下列窗格：</span><span class="sxs-lookup"><span data-stu-id="7f48a-176">The **WinEvent Settings** dialog box contains the following panes:</span></span>

- <span data-ttu-id="7f48a-177">**物件**</span><span class="sxs-lookup"><span data-stu-id="7f48a-177">**Objects**</span></span>

    <span data-ttu-id="7f48a-178">選取您希望 **AccEvent** 接聽事件的物件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-178">Select the objects that you want **AccEvent** to listen to for events.</span></span> <span data-ttu-id="7f48a-179">**AccEvent** 可以接聽源自 windows、游標或插入點的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-179">**AccEvent** can listen for events originating from windows, from the cursor, or from the caret.</span></span> <span data-ttu-id="7f48a-180">預設會選取 [**視窗]** 。</span><span class="sxs-lookup"><span data-stu-id="7f48a-180">**Window** is selected by default.</span></span>

- <span data-ttu-id="7f48a-181">**事件**</span><span class="sxs-lookup"><span data-stu-id="7f48a-181">**Events**</span></span>

    <span data-ttu-id="7f48a-182">選取您感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-182">Select the events that you are interested in.</span></span> <span data-ttu-id="7f48a-183">預設會顯示所有事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-183">All events are displayed by default.</span></span>

- <span data-ttu-id="7f48a-184">**事件資訊**</span><span class="sxs-lookup"><span data-stu-id="7f48a-184">**Event Information**</span></span>

    <span data-ttu-id="7f48a-185">選取您要在主視窗中的每個事件名稱之後顯示的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-185">Select the information you want displayed after each event's name in the main window.</span></span>

- <span data-ttu-id="7f48a-186">**物件屬性**</span><span class="sxs-lookup"><span data-stu-id="7f48a-186">**Object Properties**</span></span>

    <span data-ttu-id="7f48a-187">選取您要在主視窗中的每個事件之後顯示的屬性。</span><span class="sxs-lookup"><span data-stu-id="7f48a-187">Select the properties that you want displayed after each event in the main window.</span></span> <span data-ttu-id="7f48a-188">如果已在 [**模式]** 功能表中選取 [**顯示資訊工具提示**]，則選取的屬性也會顯示在工具提示中。</span><span class="sxs-lookup"><span data-stu-id="7f48a-188">If **Show Information Tooltip** is selected in the **Mode** menu, the selected properties are also displayed in a tooltip.</span></span> <span data-ttu-id="7f48a-189">預設會選取 [**名稱**]、[**角色**] 和 [**狀態**]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-189">**Name**, **Role**, and **State** are selected by default.</span></span>

- <span data-ttu-id="7f48a-190">**篩選**</span><span class="sxs-lookup"><span data-stu-id="7f48a-190">**Filtering**</span></span>

    <span data-ttu-id="7f48a-191">在 [篩選] 區段中選取其中一個選項按鈕，以篩選 [ **hwnd** ] 欄位中指定的視窗所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-191">Select one of the radio buttons in the filtering section to filter the events raised by the windows specified in the **hWNDs** field.</span></span> <span data-ttu-id="7f48a-192">預設會選取 [ **不要篩選** ] 選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="7f48a-192">The **Don't filter** radio button is selected by default.</span></span>

    - <span data-ttu-id="7f48a-193">選取 [ **排除** ] 選項按鈕，只顯示從指定視窗以外的物件所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-193">Select the **Exclude** radio button to display only the events raised from objects other than the specified windows.</span></span>
    - <span data-ttu-id="7f48a-194">選取 [ **僅包含** ] 選項按鈕，並指定一或多個視窗控點，只顯示從這些視窗引發的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-194">Select the **Include only** radio button and specify one or more window handles to display only events raised from those windows.</span></span>
    - <span data-ttu-id="7f48a-195">核取 [ **和** 子系] 核取方塊，以包含由指定之視窗的下階所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-195">Check the **and Descendants** check box to include events raised by the descendants of the specified windows.</span></span>

- <span data-ttu-id="7f48a-196">**選項**</span><span class="sxs-lookup"><span data-stu-id="7f48a-196">**Options**</span></span>

    <span data-ttu-id="7f48a-197">接著，選取下列任何一個選項：</span><span class="sxs-lookup"><span data-stu-id="7f48a-197">Select any of the following options:</span></span>

    

    | <span data-ttu-id="7f48a-198">選取此選項時</span><span class="sxs-lookup"><span data-stu-id="7f48a-198">When this option is selected</span></span>                                  | <span data-ttu-id="7f48a-199">**AccEvent**</span><span class="sxs-lookup"><span data-stu-id="7f48a-199">**AccEvent** does this</span></span>                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="7f48a-200">使用 Invoke</span><span class="sxs-lookup"><span data-stu-id="7f48a-200">Use Invoke</span></span>                                                    | <span data-ttu-id="7f48a-201">使用 [IDispatch：： Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 來取出物件屬性，而不是使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f48a-201">Uses [IDispatch::Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) to retrieve object properties instead of using [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods.</span></span>                               |
    | <span data-ttu-id="7f48a-202">即使未選取物件屬性，一律取得物件 () </span><span class="sxs-lookup"><span data-stu-id="7f48a-202">Always Get Object (even if no object properties selected)</span></span>     | <span data-ttu-id="7f48a-203">抓取與事件相關聯的物件，即使在 [物件屬性] 窗格中未選取任何專案。</span><span class="sxs-lookup"><span data-stu-id="7f48a-203">Retrieves the object associated with the event even if no items are selected in the Object Properties pane.</span></span>                                                                                        |
    | <span data-ttu-id="7f48a-204">除了選取的屬性外，還會顯示預設屬性 () </span><span class="sxs-lookup"><span data-stu-id="7f48a-204">Display default property (in addition to selected properties)</span></span> | <span data-ttu-id="7f48a-205">顯示與事件相關聯之物件的預設屬性（如果有的話），以及 [物件屬性] 窗格中所選取的專案。</span><span class="sxs-lookup"><span data-stu-id="7f48a-205">Displays the default property, if any, for the object associated with the event, along with the items selected in the Object Properties pane.</span></span>                                                      |
    | <span data-ttu-id="7f48a-206">顯示隱藏/隱藏視窗的事件資訊</span><span class="sxs-lookup"><span data-stu-id="7f48a-206">Display event information from invisible/hidden windows</span></span>       | <span data-ttu-id="7f48a-207">顯示所有物件的 [事件資訊] 窗格中選取的專案，包括隱藏或隱藏視窗中的專案。</span><span class="sxs-lookup"><span data-stu-id="7f48a-207">Displays the selected items from the Event Information pane for all objects, including those in invisible or hidden windows.</span></span>                                                                       |
    | <span data-ttu-id="7f48a-208">顯示隱藏/隱藏視窗的完整事件資訊</span><span class="sxs-lookup"><span data-stu-id="7f48a-208">Display full event information from invisible/hidden windows</span></span>  | <span data-ttu-id="7f48a-209">從 [事件資訊] 窗格中，顯示選取的專案，以及針對所有物件從 [物件屬性] 窗格中選取的 (或預設) 專案，包括隱藏或隱藏視窗中的物件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-209">Displays the selected items from the Event Information pane, and the selected (or default) items from the Object Properties pane, for all objects, including those in invisible or hidden windows.</span></span> |
    | <span data-ttu-id="7f48a-210">DebugBreak 下一個事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-210">DebugBreak on next event</span></span>                                      | <span data-ttu-id="7f48a-211">導致中斷點例外狀況發生在產生下一個 New-winevent 的進程中。</span><span class="sxs-lookup"><span data-stu-id="7f48a-211">Causes a breakpoint exception to occur in the process that originates the next WinEvent.</span></span> <span data-ttu-id="7f48a-212">這會指示偵錯工具處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7f48a-212">This signals the debugger to handle the exception.</span></span>                                                        |

### <a name="using-the-event-menu"></a><span data-ttu-id="7f48a-213">使用事件功能表</span><span class="sxs-lookup"><span data-stu-id="7f48a-213">Using the Event Menu</span></span>

<span data-ttu-id="7f48a-214">使用 [ **事件** ] 功能表來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="7f48a-214">Use the **Event** menu to perform the following tasks:</span></span>

| <span data-ttu-id="7f48a-215">選取此選項時</span><span class="sxs-lookup"><span data-stu-id="7f48a-215">When this option is selected</span></span> | <span data-ttu-id="7f48a-216">**AccEvent**</span><span class="sxs-lookup"><span data-stu-id="7f48a-216">**AccEvent** does this</span></span>                                    |
|------------------------------|-------------------------------------------------------|
| <span data-ttu-id="7f48a-217">開始接聽</span><span class="sxs-lookup"><span data-stu-id="7f48a-217">Start Listening</span></span>              | <span data-ttu-id="7f48a-218">開始在資料檢視中顯示事件資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-218">Starts displaying event information in the Data view.</span></span> |
| <span data-ttu-id="7f48a-219">停止接聽</span><span class="sxs-lookup"><span data-stu-id="7f48a-219">Stop Listening</span></span>               | <span data-ttu-id="7f48a-220">停止顯示資料檢視中的事件資訊。</span><span class="sxs-lookup"><span data-stu-id="7f48a-220">Stops displaying event information in the Data view.</span></span>  |
| <span data-ttu-id="7f48a-221">清除事件歷程記錄</span><span class="sxs-lookup"><span data-stu-id="7f48a-221">Clear Event History</span></span>          | <span data-ttu-id="7f48a-222">清除資料檢視的內容。</span><span class="sxs-lookup"><span data-stu-id="7f48a-222">Clears the contents of the Data view.</span></span>                 |
| <span data-ttu-id="7f48a-223">選取所有事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-223">Select All Events</span></span>            | <span data-ttu-id="7f48a-224">選取資料檢視中列出的所有事件。</span><span class="sxs-lookup"><span data-stu-id="7f48a-224">Selects all events listed in the Data view.</span></span>           |
| <span data-ttu-id="7f48a-225">複製選取的事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-225">Copy Selected Events</span></span>         | <span data-ttu-id="7f48a-226">將選取的事件複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="7f48a-226">Copies the selected events to the clipboard.</span></span>          |

### <a name="saving-active-accessibility-events"></a><span data-ttu-id="7f48a-227">正在儲存 Active Accessibility 事件</span><span class="sxs-lookup"><span data-stu-id="7f48a-227">Saving Active Accessibility Events</span></span>

<span data-ttu-id="7f48a-228">若要開始將事件儲存至文字檔，請開啟 **[檔案** ] 功能表，然後選取 [ **開始記錄至** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-228">To begin saving events to a text file, open the **File** menu and select **Start Logging to File**.</span></span> <span data-ttu-id="7f48a-229">**AccEvent** 會開始將事件寫入至指定的檔案，直到您 **從 [檔案**] 功能表選取 [**停止記錄**]。</span><span class="sxs-lookup"><span data-stu-id="7f48a-229">**AccEvent** begins writing events to the specified file until you select **Stop Logging** from the **File** menu.</span></span> <span data-ttu-id="7f48a-230">文字檔對於稍後進行疑難排解和檢查事件可能很有用。</span><span class="sxs-lookup"><span data-stu-id="7f48a-230">The text file can be useful for troubleshooting and reviewing the events at a later time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f48a-231">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f48a-231">Related topics</span></span>

- [<span data-ttu-id="7f48a-232">協助工具事件監控程式</span><span class="sxs-lookup"><span data-stu-id="7f48a-232">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="7f48a-233">測試控管</span><span class="sxs-lookup"><span data-stu-id="7f48a-233">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="7f48a-234">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="7f48a-234">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
- [<span data-ttu-id="7f48a-235">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="7f48a-235">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
- [<span data-ttu-id="7f48a-236">使用者介面自動化確認</span><span class="sxs-lookup"><span data-stu-id="7f48a-236">UI Automation Verify</span></span>](ui-automation-verify.md)
- [<span data-ttu-id="7f48a-237">WinEvents</span><span class="sxs-lookup"><span data-stu-id="7f48a-237">WinEvents</span></span>](winevents-infrastructure.md)