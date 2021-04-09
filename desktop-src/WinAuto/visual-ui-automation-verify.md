---
title: Visual 消費者介面自動化驗證
description: Visual 消費者介面自動化確認 (的 Visual UIA 確認) 是 Windows \ 32;UIA 測試程式庫的 GUI 驅動程式，專為手動測試使用者介面自動化所設計。
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675380"
---
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="fd446-103">Visual 消費者介面自動化驗證</span><span class="sxs-lookup"><span data-stu-id="fd446-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="fd446-104">Visual 消費者介面自動化確認 (的 Visual UIA 確認) 是 UIA 測試程式庫的 Windows GUI 驅動程式，專為手動測試使用者介面自動化所設計。</span><span class="sxs-lookup"><span data-stu-id="fd446-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="fd446-105">它提供 UIA 測試程式庫功能的介面，可消除命令列工具的編碼額外負荷。</span><span class="sxs-lookup"><span data-stu-id="fd446-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="fd446-106">功能表命令</span><span class="sxs-lookup"><span data-stu-id="fd446-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="fd446-107">功能窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="fd446-108">自動化元素樹狀結構窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="fd446-109">測試窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="fd446-110">顯示結果窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="fd446-111">屬性窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="fd446-112">Visual UIA Verify 僅支援 UIA Verify XML 記錄器 (WUIALoggerXml.dll) 原生。</span><span class="sxs-lookup"><span data-stu-id="fd446-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="fd446-113">使用者可選取的 XML 轉換會併入 Visual UIA 的 [驗證] 中，以在 **測試結果** 窗格中呈現 XML 記錄器報表的各種不同的觀點。</span><span class="sxs-lookup"><span data-stu-id="fd446-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="fd446-114">根據預設，Visual UIA Verify 會載入隨附于消費者介面自動化原始版本的消費者介面自動化用戶端提供者。</span><span class="sxs-lookup"><span data-stu-id="fd446-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="fd446-115">您可以在 VisualUIVerifyNative.exe 的命令列選項中新增 **/NOCLIENTSIDEPROVIDER** ，以選擇不要載入此提供者。</span><span class="sxs-lookup"><span data-stu-id="fd446-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="fd446-116">下列螢幕擷取畫面顯示 Visual UIA Verify 使用者介面的主要功能區域。</span><span class="sxs-lookup"><span data-stu-id="fd446-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![visual uia 的主要功能區域驗證使用者介面](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="fd446-118">功能表命令</span><span class="sxs-lookup"><span data-stu-id="fd446-118">Menu Commands</span></span>

