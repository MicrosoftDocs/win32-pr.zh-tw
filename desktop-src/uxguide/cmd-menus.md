---
title: '功能表 (設計基本概念) '
description: 功能表是命令的階層式清單，或可供使用者在目前內容中使用的選項。
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8054a01e4198f3592a34ae09635dd60f392da1eb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195680"
---
# <a name="menus-design-basics"></a><span data-ttu-id="1ead7-103">功能表 (設計基本概念) </span><span class="sxs-lookup"><span data-stu-id="1ead7-103">Menus (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="1ead7-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="1ead7-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="1ead7-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="1ead7-106">功能表是命令的階層式清單，或可供使用者在目前內容中使用的選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-106">Menus are hierarchical lists of commands or options available to users in the current context.</span></span>

<span data-ttu-id="1ead7-107">下拉式功能表是按滑鼠按一下或暫留時，視需要顯示的功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-107">Drop-down menus are menus displayed on demand on mouse click or hover.</span></span> <span data-ttu-id="1ead7-108">它們通常會隱藏在視野之外，因此是節省螢幕空間的有效方式。</span><span class="sxs-lookup"><span data-stu-id="1ead7-108">They are normally hidden from view and therefore are an efficient means of conserving screen space.</span></span> <span data-ttu-id="1ead7-109">子功能表或階層式功能表是從功能表內依需求顯示的次要功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-109">A submenu or cascading menu is a secondary menu displayed on demand from within a menu.</span></span> <span data-ttu-id="1ead7-110">它們是以子功能表標籤結尾的箭號表示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-110">They are indicated by an arrow at the end of the submenu label.</span></span> <span data-ttu-id="1ead7-111">功能表項目是功能表中的個別命令或選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-111">A menu item is an individual command or option within a menu.</span></span>

<span data-ttu-id="1ead7-112">功能表通常會從功能表列顯示，這是標示功能表分類的清單，通常位於視窗頂端附近。</span><span class="sxs-lookup"><span data-stu-id="1ead7-112">Menus are often displayed from a menu bar, which is a list of labeled menu categories typically located near the top of a window.</span></span> <span data-ttu-id="1ead7-113">相反地，當使用者以滑鼠右鍵按一下支援內容功能表的物件或視窗區域時，內容功能表就會下降。</span><span class="sxs-lookup"><span data-stu-id="1ead7-113">By contrast, a context menu drops down when users right-click on an object or window region that supports a context menu.</span></span>

