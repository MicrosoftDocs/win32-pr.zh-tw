---
title: AccChecker 圖形消費者介面
description: 本主題說明組成 AccChecker GUI 的元素。
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104566857"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="228ea-103">AccChecker 圖形消費者介面</span><span class="sxs-lookup"><span data-stu-id="228ea-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="228ea-104">本主題說明組成 AccChecker GUI 的元素。</span><span class="sxs-lookup"><span data-stu-id="228ea-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="228ea-105">驗證索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="228ea-106">結果索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="228ea-107">MSAA 和 UIA 螢幕讀取器索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="228ea-108">MSAA 和 UIA 樹狀索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="228ea-109">檔案功能表</span><span class="sxs-lookup"><span data-stu-id="228ea-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="228ea-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="228ea-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="228ea-111">驗證索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-111">Verifications Tab</span></span>

<span data-ttu-id="228ea-112">AccChecker 會從 [ **驗證** ] 索引標籤的預設視圖開始：</span><span class="sxs-lookup"><span data-stu-id="228ea-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![顯示 U I 協助工具檢查程式中 [驗證] 索引標籤的螢幕擷取畫面。](images/accchecker-verifications-tab.png)

<span data-ttu-id="228ea-114">[ **驗證** ] 索引標籤包含下列元件。</span><span class="sxs-lookup"><span data-stu-id="228ea-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="228ea-115">**驗證目標選取器** 提供下列選項來選取目標應用程式或控制項。</span><span class="sxs-lookup"><span data-stu-id="228ea-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="228ea-116">從預先填入的下拉式清單中選擇目標。</span><span class="sxs-lookup"><span data-stu-id="228ea-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="228ea-117">此清單包含啟動時所識別的所有最上層 Hwnd。</span><span class="sxs-lookup"><span data-stu-id="228ea-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="228ea-118">根據滑鼠游標的位置選擇 HWND (可選取的控制項會以紅色矩形) 反白顯示。</span><span class="sxs-lookup"><span data-stu-id="228ea-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="228ea-119">此選項可讓您選取具有 HWND 的任何可見物件。</span><span class="sxs-lookup"><span data-stu-id="228ea-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="228ea-120">輸入特定 HWND。</span><span class="sxs-lookup"><span data-stu-id="228ea-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="228ea-121">**驗證常式檢查清單** 提供可選取要針對應用程式或控制項執行之所需驗證常式的能力。</span><span class="sxs-lookup"><span data-stu-id="228ea-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="228ea-122">如需詳細資訊，請參閱驗證常式。</span><span class="sxs-lookup"><span data-stu-id="228ea-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="228ea-123">**錯誤和警告隱藏檔案選取器** [驗證 **結果** ] 索引標籤會產生隱藏專案檔。以滑鼠右鍵按一下錯誤或警告訊息，並從內容功能表中選取 [ **隱藏** ]，就會為該訊息設定旗標。</span><span class="sxs-lookup"><span data-stu-id="228ea-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="228ea-124">如果選取 [隱藏隱藏] 核取方塊，清單中就會顯示 **隱藏的專案** 。</span><span class="sxs-lookup"><span data-stu-id="228ea-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="228ea-125">您可以使用用來隱藏專案的相同內容功能表來非隱藏隱藏的專案。</span><span class="sxs-lookup"><span data-stu-id="228ea-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="228ea-126">隱藏專案檔會以 XML 格式 **儲存，方法是從 [檔案**] 功能表中選取 [**儲存隱藏** 專案]。</span><span class="sxs-lookup"><span data-stu-id="228ea-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="228ea-127">在將隱藏訊息的後續驗證執行上，會使用此檔案。</span><span class="sxs-lookup"><span data-stu-id="228ea-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="228ea-128">若要移除隱藏專案檔，請按一下 [ **清除**]。</span><span class="sxs-lookup"><span data-stu-id="228ea-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="228ea-129">如需特定訊息的詳細資訊，請參閱驗證記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="228ea-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="228ea-130">使用 [檔案] 功能表 **中的 [** **儲存記錄** 檔]，將整個清單儲存為 XML 格式的記錄檔，或儲存為格式化的文字檔。</span><span class="sxs-lookup"><span data-stu-id="228ea-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![反白顯示隱藏內容專案的 [accchecker 結果] 索引標籤](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="228ea-132">下列範例顯示在 Windows 防火牆控制台應用程式上執行 **屬性** 驗證所產生之隱藏專案檔的內容。</span><span class="sxs-lookup"><span data-stu-id="228ea-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="228ea-133">為此範例中的隱藏專案選擇了識別碼為 "ElementHasNoName" 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="228ea-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="228ea-134">**顯示優先順序的結果** 提供下列選項，以依優先順序篩選驗證結果。</span><span class="sxs-lookup"><span data-stu-id="228ea-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="228ea-135">**全部** 包含所有的結果（不論優先順序為何）。</span><span class="sxs-lookup"><span data-stu-id="228ea-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="228ea-136">**僅 P1** 只包含優先順序0和優先順序1的結果。</span><span class="sxs-lookup"><span data-stu-id="228ea-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="228ea-137">**僅 P1 P2** 包含優先順序0到優先順序2結果。</span><span class="sxs-lookup"><span data-stu-id="228ea-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="228ea-138">**執行選取的驗證** 提供啟動驗證程式的 [ **執行驗證** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="228ea-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="228ea-139">當驗證正在執行時，按鈕會變更為 [ **取消驗證** ]，並可用來在目前的驗證完成後停止驗證。</span><span class="sxs-lookup"><span data-stu-id="228ea-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="228ea-140">結果索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-140">Results Tab</span></span>