<span data-ttu-id="fd446-119">下表描述 [Visual UIA 驗證] 功能表中的命令。</span><span class="sxs-lookup"><span data-stu-id="fd446-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd446-120">功能表</span><span class="sxs-lookup"><span data-stu-id="fd446-120">Menu</span></span></th>
<th><span data-ttu-id="fd446-121">命令</span><span class="sxs-lookup"><span data-stu-id="fd446-121">Command</span></span></th>
<th><span data-ttu-id="fd446-122">描述</span><span class="sxs-lookup"><span data-stu-id="fd446-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd446-123"><strong>檔案</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="fd446-124"><strong>結束</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="fd446-125">Exit Visual UIA Verify。</span><span class="sxs-lookup"><span data-stu-id="fd446-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd446-126"><strong>檢視</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="fd446-127"><strong>反白顯示</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="fd446-128">在 [ <strong>自動化元素] 樹狀目錄</strong> 窗格中，反白顯示所選取專案的周框。</span><span class="sxs-lookup"><span data-stu-id="fd446-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="fd446-129">可用選項如下。</span><span class="sxs-lookup"><span data-stu-id="fd446-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="fd446-130"><strong>矩形</strong>—純紅線。</span><span class="sxs-lookup"><span data-stu-id="fd446-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="fd446-131"><strong>淡化矩形</strong>—在幾秒鐘後消失的純紅線。</span><span class="sxs-lookup"><span data-stu-id="fd446-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="fd446-132"><strong>放射線和矩形</strong>—具有額外藍色醒目提示的純紅線，可從周框矩形的每個角落中放射。</span><span class="sxs-lookup"><span data-stu-id="fd446-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="fd446-133"><strong>無</strong>-沒有可見的醒目提示。</span><span class="sxs-lookup"><span data-stu-id="fd446-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fd446-134"><strong>Automation 元素樹狀結構</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fd446-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fd446-135"><strong>重新整理選取的元素</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="fd446-136">重新整理 [ <strong>自動化元素] 樹狀目錄</strong> 窗格中選取之專案的子系。</span><span class="sxs-lookup"><span data-stu-id="fd446-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="fd446-137">專案清單是靜態的，而且不會在元素樹狀結構變更時自動重新整理 () 。</span><span class="sxs-lookup"><span data-stu-id="fd446-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd446-138"><strong>導覽</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="fd446-139">在元素樹狀結構中流覽至下列其中一個專案。</span><span class="sxs-lookup"><span data-stu-id="fd446-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="fd446-140"><strong>父系</strong>：移至父元素。</span><span class="sxs-lookup"><span data-stu-id="fd446-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="fd446-141"><strong>第一個子</strong>系—移至第一個子項目。</span><span class="sxs-lookup"><span data-stu-id="fd446-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="fd446-142"><strong>下一個同級</strong>-移至第一個同級元素。</span><span class="sxs-lookup"><span data-stu-id="fd446-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="fd446-143"><strong>上一個同級</strong>：移至上一個同級元素。</span><span class="sxs-lookup"><span data-stu-id="fd446-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="fd446-144"><strong>最後一個子</strong>系-移至最後一個子項目。</span><span class="sxs-lookup"><span data-stu-id="fd446-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="fd446-145"><strong>Mode</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fd446-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fd446-146"><strong>Always On Top</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="fd446-147">[視覺效果 UIA 驗證] 視窗會保持在桌面 z 順序的頂端。</span><span class="sxs-lookup"><span data-stu-id="fd446-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd446-148"><strong>停留模式 (使用 Ctrl) </strong></span><span class="sxs-lookup"><span data-stu-id="fd446-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="fd446-149">按下 Ctrl 鍵時，會將滑鼠游標下的元素識別為感興趣的元素。</span><span class="sxs-lookup"><span data-stu-id="fd446-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="fd446-150">[ <strong>自動化專案] 樹狀結構</strong> 窗格會重新整理，並反白顯示專案清單中的對應專案。</span><span class="sxs-lookup"><span data-stu-id="fd446-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="fd446-151"><strong>焦點追蹤</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="fd446-152">當焦點變更時，會將具有焦點的專案識別為感興趣的元素。</span><span class="sxs-lookup"><span data-stu-id="fd446-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="fd446-153">[ <strong>自動化專案] 樹狀結構</strong> 窗格會重新整理，並反白顯示專案清單中的對應專案。</span><span class="sxs-lookup"><span data-stu-id="fd446-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="fd446-154"><strong>測試</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fd446-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fd446-155"><strong>左移</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="fd446-156">將一個節點移至 [ <strong>測試</strong> ] 樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="fd446-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd446-157"><strong>向上</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="fd446-158">在 <strong>測試</strong> 樹狀結構中向上移動一個節點。</span><span class="sxs-lookup"><span data-stu-id="fd446-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="fd446-159"><strong>往下移</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="fd446-160">在 <strong>測試</strong> 樹狀結構中向下移動一個節點。</span><span class="sxs-lookup"><span data-stu-id="fd446-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="fd446-161"><strong>移至右方</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="fd446-162">在 [ <strong>測試</strong> ] 樹狀結構中，直接移動一個節點。</span><span class="sxs-lookup"><span data-stu-id="fd446-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="fd446-163"><strong>在選取的元素上執行選取的測試 (s) </strong></span><span class="sxs-lookup"><span data-stu-id="fd446-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="fd446-164">從選取專案上的 [ <strong>測試</strong> ] 樹狀結構執行選取的測試。</span><span class="sxs-lookup"><span data-stu-id="fd446-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="fd446-165"><strong>篩選已知問題</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="fd446-166">篩選來自測試結果的已知消費者介面自動化錯誤。</span><span class="sxs-lookup"><span data-stu-id="fd446-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="fd446-167"><strong>說明</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="fd446-168"><strong>關於 Visual 消費者介面自動化驗證</strong></span><span class="sxs-lookup"><span data-stu-id="fd446-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="fd446-169">顯示 Visual UIA Verify 的軟體版本和著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="fd446-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="fd446-170">功能窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-170">Functional Panes</span></span>

<span data-ttu-id="fd446-171">本章節描述 Visual UIA Verify 使用者介面中的功能窗格。</span><span class="sxs-lookup"><span data-stu-id="fd446-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="fd446-172">自動化元素樹狀結構窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="fd446-173">測試窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="fd446-174">顯示結果窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="fd446-175">屬性窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="fd446-176">自動化元素樹狀結構窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="fd446-177">[ **自動化專案] 樹狀目錄** 窗格包含可供測試之 Automation 元素物件的階層式快照集。</span><span class="sxs-lookup"><span data-stu-id="fd446-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="fd446-178">樹狀結構中的最上層元素代表桌面。</span><span class="sxs-lookup"><span data-stu-id="fd446-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="fd446-179">此視圖是在 Visual UIA Verify 開始時編譯的靜態集合。</span><span class="sxs-lookup"><span data-stu-id="fd446-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="fd446-180">若要重新整理所選節點的視圖，請使用 [重新整理 **選取** 專案] 功能表命令或工具列按鈕。</span><span class="sxs-lookup"><span data-stu-id="fd446-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="fd446-181">下列螢幕擷取畫面顯示 [ **自動化元素] 樹狀結構** 窗格。</span><span class="sxs-lookup"><span data-stu-id="fd446-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![visual uia 的自動化元素樹狀結構窗格確認](images/automation-elements-tree-pane.png)