![<span data-ttu-id="1ead7-114">功能表列具有功能表和子功能表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-114">screen shot of menu bar with menu and submenu</span></span> ](images/cmd-menus-image1.png)

<span data-ttu-id="1ead7-115">顯示下拉式功能表和子功能表的一般功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-115">A typical menu bar displaying a drop-down menu and submenu.</span></span>

> [!Note]  
> <span data-ttu-id="1ead7-116">與 [命令按鈕](ctrl-command-buttons.md)、 [工具列](cmd-toolbars.md)和 [鍵盤](inter-keyboard.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="1ead7-116">Guidelines related to [command buttons](ctrl-command-buttons.md), [Toolbars](cmd-toolbars.md), and [keyboard](inter-keyboard.md) are presented in separate articles.</span></span>

 

## <a name="usage-patterns"></a><span data-ttu-id="1ead7-117">使用模式</span><span class="sxs-lookup"><span data-stu-id="1ead7-117">Usage patterns</span></span>

<span data-ttu-id="1ead7-118">功能表有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="1ead7-118">Menus have several usage patterns:</span></span>



|                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ead7-119">**功能表列**</span><span class="sxs-lookup"><span data-stu-id="1ead7-119">**Menu bars**</span></span><br/> <span data-ttu-id="1ead7-120">功能表列會在下拉式功能表中顯示命令和選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-120">a menu bar displays commands and options in drop-down menus.</span></span> <br/>                                               | <span data-ttu-id="1ead7-121">功能表列非常常見且容易尋找，也可以有效率地使用空間。</span><span class="sxs-lookup"><span data-stu-id="1ead7-121">menu bars are very common and easy to find, as well as an efficient use of space.</span></span> <br/> ![<span data-ttu-id="1ead7-122">功能表列的螢幕擷取畫面，其中包含下拉式功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-122">screen shot of menu bar with drop-down menu</span></span> ](images/cmd-menus-image2.png)<br/> <span data-ttu-id="1ead7-123">Windows Mail 的功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-123">A menu bar from Windows Mail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1ead7-124">**工具列功能表**</span><span class="sxs-lookup"><span data-stu-id="1ead7-124">**Toolbar menus**</span></span><br/> <span data-ttu-id="1ead7-125">實作為工具列的功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-125">a menu bar implemented as a toolbar.</span></span> <br/>                                                                   | <span data-ttu-id="1ead7-126">工具列功能表是由 [功能表按鈕](ctrl-command-buttons.md) 和分割按鈕的命令所組成的工具列，如果有的話，則只有幾個直接命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-126">toolbar menus are toolbars consisting primarily of commands in [menu buttons](ctrl-command-buttons.md) and split buttons, with only a few direct commands, if any.</span></span> <br/> <span data-ttu-id="1ead7-127">![具有下拉式功能表之工具列功能表的螢幕擷取畫面 ](images/cmd-menus-image3.png)</span><span class="sxs-lookup"><span data-stu-id="1ead7-127">![screen shot of toolbar menu with drop-down menu ](images/cmd-menus-image3.png)</span></span><br/> <span data-ttu-id="1ead7-128">Windows 影像中心中的工具列功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-128">A toolbar menu in Windows Photo Gallery.</span></span><br/> <span data-ttu-id="1ead7-129">如需此模式的指導方針，請參閱 [工具列](cmd-toolbars.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-129">For guidelines on this pattern, see [Toolbars](cmd-toolbars.md).</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="1ead7-130">**索引標籤功能表**</span><span class="sxs-lookup"><span data-stu-id="1ead7-130">**Tab menus**</span></span><br/> <span data-ttu-id="1ead7-131">索引標籤中的按鈕，顯示與下拉式功能表中索引標籤相關的一組小命令和選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-131">buttons within tabs that display a small set of commands and options related to a tab in a drop-down menu.</span></span> <br/> | <span data-ttu-id="1ead7-132">具有功能表的索引標籤看起來像一般索引標籤，但其底部部分具有具有下拉箭號的按鈕。</span><span class="sxs-lookup"><span data-stu-id="1ead7-132">tabs with menus look like ordinary tabs except their bottom portion has a button with drop-down arrow.</span></span> <span data-ttu-id="1ead7-133">按一下按鈕會顯示下拉式功能表，而不是選取索引標籤。</span><span class="sxs-lookup"><span data-stu-id="1ead7-133">clicking the button displays a drop-down menu instead of selecting the tab.</span></span> <br/> ![<span data-ttu-id="1ead7-134">具有下拉式功能表之索引標籤功能表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-134">screen shot of tab menu with drop-down menu</span></span> ](images/cmd-menus-image4.png)<br/> <span data-ttu-id="1ead7-135">Windows Media Player 中使用 Tab 鍵功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-135">Tab menus are used in Windows Media Player.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1ead7-136">**功能表按鈕**</span><span class="sxs-lookup"><span data-stu-id="1ead7-136">**Menu buttons**</span></span><br/> <span data-ttu-id="1ead7-137">在下拉式功能表中顯示一組小相關命令的命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="1ead7-137">command buttons that display a small set of related commands in a drop-down menu.</span></span> <br/>                       | <span data-ttu-id="1ead7-138">[功能表按鈕](ctrl-command-buttons.md) 看起來像一般的命令按鈕，只不過它們裡面有下拉箭號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-138">[menu buttons](ctrl-command-buttons.md) look like ordinary command buttons except they have a drop-down arrow within them.</span></span> <span data-ttu-id="1ead7-139">按一下按鈕會顯示下拉式功能表，而不是執行命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-139">clicking the button displays a drop-down menu instead of performing a command.</span></span><br/> <span data-ttu-id="1ead7-140">[分割按鈕](ctrl-command-buttons.md) 類似于 [功能表] 按鈕，不同之處在于它們是命令的變化，而按一下按鈕的左邊部分會直接對標籤執行動作。</span><span class="sxs-lookup"><span data-stu-id="1ead7-140">[split buttons](ctrl-command-buttons.md) are similar to menu buttons except that they are variations of a command, and clicking the left portion of the button performs the action on the label directly.</span></span><br/> <span data-ttu-id="1ead7-141">![具有下拉式命令之功能表按鈕的螢幕擷取畫面 ](images/cmd-menus-image5.png)</span><span class="sxs-lookup"><span data-stu-id="1ead7-141">![screen shot of menu button with drop-down commands ](images/cmd-menus-image5.png)</span></span><br/> <span data-ttu-id="1ead7-142">具有一組小相關命令的功能表按鈕。</span><span class="sxs-lookup"><span data-stu-id="1ead7-142">A menu button with a small set of related commands.</span></span><br/> |
| <span data-ttu-id="1ead7-143">**操作功能表**</span><span class="sxs-lookup"><span data-stu-id="1ead7-143">**Context menus**</span></span><br/> <span data-ttu-id="1ead7-144">顯示一組與目前內容相關的一小命令和選項的下拉式功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-144">drop-down menus that display a small set of commands and options related to the current context.</span></span> <br/>       | <span data-ttu-id="1ead7-145">當使用者以滑鼠右鍵按一下支援操作功能表的物件或視窗區域時，就會出現快顯功能表下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="1ead7-145">context menus drop-down when users right-click on an object or window region that supports a context menu.</span></span> <br/> ![<span data-ttu-id="1ead7-146">顯示命令之內容功能表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-146">screen shot of context menu displaying commands</span></span> ](images/cmd-menus-image6.png)<br/> <span data-ttu-id="1ead7-147">windows explorer 中的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-147">a context menu from windows explorer.</span></span><br/> <span data-ttu-id="1ead7-148">如果內容功能表是最好的功能表選項，但是您需要適用于所有使用者的解決方案，您可以使用功能表下拉箭號按鈕。</span><span class="sxs-lookup"><span data-stu-id="1ead7-148">if context menus are the best menu choice but you need a solution suitable for all users, you can use a menu drop-down arrow button.</span></span> <br/> ![<span data-ttu-id="1ead7-149">具有下拉式功能表按鈕的相片螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-149">screen shot of photo with drop-down menu button</span></span> ](images/cmd-menus-image7.png)<br/> <span data-ttu-id="1ead7-150">顯示功能表下拉式按鈕的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-150">A context menu made visible with a menu drop-down button.</span></span><br/>                                                   |
| <span data-ttu-id="1ead7-151">**工作窗格功能表**</span><span class="sxs-lookup"><span data-stu-id="1ead7-151">**Task pane menus**</span></span><br/> <span data-ttu-id="1ead7-152">與所選物件或程式模式相關的一組小型命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-152">a small set of commands related to the selected object or program mode.</span></span> <br/>                              | <span data-ttu-id="1ead7-153">與內容功能表不同的是，它們會自動顯示在視窗窗格內，而不是依需求。</span><span class="sxs-lookup"><span data-stu-id="1ead7-153">unlike context menus, they are displayed automatically within a window pane, instead of on demand.</span></span> <br/> ![<span data-ttu-id="1ead7-154">右側有工作窗格功能表的相片螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-154">screen shot of photo with task pane menu on right</span></span> ](images/cmd-menus-image8.png)<br/> <span data-ttu-id="1ead7-155">Windows 影像中心檢視器中的工作窗格功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-155">A task pane menu from the Windows Photo Gallery viewer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="1ead7-156">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-156">Is this the right user interface?</span></span>

<span data-ttu-id="1ead7-157">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="1ead7-157">To decide, consider these questions:</span></span>

### <a name="menu-bars"></a><span data-ttu-id="1ead7-158">功能表列</span><span class="sxs-lookup"><span data-stu-id="1ead7-158">Menu bars</span></span>

<span data-ttu-id="1ead7-159">適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="1ead7-159">Do the following conditions apply:</span></span>

-   <span data-ttu-id="1ead7-160">視窗是否為主視窗？</span><span class="sxs-lookup"><span data-stu-id="1ead7-160">Is the window a primary window?</span></span>
-   <span data-ttu-id="1ead7-161">有許多功能表項目嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-161">Are there many menu items?</span></span>
-   <span data-ttu-id="1ead7-162">有許多功能表類別目錄嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-162">Are there many menu categories?</span></span>
-   <span data-ttu-id="1ead7-163">大部分的功能表項目都適用于整個程式和主視窗嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-163">Do the majority of the menu items apply to the entire program and primary window?</span></span>
-   <span data-ttu-id="1ead7-164">功能表是否需要適用于所有使用者？</span><span class="sxs-lookup"><span data-stu-id="1ead7-164">Does the menu need to work for all users?</span></span>

<span data-ttu-id="1ead7-165">如果是的話，請考慮使用功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-165">If so, consider using a menu bar.</span></span>

### <a name="toolbar-menus"></a><span data-ttu-id="1ead7-166">工具列功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-166">Toolbar menus</span></span>

<span data-ttu-id="1ead7-167">適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="1ead7-167">Do the following conditions apply:</span></span>

-   <span data-ttu-id="1ead7-168">視窗是否為主視窗？</span><span class="sxs-lookup"><span data-stu-id="1ead7-168">Is the window a primary window?</span></span>
-   <span data-ttu-id="1ead7-169">視窗是否有工具列？</span><span class="sxs-lookup"><span data-stu-id="1ead7-169">Does the window have a toolbar?</span></span>
-   <span data-ttu-id="1ead7-170">有幾個功能表類別目錄嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-170">Are there only a few menu categories?</span></span>
-   <span data-ttu-id="1ead7-171">功能表是否需要適用于所有使用者？</span><span class="sxs-lookup"><span data-stu-id="1ead7-171">Does the menu need to work for all users?</span></span>

<span data-ttu-id="1ead7-172">如果是的話，請考慮使用工具列功能表，而不是功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-172">If so, consider using a toolbar menu instead of or in addition to a menu bar.</span></span>

### <a name="tab-menus"></a><span data-ttu-id="1ead7-173">索引標籤功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-173">Tab menus</span></span>

<span data-ttu-id="1ead7-174">適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="1ead7-174">Do the following conditions apply:</span></span>

-   <span data-ttu-id="1ead7-175">視窗是否為主視窗？</span><span class="sxs-lookup"><span data-stu-id="1ead7-175">Is the window a primary window?</span></span>
-   <span data-ttu-id="1ead7-176">視窗是否有索引標籤，其中每個索引標籤會用於一組專用的工作 (而不是使用索引標籤來顯示不同的視圖) ？</span><span class="sxs-lookup"><span data-stu-id="1ead7-176">Does the window have tabs, where each tab is used for a dedicated set of tasks (as opposed to using tabs to show different views)?</span></span>
-   <span data-ttu-id="1ead7-177">有一個適用于每個索引標籤的功能表類別目錄嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-177">Is there one menu category that applies to each tab?</span></span>
-   <span data-ttu-id="1ead7-178">是否有許多命令和選項，但每個索引標籤只會有一小部分？</span><span class="sxs-lookup"><span data-stu-id="1ead7-178">Are there many commands and options, but only a small set for each tab?</span></span>

<span data-ttu-id="1ead7-179">如果是的話，請考慮使用索引標籤功能表，而不是功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-179">If so, consider using a tab menu instead of a menu bar.</span></span>

### <a name="context-menu"></a><span data-ttu-id="1ead7-180">捷徑功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-180">Context menu</span></span>

<span data-ttu-id="1ead7-181">適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="1ead7-181">Do the following conditions apply:</span></span>

-   <span data-ttu-id="1ead7-182">是否有一組適用于所選物件或視窗區域的內容相關命令和選項？</span><span class="sxs-lookup"><span data-stu-id="1ead7-182">Is there a small set of contextual commands and options that apply to the selected object or window region?</span></span>
-   <span data-ttu-id="1ead7-183">這些功能表項目是否重複？</span><span class="sxs-lookup"><span data-stu-id="1ead7-183">Are these menu items redundant?</span></span>
-   <span data-ttu-id="1ead7-184">目標使用者是否熟悉快顯功能表？</span><span class="sxs-lookup"><span data-stu-id="1ead7-184">Are the target users familiar with context menus?</span></span>

<span data-ttu-id="1ead7-185">如果是的話，請考慮為需要它們的物件和視窗區域提供快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-185">If so, consider providing context menus for the objects and window regions that need them.</span></span>

<span data-ttu-id="1ead7-186">針對以瀏覽器為基礎的程式，工作窗格功能表是更常見的內容命令解決方案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-186">For browser-based programs, task pane menus are a more common solution for contextual commands.</span></span> <span data-ttu-id="1ead7-187">目前，使用者預期以瀏覽器為基礎的程式中的內容功能表為泛型和無用。</span><span class="sxs-lookup"><span data-stu-id="1ead7-187">Currently, users expect context menus in browser-based programs to be generic and unhelpful.</span></span>

### <a name="task-pane-menu"></a><span data-ttu-id="1ead7-188">工作窗格功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-188">Task pane menu</span></span>

<span data-ttu-id="1ead7-189">適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="1ead7-189">Do the following conditions apply:</span></span>

-   <span data-ttu-id="1ead7-190">視窗是否為主視窗？</span><span class="sxs-lookup"><span data-stu-id="1ead7-190">Is the window a primary window?</span></span>
-   <span data-ttu-id="1ead7-191">是否有一組適用于所選物件或程式模式的內容相關命令和選項？</span><span class="sxs-lookup"><span data-stu-id="1ead7-191">Is there a small set of contextual commands and options that apply to the selected object or program mode?</span></span>
-   <span data-ttu-id="1ead7-192">有幾個功能表類別目錄嗎？</span><span class="sxs-lookup"><span data-stu-id="1ead7-192">Are there a few menu categories?</span></span>
-   <span data-ttu-id="1ead7-193">功能表是否需要適用于所有使用者？</span><span class="sxs-lookup"><span data-stu-id="1ead7-193">Does the menu need to work for all users?</span></span>

<span data-ttu-id="1ead7-194">如果是的話，請考慮使用工作窗格功能表，而不是操作功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-194">If so, consider using a task pane menu instead of a context menu.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="1ead7-195">設計概念</span><span class="sxs-lookup"><span data-stu-id="1ead7-195">Design concepts</span></span>

<span data-ttu-id="1ead7-196">有效的功能表，可提升絕佳的使用者體驗：</span><span class="sxs-lookup"><span data-stu-id="1ead7-196">Effective menus that promote a good user experience:</span></span>

-   <span data-ttu-id="1ead7-197">使用符合您的程式類型、視窗類型、命令使用方式和目標使用者的命令呈現。</span><span class="sxs-lookup"><span data-stu-id="1ead7-197">Use a command presentation that matches your program type, window types, command usage, and target users.</span></span>
-   <span data-ttu-id="1ead7-198">妥善地組織，並在適當時使用標準功能表組織。</span><span class="sxs-lookup"><span data-stu-id="1ead7-198">Are well organized, using standard menu organization when appropriate.</span></span>
-   <span data-ttu-id="1ead7-199">有效使用功能表列、工具列和快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-199">Use menu bars, toolbars, and context menus effectively.</span></span>
-   <span data-ttu-id="1ead7-200">有效地使用圖示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-200">Use icons effectively.</span></span>
-   <span data-ttu-id="1ead7-201">有效地使用存取金鑰和快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1ead7-201">Use access keys and shortcut keys effectively.</span></span>

<span data-ttu-id="1ead7-202">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-202">**If you do only one thing...**</span></span>

<span data-ttu-id="1ead7-203">選擇符合您的程式類型、視窗類型、命令使用方式和目標使用者的命令呈現。</span><span class="sxs-lookup"><span data-stu-id="1ead7-203">Choose a command presentation that matches your program type, window types, command usage, and target users.</span></span>

## <a name="guidelines"></a><span data-ttu-id="1ead7-204">指導方針</span><span class="sxs-lookup"><span data-stu-id="1ead7-204">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="1ead7-205">一般</span><span class="sxs-lookup"><span data-stu-id="1ead7-205">General</span></span>

-   <span data-ttu-id="1ead7-206">**功能表列以外的所有功能表模式都需要下拉式箭號，以指示下拉式功能表是否存在。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-206">**All menu patterns except menu bars need a drop-down arrow to indicate the presence of a pull-down menu.**</span></span> <span data-ttu-id="1ead7-207">功能表列中的功能表不存在，而是在其他模式下。</span><span class="sxs-lookup"><span data-stu-id="1ead7-207">The presence of menus goes without saying in a menu bar, but not in the other patterns.</span></span>
-   <span data-ttu-id="1ead7-208">**請勿動態變更功能表項目名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-208">**Don't change menu item names dynamically.**</span></span> <span data-ttu-id="1ead7-209">這麼做會造成混淆和非預期的情況。</span><span class="sxs-lookup"><span data-stu-id="1ead7-209">Doing so is confusing and unexpected.</span></span> <span data-ttu-id="1ead7-210">例如，在選取時，請勿將直向模式選項變更為橫向模式。</span><span class="sxs-lookup"><span data-stu-id="1ead7-210">For example, don't change a Portrait mode option to Landscape mode upon selection.</span></span> <span data-ttu-id="1ead7-211">若為模式，請改為使用 [專案符號和複選](#bullets-and-checkmarks) 標記。</span><span class="sxs-lookup"><span data-stu-id="1ead7-211">For modes, use [bullets and checkmarks](#bullets-and-checkmarks) instead.</span></span>
    -   <span data-ttu-id="1ead7-212">**例外狀況：** 您可以動態變更以物件名稱為基礎的功能表項目名稱。</span><span class="sxs-lookup"><span data-stu-id="1ead7-212">**Exception:** You can change menu item names that are based on object names dynamically.</span></span> <span data-ttu-id="1ead7-213">例如，最近使用的檔案或視窗名稱清單可以是動態的。</span><span class="sxs-lookup"><span data-stu-id="1ead7-213">For example, lists of recently used files or window names can be dynamic.</span></span>

### <a name="menu-bars"></a><span data-ttu-id="1ead7-214">功能表列</span><span class="sxs-lookup"><span data-stu-id="1ead7-214">Menu bars</span></span>

-   <span data-ttu-id="1ead7-215">**考慮刪除具有三個或更少功能表分類的功能表列。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-215">**Consider eliminating menu bars with three or fewer menu categories.**</span></span> <span data-ttu-id="1ead7-216">如果只有幾個命令，則偏好較輕的替代專案（例如工具列功能表），或更多直接替代專案，例如命令按鈕和連結。</span><span class="sxs-lookup"><span data-stu-id="1ead7-216">If there are only a few commands, prefer lighter alternatives such as toolbar menus, or more direct alternatives such as command buttons and links.</span></span>
-   <span data-ttu-id="1ead7-217">**沒有10個以上的功能表類別。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-217">**Don't have more than 10 menu categories.**</span></span> <span data-ttu-id="1ead7-218">太多功能表分類太大，因此不容易使用功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-218">Too many menu categories is overwhelming and makes the menu bar difficult to use.</span></span>
-   <span data-ttu-id="1ead7-219">如果工具列或直接命令提供大部分使用者所需的幾乎所有命令，**請考慮隱藏功能表列**。</span><span class="sxs-lookup"><span data-stu-id="1ead7-219">**Consider hiding the menu bar** if the toolbar or direct commands provide almost all of the commands needed by most users.</span></span> <span data-ttu-id="1ead7-220">允許使用者使用工具列功能表中的功能表列核取記號選項來顯示或隱藏。</span><span class="sxs-lookup"><span data-stu-id="1ead7-220">Allow users to show or hide with a Menu bar check mark option in a toolbar menu.</span></span>

![<span data-ttu-id="1ead7-221">選取功能表列的選項清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-221">screen shot of option list with menu bar selected</span></span> ](images/cmd-menus-image9.png)

<span data-ttu-id="1ead7-222">在此範例中，Windows Internet Explorer 提供功能表列選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-222">In this example, Windows Internet Explorer provides a menu bar option.</span></span>

<span data-ttu-id="1ead7-223">如需詳細資訊，請參閱 [隱藏功能表列](#hiding-menu-bars)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-223">For more information, see [hiding menu bars](#hiding-menu-bars).</span></span>

### <a name="hiding-menu-bars"></a><span data-ttu-id="1ead7-224">隱藏功能表列</span><span class="sxs-lookup"><span data-stu-id="1ead7-224">Hiding menu bars</span></span>

<span data-ttu-id="1ead7-225">一般而言，工具列可與功能表列一起運作，因為兩者都可讓每個使用者專注于其優勢，而不會受到危害。</span><span class="sxs-lookup"><span data-stu-id="1ead7-225">Generally, toolbars work great together with menu bars because having both allows each to focus on their strengths without compromise.</span></span>

-   <span data-ttu-id="1ead7-226">如果您的工具列設計有多餘的功能表列，預設會隱藏功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-226">Hide the menu bar by default if your toolbar design makes having a menu bar redundant.</span></span>
-   <span data-ttu-id="1ead7-227">隱藏功能表列，而不是完全移除功能表列，因為鍵盤使用者更能存取功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-227">Hide the menu bar instead of removing it completely, because menu bars are more accessible for keyboard users.</span></span>
-   <span data-ttu-id="1ead7-228">若要還原功能表列，請在 [主要工具列] 的 [視圖] (中提供功能表列核取記號選項) 或次要工具列) 功能表類別的 [工具] (。</span><span class="sxs-lookup"><span data-stu-id="1ead7-228">To restore the menu bar, provide a Menu bar checkmark option in the View (for primary toolbars) or Tools (for secondary toolbars) menu category.</span></span> <span data-ttu-id="1ead7-229">如需詳細資訊，請參閱 [標準功能表和分割按鈕](cmd-toolbars.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-229">For more information, see [Standard menu and split buttons](cmd-toolbars.md).</span></span>

### <a name="menu-categories"></a><span data-ttu-id="1ead7-230">功能表分類</span><span class="sxs-lookup"><span data-stu-id="1ead7-230">Menu categories</span></span>

-   <span data-ttu-id="1ead7-231">**選擇 [單一單字名稱] 作為功能表類別目錄。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-231">**Choose single word names for menu categories.**</span></span> <span data-ttu-id="1ead7-232">使用多個單字讓類別之間的分隔變得令人困惑。</span><span class="sxs-lookup"><span data-stu-id="1ead7-232">Using multiple words makes the separation between categories confusing.</span></span>
-   <span data-ttu-id="1ead7-233">**針對建立或查看檔的程式，請使用 [** 檔案]、[編輯]、[視圖]、[工具] 和 [說明] 等標準功能表類別。</span><span class="sxs-lookup"><span data-stu-id="1ead7-233">**For programs that create or view documents, use the standard menu categories** such as File, Edit, View, Tools, and Help.</span></span> <span data-ttu-id="1ead7-234">這麼做可讓一般功能表項目成為可預測且更容易尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-234">Doing so makes common menu items predictable and easier to find.</span></span>
-   <span data-ttu-id="1ead7-235">針對其他類型的程式，請考慮根據程式的用途以及使用者對其工作和目標的考慮，將 **命令和選項群組織成更有用的自然類別**。</span><span class="sxs-lookup"><span data-stu-id="1ead7-235">**For other types of programs, consider organizing your commands and options into more useful, natural categories** based on your program's purpose and the way users think about their tasks and goals.</span></span> <span data-ttu-id="1ead7-236">如果您的程式不適合使用標準功能表組織，請不要覺得有義務。</span><span class="sxs-lookup"><span data-stu-id="1ead7-236">Don't feel obligated to use the standard menu organization if it isn't suitable for your program.</span></span>
-   <span data-ttu-id="1ead7-237">**如果您選擇使用非標準的功能表類別目錄，您必須選擇正確的類別名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-237">**If you choose to use non-standard menu categories, you must choose good category names.**</span></span> <span data-ttu-id="1ead7-238">如需詳細資訊，請參閱 [標籤](#labels) 區段。</span><span class="sxs-lookup"><span data-stu-id="1ead7-238">For more information, see the [Labels](#labels) section.</span></span>
-   <span data-ttu-id="1ead7-239">**偏好一般分類的工作導向功能表類別。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-239">**Prefer task-oriented menu categories over generic categories.**</span></span> <span data-ttu-id="1ead7-240">工作導向類別可讓您更輕鬆地尋找功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-240">Task-oriented categories make menu items easier to find.</span></span>

![<span data-ttu-id="1ead7-241">具有翻錄、燒錄和同步的功能表列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-241">screen shot of menu bar with rip, burn, and sync</span></span> ](images/cmd-menus-image10.png)

<span data-ttu-id="1ead7-242">在此範例中，Windows Media Player 使用工作導向的功能表類別。</span><span class="sxs-lookup"><span data-stu-id="1ead7-242">In this example, Windows Media Player uses task-oriented menu categories.</span></span>

-   <span data-ttu-id="1ead7-243">**避免只有一或兩個功能表項目的功能表分類。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-243">**Avoid menu categories with only one or two menu items.**</span></span> <span data-ttu-id="1ead7-244">如果有的話，請使用子功能表來合併其他功能表類別。</span><span class="sxs-lookup"><span data-stu-id="1ead7-244">If sensible, consolidate with other menu categories, perhaps using a submenu.</span></span>
-   <span data-ttu-id="1ead7-245">**請考慮只在下列情況中，將相同的功能表項目放在多個類別中：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-245">**Consider putting the same menu item in multiple categories only if:**</span></span>
    -   <span data-ttu-id="1ead7-246">功能表項目以邏輯方式隸屬于多個功能表類別。</span><span class="sxs-lookup"><span data-stu-id="1ead7-246">The menu item logically belongs in multiple menu categories.</span></span>
    -   <span data-ttu-id="1ead7-247">您有資料顯示使用者在單一功能表類別目錄中找不到該專案的問題。</span><span class="sxs-lookup"><span data-stu-id="1ead7-247">You have data showing that users have trouble finding the item in a single menu category.</span></span>
    -   <span data-ttu-id="1ead7-248">您有多個類別中的一或兩個無人參與的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-248">You have only one or two hard-to-find menu items in multiple categories.</span></span>
-   <span data-ttu-id="1ead7-249">**請勿在多個類別中放入使用相同名稱的不同功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-249">**Don't put different menu items that use the same name in multiple categories.**</span></span> <span data-ttu-id="1ead7-250">例如，在多個類別中沒有不同的選項功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-250">For example, don't have different Options menu items in multiple categories.</span></span>
    -   <span data-ttu-id="1ead7-251">**例外狀況：** 索引標籤功能表模式在每個索引標籤功能表上可能會有不同的選項和 [說明] 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-251">**Exception:** The tab menu pattern may have different Options and Help menu items in each tab menu.</span></span>

![<span data-ttu-id="1ead7-252">具有重複功能表項目之索引標籤功能表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-252">screen shot of tab menus with repeated menu items</span></span> ](images/cmd-menus-image11.png)

<span data-ttu-id="1ead7-253">在此範例中，Windows Media Player 會在每個索引標籤功能表上提供選項和 [說明] 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-253">In this example, Windows Media Player has Options and Help menu items in each tab menu.</span></span>

### <a name="menu-item-organization-and-order"></a><span data-ttu-id="1ead7-254">功能表項目組織和訂單</span><span class="sxs-lookup"><span data-stu-id="1ead7-254">Menu item organization and order</span></span>

-   <span data-ttu-id="1ead7-255">**將功能表項目組織成具有七個或較少之強相關專案的群組。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-255">**Organize the menu items into groups of seven or fewer strongly related items.**</span></span> <span data-ttu-id="1ead7-256">在此情況下，子功能表會計算為父功能表中的單一功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-256">For this, submenus count as a single menu item in the parent menu.</span></span>
-   <span data-ttu-id="1ead7-257">**請勿在功能表的單一層級中放入超過25個專案** (不會) 的子功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-257">**Don't put more than 25 items within a single level of a menu** (not counting submenus).</span></span>
-   <span data-ttu-id="1ead7-258">**在功能表內的群組之間放置分隔符號。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-258">**Put separators between the groups within a menu.**</span></span> <span data-ttu-id="1ead7-259">分隔符號是橫跨功能表寬度的單一行。</span><span class="sxs-lookup"><span data-stu-id="1ead7-259">A separator is a single line that spans the width of the menu.</span></span>
-   <span data-ttu-id="1ead7-260">**在功能表中，將群組放在其邏輯順序中。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-260">**Within a menu, put the groups in their logical order.**</span></span> <span data-ttu-id="1ead7-261">如果沒有邏輯順序，請先放置最常使用的群組。</span><span class="sxs-lookup"><span data-stu-id="1ead7-261">If there is no logical order, place the most commonly used groups first.</span></span>
-   <span data-ttu-id="1ead7-262">**在群組中，將專案放在其邏輯順序中。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-262">**Within a group, put the items in their logical order.**</span></span> <span data-ttu-id="1ead7-263">如果沒有邏輯順序，請先放置最常使用的專案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-263">If there is no logical order, place the most commonly used items first.</span></span> <span data-ttu-id="1ead7-264">將數值專案 (例如縮放百分比) 以數位順序表示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-264">Put numeric items (such as zoom percentages) in numeric order.</span></span>

### <a name="submenus"></a><span data-ttu-id="1ead7-265">子功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-265">Submenus</span></span>

-   <span data-ttu-id="1ead7-266">**避免使用不必要的子功能表。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-266">**Avoid using submenus unnecessarily.**</span></span> <span data-ttu-id="1ead7-267">子功能表需要更多實體精力才能使用，而且通常會讓功能表項目更難找到。</span><span class="sxs-lookup"><span data-stu-id="1ead7-267">Submenus require more physical effort to use and generally make the menu items more difficult to locate.</span></span>
-   <span data-ttu-id="1ead7-268">**請勿將常用的功能表項目放在子功能表中。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-268">**Don't put frequently used menu items in a submenu.**</span></span> <span data-ttu-id="1ead7-269">這麼做會讓這些命令的使用效率不佳。</span><span class="sxs-lookup"><span data-stu-id="1ead7-269">Doing so would make using these commands inefficient.</span></span> <span data-ttu-id="1ead7-270">不過，您可以將常用的命令放在子功能表中，如果通常會直接存取，例如使用工具列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-270">However, you can put frequently used commands in a submenu if they are normally accessed more directly, such as with a toolbar.</span></span>
-   <span data-ttu-id="1ead7-271">**如果有下列情況，請考慮使用子功能表：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-271">**Consider using a submenu if:**</span></span>
    -   <span data-ttu-id="1ead7-272">這麼做會簡化上層功能表，因為它有許多專案 (20 個以上) ，或子功能表是超過七個專案的群組之一。</span><span class="sxs-lookup"><span data-stu-id="1ead7-272">Doing so simplifies the parent menu because it has many items (20 or more), or the submenu is part of a group of more than seven items.</span></span>
    -   <span data-ttu-id="1ead7-273">子功能表中的專案所使用的頻率，會比在父功能表中的專案少。</span><span class="sxs-lookup"><span data-stu-id="1ead7-273">The items in the submenu are used less frequently than those in the parent menu.</span></span>
    -   <span data-ttu-id="1ead7-274">子功能表會有三個或多個專案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-274">The submenu would have three or more items.</span></span>
    -   <span data-ttu-id="1ead7-275">有三個或多個以相同字組開頭的命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-275">There are three or more commands that begin with the same word.</span></span> <span data-ttu-id="1ead7-276">在此情況下，請使用該單字作為子功能表標籤。</span><span class="sxs-lookup"><span data-stu-id="1ead7-276">In this case, use that word as the submenu label.</span></span>

![<span data-ttu-id="1ead7-277">具有四個子功能表項目目的 [新增] 功能表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-277">screen shot of 'new' menu with four submenu items</span></span> ](images/cmd-menus-image12.png)

<span data-ttu-id="1ead7-278">在此範例中，新的子功能表會取代新的電子郵件訊息、新的新聞訊息、新資料夾和新連絡人的個別命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-278">In this example, the New submenu replaces separate commands for New mail message, New news message, New folder, and New contact.</span></span>

-   <span data-ttu-id="1ead7-279">**最多有三個層級的功能表使用。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-279">**Use at most three levels of menus.**</span></span> <span data-ttu-id="1ead7-280">也就是說，您可以有主要功能表和最多兩層的子功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-280">That is, you can have a primary menu and at most two levels of submenus.</span></span> <span data-ttu-id="1ead7-281">兩個層級的子功能表應該很罕見。</span><span class="sxs-lookup"><span data-stu-id="1ead7-281">Two levels of submenus should be rare.</span></span>

### <a name="presentation"></a><span data-ttu-id="1ead7-282">簡報</span><span class="sxs-lookup"><span data-stu-id="1ead7-282">Presentation</span></span>

-   <span data-ttu-id="1ead7-283">**停用未套用至目前內容的功能表項目，** 而不是將它們移除。</span><span class="sxs-lookup"><span data-stu-id="1ead7-283">**Disable menu items that don't apply to the current context,** instead of removing them.</span></span> <span data-ttu-id="1ead7-284">這樣做會讓功能表列內容穩定且更容易尋找。</span><span class="sxs-lookup"><span data-stu-id="1ead7-284">Doing so makes menu bar contents stable and easier to find.</span></span> <span data-ttu-id="1ead7-285">**異常：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-285">**Exceptions:**</span></span>
    -   <span data-ttu-id="1ead7-286">針對內容功能表分類，請 **移除，而不要停用未套用至目前內容的內容功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-286">For contextual menu categories, **remove rather than disable context menu items that don't apply to the current context.**</span></span> <span data-ttu-id="1ead7-287">當功能表分類只針對特定模式顯示時（例如選取特定物件類型時），就會顯示為內容。</span><span class="sxs-lookup"><span data-stu-id="1ead7-287">A menu category is contextual when it is displayed only for specific modes, such as when a certain object type is selected.</span></span> <span data-ttu-id="1ead7-288">如需詳細資訊，請參閱移除操作功能表的 [與停](#context-menus) 用指南。</span><span class="sxs-lookup"><span data-stu-id="1ead7-288">For details, see the [remove vs. disable](#context-menus) guidelines for context menus.</span></span>
    -   <span data-ttu-id="1ead7-289">如果決定何時應該停用功能表項目會造成明顯的效能問題，請讓功能表項目保持作用中狀態，並在必要時將其選取專案產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1ead7-289">If determining when a menu item should be disabled causes noticeable performance problems, leave the menu item active and if necessary have its selection result in an error message.</span></span>

### <a name="tab-menus"></a><span data-ttu-id="1ead7-290">索引標籤功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-290">Tab menus</span></span>

-   <span data-ttu-id="1ead7-291">**每個索引標籤功能表都可以有內容特定的選項和 [說明] 功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-291">**Each tab menu may have context specific Options and Help menu items.**</span></span> <span data-ttu-id="1ead7-292">這與其他所有功能表模式相反。</span><span class="sxs-lookup"><span data-stu-id="1ead7-292">This is in contrast to all other menu patterns.</span></span> <span data-ttu-id="1ead7-293">每個索引標籤都是用於一組專用的工作，因此任何跨索引標籤功能表的冗余都不會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="1ead7-293">Each tab is used for a dedicated set of tasks, so any redundancy across tab menus isn't confusing.</span></span>

### <a name="context-menus"></a><span data-ttu-id="1ead7-294">操作功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-294">Context menus</span></span>

-   <span data-ttu-id="1ead7-295">**只針對內容相關命令和選項使用操作功能表。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-295">**Use context menus only for contextual commands and options.**</span></span> <span data-ttu-id="1ead7-296">功能表項目只能套用至選取的 (，或) 物件或視窗區域（而不是整個程式）上按一下。</span><span class="sxs-lookup"><span data-stu-id="1ead7-296">The menu items should apply only to the selected (or clicked upon) object or window region, not the entire program.</span></span>
-   <span data-ttu-id="1ead7-297">**不要讓命令只能透過內容功能表使用。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-297">**Don't make commands only available through context menus.**</span></span> <span data-ttu-id="1ead7-298">如同快速鍵，操作功能表是執行命令及選擇選項的替代方法。</span><span class="sxs-lookup"><span data-stu-id="1ead7-298">Like shortcut keys, context menus are alternative means of performing commands and choosing options.</span></span> <span data-ttu-id="1ead7-299">例如，[屬性] 命令也可以透過功能表列或 Alt + Enter 存取金鑰來使用。</span><span class="sxs-lookup"><span data-stu-id="1ead7-299">For example, a Properties command is also available through the menu bar or the Alt+Enter access key.</span></span>
-   <span data-ttu-id="1ead7-300">**提供所有物件和視窗區域的內容功能表，這些物件和視窗區域** 都可受益于一組小型的內容相關命令和選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-300">**Provide context menus for all objects and window regions** that benefit from a small set of contextual commands and options.</span></span> <span data-ttu-id="1ead7-301">許多使用者定期以滑鼠右鍵按一下，並預期會在任何位置找到內容功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-301">Many users right-click regularly and expect to find context menus anywhere.</span></span>
-   <span data-ttu-id="1ead7-302">**針對以所有使用者為目標的內容功能表，請考慮使用功能表下拉箭號按鈕。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-302">**Consider using a menu drop-down arrow button for context menus targeted at all users.**</span></span> <span data-ttu-id="1ead7-303">內容功能表通常適用于以 advanced users 為目標的命令和選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-303">Normally context menus are suitable for commands and options targeted at advanced users.</span></span> <span data-ttu-id="1ead7-304">不過，您可以在內容功能表是最佳功能表選項，且您需要將目標設為所有使用者的情況下，使用功能表下拉式按鈕。</span><span class="sxs-lookup"><span data-stu-id="1ead7-304">However, you can use a menu drop-down button in cases where context menus are the best menu choice and you need to target all users.</span></span>

![<span data-ttu-id="1ead7-305">具有下拉式功能表按鈕的相片螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-305">screen shot of photo with drop-down menu button</span></span> ](images/cmd-menus-image7.png)

<span data-ttu-id="1ead7-306">在此範例中，會使用功能表下拉式按鈕來顯示內容功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-306">In this example, a menu drop-down button is used to make a context menu visible.</span></span>

<span data-ttu-id="1ead7-307">**功能表項目組織和訂單**</span><span class="sxs-lookup"><span data-stu-id="1ead7-307">**Menu item organization and order**</span></span>

-   <span data-ttu-id="1ead7-308">**將功能表項目組織成具有七個或較少之強相關專案的群組。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-308">**Organize the menu items into groups of seven or fewer strongly related items.**</span></span>
-   <span data-ttu-id="1ead7-309">**避免使用子功能表** ，讓內容功能表保持簡單、直接且有效率。</span><span class="sxs-lookup"><span data-stu-id="1ead7-309">**Avoid using submenus** to keep context menus simple, direct, and efficient.</span></span>
-   <span data-ttu-id="1ead7-310">**請勿在內容功能表中放入15個以上的專案。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-310">**Don't put more than 15 items within a context menu.**</span></span>
-   <span data-ttu-id="1ead7-311">**在功能表內的群組之間放置分隔符號。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-311">**Put separators between the groups within a menu.**</span></span> <span data-ttu-id="1ead7-312">分隔符號是橫跨功能表寬度的單一行。</span><span class="sxs-lookup"><span data-stu-id="1ead7-312">A separator is a single line that spans the width of the menu.</span></span>
-   <span data-ttu-id="1ead7-313">**使用下列順序來顯示功能表項目：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-313">**Present menu items using the following order:**</span></span>

<dl> <span data-ttu-id="1ead7-314">主要 (最常使用的) 命令</span><span class="sxs-lookup"><span data-stu-id="1ead7-314">Primary (most frequently used) commands</span></span><dl> <span data-ttu-id="1ead7-315">開啟</span><span class="sxs-lookup"><span data-stu-id="1ead7-315">Open</span></span>  
<span data-ttu-id="1ead7-316">執行</span><span class="sxs-lookup"><span data-stu-id="1ead7-316">Run</span></span>  
<span data-ttu-id="1ead7-317">播放</span><span class="sxs-lookup"><span data-stu-id="1ead7-317">Play</span></span>  
<span data-ttu-id="1ead7-318">列印 <separator>  
</span><span class="sxs-lookup"><span data-stu-id="1ead7-318">Print <separator>  
</span></span></dl> </dd> <dd><span data-ttu-id="1ead7-319">物件所支援的次要命令</span><span class="sxs-lookup"><span data-stu-id="1ead7-319">Secondary commands supported by the object</span></span><dl> <separator>  
</dl> </dd> <span data-ttu-id="1ead7-320">傳輸命令</span><span class="sxs-lookup"><span data-stu-id="1ead7-320">Transfer commands</span></span><dl> <span data-ttu-id="1ead7-321">剪下</span><span class="sxs-lookup"><span data-stu-id="1ead7-321">Cut</span></span>  
<span data-ttu-id="1ead7-322">複製</span><span class="sxs-lookup"><span data-stu-id="1ead7-322">Copy</span></span>  
<span data-ttu-id="1ead7-323">粘貼 <separator>  
</span><span class="sxs-lookup"><span data-stu-id="1ead7-323">Paste <separator>  
</span></span></dl> </dd> <dd><span data-ttu-id="1ead7-324">物件設定</span><span class="sxs-lookup"><span data-stu-id="1ead7-324">Object settings</span></span><dl> <separator>  
</dl> </dd> <span data-ttu-id="1ead7-325">物件命令</span><span class="sxs-lookup"><span data-stu-id="1ead7-325">Object commands</span></span><dl> <span data-ttu-id="1ead7-326">刪除</span><span class="sxs-lookup"><span data-stu-id="1ead7-326">Delete</span></span>  
<span data-ttu-id="1ead7-327">重 命名 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-327">Rename <separator></span></span>  
<span data-ttu-id="1ead7-328">屬性</span><span class="sxs-lookup"><span data-stu-id="1ead7-328">Properties</span></span>
</dl> </dd> </dl>

<span data-ttu-id="1ead7-329">**展示**</span><span class="sxs-lookup"><span data-stu-id="1ead7-329">**Presentation**</span></span>

-   <span data-ttu-id="1ead7-330">**使用粗體顯示預設命令。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-330">**Display the default command using bold.**</span></span> <span data-ttu-id="1ead7-331">在可行的情況下，也請將它設為第一個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-331">When practical, also make it the first menu item.</span></span> <span data-ttu-id="1ead7-332">當使用者按兩下或選取物件，然後按下 Enter 時，就會叫用預設命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-332">The default command is invoked when users double-click or select an object and press Enter.</span></span>
-   <span data-ttu-id="1ead7-333">**移除，而不是停用未套用至目前內容的內容功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-333">**Remove rather than disable context menu items that don't apply to the current context.**</span></span> <span data-ttu-id="1ead7-334">這樣做會讓操作功能表的內容和效率更高。</span><span class="sxs-lookup"><span data-stu-id="1ead7-334">Doing so makes context menus contextual and efficient.</span></span>
    -   <span data-ttu-id="1ead7-335">**例外狀況：** 如果有合理的預期可供使用，請停用不適用的功能表項目：</span><span class="sxs-lookup"><span data-stu-id="1ead7-335">**Exception:** Disable menu items that don't apply if there is a reasonable expectation for them to be available:</span></span>
        -   <span data-ttu-id="1ead7-336">一律具有相關的標準內容功能表命令，例如剪下、複製、貼上、刪除和重新命名。</span><span class="sxs-lookup"><span data-stu-id="1ead7-336">Always have the relevant standard context menu commands, such as Cut, Copy, Paste, Delete, and Rename.</span></span>
        -   <span data-ttu-id="1ead7-337">一律具有完成相關集合的命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-337">Always have the commands that complete related sets.</span></span> <span data-ttu-id="1ead7-338">例如，如果有一回，也應該要有一個轉寄。</span><span class="sxs-lookup"><span data-stu-id="1ead7-338">For example, if there is a Back, there should also be a Forward.</span></span> <span data-ttu-id="1ead7-339">如果有剪下，一律會有複製和貼上。</span><span class="sxs-lookup"><span data-stu-id="1ead7-339">If there's a Cut, always have a Copy and Paste.</span></span>

### <a name="bullets-and-checkmarks"></a><span data-ttu-id="1ead7-340">專案符號和核取記號</span><span class="sxs-lookup"><span data-stu-id="1ead7-340">Bullets and checkmarks</span></span>

-   <span data-ttu-id="1ead7-341">**選項的功能表項目可以使用專案符號和核取記號。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-341">**Menu items that are options may use bullets and checkmarks.**</span></span> <span data-ttu-id="1ead7-342">命令可能不是。</span><span class="sxs-lookup"><span data-stu-id="1ead7-342">Commands may not.</span></span>
-   <span data-ttu-id="1ead7-343">**使用專案符號，從一組較少的互斥選項中選擇一個選項。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-343">**Use a bullet to choose one option from a small set of mutually exclusive choices.**</span></span> <span data-ttu-id="1ead7-344">群組中應該一律至少有兩個專案符號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-344">There should always be at least two bullets in a group.</span></span> <span data-ttu-id="1ead7-345">如需詳細資訊，請參閱 [選項按鈕](ctrl-radio-buttons.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-345">For more information, see [Radio buttons](ctrl-radio-buttons.md).</span></span>
-   <span data-ttu-id="1ead7-346">**使用核取記號來切換獨立設定的開啟或關閉。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-346">**Use a checkmark to toggle an independent setting on or off.**</span></span> <span data-ttu-id="1ead7-347">如果選取和清除的狀態不清楚且明確地相反，請改為使用一組專案符號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-347">If the selected and cleared states aren't clear and unambiguous opposites, use a set of bullets instead.</span></span> <span data-ttu-id="1ead7-348">如需詳細資訊，請參閱 [核取方塊](ctrl-check-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-348">For more information, see [Check boxes](ctrl-check-boxes.md).</span></span>
-   <span data-ttu-id="1ead7-349">**若為混合的核取記號狀態，則顯示沒有核取記號的功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-349">**For a mixed checkmark state, display a menu item without a checkmark.**</span></span> <span data-ttu-id="1ead7-350">混合狀態用於多個選取範圍，表示已針對部分（而非全部）物件設定選項，因此每個個別物件都有選取或清除的狀態。</span><span class="sxs-lookup"><span data-stu-id="1ead7-350">The mixed state is used for multiple selection to indicate that the option is set for some, but not all, objects, so each individual object has either the selected or cleared state.</span></span> <span data-ttu-id="1ead7-351">混合狀態不會當做個別專案的第三個狀態使用。</span><span class="sxs-lookup"><span data-stu-id="1ead7-351">The mixed state is not used as a third state for an individual item.</span></span>
-   <span data-ttu-id="1ead7-352">**在相關的核取記號或專案符號集之間放置分隔符號。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-352">**Put separators between the related sets of checkmarks or bullets.**</span></span> <span data-ttu-id="1ead7-353">分隔符號是橫跨功能表寬度的單一行。</span><span class="sxs-lookup"><span data-stu-id="1ead7-353">A separator is a single line that spans the width of the menu.</span></span>

### <a name="icons"></a><span data-ttu-id="1ead7-354">圖示</span><span class="sxs-lookup"><span data-stu-id="1ead7-354">Icons</span></span>

-   <span data-ttu-id="1ead7-355">**考慮將功能表項目圖示提供給：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-355">**Consider providing menu item icons for:**</span></span>
    -   <span data-ttu-id="1ead7-356">最常使用的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-356">The most commonly used menu items.</span></span>
    -   <span data-ttu-id="1ead7-357">其圖示為標準且知名的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-357">Menu items whose icon is standard and well known.</span></span>
    -   <span data-ttu-id="1ead7-358">其圖示能清楚表明命令所做動作的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-358">Menu items whose icon well illustrates what the command does.</span></span>
-   <span data-ttu-id="1ead7-359">**如果您使用圖示，請不要擔心提供它們給所有功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-359">**If you use icons, don't feel obligated to provide them for all menu items.**</span></span> <span data-ttu-id="1ead7-360">含義模糊的圖示本身並沒有幫助、會使顯示畫面凌亂，也會讓使用者無法專注在重要的功能表項目上。</span><span class="sxs-lookup"><span data-stu-id="1ead7-360">Cryptic icons aren't helpful, create visual clutter, and prevent users from focusing on the important menu items.</span></span>

![<span data-ttu-id="1ead7-361">功能表項目的螢幕擷取畫面，其中包含和不含圖示</span><span class="sxs-lookup"><span data-stu-id="1ead7-361">screen shot of menu items with and without icons</span></span> ](images/cmd-menus-image13.png)

<span data-ttu-id="1ead7-362">在此範例中，[組織] 功能表只有最常使用之功能表項目的圖示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-362">In this example, the Organize menu has icons only for the most commonly used menu items.</span></span>

-   <span data-ttu-id="1ead7-363">**請確定功能表圖示符合 Aero 樣式的圖示指導方針。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-363">**Make sure menu icons conform to the Aero-style icon guidelines.**</span></span>

<span data-ttu-id="1ead7-364">如需詳細資訊和範例，請參閱 [圖示](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-364">For more information and examples, see [Icons](vis-icons.md).</span></span>

### <a name="access-keys"></a><span data-ttu-id="1ead7-365">便捷鍵</span><span class="sxs-lookup"><span data-stu-id="1ead7-365">Access keys</span></span>

-   <span data-ttu-id="1ead7-366">**將存取金鑰指派給所有功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-366">**Assign access keys to all menu items.**</span></span> <span data-ttu-id="1ead7-367">沒有例外狀況。</span><span class="sxs-lookup"><span data-stu-id="1ead7-367">No exceptions.</span></span>
-   <span data-ttu-id="1ead7-368">**如果可能，請根據標準存取金鑰指派，指派常用命令的存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-368">**Whenever possible, assign access keys for commonly used commands according to the Standard Access Key Assignments.**</span></span> <span data-ttu-id="1ead7-369">雖然不一定可以使用一致的存取金鑰指派，但建議您最好使用它們，尤其是經常使用的命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-369">While consistent access key assignments aren't always possible, they are certainly preferred - especially for frequently used commands.</span></span>
-   <span data-ttu-id="1ead7-370">**針對動態功能表項目 (例如) 最近使用過的檔案，請以數位方式指派存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-370">**For dynamic menu items (such as recently used files), assign access keys numerically.**</span></span>

![<span data-ttu-id="1ead7-371">具有數值存取金鑰之功能表項目的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-371">screen shot of menu items with numeric access keys</span></span> ](images/cmd-menus-image14.png)

<span data-ttu-id="1ead7-372">在此範例中，Windows 中的繪圖程式會將數值存取金鑰指派給最近使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-372">In this example, the Paint program in Windows assigns numeric access keys to recently used files.</span></span>

-   <span data-ttu-id="1ead7-373">**在功能表層級內指派唯一的存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-373">**Assign unique access keys within a menu level.**</span></span> <span data-ttu-id="1ead7-374">您可以跨不同的功能表層級重複使用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="1ead7-374">You can reuse access keys across different menu levels.</span></span>
-   <span data-ttu-id="1ead7-375">**讓存取金鑰易於尋找：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-375">**Make access keys easy to find:**</span></span>
    -   <span data-ttu-id="1ead7-376">針對最常使用的功能表項目，請在標籤的第一個或第二個單字開頭選擇字元，最好是第一個字元。</span><span class="sxs-lookup"><span data-stu-id="1ead7-376">For the most frequently used menu items, choose characters at the beginning of the first or second word of the label, preferably the first character.</span></span>
    -   <span data-ttu-id="1ead7-377">針對較不常使用的功能表項目，請選擇在標籤中為特殊的輔音或母音的字母。</span><span class="sxs-lookup"><span data-stu-id="1ead7-377">For less frequently used menu items, choose letters that are a distinctive consonant or a vowel in the label.</span></span>
-   <span data-ttu-id="1ead7-378">**偏好寬寬度的字元，** 例如 w、m 和大寫字母。</span><span class="sxs-lookup"><span data-stu-id="1ead7-378">**Prefer characters with wide widths,** such as w, m, and capital letters.</span></span>
-   <span data-ttu-id="1ead7-379">**偏好使用特殊的輔音或母音，** 例如 "x" In "Exit"。</span><span class="sxs-lookup"><span data-stu-id="1ead7-379">**Prefer a distinctive consonant or a vowel,** such as "x" in "Exit."</span></span>
-   <span data-ttu-id="1ead7-380">**避免使用使底線難以查看的字元，例如，** 從最有問題的 (到最不有問題的) ：</span><span class="sxs-lookup"><span data-stu-id="1ead7-380">**Avoid using characters that make the underline difficult to see,** such as (from most problematic to least problematic):</span></span>
    -   <span data-ttu-id="1ead7-381">只有一個圖元寬度的字母，例如 i 和 l。</span><span class="sxs-lookup"><span data-stu-id="1ead7-381">Letters that are only one pixel wide, such as i and l.</span></span>
    -   <span data-ttu-id="1ead7-382">具有下行的字母，例如 g、j、p、q 和 y。</span><span class="sxs-lookup"><span data-stu-id="1ead7-382">Letters with descenders, such as g, j, p, q, and y.</span></span>
    -   <span data-ttu-id="1ead7-383">包含下行的字母旁的字母。</span><span class="sxs-lookup"><span data-stu-id="1ead7-383">Letters next to a letter with a descender.</span></span>

<span data-ttu-id="1ead7-384">如需更多指導方針與範例，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-384">For more guidelines and examples, see [Keyboard](inter-keyboard.md).</span></span>

### <a name="shortcut-keys"></a><span data-ttu-id="1ead7-385">快速鍵</span><span class="sxs-lookup"><span data-stu-id="1ead7-385">Shortcut keys</span></span>

-   <span data-ttu-id="1ead7-386">**指派快速鍵給最常使用的功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-386">**Assign shortcut keys to the most frequently used menu items.**</span></span> <span data-ttu-id="1ead7-387">不常使用的功能表項目不需要快速鍵，因為使用者可以改用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="1ead7-387">Infrequently used menu items don't need shortcut keys because users can use access keys instead.</span></span>
-   <span data-ttu-id="1ead7-388">**不要讓快速鍵成為執行工作的唯一方法。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-388">**Don't make a shortcut key the only way to perform a task.**</span></span> <span data-ttu-id="1ead7-389">使用者也應該可以使用滑鼠或鍵盤搭配 Tab 鍵、箭號和便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1ead7-389">Users should also be able to use the mouse or the keyboard with Tab, arrow, and access keys.</span></span>
-   <span data-ttu-id="1ead7-390">**針對已知的快速鍵，請使用標準指派。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-390">**For well-known shortcut keys, use the standard assignments.**</span></span>
-   <span data-ttu-id="1ead7-391">**請勿將不同意義指派給已知快速鍵。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-391">**Don't assign different meanings to well-known shortcut keys.**</span></span> <span data-ttu-id="1ead7-392">因為它們是記下，所以已知快速鍵的不一致意義很令人沮喪，而且容易出錯。</span><span class="sxs-lookup"><span data-stu-id="1ead7-392">Because they are memorized, inconsistent meanings for well-known shortcuts are frustrating and error prone.</span></span> <span data-ttu-id="1ead7-393">如需 Windows 程式所使用之知名快速鍵的詳細說明，請參閱 Windows 鍵盤快捷方式機碼。</span><span class="sxs-lookup"><span data-stu-id="1ead7-393">See Windows Keyboard Shortcut Keys for the well-know shortcut keys used by Windows programs.</span></span>
-   <span data-ttu-id="1ead7-394">**請勿嘗試指派全系統的程式快速鍵。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-394">**Don't try to assign system-wide program shortcut keys.**</span></span> <span data-ttu-id="1ead7-395">只有當您的程式具有輸入焦點時，程式的快速鍵才會生效。</span><span class="sxs-lookup"><span data-stu-id="1ead7-395">Your program's shortcut keys will have effect only when your program has input focus.</span></span>
-   <span data-ttu-id="1ead7-396">**記錄所有快速鍵。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-396">**Document all shortcut keys.**</span></span> <span data-ttu-id="1ead7-397">這麼做可協助使用者瞭解快速鍵的指派。</span><span class="sxs-lookup"><span data-stu-id="1ead7-397">Doing so helps users learn the shortcut key assignments.</span></span>
    -   <span data-ttu-id="1ead7-398">**例外狀況：** 不要在內容功能表中顯示快速鍵指派。</span><span class="sxs-lookup"><span data-stu-id="1ead7-398">**Exception:** Don't display shortcut key assignments within context menus.</span></span> <span data-ttu-id="1ead7-399">內容功能表不會顯示快捷方式索引鍵指派，因為它們已針對效率進行優化。</span><span class="sxs-lookup"><span data-stu-id="1ead7-399">Context menus don't display the shortcut key assignments because they are optimized for efficiency.</span></span>
-   <span data-ttu-id="1ead7-400">**針對非標準的金鑰指派：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-400">**For non-standard key assignments:**</span></span>
    -   <span data-ttu-id="1ead7-401">**選擇沒有標準指派的快速鍵。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-401">**Choose shortcut keys that don't have standard assignments.**</span></span> <span data-ttu-id="1ead7-402">絕不重新指派標準快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1ead7-402">Never reassign standard shortcut keys.</span></span>
    -   <span data-ttu-id="1ead7-403">**以一致的方式在整個程式中使用非標準的金鑰指派。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-403">**Use non-standard key assignments consistently throughout your program.**</span></span> <span data-ttu-id="1ead7-404">請勿在不同的視窗中指派不同的意義。</span><span class="sxs-lookup"><span data-stu-id="1ead7-404">Don't assign different meanings in different windows.</span></span>
    -   <span data-ttu-id="1ead7-405">**可能的話，請選擇 [助憶鍵指派]，** 特別是在常用的命令。</span><span class="sxs-lookup"><span data-stu-id="1ead7-405">**If possible, choose mnemonic key assignments,** especially for frequently used commands.</span></span>
    -   <span data-ttu-id="1ead7-406">**針對具有小規模效果的命令** （例如適用于所選物件的命令），使用函式金鑰。</span><span class="sxs-lookup"><span data-stu-id="1ead7-406">**Use function keys for commands that have a small-scale effect,** such as commands that apply to the selected object.</span></span> <span data-ttu-id="1ead7-407">例如，F2 會重新命名選取的專案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-407">For example, F2 renames the selected item.</span></span>
    -   <span data-ttu-id="1ead7-408">針對具有大規模效果的命令（例如適用于整份檔的命令 **），使用 Ctrl 鍵組合**。</span><span class="sxs-lookup"><span data-stu-id="1ead7-408">**Use Ctrl key combinations for commands that have a large-scale effect,** such as commands that apply to an entire document.</span></span> <span data-ttu-id="1ead7-409">例如，Ctrl + S 會儲存目前的檔。</span><span class="sxs-lookup"><span data-stu-id="1ead7-409">For example, Ctrl+S saves the current document.</span></span>
    -   <span data-ttu-id="1ead7-410">**針對擴充或補充標準快速鍵之動作的命令，請使用 Shift 鍵組合。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-410">**Use Shift key combinations for commands that extend or complement the actions of the standard shortcut key.**</span></span> <span data-ttu-id="1ead7-411">例如，Alt + Tab 快速鍵會透過開啟的主視窗進行迴圈，而 Alt + Shift + Tab 鍵則會以反向順序進行迴圈。</span><span class="sxs-lookup"><span data-stu-id="1ead7-411">For example, the Alt+Tab shortcut key cycles through open primary windows, whereas Alt+Shift+Tab cycles in the reverse order.</span></span> <span data-ttu-id="1ead7-412">同樣地，F1 會顯示說明，而 Shift + F1 則會顯示即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="1ead7-412">Similarly, F1 displays Help, whereas Shift+F1 display context-sensitive Help.</span></span>
    -   <span data-ttu-id="1ead7-413">**請勿使用下列字元作為快速鍵：** @ $ {} \[ \] \\  ~  \| ^ '  < >。</span><span class="sxs-lookup"><span data-stu-id="1ead7-413">**Don't use the following characters for shortcut keys:** @ $ {} \[\] \\ ~ \| ^ ' < >.</span></span> <span data-ttu-id="1ead7-414">這些字元需要跨語言的不同按鍵組合，或是地區設定專屬的。</span><span class="sxs-lookup"><span data-stu-id="1ead7-414">These characters require different key combinations across languages or are locale specific.</span></span>
    -   <span data-ttu-id="1ead7-415">**請勿使用 Ctrl + Alt 組合，** 因為 Windows 會將某些語言版本中的此組合解讀為 AltGR 索引鍵，以產生英數位元。</span><span class="sxs-lookup"><span data-stu-id="1ead7-415">**Don't use Ctrl+Alt combinations,** because Windows interprets this combination in some language versions as an AltGR key, which generates alphanumeric characters.</span></span>
-   <span data-ttu-id="1ead7-416">**如果您的程式指派許多快速鍵，請提供自訂指派的能力。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-416">**If your program assigns many shortcut keys, provide the ability to customize the assignments.**</span></span> <span data-ttu-id="1ead7-417">這麼做可讓使用者重新指派衝突的快速鍵，並從其他產品遷移。</span><span class="sxs-lookup"><span data-stu-id="1ead7-417">Doing so allows users to reassign conflicting shortcut keys and migrate from other products.</span></span> <span data-ttu-id="1ead7-418">大部分的程式都不會指派足夠的快速鍵來需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="1ead7-418">Most programs don't assign enough shortcut keys to need this feature.</span></span>

<span data-ttu-id="1ead7-419">如需更多指導方針和標準快速鍵指派，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="1ead7-419">For more guidelines and standard shortcut key assignments, see [Keyboard](inter-keyboard.md).</span></span>

### <a name="standard-menus"></a><span data-ttu-id="1ead7-420">標準功能表</span><span class="sxs-lookup"><span data-stu-id="1ead7-420">Standard menus</span></span>

-   <span data-ttu-id="1ead7-421">**針對建立或查看檔的程式使用標準功能表組織。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-421">**Use the standard menu organization for programs that create or view documents.**</span></span> <span data-ttu-id="1ead7-422">標準功能表組織可預測一般功能表項目，而且更容易尋找。</span><span class="sxs-lookup"><span data-stu-id="1ead7-422">The standard menu organization makes common menu items predictable and easier to find.</span></span>
-   <span data-ttu-id="1ead7-423">**若為其他類型的程式，請使用 [標準] 功能表組織，只有在合理的情況下才會使用。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-423">**For other types of programs, use the standard menu organization only when it makes sense to.**</span></span> <span data-ttu-id="1ead7-424">根據您的程式用途，以及使用者對其工作和目標的思考方式，考慮將命令和選項群組織成更有用的自然類別。</span><span class="sxs-lookup"><span data-stu-id="1ead7-424">Consider organizing your commands and options into more useful, natural categories based on your program's purpose and the way users think about their tasks and goals.</span></span>

<span data-ttu-id="1ead7-425">**標準功能表列**</span><span class="sxs-lookup"><span data-stu-id="1ead7-425">**Standard menu bars**</span></span>

<span data-ttu-id="1ead7-426">標準功能表列結構如下所示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-426">The standard menu bar structure is as follows.</span></span> <span data-ttu-id="1ead7-427">此清單會顯示功能表分類和專案標籤、其順序的分隔符號、其存取和快速鍵，以及其省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-427">This list shows the menu category and item labels, their order with separators, their access and shortcut keys, and their ellipses.</span></span>

<dl> <span data-ttu-id="1ead7-428">檔案</span><span class="sxs-lookup"><span data-stu-id="1ead7-428">File</span></span><dl> <span data-ttu-id="1ead7-429">新 Ctrl + N</span><span class="sxs-lookup"><span data-stu-id="1ead7-429">New Ctrl+N</span></span>  
<span data-ttu-id="1ead7-430">打開。。。Ctrl + O</span><span class="sxs-lookup"><span data-stu-id="1ead7-430">Open... Ctrl+O</span></span>  
<span data-ttu-id="1ead7-431">關閉 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-431">Close <separator></span></span>  
<span data-ttu-id="1ead7-432">儲存 Ctrl + S</span><span class="sxs-lookup"><span data-stu-id="1ead7-432">Save Ctrl+S</span></span>  
<span data-ttu-id="1ead7-433">另存新檔 .。。 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-433">Save as... <separator></span></span>  
<span data-ttu-id="1ead7-434">傳送至 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-434">Send to <separator></span></span>  
<span data-ttu-id="1ead7-435">列印。。。Ctrl + P</span><span class="sxs-lookup"><span data-stu-id="1ead7-435">Print... Ctrl+P</span></span>  
<span data-ttu-id="1ead7-436">預覽列印</span><span class="sxs-lookup"><span data-stu-id="1ead7-436">Print preview</span></span>  
<span data-ttu-id="1ead7-437">頁面設定 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-437">Page setup <separator></span></span>  
<span data-ttu-id="1ead7-438">1 <filename> 2 <filename> 3 <filename> .。。 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-438">1 <filename> 2 <filename> 3 <filename> ... <separator></span></span>  
<span data-ttu-id="1ead7-439">結束 Alt + F4 (的快捷方式通常不提供) </span><span class="sxs-lookup"><span data-stu-id="1ead7-439">Exit Alt+F4 (shortcut usually not given)</span></span>
</dl> </dd> Edit<dl> <span data-ttu-id="1ead7-440">復原 Ctrl + Z</span><span class="sxs-lookup"><span data-stu-id="1ead7-440">Undo Ctrl+Z</span></span>  
<span data-ttu-id="1ead7-441">重做 Ctrl + Y <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-441">Redo Ctrl+Y <separator></span></span>  
<span data-ttu-id="1ead7-442">剪下 Ctrl + X</span><span class="sxs-lookup"><span data-stu-id="1ead7-442">Cut Ctrl+X</span></span>  
<span data-ttu-id="1ead7-443">複製 Ctrl + C</span><span class="sxs-lookup"><span data-stu-id="1ead7-443">Copy Ctrl+C</span></span>  
<span data-ttu-id="1ead7-444">貼上 Ctrl + V <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-444">Paste Ctrl+V <separator></span></span>  
<span data-ttu-id="1ead7-445">全選 Ctrl + A <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-445">Select all Ctrl+A <separator></span></span>  
<span data-ttu-id="1ead7-446">通常不會將 Del (的快捷方式刪除) <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-446">Delete Del (shortcut usually not given) <separator></span></span>  
<span data-ttu-id="1ead7-447">找到。。。Ctrl + F</span><span class="sxs-lookup"><span data-stu-id="1ead7-447">Find... Ctrl+F</span></span>  
<span data-ttu-id="1ead7-448">尋找下一個 F3 (命令通常不會指定) </span><span class="sxs-lookup"><span data-stu-id="1ead7-448">Find next F3 (command usually not given)</span></span>  
<span data-ttu-id="1ead7-449">取代。。。Ctrl + H</span><span class="sxs-lookup"><span data-stu-id="1ead7-449">Replace... Ctrl+H</span></span>  
<span data-ttu-id="1ead7-450">轉到 (G) 。。。Ctrl + G</span><span class="sxs-lookup"><span data-stu-id="1ead7-450">Go to... Ctrl+G</span></span>
</dl> </dd> View<dl> <span data-ttu-id="1ead7-451">工具列</span><span class="sxs-lookup"><span data-stu-id="1ead7-451">Toolbars</span></span>  
<span data-ttu-id="1ead7-452">狀態列 <separator>  
</span><span class="sxs-lookup"><span data-stu-id="1ead7-452">Status bar <separator>  
</span></span></dl> </dd> Zoom<dl> <span data-ttu-id="1ead7-453">放大 Ctrl + +</span><span class="sxs-lookup"><span data-stu-id="1ead7-453">Zoom in Ctrl++</span></span>  
<span data-ttu-id="1ead7-454">縮小 Ctrl +- <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-454">Zoom out Ctrl+- <separator></span></span>  
<span data-ttu-id="1ead7-455">全螢幕 F11</span><span class="sxs-lookup"><span data-stu-id="1ead7-455">Full screen F11</span></span>  
<span data-ttu-id="1ead7-456">重新整理 F5</span><span class="sxs-lookup"><span data-stu-id="1ead7-456">Refresh F5</span></span>
</dl> </dd> <dd><span data-ttu-id="1ead7-457">工具</span><span class="sxs-lookup"><span data-stu-id="1ead7-457">Tools</span></span><dl> <span data-ttu-id="1ead7-458">... <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-458">... <separator></span></span>  
<span data-ttu-id="1ead7-459">選項</span><span class="sxs-lookup"><span data-stu-id="1ead7-459">Options</span></span>
</dl> </dd> <span data-ttu-id="1ead7-460">Help</span><span class="sxs-lookup"><span data-stu-id="1ead7-460">Help</span></span><dl> <span data-ttu-id="1ead7-461"><program name> 說明 F1 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-461"><program name> help F1 <separator></span></span>  
<span data-ttu-id="1ead7-462">詢問 <program name>  
</span><span class="sxs-lookup"><span data-stu-id="1ead7-462">About <program name>  
</span></span></dl> </dd> </dl>

<span data-ttu-id="1ead7-463">**標準工具列功能表按鈕**</span><span class="sxs-lookup"><span data-stu-id="1ead7-463">**Standard toolbar menu buttons**</span></span>

<span data-ttu-id="1ead7-464">標準工具列功能表按鈕如下所示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-464">The standard toolbar menu buttons are as follows.</span></span> <span data-ttu-id="1ead7-465">此清單會顯示功能表分類和專案標籤、其順序的分隔符號、其快速鍵和省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-465">This list shows the menu category and item labels, their order with separators, their shortcut keys, and their ellipses.</span></span>

<dl> <span data-ttu-id="1ead7-466">工具</span><span class="sxs-lookup"><span data-stu-id="1ead7-466">Tools</span></span><dl> <span data-ttu-id="1ead7-467">完整 screenF11 (重新指派存取金鑰（如果也使用了 Find）。 ) </span><span class="sxs-lookup"><span data-stu-id="1ead7-467">Full screenF11(Reassign access key if Find is also used.)</span></span>  
<span data-ttu-id="1ead7-468">工具列 (請注意，功能表列命令會出現在這裡。 ) <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-468">Toolbars(Note that the Menu bar command goes here.) <separator></span></span>  
<span data-ttu-id="1ead7-469">列印...</span><span class="sxs-lookup"><span data-stu-id="1ead7-469">Print...</span></span>  
<span data-ttu-id="1ead7-470">找到。。。 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-470">Find... <separator></span></span>  
<span data-ttu-id="1ead7-471">Zoom</span><span class="sxs-lookup"><span data-stu-id="1ead7-471">Zoom</span></span>  
<span data-ttu-id="1ead7-472">文字大小 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-472">Text size <separator></span></span>  
<span data-ttu-id="1ead7-473">選項</span><span class="sxs-lookup"><span data-stu-id="1ead7-473">Options</span></span>
</dl> </dd> Organize<dl> <span data-ttu-id="1ead7-474">New folderCtrl + N <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-474">New folderCtrl+N <separator></span></span>  
<span data-ttu-id="1ead7-475">CutCtrl + X</span><span class="sxs-lookup"><span data-stu-id="1ead7-475">CutCtrl+X</span></span>  
<span data-ttu-id="1ead7-476">CopyCtrl + C</span><span class="sxs-lookup"><span data-stu-id="1ead7-476">CopyCtrl+C</span></span>  
<span data-ttu-id="1ead7-477">PasteCtrl + V <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-477">PasteCtrl+V <separator></span></span>  
<span data-ttu-id="1ead7-478">選取 allCtrl + A <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-478">Select allCtrl+A <separator></span></span>  
<span data-ttu-id="1ead7-479">通常不會提供 DeleteDel (的快捷方式) </span><span class="sxs-lookup"><span data-stu-id="1ead7-479">DeleteDel(shortcut usually not given)</span></span>  
<span data-ttu-id="1ead7-480">重 命名 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-480">Rename <separator></span></span>  
<span data-ttu-id="1ead7-481">選項</span><span class="sxs-lookup"><span data-stu-id="1ead7-481">Options</span></span>
</dl> </dd> Page<dl> <span data-ttu-id="1ead7-482">New windowCtrl + N <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-482">New windowCtrl+N <separator></span></span>  
<span data-ttu-id="1ead7-483">Zoom</span><span class="sxs-lookup"><span data-stu-id="1ead7-483">Zoom</span></span>  
<span data-ttu-id="1ead7-484">文字大小</span><span class="sxs-lookup"><span data-stu-id="1ead7-484">Text size</span></span>
</dl> </dd> </dl>

<span data-ttu-id="1ead7-485">**標準內容功能表**</span><span class="sxs-lookup"><span data-stu-id="1ead7-485">**Standard context menus**</span></span>

<span data-ttu-id="1ead7-486">標準內容功能表內容如下所示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-486">The standard context menu contents are as follows.</span></span> <span data-ttu-id="1ead7-487">這份清單會顯示功能表項目標籤、其順序的分隔符號、其存取金鑰，以及它們的省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-487">This list shows the menu item labels, their order with separators, their access keys, and their ellipses.</span></span> <span data-ttu-id="1ead7-488">內容功能表不會顯示快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1ead7-488">Context menus don't show shortcut keys.</span></span>

<dl> <span data-ttu-id="1ead7-489">開啟</span><span class="sxs-lookup"><span data-stu-id="1ead7-489">Open</span></span>  
<span data-ttu-id="1ead7-490">執行</span><span class="sxs-lookup"><span data-stu-id="1ead7-490">Run</span></span>  
<span data-ttu-id="1ead7-491">播放</span><span class="sxs-lookup"><span data-stu-id="1ead7-491">Play</span></span>  
<span data-ttu-id="1ead7-492">編輯</span><span class="sxs-lookup"><span data-stu-id="1ead7-492">Edit</span></span>  
<span data-ttu-id="1ead7-493">列印。。。 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-493">Print... <separator></span></span>  
<span data-ttu-id="1ead7-494">剪下</span><span class="sxs-lookup"><span data-stu-id="1ead7-494">Cut</span></span>  
<span data-ttu-id="1ead7-495">複製</span><span class="sxs-lookup"><span data-stu-id="1ead7-495">Copy</span></span>  
<span data-ttu-id="1ead7-496">粘貼 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-496">Paste <separator></span></span>  
<span data-ttu-id="1ead7-497">刪除</span><span class="sxs-lookup"><span data-stu-id="1ead7-497">Delete</span></span>  
<span data-ttu-id="1ead7-498">重 命名 <separator></span><span class="sxs-lookup"><span data-stu-id="1ead7-498">Rename <separator></span></span>  
<span data-ttu-id="1ead7-499">鎖定 <object name> (核取記號) </span><span class="sxs-lookup"><span data-stu-id="1ead7-499">Lock the <object name>(checkmark)</span></span>  
<span data-ttu-id="1ead7-500">屬性</span><span class="sxs-lookup"><span data-stu-id="1ead7-500">Properties</span></span>
</dl>

### <a name="using-ellipses"></a><span data-ttu-id="1ead7-501">使用省略號</span><span class="sxs-lookup"><span data-stu-id="1ead7-501">Using ellipses</span></span>

<span data-ttu-id="1ead7-502">雖然功能表命令可用於立即動作，但可能需要更多的資訊來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="1ead7-502">While menu commands are used for immediate actions, more information might be needed to perform the action.</span></span> <span data-ttu-id="1ead7-503">**指出需要額外資訊的命令 (包括確認) ，方法是在標籤結尾加上省略號。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-503">**Indicate a command that needs additional information (including a confirmation) by adding an ellipsis at the end of the label.**</span></span>

![<span data-ttu-id="1ead7-504">[列印命令和列印] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-504">screen shot of print command and print dialog box</span></span> ](images/cmd-menus-image15.png)

<span data-ttu-id="1ead7-505">在此範例中，Print .。。命令會顯示 [列印] 對話方塊，以收集詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1ead7-505">In this example, the Print... command displays a Print dialog box to gather more information.</span></span>

<span data-ttu-id="1ead7-506">**適當地使用省略號很重要，這表示使用者可以在執行動作之前做出進一步的選擇，或甚至完全取消動作。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-506">**Proper use of ellipses is important to indicate that users can make further choices before performing the action, or even cancel the action entirely.**</span></span> <span data-ttu-id="1ead7-507">省略號提供的視覺提示可讓使用者探索您的軟體，而不需要擔心。</span><span class="sxs-lookup"><span data-stu-id="1ead7-507">The visual cue offered by an ellipsis allows users to explore your software without fear.</span></span>

<span data-ttu-id="1ead7-508">這並不表示每當動作只在執行動作需要額外的資訊時，才會 **顯示另一個視窗時，您應該使用省略號**。</span><span class="sxs-lookup"><span data-stu-id="1ead7-508">**This doesn't mean you should use an ellipsis whenever an action displays another window** only when additional information is required to perform the action.</span></span> <span data-ttu-id="1ead7-509">例如，[關於]、[Advanced]、[說明]、[選項]、[屬性] 和 [設定] 的命令必須在按下時顯示另一個視窗，但不需要使用者提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="1ead7-509">For example, the commands About, Advanced, Help, Options, Properties, and Settings must display another window when clicked, but don't require additional information from the user.</span></span> <span data-ttu-id="1ead7-510">因此不需要省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-510">Therefore they don't need ellipses.</span></span>

<span data-ttu-id="1ead7-511">**如果有不明確的 (例如，命令標籤缺少動詞) ，請根據最可能的使用者動作來決定。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-511">**In case of ambiguity (for example, the command label lacks a verb), decide based on the most likely user action.**</span></span> <span data-ttu-id="1ead7-512">如果單純地查看視窗是常見的動作，請不要使用省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-512">If simply viewing the window is a common action, don't use an ellipsis.</span></span>

<span data-ttu-id="1ead7-513">**正確：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-513">**Correct:**</span></span>

<span data-ttu-id="1ead7-514">其他色彩 .。。</span><span class="sxs-lookup"><span data-stu-id="1ead7-514">More colors...</span></span>

<span data-ttu-id="1ead7-515">版本資訊</span><span class="sxs-lookup"><span data-stu-id="1ead7-515">Version information</span></span>

<span data-ttu-id="1ead7-516">在第一個範例中，使用者很可能會選擇色彩，因此使用省略號是正確的。</span><span class="sxs-lookup"><span data-stu-id="1ead7-516">In the first example, users are most likely going to choose a color, so using an ellipses is correct.</span></span> <span data-ttu-id="1ead7-517">在第二個範例中，使用者很可能會看到版本資訊，因此不需要省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-517">In the second example, users are most likely going to view the version information, making ellipses unnecessary.</span></span>

> [!Note]  
> <span data-ttu-id="1ead7-518">判斷功能表命令是否需要省略號時，請不要使用將 [許可權提升](winenv-uac.md) 為因素的需求。</span><span class="sxs-lookup"><span data-stu-id="1ead7-518">When determining if a menu command needs an ellipsis, don't use the need to [elevate privileges](winenv-uac.md) as a factor.</span></span>

 

<span data-ttu-id="1ead7-519">提高許可權不是執行命令 (所需的資訊，而是用於許可權) ，而提高許可權的需求則會以安全性保護盾表示。</span><span class="sxs-lookup"><span data-stu-id="1ead7-519">Elevation isn't information needed to perform a command (rather, it's for permission) and the need to elevate is indicated with the security shield.</span></span>

## <a name="labels"></a><span data-ttu-id="1ead7-520">標籤</span><span class="sxs-lookup"><span data-stu-id="1ead7-520">Labels</span></span>

-   <span data-ttu-id="1ead7-521">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-521">**Use sentence-style capitalization.**</span></span>
    -   <span data-ttu-id="1ead7-522">**例外狀況：** 若為繼承應用程式，您可以在必要時使用標題樣式的大小寫，以避免混用大小寫樣式。</span><span class="sxs-lookup"><span data-stu-id="1ead7-522">**Exception:** For legacy applications, you may use title-style capitalization if necessary to avoid mixing capitalization styles.</span></span>

### <a name="menu-category-names"></a><span data-ttu-id="1ead7-523">功能表分類名稱</span><span class="sxs-lookup"><span data-stu-id="1ead7-523">Menu category names</span></span>

-   <span data-ttu-id="1ead7-524">**使用屬於單一單字動詞或名詞的功能表分類名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-524">**Use menu category names that are single word verbs or nouns.**</span></span> <span data-ttu-id="1ead7-525">多個單字標籤可能會混淆 2 1-字組標籤。</span><span class="sxs-lookup"><span data-stu-id="1ead7-525">A multiple-word label might be confused for two one-word labels.</span></span>
-   <span data-ttu-id="1ead7-526">**偏好以動詞為基礎的功能表名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-526">**Prefer verb-based menu names.**</span></span> <span data-ttu-id="1ead7-527">但是，如果動詞命令是建立、顯示、查看或管理，請省略該動詞。</span><span class="sxs-lookup"><span data-stu-id="1ead7-527">However, omit the verb if it is Create, Show, View, or Manage.</span></span> <span data-ttu-id="1ead7-528">例如，下列功能表分類沒有動詞：</span><span class="sxs-lookup"><span data-stu-id="1ead7-528">For example, the following menu categories don't have verbs:</span></span>
    -   <span data-ttu-id="1ead7-529">資料表</span><span class="sxs-lookup"><span data-stu-id="1ead7-529">Table</span></span>
    -   <span data-ttu-id="1ead7-530">工具</span><span class="sxs-lookup"><span data-stu-id="1ead7-530">Tools</span></span>
    -   <span data-ttu-id="1ead7-531">時間範圍</span><span class="sxs-lookup"><span data-stu-id="1ead7-531">Window</span></span>
-   <span data-ttu-id="1ead7-532">若為非標準的分類名稱，請 **使用可清楚且準確地描述功能表內容的單一特定單字。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-532">For non-standard category names, **use a single, specific word that clearly and accurately describes the menu contents.**</span></span> <span data-ttu-id="1ead7-533">雖然這些名稱不一定要用來描述功能表中的所有專案，但它們應該是可預測的，如此一來，使用者在功能表中找到的內容就不會驚訝。</span><span class="sxs-lookup"><span data-stu-id="1ead7-533">While the names don't have to be so general that they describe everything in the menu, they should be predictable enough so that users aren't surprised by what they find in the menu.</span></span>

### <a name="menu-item-names"></a><span data-ttu-id="1ead7-534">功能表項目名稱</span><span class="sxs-lookup"><span data-stu-id="1ead7-534">Menu item names</span></span>

-   <span data-ttu-id="1ead7-535">**使用以動詞、名詞或名詞片語開頭的功能表項目名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-535">**Use menu item names that start with a verb, noun, or noun phrase.**</span></span>
-   <span data-ttu-id="1ead7-536">**偏好以動詞為基礎的功能表名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-536">**Prefer verb-based menu names.**</span></span> <span data-ttu-id="1ead7-537">但是，如果有下列情況，請省略動詞：</span><span class="sxs-lookup"><span data-stu-id="1ead7-537">However, omit the verb if:</span></span>
    -   <span data-ttu-id="1ead7-538">**此動詞命令為 Create、Show、View 或 Manage。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-538">**The verb is Create, Show, View, or Manage.**</span></span> <span data-ttu-id="1ead7-539">例如，下列命令沒有動詞：</span><span class="sxs-lookup"><span data-stu-id="1ead7-539">For example, the following commands don't have verbs:</span></span>
        -   <span data-ttu-id="1ead7-540">關於</span><span class="sxs-lookup"><span data-stu-id="1ead7-540">About</span></span>
        -   <span data-ttu-id="1ead7-541">進階</span><span class="sxs-lookup"><span data-stu-id="1ead7-541">Advanced</span></span>
        -   <span data-ttu-id="1ead7-542">全螢幕</span><span class="sxs-lookup"><span data-stu-id="1ead7-542">Full screen</span></span>
        -   <span data-ttu-id="1ead7-543">新增</span><span class="sxs-lookup"><span data-stu-id="1ead7-543">New</span></span>
        -   <span data-ttu-id="1ead7-544">選項</span><span class="sxs-lookup"><span data-stu-id="1ead7-544">Options</span></span>
        -   <span data-ttu-id="1ead7-545">屬性</span><span class="sxs-lookup"><span data-stu-id="1ead7-545">Properties</span></span>
    -   <span data-ttu-id="1ead7-546">**動詞與功能表分類名稱相同，以避免重複。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-546">**The verb is the same as the menu category name to avoid repetition.**</span></span> <span data-ttu-id="1ead7-547">例如，在 [插入] 功能表分類中，請使用 [文字]、[資料表] 和 [圖片]，而非 [插入文字]、[插入表格] 和 [插入圖片]</span><span class="sxs-lookup"><span data-stu-id="1ead7-547">For example, in the Insert menu category, use Text, Table, and Picture instead of Insert text, Insert table, and Insert picture.</span></span>
-   <span data-ttu-id="1ead7-548">**使用特定的動詞命令。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-548">**Use specific verbs.**</span></span> <span data-ttu-id="1ead7-549">避免泛型、無用動詞，例如變更和管理。</span><span class="sxs-lookup"><span data-stu-id="1ead7-549">Avoid generic, unhelpful verbs, such as Change and Manage.</span></span>
-   <span data-ttu-id="1ead7-550">**針對適用于單一物件的命令使用單數名詞**，否則請使用複數名詞。</span><span class="sxs-lookup"><span data-stu-id="1ead7-550">**Use singular nouns for commands that apply to a single object**, otherwise use plural nouns.</span></span>
-   <span data-ttu-id="1ead7-551">**請視需要使用修飾詞來區別類似的命令。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-551">**Use modifiers as necessary to distinguish between similar commands.**</span></span> <span data-ttu-id="1ead7-552">範例：上面的插入資料列，在下方插入資料列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-552">Examples: Insert row above, Insert row below.</span></span>
-   <span data-ttu-id="1ead7-553">**針對互補命令配對，選擇清楚互補的名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-553">**For pairs of complementary commands, choose clearly complementary names.**</span></span> <span data-ttu-id="1ead7-554">範例：新增、移除、顯示、隱藏;Insert、Delete。</span><span class="sxs-lookup"><span data-stu-id="1ead7-554">Examples: Add, Remove; Show, Hide; Insert, Delete.</span></span>
-   <span data-ttu-id="1ead7-555">**根據使用者目標和工作（而非技術），選擇功能表項目名稱。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-555">**Choose menu item names based on user goals and tasks, not on technology.**</span></span>

<span data-ttu-id="1ead7-556">**正確：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-556">**Correct:**</span></span>

![<span data-ttu-id="1ead7-557">具有格式功能表項目的 [rip] 功能表螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-557">screen shot of rip menu with format menu item</span></span> ](images/cmd-menus-image16.png)

<span data-ttu-id="1ead7-558">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-558">**Incorrect:**</span></span>

![<span data-ttu-id="1ead7-559">具有編解碼器功能表項目的 [rip] 功能表螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-559">screen shot of rip menu with codec menu item</span></span> ](images/cmd-menus-image17.png)

<span data-ttu-id="1ead7-560">在不正確的範例中，功能表項目是以其技術為基礎。</span><span class="sxs-lookup"><span data-stu-id="1ead7-560">In the incorrect example, the menu item is based on its technology.</span></span>

-   <span data-ttu-id="1ead7-561">針對指定的目的使用下列功能表項目名稱：</span><span class="sxs-lookup"><span data-stu-id="1ead7-561">Use the following menu item names for the stated purpose:</span></span>
    -   <span data-ttu-id="1ead7-562">**選項** 以顯示程式選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-562">**Options** To display program options.</span></span>
    -   <span data-ttu-id="1ead7-563">**自訂** 顯示特別與機械 UI 設定相關的程式選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-563">**Customize** To display the program options specifically related to mechanical UI configuration.</span></span>
    -   <span data-ttu-id="1ead7-564">**個人** 化顯示常用 [個人](glossary.md) 化設定的摘要。</span><span class="sxs-lookup"><span data-stu-id="1ead7-564">**Personalize** To display a summary of commonly used [personalization](glossary.md) settings.</span></span>
    -   <span data-ttu-id="1ead7-565">**喜好** 設定請勿使用。</span><span class="sxs-lookup"><span data-stu-id="1ead7-565">**Preferences** Don't use.</span></span> <span data-ttu-id="1ead7-566">請改用選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-566">Use Options instead.</span></span>
    -   <span data-ttu-id="1ead7-567">**屬性** 以顯示物件的屬性視窗。</span><span class="sxs-lookup"><span data-stu-id="1ead7-567">**Properties** To display an object's property window.</span></span>
    -   <span data-ttu-id="1ead7-568">**設定** 請勿使用做為功能表標籤。</span><span class="sxs-lookup"><span data-stu-id="1ead7-568">**Settings** Don't use as a menu label.</span></span> <span data-ttu-id="1ead7-569">請改用選項。</span><span class="sxs-lookup"><span data-stu-id="1ead7-569">Use Options instead.</span></span>

### <a name="submenu-names"></a><span data-ttu-id="1ead7-570">子功能表名稱</span><span class="sxs-lookup"><span data-stu-id="1ead7-570">Submenu names</span></span>

-   <span data-ttu-id="1ead7-571">**顯示子功能表的功能表項目在其標籤上絕對沒有省略號。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-571">**Menu items that display submenus never have an ellipsis on their label.**</span></span> <span data-ttu-id="1ead7-572">子功能表箭號表示需要另一個選取專案。</span><span class="sxs-lookup"><span data-stu-id="1ead7-572">The submenu arrow indicates that another selection is required.</span></span>

<span data-ttu-id="1ead7-573">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="1ead7-573">**Incorrect:**</span></span>

![<span data-ttu-id="1ead7-574">具有省略號的新功能表項目的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1ead7-574">screen shot of new menu item with ellipsis</span></span> ](images/cmd-menus-image18.png)

<span data-ttu-id="1ead7-575">在此範例中，新的功能表項目不正確地有省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-575">In this example, the New menu item incorrectly has an ellipsis.</span></span>

## <a name="documentation"></a><span data-ttu-id="1ead7-576">文件</span><span class="sxs-lookup"><span data-stu-id="1ead7-576">Documentation</span></span>

<span data-ttu-id="1ead7-577">參考功能表時：</span><span class="sxs-lookup"><span data-stu-id="1ead7-577">When referring to menus:</span></span>

-   <span data-ttu-id="1ead7-578">在顯示或隱藏功能表的命令中，請參閱功能表列。</span><span class="sxs-lookup"><span data-stu-id="1ead7-578">In commands that show or hide menus, refer to menu bars.</span></span> <span data-ttu-id="1ead7-579">請勿以傳統功能表的形式來參考它們。</span><span class="sxs-lookup"><span data-stu-id="1ead7-579">Don't refer to them as classic menus.</span></span>
-   <span data-ttu-id="1ead7-580">依其標籤來參考功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-580">Refer to menus by their labels.</span></span> <span data-ttu-id="1ead7-581">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線或省略號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-581">Use the exact label text, including its capitalization, but don't include the access key underscore or ellipsis.</span></span>
-   <span data-ttu-id="1ead7-582">若要參考功能表分類，請使用 [在 <category name> 功能表上]。</span><span class="sxs-lookup"><span data-stu-id="1ead7-582">To refer to menu categories, use "On the <category name> menu."</span></span> <span data-ttu-id="1ead7-583">如果內容中的功能表項目位置清楚，您就不需要提及功能表分類。</span><span class="sxs-lookup"><span data-stu-id="1ead7-583">If the location of a menu item is clear from the context, you don't need to mention the menu category.</span></span>
-   <span data-ttu-id="1ead7-584">若要描述功能表項目的使用者互動，請在不使用 word 功能表或命令的情況下，使用 click。</span><span class="sxs-lookup"><span data-stu-id="1ead7-584">To describe user interaction of menu items, use click, without the word menu or command.</span></span> <span data-ttu-id="1ead7-585">請勿使用 [選擇]、[選取] 或 [挑選]。</span><span class="sxs-lookup"><span data-stu-id="1ead7-585">Don't use choose, select, or pick.</span></span> <span data-ttu-id="1ead7-586">除了技術檔之外，請不要將功能表項目稱為功能表項目。</span><span class="sxs-lookup"><span data-stu-id="1ead7-586">Don't refer to a menu item as a menu item except in technical documentation.</span></span>
-   <span data-ttu-id="1ead7-587">若要描述從功能表選項中移除核取記號，請使用按一下以移除核取記號。</span><span class="sxs-lookup"><span data-stu-id="1ead7-587">To describe removing a check mark from a menu option, use click to remove the check mark.</span></span> <span data-ttu-id="1ead7-588">請勿使用 clear。</span><span class="sxs-lookup"><span data-stu-id="1ead7-588">Don't use clear.</span></span>
-   <span data-ttu-id="1ead7-589">以操作功能表的形式來參考內容功能表，而不是快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-589">Refer to context menus as context menus, not shortcut menus.</span></span>
-   <span data-ttu-id="1ead7-590">除非在程式設計檔中，否則請不要使用串聯、下拉式、下拉式或快顯來描述功能表。</span><span class="sxs-lookup"><span data-stu-id="1ead7-590">Don't use cascading, pull-down, drop-down, or pop-up to describe menus, except in programming documentation.</span></span>
-   <span data-ttu-id="1ead7-591">請參閱無法使用的功能表項目，而不是灰色、已停用或灰色。</span><span class="sxs-lookup"><span data-stu-id="1ead7-591">Refer to unavailable menu items as unavailable, not as dimmed, disabled, or grayed.</span></span> <span data-ttu-id="1ead7-592">在程式設計檔中使用 disabled。</span><span class="sxs-lookup"><span data-stu-id="1ead7-592">Use disabled in programming documentation.</span></span>
-   <span data-ttu-id="1ead7-593">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="1ead7-593">When possible, format the labels using bold text.</span></span> <span data-ttu-id="1ead7-594">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="1ead7-594">Otherwise, put the labels in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="1ead7-595">範例：</span><span class="sxs-lookup"><span data-stu-id="1ead7-595">Examples:</span></span>

-   <span data-ttu-id="1ead7-596">在 [檔案] 功能表上，按一下 [**列印**] 以 **列印檔案。**</span><span class="sxs-lookup"><span data-stu-id="1ead7-596">On the **File** menu, click **Print** to print the document.</span></span>
-   <span data-ttu-id="1ead7-597">在 [ **View** ] 功能表上，指向 [ **工具列**]，然後按一下 [ **格式化**]。</span><span class="sxs-lookup"><span data-stu-id="1ead7-597">On the **View** menu, point to **Toolbars**, and then click **Formatting**.</span></span>

 