<span data-ttu-id="228ea-141">[ **結果** ] 索引標籤會在選取的驗證工作完成後填入。</span><span class="sxs-lookup"><span data-stu-id="228ea-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="228ea-142">它是由下列元件所組成。</span><span class="sxs-lookup"><span data-stu-id="228ea-142">It consists of the following components.</span></span>

-   <span data-ttu-id="228ea-143">此清單會顯示選取的驗證工作所產生的錯誤、警告和資訊訊息。</span><span class="sxs-lookup"><span data-stu-id="228ea-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="228ea-144">您可以使用訊息清單上方的核取方塊，依類型篩選顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="228ea-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="228ea-145">驗證目標的訊息詳細資料和螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="228ea-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="228ea-146">從郵寄清單中選取訊息會顯示更多詳細資料，並在 [螢幕擷取畫面] 窗格中反白顯示對應的元素。</span><span class="sxs-lookup"><span data-stu-id="228ea-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="228ea-147">[ **視覺化** ] 按鈕會將 AccChecker 切換至 [ **MSAA 樹** ] 索引標籤。如果在 [ **結果** ] 索引標籤上反白顯示錯誤，則會在 [ **MSAA 樹** ] 索引標籤上反白顯示對應專案。</span><span class="sxs-lookup"><span data-stu-id="228ea-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="228ea-148">以滑鼠右鍵按一下訊息，會顯示具有下列專案的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="228ea-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="228ea-149">**隱藏** 將訊息新增至隱藏清單。</span><span class="sxs-lookup"><span data-stu-id="228ea-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="228ea-150">**複製到剪貼** 簿將訊息詳細資料複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="228ea-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="228ea-151">**視覺化** 將 AccChecker 切換至 [ **MSAA 樹** ] 索引標籤。會反白顯示對應至所選錯誤的專案。</span><span class="sxs-lookup"><span data-stu-id="228ea-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="228ea-152">說明顯示訊息的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="228ea-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="228ea-153">MSAA 和 UIA 螢幕讀取器索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="228ea-154">MSAA 螢幕讀取器和 [UIA 螢幕讀取器] 索引標籤很類似。</span><span class="sxs-lookup"><span data-stu-id="228ea-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="228ea-155">這兩者都會顯示幕幕讀取器在驗證目標的模擬遍歷中遇到的元素文字記錄，不同之處在于它會顯示 MSAA 的執行，另一個則顯示 UIA 實作此實作。</span><span class="sxs-lookup"><span data-stu-id="228ea-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="228ea-156">專案的流覽和記錄方式，就像螢幕讀取器一樣。</span><span class="sxs-lookup"><span data-stu-id="228ea-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="228ea-157">此索引標籤上所顯示的資訊，是確認只會宣告有用和相關資訊的必要資訊。</span><span class="sxs-lookup"><span data-stu-id="228ea-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="228ea-158">例如，可以接受一般發音的控制項名稱，例如「MenuItem 編輯」或「按鈕關閉」。但是，無法接受沒有意義的控制項名稱，例如 "CPNavPanel22" 或 "DefaultValue1"。</span><span class="sxs-lookup"><span data-stu-id="228ea-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="228ea-159">[ **視覺化** ] 按鈕會使 AccChecker 切換至 [ **MSAA 樹狀結構** ] 或 [ **UIA 樹** ] 索引標籤。如果專案在 [ **螢幕閱讀** 程式] 索引標籤上反白顯示，則會在 [ **MSAA 樹狀目錄** ] 或 [ **UIA 樹** ] 索引標籤上反白</span><span class="sxs-lookup"><span data-stu-id="228ea-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="228ea-160">您必須在 [**驗證**] 索引標籤中選取 [**一致性**] 下的 [ **ScreenReader** ] 驗證常式，才能顯示 [ **MSAA 螢幕閱讀程式]** 索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="228ea-161">同樣地，您必須選取 [ **UiaScreenReader** ] 驗證常式，才能顯示 [ **UIA 螢幕閱讀** 程式] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="228ea-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="228ea-162">下列螢幕擷取畫面顯示 [UIA 螢幕閱讀程式] 索引標籤，其中包含 [記事本] 的範例驗證。</span><span class="sxs-lookup"><span data-stu-id="228ea-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![顯示範例驗證結果的 [accchecker 螢幕讀取器] 索引標籤](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="228ea-164">MSAA 和 UIA 樹狀索引標籤</span><span class="sxs-lookup"><span data-stu-id="228ea-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="228ea-165">執行任何驗證常式都會使 AccChecker 編譯驗證目標中所有可見的元素，並以階層方式顯示在 [ **MSAA 樹** ] 索引標籤和 [ **UIA 樹** ] 索引標籤上。下列螢幕擷取畫面顯示 [MSAA 樹] 索引標籤與 [記事本] 的元素階層。</span><span class="sxs-lookup"><span data-stu-id="228ea-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![accchecker msaa 樹狀結構索引標籤](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="228ea-167">檔案功能表</span><span class="sxs-lookup"><span data-stu-id="228ea-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="228ea-168">功能表</span><span class="sxs-lookup"><span data-stu-id="228ea-168">Menu</span></span></th>
<th><span data-ttu-id="228ea-169">命令</span><span class="sxs-lookup"><span data-stu-id="228ea-169">Command</span></span></th>
<th><span data-ttu-id="228ea-170">描述</span><span class="sxs-lookup"><span data-stu-id="228ea-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="228ea-171"><strong>File</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="228ea-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="228ea-172"><strong>開啟</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="228ea-173">提供下列選項。</span><span class="sxs-lookup"><span data-stu-id="228ea-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="228ea-174"><strong>驗證 DLL</strong> 開啟驗證 DLL。</span><span class="sxs-lookup"><span data-stu-id="228ea-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="228ea-175">原生 AccChecker 驗證會封裝在獨立 DLL (VerificationRoutines.dll) 中。</span><span class="sxs-lookup"><span data-stu-id="228ea-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="228ea-176">這項設計可讓測試小組根據所測試的 UI 平臺來建立自己的一組驗證。</span><span class="sxs-lookup"><span data-stu-id="228ea-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="228ea-177"><strong>記錄</strong> 檔可讓您選擇要開啟的驗證記錄檔。</span><span class="sxs-lookup"><span data-stu-id="228ea-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="228ea-178"><strong>自動載入可用的驗證</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="228ea-179">自動載入所有可用的 AccChecker 驗證。</span><span class="sxs-lookup"><span data-stu-id="228ea-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="228ea-180"><strong>儲存記錄檔</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="228ea-181">將驗證記錄檔儲存為 XML 或純文字。</span><span class="sxs-lookup"><span data-stu-id="228ea-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="228ea-182">純文字較容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="228ea-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="228ea-183"><strong>儲存隱藏專案</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="228ea-184">將隱藏專案記錄儲存為 XML。</span><span class="sxs-lookup"><span data-stu-id="228ea-184">Save the suppression log as XML.</span></span> <span data-ttu-id="228ea-185">此檔案會指定要在迴歸測試中忽略的驗證訊息。</span><span class="sxs-lookup"><span data-stu-id="228ea-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="228ea-186"><strong>結束</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="228ea-187">關閉 AccChecker 工具。</span><span class="sxs-lookup"><span data-stu-id="228ea-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="228ea-188"><strong>驗證</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="228ea-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="228ea-189"><strong>立即執行</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="228ea-190">依所選驗證目標執行指定的驗證常式。</span><span class="sxs-lookup"><span data-stu-id="228ea-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="228ea-191"><strong>全部啟用</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="228ea-192">檢查所有的驗證常式核取方塊。</span><span class="sxs-lookup"><span data-stu-id="228ea-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="228ea-193"><strong>全部停用</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="228ea-194">取消核取 [所有驗證常式] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="228ea-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="228ea-195"><strong>選項</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="228ea-196"><strong>Always On Top</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="228ea-197">讓 AccChecker 成為迭置順序的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="228ea-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="228ea-198"><strong>Help</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="228ea-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="228ea-199"><strong>說明</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="228ea-200">顯示說明資訊。</span><span class="sxs-lookup"><span data-stu-id="228ea-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="228ea-201"><strong>關於</strong></span><span class="sxs-lookup"><span data-stu-id="228ea-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="228ea-202">顯示 AccChecker 版本和電子郵件地址，以便與 Microsoft 聯絡 AccChecker。</span><span class="sxs-lookup"><span data-stu-id="228ea-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="228ea-203">相關主題</span><span class="sxs-lookup"><span data-stu-id="228ea-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="228ea-204">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="228ea-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