<span data-ttu-id="fd446-183">[ **自動化元素] 樹狀結構** 中的 [無法使用] () 節點，表示專案是消費者介面自動化原始視圖的成員，但不符合要被視為內容檢視器或控制項視圖成員的條件。</span><span class="sxs-lookup"><span data-stu-id="fd446-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="fd446-184">不過，您仍然可以從 Visual 消費者介面自動化 Verify 測試專案。</span><span class="sxs-lookup"><span data-stu-id="fd446-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="fd446-185">如需詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="fd446-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="fd446-186">可從 [ **自動化元素] 樹狀** 工具列使用的命令包括：</span><span class="sxs-lookup"><span data-stu-id="fd446-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="fd446-187">重新 **整理：重新** 整理選取的節點及其子系。</span><span class="sxs-lookup"><span data-stu-id="fd446-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="fd446-188">除非已選取根節點，否則這個命令不會重新整理整個元素樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="fd446-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="fd446-189">**父 (Ctrl + Shift + F6)**-移至目前節點的父代。</span><span class="sxs-lookup"><span data-stu-id="fd446-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="fd446-190">**第一個子 (Ctrl + Shift + F7)**-移至目前節點的第一個子系。</span><span class="sxs-lookup"><span data-stu-id="fd446-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="fd446-191">**下一個同級 (Ctrl + Shift + F8)**-移至目前節點的下一個同級子系。</span><span class="sxs-lookup"><span data-stu-id="fd446-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="fd446-192">**上一個同級 (Ctrl + Shift + F9)**-移至目前節點的上一個同級。</span><span class="sxs-lookup"><span data-stu-id="fd446-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="fd446-193">**最後一個子 (Ctrl + Shift + F10)**-移至目前節點的最後一個子系。</span><span class="sxs-lookup"><span data-stu-id="fd446-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="fd446-194">**焦點追蹤**：根據焦點追蹤，開啟或關閉節點選取。</span><span class="sxs-lookup"><span data-stu-id="fd446-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="fd446-195">測試窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-195">Tests Pane</span></span>

<span data-ttu-id="fd446-196">[ **測試** ] 窗格包含依測試類型組織 (**Automation 元素**、 **控制項** 和 **模式**) 的消費者介面自動化測試清單，以及 (**組建驗證**、優先順序 **0**、優先順序 **1**、 **優先順序 2** 和 **優先順序 3**) 。</span><span class="sxs-lookup"><span data-stu-id="fd446-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="fd446-197">這份清單是根據 [ **自動化元素] 樹狀目錄** 窗格中選取之專案的控制項類型所產生。</span><span class="sxs-lookup"><span data-stu-id="fd446-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="fd446-198">如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="fd446-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="fd446-199">下列螢幕擷取畫面顯示 [ **測試** ] 窗格。</span><span class="sxs-lookup"><span data-stu-id="fd446-199">The following screen shot shows the **Tests** pane.</span></span>

![測試窗格](images/test-pane.png)

<span data-ttu-id="fd446-201">可從 [ **測試** ] 工具列使用的命令包括：</span><span class="sxs-lookup"><span data-stu-id="fd446-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="fd446-202">**顯示**-指定要顯示的消費者介面自動化測試;也就是說，會顯示所有測試，或只顯示 [ **Automation 元素] 樹狀結構** 中選取之專案的控制項類型所適用的測試 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="fd446-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="fd446-203">**類型**-指定要顯示的測試類型： **Automation 元素**、 **模式** 或 **控制項**。</span><span class="sxs-lookup"><span data-stu-id="fd446-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="fd446-204">**優先順序**：指定要顯示的測試優先順序： **組建驗證**、 **優先順序 0**、 **優先順序 1**、 **優先順序 2** 或 **優先權 3**。</span><span class="sxs-lookup"><span data-stu-id="fd446-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="fd446-205">往 **左**-移至目前節點的父代。</span><span class="sxs-lookup"><span data-stu-id="fd446-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="fd446-206">**上一步-移** 至目前節點的上一個同級。</span><span class="sxs-lookup"><span data-stu-id="fd446-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="fd446-207">**下一步-移** 至目前節點的下一個同級。</span><span class="sxs-lookup"><span data-stu-id="fd446-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="fd446-208">**移** 至目前節點的第一個子系。</span><span class="sxs-lookup"><span data-stu-id="fd446-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="fd446-209">**執行選取的測試 (s)**：在 [ **Automation 元素] 樹狀結構** 中選取的元素上執行測試。</span><span class="sxs-lookup"><span data-stu-id="fd446-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="fd446-210">顯示結果窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-210">Test Results Pane</span></span>

<span data-ttu-id="fd446-211">**測試結果** 窗格包含 Visual UIA 驗證記錄功能。</span><span class="sxs-lookup"><span data-stu-id="fd446-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="fd446-212">下列螢幕擷取畫面顯示 **測試結果** 窗格。</span><span class="sxs-lookup"><span data-stu-id="fd446-212">The following screen shot shows the **Test Results** pane.</span></span>

![測試結果窗格](images/test-results-pane.png)

<span data-ttu-id="fd446-214">可從 [ **測試結果** ] 工具列使用的命令包括：</span><span class="sxs-lookup"><span data-stu-id="fd446-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="fd446-215">**上一頁**：報表查看歷程記錄中的上一頁。</span><span class="sxs-lookup"><span data-stu-id="fd446-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="fd446-216">**向前**：在報表查看歷程記錄中向前復原頁面。</span><span class="sxs-lookup"><span data-stu-id="fd446-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="fd446-217">**整體**：顯示測試結果的摘要， (**通過**、**失敗及未\*\*\*\*預期的錯誤**) 。</span><span class="sxs-lookup"><span data-stu-id="fd446-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="fd446-218">測試結果會連結到 [ **所有結果** ] 視圖。</span><span class="sxs-lookup"><span data-stu-id="fd446-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="fd446-219">**整體** 的命令會顯示如下的表格。</span><span class="sxs-lookup"><span data-stu-id="fd446-219">The **Overall** command displays a table like the following one.</span></span>

    ![整體測試結果資料表](images/overall-test-results.png)

-   <span data-ttu-id="fd446-221">**所有結果**-顯示每個測試結果的詳細記錄，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fd446-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![從所有結果檢視記錄結果詳細資料的範例](images/all-results-log.png)

    <span data-ttu-id="fd446-223">[ **全部結果** ] 資料表中的測試名稱會連結到元素的測試案例描述，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fd446-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![測試案例詳細資料](images/test-case-detail.png)

-   <span data-ttu-id="fd446-225">**完整記錄**：顯示每個測試結果詳細記錄的替代視圖，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="fd446-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![測試案例詳細資料的替代視圖](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="fd446-227">**Xml**：顯示 xml 記錄器所產生的原始 xml。</span><span class="sxs-lookup"><span data-stu-id="fd446-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="fd446-228">**快速尋找**： **測試結果** 窗格中的目前視圖的簡單文字搜尋。</span><span class="sxs-lookup"><span data-stu-id="fd446-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="fd446-229">**在新視窗中開啟**-在 Internet Explorer 的新實例中開啟目前的視圖。</span><span class="sxs-lookup"><span data-stu-id="fd446-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="fd446-230">屬性窗格</span><span class="sxs-lookup"><span data-stu-id="fd446-230">Properties Pane</span></span>

<span data-ttu-id="fd446-231">[ **屬性** ] 窗格包含依屬性類型組織的消費者介面自動化屬性和屬性值的清單： **一般協助工具**、 **識別**、 **模式** (控制項模式) 、 **狀態** 和 **可見度**。</span><span class="sxs-lookup"><span data-stu-id="fd446-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="fd446-232">屬性值會根據 [ **自動化元素] 樹狀目錄** 窗格中選取之物件的控制項類型，動態填入。</span><span class="sxs-lookup"><span data-stu-id="fd446-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="fd446-233">下列螢幕擷取畫面顯示 [ **屬性** ] 窗格。</span><span class="sxs-lookup"><span data-stu-id="fd446-233">The following screen shot shows the **Properties** pane.</span></span>

![屬性窗格](images/properties-pane.png)

<span data-ttu-id="fd446-235">如果選取的控制項支援特定的控制項模式，則 Visual UIA Verify 會提供呼叫該控制項模式所支援之方法的能力。</span><span class="sxs-lookup"><span data-stu-id="fd446-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="fd446-236">例如， [window 控制項類型](uiauto-supportwindowcontroltype.md)支援 [視窗控制項模式](uiauto-implementingwindow.md)，其具有可從 [**屬性**] 窗格中叫用的 [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close)方法，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="fd446-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="fd446-237">如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="fd446-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![從 [屬性] 窗格叫用之視窗控制項模式的關閉方法](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="fd446-239">可從 [ **屬性** ] 工具列使用的命令包括：</span><span class="sxs-lookup"><span data-stu-id="fd446-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="fd446-240">重新 **整理：重新** 整理 [**屬性**] 樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="fd446-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="fd446-241">**全部展開**：展開 **屬性** 樹狀結構中的所有節點。</span><span class="sxs-lookup"><span data-stu-id="fd446-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




