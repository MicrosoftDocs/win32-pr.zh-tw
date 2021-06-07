---
title: " (設計基本概念的對話方塊) "
description: 對話方塊是一種次要視窗，可讓使用者執行命令、詢問使用者問題，或是為使用者提供資訊或進度的意見反應。
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0e0deb28a706436e4d33ece35a40c26bd7499e0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444849"
---
# <a name="dialog-boxes-design-basics"></a><span data-ttu-id="a356f-103"> (設計基本概念的對話方塊) </span><span class="sxs-lookup"><span data-stu-id="a356f-103">Dialog Boxes (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="a356f-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="a356f-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="a356f-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="a356f-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="a356f-106">對話方塊是一種次要視窗，可讓使用者執行命令、詢問使用者問題，或是為使用者提供資訊或進度的意見反應。</span><span class="sxs-lookup"><span data-stu-id="a356f-106">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span>

![<span data-ttu-id="a356f-107">螢幕擷取畫面的識別對話方塊元素</span><span class="sxs-lookup"><span data-stu-id="a356f-107">screen shot identifying dialog box elements</span></span> ](images/win-dialog-box-image1.png)

<span data-ttu-id="a356f-108">一般的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-108">A typical dialog box.</span></span>

<span data-ttu-id="a356f-109">對話方塊包含標題列 (用來識別對話方塊來自) 的命令、功能或程式、選擇性的主要指示 (以對話方塊來說明使用者的目標) 、內容區域中的各種控制項 (顯示選項) 和認可按鈕 (表示使用者想要如何認可至工作) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-109">Dialog boxes consist of a title bar (to identify the command, feature, or program where a dialog box came from), an optional main instruction (to explain the user's objective with the dialog box), various controls in the content area (to present options), and commit buttons (to indicate how the user wants to commit to the task).</span></span>

<span data-ttu-id="a356f-110">對話方塊有兩種基本類型：</span><span class="sxs-lookup"><span data-stu-id="a356f-110">Dialog boxes have two fundamental types:</span></span>

-   <span data-ttu-id="a356f-111">**強制回應對話方塊** 需要使用者完成和關閉，才能繼續使用擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="a356f-111">**Modal dialog boxes** require users to complete and close before continuing with the owner window.</span></span> <span data-ttu-id="a356f-112">這些對話方塊最適合用於需要完成的重要或不頻繁的一次性工作，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="a356f-112">These dialog boxes are best used for critical or infrequent, one-off tasks that require completion before continuing.</span></span>
-   <span data-ttu-id="a356f-113">非 **強制回應對話方塊** 可讓使用者視需要在對話方塊和擁有者視窗之間切換。</span><span class="sxs-lookup"><span data-stu-id="a356f-113">**Modeless dialog boxes** allow users to switch between the dialog box and the owner window as desired.</span></span> <span data-ttu-id="a356f-114">這些對話方塊最適合用來進行頻繁、重複的持續工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-114">These dialog boxes are best used for frequent, repetitive, on-going tasks.</span></span>

<span data-ttu-id="a356f-115">**工作對話方塊是使用工作對話方塊應用程式開發介面 (API) 來執行的對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-115">**A task dialog is a dialog box implemented using the task dialog application programming interface (API).**</span></span> <span data-ttu-id="a356f-116">它們是由下列元件所組成，這些元件可以組合成各種不同的組合：</span><span class="sxs-lookup"><span data-stu-id="a356f-116">They consist of the following parts, which can be assembled in a variety of combinations:</span></span>

-   <span data-ttu-id="a356f-117">**標題列**，用來識別對話方塊來源的應用程式或系統功能。</span><span class="sxs-lookup"><span data-stu-id="a356f-117">A **title bar** to identify the application or system feature where the dialog box came from.</span></span>
-   <span data-ttu-id="a356f-118">具有選擇性圖示的 **主要指示**，用來識別使用者在對話方塊中的目標。</span><span class="sxs-lookup"><span data-stu-id="a356f-118">A **main instruction**, with an optional icon, to identify the user's objective with the dialog.</span></span>
-   <span data-ttu-id="a356f-119">描述資訊和控制項的 **內容區域** 。</span><span class="sxs-lookup"><span data-stu-id="a356f-119">A **content area** for descriptive information and controls.</span></span>
-   <span data-ttu-id="a356f-120">認可按鈕的 **命令區域** ，包括 [取消] 按鈕，以及其他選擇性的選項但不顯示</span><span class="sxs-lookup"><span data-stu-id="a356f-120">A **command area** for commit buttons, including a Cancel button, and optional More options and Don't show this</span></span> <item> <span data-ttu-id="a356f-121">同樣的控制項。</span><span class="sxs-lookup"><span data-stu-id="a356f-121">again controls.</span></span>
-   <span data-ttu-id="a356f-122">選擇性的其他說明和說明的 **註腳區域** ，通常以較不具經驗的使用者為目標。</span><span class="sxs-lookup"><span data-stu-id="a356f-122">A **footnote area** for optional additional explanations and help, typically targeted at less experienced users.</span></span>

![<span data-ttu-id="a356f-123">一般工作對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-123">screen shot of a typical task dialog box</span></span> ](images/win-dialog-box-image2.png)

<span data-ttu-id="a356f-124">一般工作對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-124">A typical task dialog.</span></span>

<span data-ttu-id="a356f-125">**建議您盡可能使用工作對話方塊，因為這些對話方塊很容易建立，且能達到一致的外觀。**</span><span class="sxs-lookup"><span data-stu-id="a356f-125">**Task dialogs are recommended whenever appropriate because they are easy to create and they achieve a consistent look.**</span></span> <span data-ttu-id="a356f-126">工作對話方塊需要 Windows Vista 或更新版本，因此不適用於舊版的 Microsoft Windows。</span><span class="sxs-lookup"><span data-stu-id="a356f-126">Task dialogs do require Windows Vista or later, so they aren't suitable for earlier versions of Microsoft Windows.</span></span>

<span data-ttu-id="a356f-127">工作窗格就像對話方塊一樣，不同之處在于它會在視窗窗格中顯示，而不是在另一個視窗中顯示。</span><span class="sxs-lookup"><span data-stu-id="a356f-127">A task pane is like a dialog box, except that it is presented within a window pane instead of a separate window.</span></span> <span data-ttu-id="a356f-128">如此一來，工作窗格就會有比對話方塊更直接、內容相關的感覺。</span><span class="sxs-lookup"><span data-stu-id="a356f-128">As a result, task panes have a more direct, contextual feel than dialog boxes.</span></span> <span data-ttu-id="a356f-129">雖然技術上來說並不相同，但是工作 **窗格也類似于在本文中提供其指導方針的對話方塊**。</span><span class="sxs-lookup"><span data-stu-id="a356f-129">Even though technically they are not the same, **task panes are so similar to dialog boxes that their guidelines are presented in this article**.</span></span>

![<span data-ttu-id="a356f-130">一般工作窗格的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-130">screen shot of a typical task pane</span></span> ](images/win-dialog-box-image3.png)

<span data-ttu-id="a356f-131">典型的工作窗格。</span><span class="sxs-lookup"><span data-stu-id="a356f-131">A typical task pane.</span></span>

<span data-ttu-id="a356f-132">[[屬性視窗](win-property-win.md)] 是一種特製化的對話方塊類型，可用來查看和變更物件、物件集合或程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="a356f-132">[Property windows](win-property-win.md) are a specialized type of dialog box used to view and change properties for an object, collection of objects, or a program.</span></span> <span data-ttu-id="a356f-133">此外，屬性視窗通常支援數個工作，而對話方塊通常支援工作中的單一工作或步驟。</span><span class="sxs-lookup"><span data-stu-id="a356f-133">Additionally, property windows typically support several tasks, whereas dialog boxes typically support a single task or step in a task.</span></span> <span data-ttu-id="a356f-134">因為其使用方式是特製化的，所以 **屬性視窗會以一組不同的指導方針來涵蓋**。</span><span class="sxs-lookup"><span data-stu-id="a356f-134">Because their usage is specialized, **property windows are covered in a different set of guidelines**.</span></span>

<span data-ttu-id="a356f-135">對話方塊 [可以有索引](ctrl-tabs.md)標籤，如果是，則稱為索引標籤式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-135">Dialog boxes can have [tabs](ctrl-tabs.md), and if so they are called tabbed dialog boxes.</span></span> <span data-ttu-id="a356f-136">屬性視窗取決於屬性的內容呈現，而不是使用索引標籤。</span><span class="sxs-lookup"><span data-stu-id="a356f-136">Property windows are determined by their presentation of properties, not by the use of tabs.</span></span>

<span data-ttu-id="a356f-137">**注意：** 與 [版面](vis-layout.md)配置、 [視窗管理](win-window-mgt.md)、通用對話方塊、 [屬性視窗](win-property-win.md)、 [嚮導](win-wizards.md)、 [確認](mess-confirm.md)、 [錯誤訊息](mess-error.md)和 [警告訊息](mess-warn.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="a356f-137">**Note:** Guidelines related to [layout](vis-layout.md), [window management](win-window-mgt.md), common dialog boxes, [property windows](win-property-win.md), [wizards](win-wizards.md), [confirmations](mess-confirm.md), [error messages](mess-error.md), and [warning messages](mess-warn.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="a356f-138">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="a356f-138">Is this the right user interface?</span></span>

<span data-ttu-id="a356f-139">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="a356f-139">To decide, consider these questions:</span></span>

-   <span data-ttu-id="a356f-140">**這是為使用者提供資訊、詢問使用者問題，還是允許使用者選取選項來執行命令或工作的目的？**</span><span class="sxs-lookup"><span data-stu-id="a356f-140">**Is the purpose to provide users with information, ask users a question, or allow users to select options to perform a command or task?**</span></span> <span data-ttu-id="a356f-141">如果沒有，請使用 (UI) 的其他使用者介面。</span><span class="sxs-lookup"><span data-stu-id="a356f-141">If not, use another user interface (UI).</span></span>
-   <span data-ttu-id="a356f-142">**這是用來查看和變更物件、物件集合或程式之屬性的用途嗎？**</span><span class="sxs-lookup"><span data-stu-id="a356f-142">**Is the purpose to view and change properties for an object, collection of objects, or a program?**</span></span> <span data-ttu-id="a356f-143">如果是的話，請改用 [屬性視窗](win-property-win.md) 或 [工具列](cmd-toolbars.md) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-143">If so, use a [property window](win-property-win.md) or [toolbar](cmd-toolbars.md) instead.</span></span>
-   <span data-ttu-id="a356f-144">**用來呈現命令或工具集合的目的是什麼？**</span><span class="sxs-lookup"><span data-stu-id="a356f-144">**Is the purpose to present a collection of commands or tools?**</span></span> <span data-ttu-id="a356f-145">如果是的話，請使用工具列或 [ [調色板] 視窗](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-145">If so, use a toolbar or [palette window](glossary.md).</span></span>
-   <span data-ttu-id="a356f-146">**驗證使用者是否想要繼續進行動作的目的是要驗證嗎？**</span><span class="sxs-lookup"><span data-stu-id="a356f-146">**Is the purpose to verify that the user wants to proceed with an action?**</span></span> <span data-ttu-id="a356f-147">是否有清楚的理由不會繼續進行，而且有時候使用者可能不會有合理的可能性？</span><span class="sxs-lookup"><span data-stu-id="a356f-147">Is there a clear reason not to proceed and a reasonable chance that sometimes users won't?</span></span> <span data-ttu-id="a356f-148">若是如此，請使用 [確認](mess-confirm.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-148">If so, use a [confirmation](mess-confirm.md).</span></span>
-   <span data-ttu-id="a356f-149">**提供錯誤或警告訊息的目的是什麼？**</span><span class="sxs-lookup"><span data-stu-id="a356f-149">**Is the purpose to give an error or warning message?**</span></span> <span data-ttu-id="a356f-150">如果是的話，請使用 [錯誤訊息](mess-error.md) 或 [警告訊息](mess-warn.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-150">If so, use an [error message](mess-error.md) or [warning message](mess-warn.md).</span></span>
-   <span data-ttu-id="a356f-151">的目的是要：</span><span class="sxs-lookup"><span data-stu-id="a356f-151">Is the purpose to:</span></span>
    -   <span data-ttu-id="a356f-152">開啟檔案</span><span class="sxs-lookup"><span data-stu-id="a356f-152">Open files</span></span>
    -   <span data-ttu-id="a356f-153">儲存檔案</span><span class="sxs-lookup"><span data-stu-id="a356f-153">Save files</span></span>
    -   <span data-ttu-id="a356f-154">開啟資料夾</span><span class="sxs-lookup"><span data-stu-id="a356f-154">Open folders</span></span>
    -   <span data-ttu-id="a356f-155">尋找或取代文字</span><span class="sxs-lookup"><span data-stu-id="a356f-155">Find or replace text</span></span>
    -   <span data-ttu-id="a356f-156">列印檔案</span><span class="sxs-lookup"><span data-stu-id="a356f-156">Print a document</span></span>
    -   <span data-ttu-id="a356f-157">選取列印頁面的屬性</span><span class="sxs-lookup"><span data-stu-id="a356f-157">Select attributes of a printed page</span></span>
    -   <span data-ttu-id="a356f-158">選取字型</span><span class="sxs-lookup"><span data-stu-id="a356f-158">Select a font</span></span>
    -   <span data-ttu-id="a356f-159">選擇色彩</span><span class="sxs-lookup"><span data-stu-id="a356f-159">Choose a color</span></span>
    -   <span data-ttu-id="a356f-160">流覽檔案、資料夾、電腦或印表機</span><span class="sxs-lookup"><span data-stu-id="a356f-160">Browse for a file, folder, computer, or printer</span></span>
    -   <span data-ttu-id="a356f-161">搜尋 Microsoft Active Directory 中的使用者、電腦或群組</span><span class="sxs-lookup"><span data-stu-id="a356f-161">Search for users, computers, or groups in Microsoft Active Directory</span></span>
    -   <span data-ttu-id="a356f-162">提示輸入使用者名稱和密碼嗎？</span><span class="sxs-lookup"><span data-stu-id="a356f-162">Prompt for a user name and password?</span></span>

<span data-ttu-id="a356f-163">若是如此，請改用適當的 [通用對話方塊](win-common-dlg.md) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-163">If so, use the appropriate [common dialog](win-common-dlg.md) instead.</span></span> <span data-ttu-id="a356f-164">其中許多常見的對話方塊都是可擴充的。</span><span class="sxs-lookup"><span data-stu-id="a356f-164">Many of these common dialogs are extensible.</span></span>

-   <span data-ttu-id="a356f-165">**執行需要多個單一視窗的多步驟工作的目的是什麼？**</span><span class="sxs-lookup"><span data-stu-id="a356f-165">**Is the purpose to perform a multi-step task that requires more than a single window?**</span></span> <span data-ttu-id="a356f-166">若是如此，請改用工作 [流程](glossary.md) 或 [wizard](win-wizards.md) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-166">If so, use a [task flow](glossary.md) or [wizard](win-wizards.md) instead.</span></span>
-   <span data-ttu-id="a356f-167">**這是用來通知使用者與目前使用者活動不相關的系統或程式事件的目的，而不需要立即的使用者動作，而且使用者可以自由地略過？**</span><span class="sxs-lookup"><span data-stu-id="a356f-167">**Is the purpose to inform users of a system or program event that isn't related to the current user activity, that doesn't require immediate user action, and users can freely ignore?**</span></span> <span data-ttu-id="a356f-168">若是如此，請改為使用 [通知](mess-notif.md) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-168">If so, use a [notification](mess-notif.md) instead.</span></span>
-   <span data-ttu-id="a356f-169">**顯示程式狀態的目的是什麼？**</span><span class="sxs-lookup"><span data-stu-id="a356f-169">**Is the purpose to show program status?**</span></span> <span data-ttu-id="a356f-170">若是如此，請改用 [狀態列](ctrl-status-bars.md) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-170">If so, use a [status bar](ctrl-status-bars.md) instead.</span></span>
-   <span data-ttu-id="a356f-171">**最好使用就地 UI 嗎？**</span><span class="sxs-lookup"><span data-stu-id="a356f-171">**Would it be preferable to use in-place UI?**</span></span> <span data-ttu-id="a356f-172">對話方塊可以藉由要求注意來中斷使用者的流程。</span><span class="sxs-lookup"><span data-stu-id="a356f-172">Dialog boxes can break the user's flow by demanding attention.</span></span> <span data-ttu-id="a356f-173">有時候，流程中的中斷會對齊，例如，當使用者必須執行目前內容以外的動作時。</span><span class="sxs-lookup"><span data-stu-id="a356f-173">Sometimes that break in flow is justified, such as when the user must perform an action that is outside the current context.</span></span> <span data-ttu-id="a356f-174">在其他情況下，更好的方法是將 UI 呈現在內容中，不論是直接使用就地 UI (（例如工作窗格) ），或是使用 [漸進式洩漏](ctrl-progressive-disclosure-controls.md)的隨選。</span><span class="sxs-lookup"><span data-stu-id="a356f-174">In other cases, a better approach is to present the UI in context, either directly with in-place UI (such as a task pane), or on demand using [progressive disclosure](ctrl-progressive-disclosure-controls.md).</span></span>
-   <span data-ttu-id="a356f-175">**顯示非關鍵性使用者輸入問題或特殊條件的目的為何？**</span><span class="sxs-lookup"><span data-stu-id="a356f-175">**Is the purpose to display a non-critical user input problem or special condition?**</span></span> <span data-ttu-id="a356f-176">如果是的話，請改用 [球形球形](ctrl-balloons.md) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-176">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="a356f-177">**針對工作流程，最好使用其他頁面嗎？**</span><span class="sxs-lookup"><span data-stu-id="a356f-177">**For task flows, would it be preferable to use another page?**</span></span> <span data-ttu-id="a356f-178">一般來說，您會想要讓工作在單一視窗內從頁面流向頁面。</span><span class="sxs-lookup"><span data-stu-id="a356f-178">Generally you want a task to flow from page to page within a single window.</span></span> <span data-ttu-id="a356f-179">您可以使用對話方塊來確認就地命令、取得就地命令的輸入，以及執行最適合在主要工作流程之外獨立完成的次要獨立工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-179">Use dialog boxes to confirm in-place commands, to get input for in-place commands, and to perform secondary, stand-alone tasks that are best done independently and outside the main task flow.</span></span>
-   <span data-ttu-id="a356f-180">**針對選取選項，使用者是否有可能變更選項？**</span><span class="sxs-lookup"><span data-stu-id="a356f-180">**For selecting options, are users likely to change the options?**</span></span> <span data-ttu-id="a356f-181">如果沒有，請考慮替代方案，例如：</span><span class="sxs-lookup"><span data-stu-id="a356f-181">If not, consider alternatives, such as:</span></span>
    -   <span data-ttu-id="a356f-182">使用預設選項而不要求，但允許使用者稍後進行變更。</span><span class="sxs-lookup"><span data-stu-id="a356f-182">Using the default options without asking, but allowing users to make changes later.</span></span>
    -   <span data-ttu-id="a356f-183">提供具有選項的版本 (例如，在功能表中的 [ **列印 ...** ]) 以及沒有選項的版本 (例如，在工具列) 中 **列印** 。</span><span class="sxs-lookup"><span data-stu-id="a356f-183">Providing a version with options (for example, **Print...** in a menu) as well as a version without options (for example, **Print** in the toolbar).</span></span> <span data-ttu-id="a356f-184">一般情況下，工具列命令應該是立即的，避免顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-184">Generally, toolbar commands should be immediate and avoid displaying dialog boxes.</span></span>
-   <span data-ttu-id="a356f-185">**針對選取選項，是否有更簡單、更直接的方式來呈現選項？**</span><span class="sxs-lookup"><span data-stu-id="a356f-185">**For selecting options, is there a simpler, more direct way to present the options?**</span></span> <span data-ttu-id="a356f-186">若是如此，請考慮替代方案，例如：</span><span class="sxs-lookup"><span data-stu-id="a356f-186">If so, consider alternatives, such as:</span></span>
    -   <span data-ttu-id="a356f-187">使用 [分割按鈕](ctrl-command-buttons.md) 選取命令的變化。</span><span class="sxs-lookup"><span data-stu-id="a356f-187">Using a [split button](ctrl-command-buttons.md) to select variations of a command.</span></span>
    -   <span data-ttu-id="a356f-188">針對命令、核取方塊、選項按鈕和簡單列表使用子功能表。</span><span class="sxs-lookup"><span data-stu-id="a356f-188">Using a submenu for commands, check boxes, radio buttons and simple lists.</span></span>

![顯示功能表和子功能表的螢幕擷取畫面。](images/win-dialog-box-image4.png)

![<span data-ttu-id="a356f-190">功能表和子功能表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-190">screen shot of a menu and submenu</span></span> ](images/win-dialog-box-image5.png)

<span data-ttu-id="a356f-191">在這些範例中，會使用子功能表，而不是對話方塊來進行簡單的選擇。</span><span class="sxs-lookup"><span data-stu-id="a356f-191">In these examples, submenus are used instead of dialog boxes for simple selections.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="a356f-192">設計概念</span><span class="sxs-lookup"><span data-stu-id="a356f-192">Design concepts</span></span>

<span data-ttu-id="a356f-193">適當地使用時，對話方塊是為您的程式提供強大功能和彈性的絕佳方法。</span><span class="sxs-lookup"><span data-stu-id="a356f-193">When properly used, dialog boxes are a great way to give power and flexibility to your program.</span></span> <span data-ttu-id="a356f-194">當誤用時，對話方塊可讓使用者更輕鬆地干擾使用者、中斷其流程，並讓程式感覺更容易使用。</span><span class="sxs-lookup"><span data-stu-id="a356f-194">When misused, dialog boxes are an easy way to annoy users, interrupt their flow, and make the program feel indirect and tedious to use.</span></span> <span data-ttu-id="a356f-195">**強制回應對話方塊會要求使用者注意。**</span><span class="sxs-lookup"><span data-stu-id="a356f-195">**Modal dialog boxes demand users' attention.**</span></span> <span data-ttu-id="a356f-196">對話方塊通常比替代 Ui 更容易執行，因此通常會過度採用。</span><span class="sxs-lookup"><span data-stu-id="a356f-196">Dialog boxes are often easier to implement than alternative UIs, so they tend to be overused.</span></span>

<span data-ttu-id="a356f-197">**當對話方塊的設計特性符合其使用方式時，對話方塊會最有效。**</span><span class="sxs-lookup"><span data-stu-id="a356f-197">**A dialog box is most effective when its design characteristics match its usage.**</span></span> <span data-ttu-id="a356f-198">對話方塊的設計主要取決於其用途 (可提供選項、提出問題、提供資訊或意見反應) 、輸入 (強制回應) 或非強制回應，以及 (必要的使用者互動、選擇性的回應或通知) ，而其使用方式主要取決於使用者或程式起始 (的內容、使用者動作的機率，以及顯示的頻率。</span><span class="sxs-lookup"><span data-stu-id="a356f-198">A dialog box's design is largely determined by its purpose (to offer options, ask questions, provide information or feedback), type (modal or modeless), and user interaction (required, optional response, or acknowledgment), whereas its usage is largely determined by its context (user or program initiated), probability of user action, and frequency of display.</span></span>

<span data-ttu-id="a356f-199">若要設計有效的對話方塊，請有效地使用下列元素：</span><span class="sxs-lookup"><span data-stu-id="a356f-199">To design effective dialog boxes, use the following elements effectively:</span></span>

-   <span data-ttu-id="a356f-200">對話方塊文字</span><span class="sxs-lookup"><span data-stu-id="a356f-200">Dialog box text</span></span>
-   <span data-ttu-id="a356f-201">主要指示</span><span class="sxs-lookup"><span data-stu-id="a356f-201">Main instructions</span></span>
-   <span data-ttu-id="a356f-202">不要顯示此</span><span class="sxs-lookup"><span data-stu-id="a356f-202">Don't show this</span></span> <item> <span data-ttu-id="a356f-203">同樣的選項</span><span class="sxs-lookup"><span data-stu-id="a356f-203">again option</span></span>

<span data-ttu-id="a356f-204">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="a356f-204">**If you do only one thing...**</span></span>

<span data-ttu-id="a356f-205">確定您的對話方塊設計 (取決於其用途、類型和使用者互動) 符合其使用方式 (取決於其內容、使用者動作的機率，以及顯示) 的頻率。</span><span class="sxs-lookup"><span data-stu-id="a356f-205">Make sure that your dialog box design (determined by its purpose, type, and user interaction) matches its usage (determined by its context, probability of user action, and frequency of display).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="a356f-206">使用模式</span><span class="sxs-lookup"><span data-stu-id="a356f-206">Usage patterns</span></span>

<span data-ttu-id="a356f-207">對話方塊有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="a356f-207">Dialog boxes have several usage patterns:</span></span>

-   <span data-ttu-id="a356f-208">問題對話方塊 (使用按鈕) 詢問使用者單一問題或確認命令，並在水準排列的命令按鈕中使用簡單的回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-208">Question dialogs (using buttons) ask users a single question or to confirm a command, and use simple responses in horizontally arranged command buttons.</span></span>
-   <span data-ttu-id="a356f-209">問題對話方塊 (使用命令連結) 詢問使用者單一問題或選取要執行的工作，並在垂直排列的命令連結中使用詳細的回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-209">Question dialogs (using command links) ask users a single question or to select a task to perform, and use detailed responses in vertically arranged command links.</span></span>
-   <span data-ttu-id="a356f-210">選擇對話方塊會為使用者提供一組選項，通常可以更完整地指定命令。</span><span class="sxs-lookup"><span data-stu-id="a356f-210">Choice dialogs present users with a set of choices, usually to specify a command more completely.</span></span> <span data-ttu-id="a356f-211">不同于問題對話方塊，選擇對話方塊可以提出多個問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-211">Unlike question dialogs, choice dialogs can ask multiple questions.</span></span>
-   <span data-ttu-id="a356f-212">進度對話方塊讓使用者在冗長的作業期間提供進度回饋 (超過五秒的) ，以及取消或停止作業的命令。</span><span class="sxs-lookup"><span data-stu-id="a356f-212">Progress dialogs present users with progress feedback during a lengthy operation (longer than five seconds), along with a command to cancel or stop the operation.</span></span>
-   <span data-ttu-id="a356f-213">資訊對話方塊顯示使用者要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="a356f-213">Informational dialogs display information requested by the user.</span></span>

## <a name="guidelines"></a><span data-ttu-id="a356f-214">指導方針</span><span class="sxs-lookup"><span data-stu-id="a356f-214">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="a356f-215">一般</span><span class="sxs-lookup"><span data-stu-id="a356f-215">General</span></span>

-   <span data-ttu-id="a356f-216">**請勿使用可滾動的對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-216">**Don't use scrollable dialog boxes.**</span></span> <span data-ttu-id="a356f-217">請不要使用需要在正常使用期間完全查看捲軸的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-217">Don't use dialog boxes that require the use of a scroll bar to be viewed completely during normal usage.</span></span> <span data-ttu-id="a356f-218">請改為重新設計對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-218">Redesign the dialog box instead.</span></span> <span data-ttu-id="a356f-219">請考慮使用[漸進式洩漏](ctrl-progressive-disclosure-controls.md)[或索引](ctrl-tabs.md)標籤。</span><span class="sxs-lookup"><span data-stu-id="a356f-219">Consider using [progressive disclosure](ctrl-progressive-disclosure-controls.md) or [tabs](ctrl-tabs.md).</span></span>
-   <span data-ttu-id="a356f-220">**沒有功能表列或狀態列。**</span><span class="sxs-lookup"><span data-stu-id="a356f-220">**Don't have a menu bar or status bar.**</span></span> <span data-ttu-id="a356f-221">相反地，您可以直接在對話方塊本身或使用相關控制項上的內容功能表，提供命令和狀態的存取權。</span><span class="sxs-lookup"><span data-stu-id="a356f-221">Instead, provide access to commands and status directly on the dialog box itself, or by using context menus on the relevant controls.</span></span>

    -   <span data-ttu-id="a356f-222">**例外狀況：** 當使用對話方塊來執行主視窗 (（例如公用程式) ）時，可以接受功能表列。</span><span class="sxs-lookup"><span data-stu-id="a356f-222">**Exception:** Menu bars are acceptable when a dialog box is used to implement a primary window (such as a utility).</span></span>

    <span data-ttu-id="a356f-223">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-223">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-224">具有功能表列之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-224">screen shot of a dialog box with a menu bar</span></span> ](images/win-dialog-box-image6.png)

    <span data-ttu-id="a356f-225">在此範例中，[尋找憑證] 是具有功能表列的非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-225">In this example, Find Certificates is a modeless dialog box with a menu bar.</span></span>

-   <span data-ttu-id="a356f-226">如果對話方塊需要立即注意，而且程式未在使用中，請將 **其工作列按鈕閃爍三次，以醒目提示，並將其反白顯示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-226">If a dialog box requires immediate attention and the program isn't active, **flash its taskbar button three times to draw attention, and leave it highlighted.**</span></span> <span data-ttu-id="a356f-227">請勿執行任何動作：請勿還原或啟用視窗，也不會播放任何音效效果。</span><span class="sxs-lookup"><span data-stu-id="a356f-227">Don't do anything else: don't restore or activate the window and don't play any sound effects.</span></span> <span data-ttu-id="a356f-228">相反地，請考慮使用者的視窗狀態選擇，並讓使用者在準備就緒時啟動視窗。</span><span class="sxs-lookup"><span data-stu-id="a356f-228">Instead, respect the user's window state selection and let the user activate the window when ready.</span></span>
-   <span data-ttu-id="a356f-229">如需更多指導方針與範例，請參閱 [工作列](winenv-taskbar.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-229">For more guidelines and examples, see [Taskbar](winenv-taskbar.md).</span></span>

### <a name="modal-dialog-boxes"></a><span data-ttu-id="a356f-230">強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="a356f-230">Modal dialog boxes</span></span>

-   <span data-ttu-id="a356f-231">**用於需要完成的重要或不頻繁的一次性工作，再繼續進行。**</span><span class="sxs-lookup"><span data-stu-id="a356f-231">**Use for critical or infrequent, one-off tasks that require completion before continuing.**</span></span>
-   <span data-ttu-id="a356f-232">使用 [延遲的認可模型](glossary.md) ，讓變更在明確認可之前不會生效。</span><span class="sxs-lookup"><span data-stu-id="a356f-232">Use a [delayed commit model](glossary.md) so that changes don't take effect until explicitly committed.</span></span>
-   <span data-ttu-id="a356f-233">**在適當時使用工作對話方塊來達成一致的外觀。**</span><span class="sxs-lookup"><span data-stu-id="a356f-233">**Implement using a task dialog whenever appropriate to achieve a consistent look.**</span></span> <span data-ttu-id="a356f-234">工作對話方塊需要 Windows Vista 或更新版本，因此不適用於舊版 Windows。</span><span class="sxs-lookup"><span data-stu-id="a356f-234">Task dialogs do require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>

### <a name="modeless-dialog-boxes"></a><span data-ttu-id="a356f-235">非強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="a356f-235">Modeless dialog boxes</span></span>

-   <span data-ttu-id="a356f-236">**使用於頻繁、重複的持續工作。**</span><span class="sxs-lookup"><span data-stu-id="a356f-236">**Use for frequent, repetitive, on-going tasks.**</span></span>
-   <span data-ttu-id="a356f-237">使用 [立即認可模型](glossary.md) ，讓變更立即生效。</span><span class="sxs-lookup"><span data-stu-id="a356f-237">Use an [immediate commit model](glossary.md) so that changes take effect immediately.</span></span>
-   <span data-ttu-id="a356f-238">若為非強制回應對話方塊，請使用對話方塊中的明確關閉命令按鈕來關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="a356f-238">For modeless dialogs, use an explicit Close command button in the dialog to close the window.</span></span> <span data-ttu-id="a356f-239">針對這兩個專案，請使用標題列上的 [關閉] 按鈕來關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="a356f-239">For both, use a Close button on the title bar to close the window.</span></span>
-   <span data-ttu-id="a356f-240">**請考慮使非強制回應對話方塊可停駐。**</span><span class="sxs-lookup"><span data-stu-id="a356f-240">**Consider making modeless dialog boxes dockable.**</span></span> <span data-ttu-id="a356f-241">可停駐的非強制回應對話方塊允許更具彈性的放置。</span><span class="sxs-lookup"><span data-stu-id="a356f-241">Dockable modeless dialogs allow for more flexible placement.</span></span>

![<span data-ttu-id="a356f-242">可停駐、非強制回應對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-242">screen shot of a dockable, modeless dialog box</span></span> ](images/win-dialog-box-image7.png)

<span data-ttu-id="a356f-243">Microsoft Office 中使用的某些非強制回應對話方塊是可停駐的。</span><span class="sxs-lookup"><span data-stu-id="a356f-243">Some modeless dialog boxes used in Microsoft Office are dockable.</span></span>

### <a name="multiple-dialog-boxes"></a><span data-ttu-id="a356f-244">多個對話方塊</span><span class="sxs-lookup"><span data-stu-id="a356f-244">Multiple dialog boxes</span></span>

-   <span data-ttu-id="a356f-245">**不要一次從擁有者選擇對話方塊顯示一個以上擁有的選擇對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-245">**Don't display more than one owned choice dialog at a time from an owner choice dialog.**</span></span> <span data-ttu-id="a356f-246">顯示多個可讓使用者難以理解認可按鈕的意義。</span><span class="sxs-lookup"><span data-stu-id="a356f-246">Displaying more than one makes the meaning of the commit buttons difficult for users to understand.</span></span> <span data-ttu-id="a356f-247">您可以視需要顯示 (這類問題對話方塊) 的其他類型對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-247">You may display other types of dialog boxes (such question dialogs) as needed.</span></span>
-   <span data-ttu-id="a356f-248">**如需相關的對話順序，請考慮使用多頁對話方塊（如果可能的話）。**</span><span class="sxs-lookup"><span data-stu-id="a356f-248">**For a sequence of related dialogs, consider using a multi-page dialog if possible.**</span></span> <span data-ttu-id="a356f-249">如果沒有清楚相關，請使用個別的對話。</span><span class="sxs-lookup"><span data-stu-id="a356f-249">Use individual dialogs if they aren't clearly related.</span></span>

### <a name="multi-page-dialog-boxes"></a><span data-ttu-id="a356f-250">多頁對話方塊</span><span class="sxs-lookup"><span data-stu-id="a356f-250">Multi-page dialog boxes</span></span>

-   <span data-ttu-id="a356f-251">當您有下列相關頁面順序時，請使用多頁對話方塊，而不是個別的對話方塊：</span><span class="sxs-lookup"><span data-stu-id="a356f-251">Use a multi-page dialog box instead of individual dialog boxes when you have the following sequence of related pages:</span></span>
    -   <span data-ttu-id="a356f-252"> (選擇性的單一輸入頁面) </span><span class="sxs-lookup"><span data-stu-id="a356f-252">A single input page (optional)</span></span>
    -   <span data-ttu-id="a356f-253">進度頁面</span><span class="sxs-lookup"><span data-stu-id="a356f-253">A progress page</span></span>
    -   <span data-ttu-id="a356f-254">單一結果頁面</span><span class="sxs-lookup"><span data-stu-id="a356f-254">A single results page</span></span>

<span data-ttu-id="a356f-255">輸入頁面是選擇性的，因為工作可能已在其他地方起始。</span><span class="sxs-lookup"><span data-stu-id="a356f-255">The input page is optional because the task may have been initiated somewhere else.</span></span> <span data-ttu-id="a356f-256">**這樣做會讓產生的體驗變得穩定、簡單、輕巧的感覺。**</span><span class="sxs-lookup"><span data-stu-id="a356f-256">**Doing so gives the resulting experience a stable, simple, lightweight feel.**</span></span>

![<span data-ttu-id="a356f-257">進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-257">screen shot of a progress bar</span></span> ](images/win-dialog-box-image8.png)

![<span data-ttu-id="a356f-258">[找不到問題] 訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-258">screen shot of 'no problems found' message</span></span> ](images/win-dialog-box-image9.png)

<span data-ttu-id="a356f-259">在此範例中，Windows 網路診斷是由進度和結果頁面所組成。</span><span class="sxs-lookup"><span data-stu-id="a356f-259">In this example, Windows Network Diagnostics consists of progress and results pages.</span></span>

-   <span data-ttu-id="a356f-260">**如果輸入頁面是標準對話方塊，請勿使用多頁對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-260">**Don't use a multi-page dialog if the input page is a standard dialog.**</span></span> <span data-ttu-id="a356f-261">在此情況下，使用標準對話方塊的一致性比較重要。</span><span class="sxs-lookup"><span data-stu-id="a356f-261">In this case the consistency of using a standard dialog is more important.</span></span>
-   <span data-ttu-id="a356f-262">**請勿使用 [下一步] 或 [上一頁] 按鈕，而且沒有三個頁面。**</span><span class="sxs-lookup"><span data-stu-id="a356f-262">**Don't use Next or Back buttons and don't have more than three pages.**</span></span> <span data-ttu-id="a356f-263">多頁對話方塊適用于具有意見反應的單一步驟工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-263">Multi-page dialog boxes are for single-step tasks with feedback.</span></span> <span data-ttu-id="a356f-264">它們不是用來進行多步驟工作的「 [嚮導](win-wizards.md)」。</span><span class="sxs-lookup"><span data-stu-id="a356f-264">They aren't [wizards](win-wizards.md), which are used for multi-step tasks.</span></span> <span data-ttu-id="a356f-265">與多頁對話方塊相較之下，嚮導會有相當大的間接風格。</span><span class="sxs-lookup"><span data-stu-id="a356f-265">Wizards have a heavy, indirect feel compared to multi-page dialog boxes.</span></span>
-   <span data-ttu-id="a356f-266">**在 [輸入] 頁面上，使用特定的命令按鈕或命令連結來起始工作。**</span><span class="sxs-lookup"><span data-stu-id="a356f-266">**On the input page, use specific command buttons or command links to initiate the task.**</span></span>
-   <span data-ttu-id="a356f-267">**使用 [輸入] 和 [進度] 頁面上的 [取消] 按鈕，以及 [結果] 頁面上的 [關閉] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-267">**Use a Cancel button on the input and progress pages, and a Close button on the results page.**</span></span>

<span data-ttu-id="a356f-268">**開發人員：** 您可以使用 [TDM \_ 流覽 \_ 頁面](../controls/tdm-navigate-page.md) 訊息來建立多頁工作對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-268">**Developers:** You can create multi-page task dialogs using the [TDM\_NAVIGATE\_PAGE](../controls/tdm-navigate-page.md) message.</span></span>

### <a name="presentation"></a><span data-ttu-id="a356f-269">簡報</span><span class="sxs-lookup"><span data-stu-id="a356f-269">Presentation</span></span>

<span data-ttu-id="a356f-270">若要讓對話方塊易於尋找和存取，可清楚地將對話與其來源建立關聯，並與多個監視器搭配運作：</span><span class="sxs-lookup"><span data-stu-id="a356f-270">To make dialog boxes easy to find and access, clearly associate the dialog with its source, and work well with multiple monitors:</span></span>

-   <span data-ttu-id="a356f-271">**一開始會在主控視窗頂端顯示「置中」對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-271">**Initially display dialogs "centered" on top of the owner window.**</span></span> <span data-ttu-id="a356f-272">針對後續顯示，請考慮將它顯示在其最後一個位置 (相對於擁有者視窗) 如果這麼做，可能會比較方便。</span><span class="sxs-lookup"><span data-stu-id="a356f-272">For subsequent display, consider displaying it in its last location (relative to the owner window) if doing so is likely to be more convenient.</span></span>

![<span data-ttu-id="a356f-273">以視窗背後的視窗為中心的對話方塊圖表</span><span class="sxs-lookup"><span data-stu-id="a356f-273">diagram of dialog box centered on window behind it</span></span> ](images/win-dialog-box-image10.png)

<span data-ttu-id="a356f-274">最初將對話置中在主控視窗上方。</span><span class="sxs-lookup"><span data-stu-id="a356f-274">Initially center dialogs on top of the owner window.</span></span>

-   <span data-ttu-id="a356f-275">**如果對話方塊為內容，則會將它顯示在其啟動所在的物件附近。**</span><span class="sxs-lookup"><span data-stu-id="a356f-275">**If a dialog is contextual, display it near the object from which it was launched.**</span></span> <span data-ttu-id="a356f-276">不過，請將它放在 (最好的位移和右邊的) ，讓對話方塊不會涵蓋物件。</span><span class="sxs-lookup"><span data-stu-id="a356f-276">However, place it out of the way (preferably offset down and to the right) so that the object isn't covered by the dialog.</span></span>

![<span data-ttu-id="a356f-277">對話方塊位移向下和向右的圖表</span><span class="sxs-lookup"><span data-stu-id="a356f-277">diagram of dialog box offset down and to the right</span></span> ](images/win-dialog-box-image11.png)

<span data-ttu-id="a356f-278">物件的屬性會顯示在物件附近。</span><span class="sxs-lookup"><span data-stu-id="a356f-278">An object's properties are displayed near to the object.</span></span>

-   <span data-ttu-id="a356f-279">**若為非強制回應對話方塊，請先在主控視窗頂端顯示，以方便尋找。**</span><span class="sxs-lookup"><span data-stu-id="a356f-279">**For modeless dialogs, display initially on top of the owner window to make it easy to find.**</span></span> <span data-ttu-id="a356f-280">如果使用者啟動擁有者視窗，可能會混淆非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-280">If the user activates the owner window, that may obscure the modeless dialog.</span></span>
-   <span data-ttu-id="a356f-281">**如有必要，請調整初始位置，讓整個對話方塊在目標監視器內都能看見。**</span><span class="sxs-lookup"><span data-stu-id="a356f-281">**If necessary, adjust the initial location so that the entire dialog is visible within the target monitor.**</span></span> <span data-ttu-id="a356f-282">如果可調整大小的視窗大於目標監視器，請將它縮小為適當大小。</span><span class="sxs-lookup"><span data-stu-id="a356f-282">If a resizable window is larger than the target monitor, reduce it to fit.</span></span>
-   <span data-ttu-id="a356f-283">**重新顯示對話方塊時，請考慮將它顯示為與上次存取相同的狀態。**</span><span class="sxs-lookup"><span data-stu-id="a356f-283">**When a dialog is redisplayed, consider displaying it in the same state as last accessed.**</span></span> <span data-ttu-id="a356f-284">關閉時，儲存所使用的監視器、視窗大小、位置和狀態 (最大化與還原) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-284">On close, save the monitor used, window size, location, and state (maximized vs. restore).</span></span> <span data-ttu-id="a356f-285">重新顯示時，使用適當的監視來還原已儲存的對話方塊大小、位置和狀態。</span><span class="sxs-lookup"><span data-stu-id="a356f-285">On redisplay, restore the saved dialog size, location, and state using the appropriate monitor.</span></span> <span data-ttu-id="a356f-286">此外，請考慮以每個使用者為基礎，將這些屬性保存在程式實例之間。</span><span class="sxs-lookup"><span data-stu-id="a356f-286">Also, consider making these attributes persist across program instances on a per-user basis.</span></span>
-   <span data-ttu-id="a356f-287">**若為可調整大小的視窗，請設定最小的視窗大小（如果大小低於此值，內容就無法再使用）。**</span><span class="sxs-lookup"><span data-stu-id="a356f-287">**For resizable windows, set a minimum window size if there is a size below which the content is no longer usable.**</span></span> <span data-ttu-id="a356f-288">請考慮改變簡報，讓內容可以使用較小的大小。</span><span class="sxs-lookup"><span data-stu-id="a356f-288">Consider altering the presentation to make the content usable at smaller sizes.</span></span>

![<span data-ttu-id="a356f-289">中央媒體播放機按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-289">screen shot of centered media player buttons</span></span> ](images/win-dialog-box-image12.png)

<span data-ttu-id="a356f-290">在此範例中，Windows Media Player 會在視窗對標準格式變得太小時變更其格式。</span><span class="sxs-lookup"><span data-stu-id="a356f-290">In this example, Windows Media Player changes its format when the window becomes too small for the standard format.</span></span>

-   <span data-ttu-id="a356f-291">**請勿使用 Always on Top 屬性。**</span><span class="sxs-lookup"><span data-stu-id="a356f-291">**Don't use the Always on Top attribute.**</span></span>
    -   <span data-ttu-id="a356f-292">**例外狀況：** 只有在對話方塊執行基本上是強制回應的作業時才使用，但必須短暫暫停才能存取主控視窗。</span><span class="sxs-lookup"><span data-stu-id="a356f-292">**Exception:** Use only when a dialog box implements an essentially modal operation, but it needs to be suspended briefly to access the owner window.</span></span> <span data-ttu-id="a356f-293">例如，在檢查檔時，使用者可能偶爾會離開 [拼寫檢查] 對話方塊，並存取檔以更正錯誤。</span><span class="sxs-lookup"><span data-stu-id="a356f-293">For example, when spell-checking a document, users may occasionally leave the spell check dialog box and access the document to correct errors.</span></span>

<span data-ttu-id="a356f-294">如需詳細資訊和範例，請參閱 [視窗管理](win-window-mgt.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-294">For more information and examples, see [Window Management](win-window-mgt.md).</span></span>

### <a name="title-bars"></a><span data-ttu-id="a356f-295">標題列</span><span class="sxs-lookup"><span data-stu-id="a356f-295">Title bars</span></span>

-   <span data-ttu-id="a356f-296">**對話方塊沒有標題列圖示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-296">**Dialog boxes don't have title bar icons.**</span></span> <span data-ttu-id="a356f-297">標題列圖示會用來做為 [主視窗](glossary.md) 與 [次要視窗](glossary.md)之間的視覺差異。</span><span class="sxs-lookup"><span data-stu-id="a356f-297">Title bar icons are used as a visual distinction between [primary windows](glossary.md) and [secondary windows](glossary.md).</span></span>
    -   <span data-ttu-id="a356f-298">**例外狀況：** 如果使用對話方塊來執行主視窗 (例如公用程式) ，因此會出現在工作列上，它的確有標題列圖示。</span><span class="sxs-lookup"><span data-stu-id="a356f-298">**Exception:** If a dialog box is used to implement a primary window (such as a utility) and therefore appears on the taskbar, it does have a title bar icon.</span></span> <span data-ttu-id="a356f-299">在這種情況下，請先精確地放置區分的資訊，以優化工作列上顯示的標題。</span><span class="sxs-lookup"><span data-stu-id="a356f-299">In this case, optimize the title for display on the taskbar by concisely placing the distinguishing information first.</span></span>
-   <span data-ttu-id="a356f-300">**對話方塊一律會有 [關閉] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-300">**Dialog boxes always have a Close button.**</span></span> <span data-ttu-id="a356f-301">非強制回應對話方塊也可以有最小化按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-301">Modeless dialogs can also have a Minimize button.</span></span> <span data-ttu-id="a356f-302">可調整大小的對話方塊可以有最大化按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-302">Resizable dialogs can have a Maximize button.</span></span>
-   <span data-ttu-id="a356f-303">**請勿停用 [關閉] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-303">**Don't disable the Close button.**</span></span> <span data-ttu-id="a356f-304">有了 [關閉] 按鈕，可讓使用者關閉他們不想要的視窗，以協助使用者保持控制。</span><span class="sxs-lookup"><span data-stu-id="a356f-304">Having a Close button helps users stay in control by allowing them to close windows they don't want.</span></span>
    -   <span data-ttu-id="a356f-305">**例外狀況：** 在 [進度] 對話方塊中，如果工作必須執行到完成才能達成有效的狀態或防止資料遺失，您可以停用 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-305">**Exception:** For progress dialogs, you may disable the Close button if the task must run to completion to achieve a valid state or prevent data loss.</span></span>
-   <span data-ttu-id="a356f-306">**標題列上的 [關閉] 按鈕應該與對話方塊內的 [取消] 或 [關閉] 按鈕具有相同的效果** 。</span><span class="sxs-lookup"><span data-stu-id="a356f-306">**The Close button on the title bar should have the same effect as the Cancel or Close button** within the dialog box.</span></span> <span data-ttu-id="a356f-307">請勿為它提供與「確定」相同的效果。</span><span class="sxs-lookup"><span data-stu-id="a356f-307">Never give it the same effect as OK.</span></span>
-   <span data-ttu-id="a356f-308">如果標題列標題和圖示已經以顯著的方式顯示在靠近視窗頂端的上方，您可以隱藏標題列標題和圖示來避免重複。</span><span class="sxs-lookup"><span data-stu-id="a356f-308">If the title bar caption and icon are already displayed in a prominent way near the top of the window, you can hide the title bar caption and icon to avoid redundancy.</span></span> <span data-ttu-id="a356f-309">不過，您仍然必須在內部設定適合用於 Windows 的標題。</span><span class="sxs-lookup"><span data-stu-id="a356f-309">However, you still have to set a suitable title internally for use by Windows.</span></span>

### <a name="interaction"></a><span data-ttu-id="a356f-310">互動</span><span class="sxs-lookup"><span data-stu-id="a356f-310">Interaction</span></span>

-   <span data-ttu-id="a356f-311">**顯示時，使用者起始的對話方塊應該一律採用輸入焦點。**</span><span class="sxs-lookup"><span data-stu-id="a356f-311">**When displayed, user initiated dialog boxes should always take input focus.**</span></span> <span data-ttu-id="a356f-312">程式起始對話方塊不應取得輸入焦點，因為使用者可能會與另一個視窗互動。</span><span class="sxs-lookup"><span data-stu-id="a356f-312">Program initiated dialog boxes shouldn't take input focus because the user may be interacting with another window.</span></span> <span data-ttu-id="a356f-313">在對話方塊中不當導向的互動可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="a356f-313">Such interaction misdirected at the dialog box may have unintended consequences.</span></span>
-   <span data-ttu-id="a356f-314">**將初始輸入焦點指派給使用者最有可能與第一個** 互動的控制項（通常是 (，但不一定會) 第一個互動式控制項）。</span><span class="sxs-lookup"><span data-stu-id="a356f-314">**Assign initial input focus to the control that users are most likely to interact with first**, which is usually (but not always) the first interactive control.</span></span> <span data-ttu-id="a356f-315">避免將初始輸入焦點指派給說明連結。</span><span class="sxs-lookup"><span data-stu-id="a356f-315">Avoid assigning initial input focus to a Help link.</span></span>
-   <span data-ttu-id="a356f-316">**針對鍵盤流覽，定位順序應該以邏輯順序流動，通常是由左至右，從上到下。**</span><span class="sxs-lookup"><span data-stu-id="a356f-316">**For keyboard navigation, tab order should flow in a logical order, generally from left to right, top to bottom.**</span></span> <span data-ttu-id="a356f-317">索引標籤順序通常會遵循讀取順序，但請考慮進行下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="a356f-317">Usually tab order follows reading order, but consider making these exceptions:</span></span>

    -   <span data-ttu-id="a356f-318">將最常使用的控制項放在定位順序的前面。</span><span class="sxs-lookup"><span data-stu-id="a356f-318">Put the most commonly used controls earlier in tab order.</span></span>
    -   <span data-ttu-id="a356f-319">在定位順序中的 [認可] 按鈕之後，將 [說明] 連結放在對話方塊底部。</span><span class="sxs-lookup"><span data-stu-id="a356f-319">Put Help links at the bottom of a dialog box, after the commit buttons in tab order.</span></span>

    <span data-ttu-id="a356f-320">指派訂單時，假設使用者針對其預定用途顯示對話方塊;例如，使用者會顯示選擇對話方塊來進行選擇，而不是檢查並按一下 [取消]。</span><span class="sxs-lookup"><span data-stu-id="a356f-320">When assigning order, assume that users display dialog boxes for their intended purpose; so, for example, users display choice dialogs to make choices, not to review and click Cancel.</span></span>

-   <span data-ttu-id="a356f-321">**按下 Esc 鍵時，一律會關閉作用中的對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-321">**Pressing the Esc key always closes an active dialog box.**</span></span> <span data-ttu-id="a356f-322">這適用于具有 [取消] 或 [關閉] 的對話方塊，即使取消已重新命名為 [關閉]，因為結果無法再復原。</span><span class="sxs-lookup"><span data-stu-id="a356f-322">This is true for dialog boxes with Cancel or Close, and even if Cancel has been renamed to Close because the results can no longer be undone.</span></span>

<span data-ttu-id="a356f-323">**存取金鑰**</span><span class="sxs-lookup"><span data-stu-id="a356f-323">**Access keys**</span></span>

-   <span data-ttu-id="a356f-324">**請盡可能將唯一的存取金鑰指派給所有互動式控制項或其標籤。**[唯讀文字方塊](ctrl-text-boxes.md) 是互動式控制項 (因為使用者可以將文字滾動並複製文字，) 讓它們受益于存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-324">**Whenever possible, assign unique access keys to all interactive controls or their labels.**[Read-only text boxes](ctrl-text-boxes.md) are interactive controls (because users can scroll them and copy text) so they benefit from access keys.</span></span> <span data-ttu-id="a356f-325">**請勿將存取金鑰指派給：**</span><span class="sxs-lookup"><span data-stu-id="a356f-325">**Don't assign access keys to:**</span></span>
    -   <span data-ttu-id="a356f-326">**[確定]、[取消] 和 [關閉] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-326">**OK, Cancel, and Close buttons.**</span></span> <span data-ttu-id="a356f-327">輸入和 Esc 可用於其存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-327">Enter and Esc are used for their access keys.</span></span> <span data-ttu-id="a356f-328">不過，請一律將便捷鍵指派給表示 [確定] 或 [取消]，但具有不同標籤的控制項。</span><span class="sxs-lookup"><span data-stu-id="a356f-328">However, always assign an access key to a control that means OK or Cancel, but has a different label.</span></span>

        ![<span data-ttu-id="a356f-329">[刪除檔案] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-329">screen shot of delete file dialog box</span></span> ](images/win-dialog-box-image13.png)

        <span data-ttu-id="a356f-330">在此範例中，正認可按鈕具有指派的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-330">In this example, the positive commit button has an access key assigned.</span></span>

    -   <span data-ttu-id="a356f-331">**群組標籤。**</span><span class="sxs-lookup"><span data-stu-id="a356f-331">**Group labels.**</span></span> <span data-ttu-id="a356f-332">一般情況下，群組內的個別控制項都會被指派存取金鑰，因此群組標籤不需要一個。</span><span class="sxs-lookup"><span data-stu-id="a356f-332">Normally, the individual controls within a group are assigned access keys, so the group label doesn't need one.</span></span> <span data-ttu-id="a356f-333">但是，如果存取金鑰不足，請將存取金鑰指派給群組標籤，而不是個別控制項。</span><span class="sxs-lookup"><span data-stu-id="a356f-333">However, if there is a shortage of access keys, assign an access key to the group label and not the individual controls.</span></span>
    -   <span data-ttu-id="a356f-334">以 F1 存取的一般 [說明]**按鈕**。</span><span class="sxs-lookup"><span data-stu-id="a356f-334">**Generic Help buttons,** which are accessed with F1.</span></span>
    -   <span data-ttu-id="a356f-335">**連結標籤。**</span><span class="sxs-lookup"><span data-stu-id="a356f-335">**Link labels.**</span></span> <span data-ttu-id="a356f-336">通常會有太多連結可指派唯一的存取金鑰，而用來表示連結的底線通常會隱藏存取金鑰底線。</span><span class="sxs-lookup"><span data-stu-id="a356f-336">There are often too many links to assign unique access keys, and the underscores often used to signify links hide the access key underscores.</span></span> <span data-ttu-id="a356f-337">改為使用 Tab 鍵存取連結。</span><span class="sxs-lookup"><span data-stu-id="a356f-337">Access links with the Tab key instead.</span></span>
    -   <span data-ttu-id="a356f-338">**Tab 鍵名稱。**</span><span class="sxs-lookup"><span data-stu-id="a356f-338">**Tab names.**</span></span> <span data-ttu-id="a356f-339">索引標籤會使用 Ctrl + Tab 和 Ctrl + Shift + Tab 鍵來迴圈。</span><span class="sxs-lookup"><span data-stu-id="a356f-339">Tabs are cycled using Ctrl+Tab and Ctrl+Shift+Tab.</span></span>
    -   <span data-ttu-id="a356f-340">**流覽標示為「...」的按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-340">**Browse buttons labeled "...".**</span></span> <span data-ttu-id="a356f-341">這些瀏覽按鈕無法唯一指派存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-341">These Browse buttons can't be assigned access keys uniquely.</span></span>
    -   <span data-ttu-id="a356f-342">未 **標記的控制項，** 例如微調控制項、圖形命令按鈕，以及未標記的漸進式洩漏控制項。</span><span class="sxs-lookup"><span data-stu-id="a356f-342">**Unlabeled controls,** such as spin controls, graphic command buttons, and unlabeled progressive disclosure controls.</span></span>
    -   <span data-ttu-id="a356f-343">**非互動式控制項（例如進度列）的非標籤靜態文字或標籤** 。</span><span class="sxs-lookup"><span data-stu-id="a356f-343">**Non-label static text or labels for controls that aren't interactive,** such as progress bars.</span></span>

-   <span data-ttu-id="a356f-344">**如果可能，請根據標準存取金鑰指派，指派常用命令的存取金鑰**。</span><span class="sxs-lookup"><span data-stu-id="a356f-344">**Whenever possible, assign access keys for commonly used commands according to the Standard Access Key Assignments**.</span></span> <span data-ttu-id="a356f-345">雖然不一定能夠維持一致的存取金鑰指派，但特別是常用的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-345">While consistent access key assignments aren't always possible, they are certainly preferred especially for frequently used dialog boxes.</span></span>
-   <span data-ttu-id="a356f-346">**先指派認可按鈕存取金鑰，以確保它們具有標準金鑰指派。**</span><span class="sxs-lookup"><span data-stu-id="a356f-346">**Assign commit button access keys first to ensure that they have the standard key assignments.**</span></span> <span data-ttu-id="a356f-347">如果沒有標準金鑰指派，請使用第一個單字的第一個字母。</span><span class="sxs-lookup"><span data-stu-id="a356f-347">If there isn't a standard key assignment, use the first letter of the first word.</span></span> <span data-ttu-id="a356f-348">例如，不論對話方塊中的其他控制項為何，[是] 和 [無認可] 按鈕的存取金鑰都應該一律為 "Y" 和 "N"。</span><span class="sxs-lookup"><span data-stu-id="a356f-348">For example, the access key for Yes and No commit buttons should always be "Y" and "N", regardless of the other controls in the dialog box.</span></span>
-   <span data-ttu-id="a356f-349">**若要讓存取金鑰易於尋找，請將存取金鑰指派給在標籤中提早出現的字元，** 最好是第一個字元，即使標籤稍後出現關鍵字也是如此。</span><span class="sxs-lookup"><span data-stu-id="a356f-349">**To make access keys easy to find, assign the access keys to a character that appears early in the label,** ideally the first character, even if there is a keyword that appears later in the label.</span></span>
-   <span data-ttu-id="a356f-350">**偏好寬寬度的字元，** 例如 w、m 和大寫字母。</span><span class="sxs-lookup"><span data-stu-id="a356f-350">**Prefer characters with wide widths,** such as w, m, and capital letters.</span></span>
-   <span data-ttu-id="a356f-351">**偏好使用特殊的輔音或母音，** 例如 "x" 結束。</span><span class="sxs-lookup"><span data-stu-id="a356f-351">**Prefer a distinctive consonant or a vowel,** such as "x" in Exit.</span></span>
-   <span data-ttu-id="a356f-352">**避免使用使底線難以查看的字元，例如，** 從最有問題的 (到最不有問題的) ：</span><span class="sxs-lookup"><span data-stu-id="a356f-352">**Avoid using characters that make the underline difficult to see,** such as (from most problematic to least problematic):</span></span>
    -   <span data-ttu-id="a356f-353">只有一個圖元寬度的字母，例如 i 和 l。</span><span class="sxs-lookup"><span data-stu-id="a356f-353">Letters that are only one pixel wide, such as i and l.</span></span>
    -   <span data-ttu-id="a356f-354">具有下行的字母，例如 g、j、p、q 和 y。</span><span class="sxs-lookup"><span data-stu-id="a356f-354">Letters with descenders, such as g, j, p, q, and y.</span></span>
    -   <span data-ttu-id="a356f-355">包含下行的字母旁的字母。</span><span class="sxs-lookup"><span data-stu-id="a356f-355">Letters next to a letter with a descender.</span></span>

<span data-ttu-id="a356f-356">如需更多指導方針與範例，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-356">For more guidelines and examples, see [Keyboard](inter-keyboard.md).</span></span>

### <a name="progress-dialogs"></a><span data-ttu-id="a356f-357">進度對話方塊</span><span class="sxs-lookup"><span data-stu-id="a356f-357">Progress dialogs</span></span>

<span data-ttu-id="a356f-358">若為長時間執行的工作，請 **假設使用者會在工作完成時執行其他** 作業。</span><span class="sxs-lookup"><span data-stu-id="a356f-358">For long-running tasks, **assume that users will do something else while the task is completing**.</span></span> <span data-ttu-id="a356f-359">設計要自動執行的工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-359">Design the task to run unattended.</span></span>

-   <span data-ttu-id="a356f-360">**如果作業花費的時間超過五秒，則顯示具有進度意見反應對話方塊的使用者**，以及取消或停止作業的命令。</span><span class="sxs-lookup"><span data-stu-id="a356f-360">**Present users with progress feedback dialog box if an operation takes longer than five seconds to complete**, along with a command to cancel or stop the operation.</span></span>
    -   <span data-ttu-id="a356f-361">**例外狀況：** 針對 [嚮導] 和 [工作流程]，只有在工作維持在相同的頁面上 (時，才會使用強制回應對話方塊進行處理，而不是前進到另一個頁面) 而且使用者在等待時不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="a356f-361">**Exception:** For wizards and task flows, use a modal dialog for progress only if the task stays on the same page (as opposed to advancing to another page) and users can't do anything while waiting.</span></span> <span data-ttu-id="a356f-362">否則，請使用進度頁面或就地進度。</span><span class="sxs-lookup"><span data-stu-id="a356f-362">Otherwise, use a progress page or in-place progress.</span></span>
-   <span data-ttu-id="a356f-363">如果作業是長時間執行的工作 (超過30秒) 並可在背景中執行，請使用非模式進度對話方塊，讓使用者可以在等候時繼續使用您的程式。</span><span class="sxs-lookup"><span data-stu-id="a356f-363">If the operation is a long-running task (over 30 seconds) and can be performed in the background, use a modeless progress dialog so that users can continue to use your program while waiting.</span></span>
-   <span data-ttu-id="a356f-364">無模式進度對話方塊：</span><span class="sxs-lookup"><span data-stu-id="a356f-364">Modeless progress dialogs:</span></span>
    -   <span data-ttu-id="a356f-365">在標題列上具有最小化按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-365">Have a Minimize button on the title bar.</span></span>
    -   <span data-ttu-id="a356f-366">會顯示在工作列上。</span><span class="sxs-lookup"><span data-stu-id="a356f-366">Are displayed on the taskbar.</span></span>
-   <span data-ttu-id="a356f-367">執行非強制回應的進度對話方塊，讓它們繼續執行，即使擁有者視窗已關閉也一樣。</span><span class="sxs-lookup"><span data-stu-id="a356f-367">Implement modeless progress dialogs so that they continue to run even if the owner window is closed.</span></span>

![<span data-ttu-id="a356f-368">具有進度列之 [複製] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-368">screen shot of copy dialog box with progress bar</span></span> ](images/win-dialog-box-image14.png)

<span data-ttu-id="a356f-369">在此範例中，即使擁有者視窗已關閉，仍會繼續進行檔案複製。</span><span class="sxs-lookup"><span data-stu-id="a356f-369">In this example, the file copy continues even if the owner window is closed.</span></span>

-   <span data-ttu-id="a356f-370">**如果需要超過幾秒鐘的時間才能完成作業，或有可能永遠無法完成，請提供命令按鈕來停止作業。**</span><span class="sxs-lookup"><span data-stu-id="a356f-370">**Provide a command button to halt the operation if it takes more than a few seconds to complete, or has the potential never to complete.**</span></span> <span data-ttu-id="a356f-371">如果取消將環境傳回至先前的狀態，請將按鈕標示為 [取消]， (不會造成任何副作用) ;否則，請將按鈕標示為停止，表示它會讓部分完成的作業保持不變。</span><span class="sxs-lookup"><span data-stu-id="a356f-371">Label the button Cancel if canceling returns the environment to its previous state (leaving no side effects); otherwise, label the button Stop to indicate that it leaves the partially completed operation intact.</span></span> <span data-ttu-id="a356f-372">您可以將按鈕標籤從 [取消] 變更為在作業過程中停止，如果某個時間點，則無法將環境回復為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="a356f-372">You can change the button label from Cancel to Stop in the middle of the operation, if at some point it isn't possible to return the environment to its previous state.</span></span>

![<span data-ttu-id="a356f-373">具有 [取消] 按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-373">screen shot of dialog box with cancel button</span></span> ](images/win-dialog-box-image15.png)

<span data-ttu-id="a356f-374">在此範例中，暫停問題診斷沒有副作用。</span><span class="sxs-lookup"><span data-stu-id="a356f-374">In this example, halting the problem diagnosis has no side effect.</span></span>

-   <span data-ttu-id="a356f-375">**如果需要超過數分鐘才能完成作業，請提供命令按鈕來暫停作業，並讓使用者能夠完成工作。**</span><span class="sxs-lookup"><span data-stu-id="a356f-375">**Provide a command button to pause the operation if it takes more than several minutes to complete, and it impairs users' ability to get work done.**</span></span> <span data-ttu-id="a356f-376">這樣做並不會強制使用者在完成工作和完成工作之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="a356f-376">Doing so doesn't force the user to choose between completing the task and getting their work done.</span></span>
-   <span data-ttu-id="a356f-377">**在開始工作之前，盡可能收集最多的資訊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-377">**Gather as much information as you can before starting the task.**</span></span>
-   <span data-ttu-id="a356f-378">**如果偵測到可復原的問題，請讓使用者處理在工作結束時所發現的所有問題。**</span><span class="sxs-lookup"><span data-stu-id="a356f-378">**If recoverable problems are detected, have users deal with all problems found at the end of the task.**</span></span> <span data-ttu-id="a356f-379">如果這不可行，請讓使用者在發生問題時處理問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-379">If that isn't practical, have users deal with problems as they happen.</span></span>
-   <span data-ttu-id="a356f-380">**請勿放棄復原錯誤的結果。**</span><span class="sxs-lookup"><span data-stu-id="a356f-380">**Don't abandon tasks as the result of recoverable errors.**</span></span>

![<span data-ttu-id="a356f-381">對話方塊的螢幕擷取畫面，其中包含 [再試一次] 按鈕</span><span class="sxs-lookup"><span data-stu-id="a356f-381">screen shot of dialog box with try again button</span></span> ](images/win-dialog-box-image16.png)

<span data-ttu-id="a356f-382">在此範例中，Windows 檔案總管可讓使用者在可復原的錯誤之後繼續執行工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-382">In this example, Windows Explorer allows users to continue with the task after a recoverable error.</span></span>

-   <span data-ttu-id="a356f-383">**藉由將進度列變成紅色來指出問題。**</span><span class="sxs-lookup"><span data-stu-id="a356f-383">**Indicate problems by turning the progress bar red.**</span></span>

![<span data-ttu-id="a356f-384">進度列的螢幕擷取畫面，然後再試一次按鈕</span><span class="sxs-lookup"><span data-stu-id="a356f-384">screen shot of progress bar and try again button</span></span> ](images/win-dialog-box-image17.png)

<span data-ttu-id="a356f-385">在此範例中，會在檔案複製期間移除卸載式磁片。</span><span class="sxs-lookup"><span data-stu-id="a356f-385">In this example, a removable disk was removed during a file copy.</span></span>

-   <span data-ttu-id="a356f-386">**如果使用者清楚看出結果，請在成功完成時自動關閉進度對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-386">**If the results are clearly apparent to users, close the progress dialog automatically on successful completion.**</span></span> <span data-ttu-id="a356f-387">否則，請只使用意見反應來回報問題：</span><span class="sxs-lookup"><span data-stu-id="a356f-387">Otherwise, use feedback only to report problems:</span></span>
    -   <span data-ttu-id="a356f-388">若要顯示簡單的意見反應，請在 [進度] 對話方塊中顯示意見反應，然後變更 [取消] 按鈕以關閉。</span><span class="sxs-lookup"><span data-stu-id="a356f-388">To display simple feedback, display the feedback in the progress dialog, and change the Cancel button to Close.</span></span>
    -   <span data-ttu-id="a356f-389">若要顯示詳細的意見反應，請關閉 [進度] 對話方塊並顯示資訊對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-389">To display detailed feedback, close the progress dialog box and display an informational dialog.</span></span>

<span data-ttu-id="a356f-390">**請勿使用通知完成意見反應。**</span><span class="sxs-lookup"><span data-stu-id="a356f-390">**Don't use a notification for completion feedback.**</span></span> <span data-ttu-id="a356f-391">您可以使用進度對話方塊或 [動作成功通知](mess-notif.md)，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="a356f-391">Use either a progress dialog or an [action success notification](mess-notif.md), but not both.</span></span>

<span data-ttu-id="a356f-392">**剩餘時間**</span><span class="sxs-lookup"><span data-stu-id="a356f-392">**Time remaining**</span></span>

-   <span data-ttu-id="a356f-393">**使用下列時間格式。**</span><span class="sxs-lookup"><span data-stu-id="a356f-393">**Use the following time formats.**</span></span> <span data-ttu-id="a356f-394">從最大時間單位不是零的下列其中一種格式開始，然後在最大時間單位變成零之後變更為下一個格式。</span><span class="sxs-lookup"><span data-stu-id="a356f-394">Start with the first of the following formats where the largest time unit isn't zero, then change to the next format once the largest time unit becomes zero.</span></span>

<span data-ttu-id="a356f-395">**針對進度列：**</span><span class="sxs-lookup"><span data-stu-id="a356f-395">**For progress bars:**</span></span>

<span data-ttu-id="a356f-396">**如果相關資訊顯示為冒號格式：**</span><span class="sxs-lookup"><span data-stu-id="a356f-396">**If related information is shown in a colon format:**</span></span>

<span data-ttu-id="a356f-397">剩餘時間： h 小時、m 分鐘</span><span class="sxs-lookup"><span data-stu-id="a356f-397">Time remaining: h hours, m minutes</span></span>

<span data-ttu-id="a356f-398">剩餘時間： m 分鐘、秒</span><span class="sxs-lookup"><span data-stu-id="a356f-398">Time remaining: m minutes, s seconds</span></span>

<span data-ttu-id="a356f-399">剩餘時間：秒</span><span class="sxs-lookup"><span data-stu-id="a356f-399">Time remaining: s seconds</span></span>

<span data-ttu-id="a356f-400">**如果螢幕空間位於 premium：**</span><span class="sxs-lookup"><span data-stu-id="a356f-400">**If screen space is at a premium:**</span></span>

<span data-ttu-id="a356f-401">h 小時，剩餘 m 分鐘</span><span class="sxs-lookup"><span data-stu-id="a356f-401">h hrs, m mins remaining</span></span>

<span data-ttu-id="a356f-402">分鐘，剩餘的秒數</span><span class="sxs-lookup"><span data-stu-id="a356f-402">m mins, s secs remaining</span></span>

<span data-ttu-id="a356f-403">秒數</span><span class="sxs-lookup"><span data-stu-id="a356f-403">s seconds remaining</span></span>

<span data-ttu-id="a356f-404">**否則：**</span><span class="sxs-lookup"><span data-stu-id="a356f-404">**Otherwise:**</span></span>

<span data-ttu-id="a356f-405">小時，剩餘 m 分鐘</span><span class="sxs-lookup"><span data-stu-id="a356f-405">h hours, m minutes remaining</span></span>

<span data-ttu-id="a356f-406">分鐘，剩餘秒數</span><span class="sxs-lookup"><span data-stu-id="a356f-406">m minutes, s seconds remaining</span></span>

<span data-ttu-id="a356f-407">秒數</span><span class="sxs-lookup"><span data-stu-id="a356f-407">s seconds remaining</span></span>

<span data-ttu-id="a356f-408">**針對標題列：**</span><span class="sxs-lookup"><span data-stu-id="a356f-408">**For title bars:**</span></span>

<span data-ttu-id="a356f-409">hh： mm 剩餘</span><span class="sxs-lookup"><span data-stu-id="a356f-409">hh:mm remaining</span></span>

<span data-ttu-id="a356f-410">mm：剩餘的 ss</span><span class="sxs-lookup"><span data-stu-id="a356f-410">mm:ss remaining</span></span>

<span data-ttu-id="a356f-411">0： ss 剩餘</span><span class="sxs-lookup"><span data-stu-id="a356f-411">0:ss remaining</span></span>

<span data-ttu-id="a356f-412">此壓縮格式會先顯示最重要的資訊，使其不會在工作列上被截斷。</span><span class="sxs-lookup"><span data-stu-id="a356f-412">This compact format shows the most important information first so that it isn't truncated on the taskbar.</span></span>

-   <span data-ttu-id="a356f-413">**讓預估結果正確無誤，但不提供 false 精確度。**</span><span class="sxs-lookup"><span data-stu-id="a356f-413">**Make estimates accurate, but don't give false precision.**</span></span> <span data-ttu-id="a356f-414">如果最大單位為小時，請在有意義的) （而不是秒）時，提供分鐘 (。</span><span class="sxs-lookup"><span data-stu-id="a356f-414">If largest unit is hours, give minutes (if meaningful) but not seconds.</span></span>

<span data-ttu-id="a356f-415">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-415">**Incorrect:**</span></span>

<span data-ttu-id="a356f-416">hh 小時、mm 分鐘、ss 秒</span><span class="sxs-lookup"><span data-stu-id="a356f-416">hh hours, mm minutes, ss seconds</span></span>

-   <span data-ttu-id="a356f-417">**將預估保持在最新狀態。**</span><span class="sxs-lookup"><span data-stu-id="a356f-417">**Keep the estimate up-to-date.**</span></span> <span data-ttu-id="a356f-418">更新剩餘時間至少每5秒估計一次。</span><span class="sxs-lookup"><span data-stu-id="a356f-418">Update time remaining estimates at least every 5 seconds.</span></span>
-   <span data-ttu-id="a356f-419">將 **焦點放在剩餘的時間**，因為這是使用者最在意的資訊。</span><span class="sxs-lookup"><span data-stu-id="a356f-419">**Focus on the time remaining** because that is the information users care about most.</span></span> <span data-ttu-id="a356f-420">只有在某些情況下，已耗用時間很有説明 (例如工作可能重複) 時，才提供總經過時間。</span><span class="sxs-lookup"><span data-stu-id="a356f-420">Give total elapsed time only when there are scenarios where elapsed time is helpful (such as when the task is likely to be repeated).</span></span> <span data-ttu-id="a356f-421">如果剩餘的預估時間與進度列相關聯，則沒有百分比的完成文字，因為該資訊是由進度列本身所傳達。</span><span class="sxs-lookup"><span data-stu-id="a356f-421">If the time remaining estimate is associated with a progress bar, don't have percent complete text because that information is conveyed by the progress bar itself.</span></span>
-   <span data-ttu-id="a356f-422">**語法正確。**</span><span class="sxs-lookup"><span data-stu-id="a356f-422">**Be grammatically correct.**</span></span> <span data-ttu-id="a356f-423">當數位為1時，請使用單一單位。</span><span class="sxs-lookup"><span data-stu-id="a356f-423">Use singular units when the number is one.</span></span>

<span data-ttu-id="a356f-424">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-424">**Incorrect:**</span></span>

<span data-ttu-id="a356f-425">1分鐘，1秒</span><span class="sxs-lookup"><span data-stu-id="a356f-425">1 minutes, 1 seconds</span></span>

-   <span data-ttu-id="a356f-426">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="a356f-426">**Use sentence-style capitalization.**</span></span>

<span data-ttu-id="a356f-427">如需詳細資訊和範例，請參閱 [進度](progress-bars.md)列。</span><span class="sxs-lookup"><span data-stu-id="a356f-427">For more information and examples, see [Progress Bars](progress-bars.md).</span></span>

### <a name="icons-and-graphics"></a><span data-ttu-id="a356f-428">圖示和圖形</span><span class="sxs-lookup"><span data-stu-id="a356f-428">Icons and graphics</span></span>

<span data-ttu-id="a356f-429">**圖形**</span><span class="sxs-lookup"><span data-stu-id="a356f-429">**Graphics**</span></span>

-   <span data-ttu-id="a356f-430">**請勿使用不使用視覺指標填滿空間的大型圖形。**</span><span class="sxs-lookup"><span data-stu-id="a356f-430">**Don't use large graphics that serve no purpose beyond filling space with eye candy.**</span></span> <span data-ttu-id="a356f-431">請改用簡單的外觀。</span><span class="sxs-lookup"><span data-stu-id="a356f-431">Keep the appearance simple instead.</span></span>

<span data-ttu-id="a356f-432">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-432">**Incorrect:**</span></span>

![<span data-ttu-id="a356f-433">具有大型圖形之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-433">screen shot of dialog box with a large graphic</span></span> ](images/win-dialog-box-image18.png)

<span data-ttu-id="a356f-434">在此範例中，大型圖形沒有任何用途。</span><span class="sxs-lookup"><span data-stu-id="a356f-434">In this example, the large graphic serves no purpose.</span></span>

<span data-ttu-id="a356f-435">**標題列圖示**</span><span class="sxs-lookup"><span data-stu-id="a356f-435">**Title bar icons**</span></span>

-   <span data-ttu-id="a356f-436">**對話方塊沒有標題列圖示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-436">**Dialog boxes don't have title bar icons.**</span></span>
    -   <span data-ttu-id="a356f-437">**例外狀況：** 如果使用對話方塊來執行主視窗 (例如公用程式) ，因此會出現在工作列上，它的確有標題列圖示。</span><span class="sxs-lookup"><span data-stu-id="a356f-437">**Exception:** If a dialog box is used to implement a primary window (such as a utility) and therefore appears on the taskbar, it does have a title bar icon.</span></span>

<span data-ttu-id="a356f-438">**主體圖示**</span><span class="sxs-lookup"><span data-stu-id="a356f-438">**Body icons**</span></span>

-   <span data-ttu-id="a356f-439">**選擇以設計模式為基礎的主體圖示：**</span><span class="sxs-lookup"><span data-stu-id="a356f-439">**Choose the body icon based on the design pattern:**</span></span>



| <span data-ttu-id="a356f-440">模式</span><span class="sxs-lookup"><span data-stu-id="a356f-440">Pattern</span></span> | <span data-ttu-id="a356f-441">主體圖示</span><span class="sxs-lookup"><span data-stu-id="a356f-441">Body icon</span></span> |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a356f-442">**問題對話方塊**</span><span class="sxs-lookup"><span data-stu-id="a356f-442">**Question dialogs**</span></span><br/>      | <span data-ttu-id="a356f-443">程式、功能、物件、警告圖示 (是否可能遺失資料或系統存取) 、安全性警告或無。</span><span class="sxs-lookup"><span data-stu-id="a356f-443">Program, feature, object, warning icon (if potential loss of data or system access), security warning, or none.</span></span><br/> |
| <span data-ttu-id="a356f-444">**選擇對話方塊**</span><span class="sxs-lookup"><span data-stu-id="a356f-444">**Choice dialogs**</span></span><br/>        | <span data-ttu-id="a356f-445">無。</span><span class="sxs-lookup"><span data-stu-id="a356f-445">None.</span></span><br/>                                                                                                           |
| <span data-ttu-id="a356f-446">**進度對話方塊**</span><span class="sxs-lookup"><span data-stu-id="a356f-446">**Progress dialogs**</span></span><br/>      | <span data-ttu-id="a356f-447">無 (但可能有動畫) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-447">None (but may have an animation).</span></span><br/>                                                                               |
| <span data-ttu-id="a356f-448">**資訊對話方塊**</span><span class="sxs-lookup"><span data-stu-id="a356f-448">**Informational dialogs**</span></span><br/> | <span data-ttu-id="a356f-449">無。</span><span class="sxs-lookup"><span data-stu-id="a356f-449">None.</span></span><br/>                                                                                                           |



 

-   <span data-ttu-id="a356f-450">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-450">**Incorrect:**</span></span>

![<span data-ttu-id="a356f-451">對話方塊的螢幕擷取畫面和警告圖示</span><span class="sxs-lookup"><span data-stu-id="a356f-451">screen shot of dialog box with warning icon</span></span> ](images/win-dialog-box-image19.png)

<span data-ttu-id="a356f-452">在此範例中，不會有可能遺失資料或系統存取權的問題，會有不正確使用的警告圖示。</span><span class="sxs-lookup"><span data-stu-id="a356f-452">In this example, a warning icon is incorrectly used for a question that doesn't involve potential loss of data or system access.</span></span>

- <span data-ttu-id="a356f-453">**請考慮使用圖示來協助使用者以視覺方式辨識您的程式功能。**</span><span class="sxs-lookup"><span data-stu-id="a356f-453">**Consider using icons to help users visually recognize your program's features.**</span></span> <span data-ttu-id="a356f-454">當您在程式中的數個位置輕鬆辨識並使用圖示時，這項技術最有效。</span><span class="sxs-lookup"><span data-stu-id="a356f-454">This technique is most effective when the icons are easily recognizable and used in several locations within your program.</span></span>

![<span data-ttu-id="a356f-455">[我的最愛] 對話方塊的螢幕擷取畫面（具有星星圖示）</span><span class="sxs-lookup"><span data-stu-id="a356f-455">screen shot of favorites dialog box with star icon</span></span> ](images/win-dialog-box-image20.png)

<span data-ttu-id="a356f-456">在此範例中，黃色星形圖示代表我的最愛。</span><span class="sxs-lookup"><span data-stu-id="a356f-456">In this example, the yellow star icon represents Favorites.</span></span> <span data-ttu-id="a356f-457">這個圖示很容易辨識，而且在整個視窗中都是以一致的方式使用，</span><span class="sxs-lookup"><span data-stu-id="a356f-457">The icon is easily recognizable and is used consistently throughout Windows to represent Favorites.</span></span>

-   <span data-ttu-id="a356f-458">**使用圖示來協助使用者辨識有問題的物件。**</span><span class="sxs-lookup"><span data-stu-id="a356f-458">**Use icons to help users recognize the object in question.**</span></span>

![<span data-ttu-id="a356f-459">具有 powerpoint 圖示之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-459">screen shot of dialog box with powerpoint icon</span></span> ](images/win-dialog-box-image21.png)

<span data-ttu-id="a356f-460">在此範例中，物件的圖示可協助使用者辨識要開啟或儲存的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="a356f-460">In this example, the object's icon helps users recognize the type of file being opened or saved.</span></span>

-   <span data-ttu-id="a356f-461">**請考慮使用圖示來協助讓功能一目了然。**</span><span class="sxs-lookup"><span data-stu-id="a356f-461">**Consider using icons to help make features self-explanatory.**</span></span>

![<span data-ttu-id="a356f-462">顯示如何定位監視的箭號影像</span><span class="sxs-lookup"><span data-stu-id="a356f-462">images of arrows showing how to position monitor</span></span> ](images/win-dialog-box-image22.png)

<span data-ttu-id="a356f-463">在此範例中，這些圖示可協助使用者視覺化其功能的效果。</span><span class="sxs-lookup"><span data-stu-id="a356f-463">In this example, these icons help users visualize the effect of their features.</span></span>

-   <span data-ttu-id="a356f-464">**使用關於應用程式商標的 [關於] 方塊對話方塊中的圖示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-464">**Use an icon in About Box dialogs for application branding.**</span></span>

![<span data-ttu-id="a356f-465">具有 windows 標誌的 [關於] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-465">screen shot of about dialog box with windows logo</span></span> ](images/win-dialog-box-image23.png)

<span data-ttu-id="a356f-466">在此範例中，會在 [關於] 方塊中使用點陣圖來識別應用程式並為其建立品牌。</span><span class="sxs-lookup"><span data-stu-id="a356f-466">In this example, a bitmap is used in the About Box to identify and brand the application.</span></span>

<span data-ttu-id="a356f-467">**註腳圖示**</span><span class="sxs-lookup"><span data-stu-id="a356f-467">**Footnote icons**</span></span>

-   <span data-ttu-id="a356f-468">**如果您有註腳，請考慮使用註腳圖示來摘要註腳的主旨。**</span><span class="sxs-lookup"><span data-stu-id="a356f-468">**If you have a footnote, consider using a footnote icon to summarize the footnote's subject.**</span></span>

![<span data-ttu-id="a356f-469">包含註腳圖示之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-469">screen shot of dialog box with footnote icon</span></span> ](images/win-dialog-box-image24.png)

<span data-ttu-id="a356f-470">在此範例中，註腳圖示指出問題有安全性含意。</span><span class="sxs-lookup"><span data-stu-id="a356f-470">In this example, the footnote icon indicates that the question has security implications.</span></span>

-   <span data-ttu-id="a356f-471">**請勿使用重複主體圖示的註腳圖示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-471">**Don't use a footnote icon that repeats the body icon.**</span></span>
-   <span data-ttu-id="a356f-472">**請勿使用「錯誤」或「資訊標準」圖示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-472">**Don't use the error or information standard icons.**</span></span> <span data-ttu-id="a356f-473">錯誤條件必須透過內文圖示傳達，而且註腳一律為資訊，讓資訊圖示成為多餘的。</span><span class="sxs-lookup"><span data-stu-id="a356f-473">Error conditions must be conveyed through the body icon and footnotes are always for information, making the information icon redundant.</span></span> <span data-ttu-id="a356f-474">不過，您可以使用標準警告圖示和黃色的安全性防護，來警示使用者有風險的後果。</span><span class="sxs-lookup"><span data-stu-id="a356f-474">However, you can use the standard warning icon and the yellow security shield to alert users of risky consequences.</span></span>

<span data-ttu-id="a356f-475">如需詳細資訊和範例，請參閱 [圖示](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-475">For more information and examples, see [Icons](vis-icons.md).</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="a356f-476">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="a356f-476">Commit buttons</span></span>

<span data-ttu-id="a356f-477">**注意：**</span><span class="sxs-lookup"><span data-stu-id="a356f-477">**Notes:**</span></span>

-   <span data-ttu-id="a356f-478">這些指導方針不適用於使用命令連結的問題對話方塊，因為該模式會使用命令連結，而不是按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-478">These guidelines don't apply to question dialogs using command links, because that pattern uses command links instead of buttons.</span></span>
-   <span data-ttu-id="a356f-479">\[這樣做 \] 並不 \[ \] 會將其分別肯定和消極回應至主要指令。</span><span class="sxs-lookup"><span data-stu-id="a356f-479">\[Do it\] and \[Don't do it\] are affirmative and negative responses, respectively, to the main instruction.</span></span>

<span data-ttu-id="a356f-480">**一般**</span><span class="sxs-lookup"><span data-stu-id="a356f-480">**General**</span></span>

-   <span data-ttu-id="a356f-481">**根據設計模式選擇認可按鈕：**</span><span class="sxs-lookup"><span data-stu-id="a356f-481">**Choose the commit buttons based on the design pattern:**</span></span>

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="a356f-482"><strong>模式</strong></span><span class="sxs-lookup"><span data-stu-id="a356f-482"><strong>Pattern</strong></span></span><br/></td>
    <td><span data-ttu-id="a356f-483"><strong>認可按鈕</strong></span><span class="sxs-lookup"><span data-stu-id="a356f-483"><strong>Commit buttons</strong></span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a356f-484"><strong>使用按鈕) 的問題對話方塊 (</strong></span><span class="sxs-lookup"><span data-stu-id="a356f-484"><strong>Question dialogs (using buttons)</strong></span></span><br/></td>
    <td><span data-ttu-id="a356f-485">下列其中一組精簡的命令： Yes/No、Yes/No/Cancel、[Do it]/Cancel、[do it]/[do do]、[Do it do]/[no do it]/Cancel。</span><span class="sxs-lookup"><span data-stu-id="a356f-485">One of the following sets of concise commands: Yes/No, Yes/No/Cancel, [Do it]/Cancel, [Do it]/[Don't do it], [Do it]/[Don't do it]/Cancel.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a356f-486"><strong>問題對話方塊 (使用連結) </strong></span><span class="sxs-lookup"><span data-stu-id="a356f-486"><strong>Question dialogs (using links)</strong></span></span><br/></td>
    <td><span data-ttu-id="a356f-487">取消。</span><span class="sxs-lookup"><span data-stu-id="a356f-487">Cancel.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a356f-488"><strong>選擇對話方塊</strong></span><span class="sxs-lookup"><span data-stu-id="a356f-488"><strong>Choice dialogs</strong></span></span><br/></td>
    <td><ul>
    <li><span data-ttu-id="a356f-489">強制回應對話方塊：確定/取消或 [執行]/Cancel</span><span class="sxs-lookup"><span data-stu-id="a356f-489">Modal dialogs: OK/Cancel or [Do it]/Cancel</span></span></li>
    <li><span data-ttu-id="a356f-490">非強制回應對話方塊：對話方塊和標題列上的關閉按鈕</span><span class="sxs-lookup"><span data-stu-id="a356f-490">Modeless dialogs: Close button on dialog box and title bar</span></span></li>
    <li><span data-ttu-id="a356f-491">工作窗格：標題列上的 [關閉] 按鈕</span><span class="sxs-lookup"><span data-stu-id="a356f-491">Task pane: Close button on title bar</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a356f-492"><strong>進度對話方塊</strong></span><span class="sxs-lookup"><span data-stu-id="a356f-492"><strong>Progress dialogs</strong></span></span><br/></td>
    <td><span data-ttu-id="a356f-493">如果將環境傳回至先前的狀態，請使用 [取消]， (不會有副作用) ;否則，請使用 Stop。</span><span class="sxs-lookup"><span data-stu-id="a356f-493">Use Cancel if returns the environment to its previous state (leaving no side effect); otherwise, use Stop.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a356f-494"><strong>資訊對話方塊</strong></span><span class="sxs-lookup"><span data-stu-id="a356f-494"><strong>Informational dialogs</strong></span></span><br/></td>
    <td><span data-ttu-id="a356f-495">很接近了。</span><span class="sxs-lookup"><span data-stu-id="a356f-495">Close.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="a356f-496">**除了套用結果之外，所有的認可按鈕都會關閉對話方塊視窗。**</span><span class="sxs-lookup"><span data-stu-id="a356f-496">**All commit buttons except Apply result in closing the dialog box window.**</span></span>
-   <span data-ttu-id="a356f-497">**不要確認認可按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-497">**Don't confirm commit buttons.**</span></span> <span data-ttu-id="a356f-498">這麼做不必要，可能會很討厭。</span><span class="sxs-lookup"><span data-stu-id="a356f-498">Doing so unnecessarily can be very annoying.</span></span> <span data-ttu-id="a356f-499">**異常：**</span><span class="sxs-lookup"><span data-stu-id="a356f-499">**Exceptions:**</span></span>

    -   <span data-ttu-id="a356f-500">動作可能是災難性的。</span><span class="sxs-lookup"><span data-stu-id="a356f-500">The action is potentially catastrophic.</span></span>
    -   <span data-ttu-id="a356f-501">動作與其他動作明顯不一致。</span><span class="sxs-lookup"><span data-stu-id="a356f-501">The action is clearly inconsistent with other actions.</span></span>
    -   <span data-ttu-id="a356f-502">如果不正確，此動作可能會代表使用者大量遺失資料、時間或工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-502">If incorrect, the action may result in a significant loss of data, time, or effort on behalf of the user.</span></span>

    <span data-ttu-id="a356f-503">如需詳細的指導方針與範例，請參閱 [確認](mess-confirm.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-503">For more guidelines and examples, see [Confirmations](mess-confirm.md).</span></span>

-   <span data-ttu-id="a356f-504">**不要停用認可按鈕。異常：**</span><span class="sxs-lookup"><span data-stu-id="a356f-504">**Don't disable commit buttons. Exceptions:**</span></span>
    -   <span data-ttu-id="a356f-505">**如果使用者必須提升以進行變更，請停用正面的認可按鈕，直到使用者進行變更為止。**</span><span class="sxs-lookup"><span data-stu-id="a356f-505">**If users must elevate to make a change, disable the positive commit buttons until the user makes a change.**</span></span> <span data-ttu-id="a356f-506">這麼做可防止使用者藉由強制按一下 [取消] 來關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="a356f-506">Doing so prevents users from elevating just to close a window by forcing them to click Cancel.</span></span>
    -   <span data-ttu-id="a356f-507">如需更多例外狀況，請參閱 [停用或移除控制項與提供錯誤訊息](#disabling-or-removing-controls-vs-giving-error-messages)。</span><span class="sxs-lookup"><span data-stu-id="a356f-507">For more exceptions, see [Disabling or removing controls vs. giving error messages](#disabling-or-removing-controls-vs-giving-error-messages).</span></span>
-   <span data-ttu-id="a356f-508">在 **對話方塊底部的單一資料列中，將認可按鈕靠右對齊，** 但在註腳區域上方。</span><span class="sxs-lookup"><span data-stu-id="a356f-508">**Right-align commit buttons in a single row across the bottom of the dialog box,** but above the footnote area.</span></span> <span data-ttu-id="a356f-509">即使有單一 [認可] 按鈕 (例如 [確定]) ，也請這麼做。</span><span class="sxs-lookup"><span data-stu-id="a356f-509">Do this even if there is a single commit button (such as OK).</span></span>

    <span data-ttu-id="a356f-510">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-510">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-511">具有中間 [確定] 按鈕之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-511">screen shot of message with centered ok button</span></span> ](images/win-dialog-box-image25.png)

    <span data-ttu-id="a356f-512">在此範例中，[確定] 按鈕的位置不正確。</span><span class="sxs-lookup"><span data-stu-id="a356f-512">In this example, the OK button is incorrectly centered.</span></span>

-   <span data-ttu-id="a356f-513">**依下列順序顯示認可按鈕：**</span><span class="sxs-lookup"><span data-stu-id="a356f-513">**Present the commit buttons in the following order:**</span></span>
    1.  <span data-ttu-id="a356f-514">確定/ \[ \] /Yes</span><span class="sxs-lookup"><span data-stu-id="a356f-514">OK/\[Do it\]/Yes</span></span>
    2.  <span data-ttu-id="a356f-515">\[不要 \] /No</span><span class="sxs-lookup"><span data-stu-id="a356f-515">\[Don't do it\]/No</span></span>
    3.  <span data-ttu-id="a356f-516">取消</span><span class="sxs-lookup"><span data-stu-id="a356f-516">Cancel</span></span>
    4.  <span data-ttu-id="a356f-517">套用 (（如果有的話）) </span><span class="sxs-lookup"><span data-stu-id="a356f-517">Apply (if present)</span></span>
    5.  <span data-ttu-id="a356f-518">說明 (是否存在) </span><span class="sxs-lookup"><span data-stu-id="a356f-518">Help (if present)</span></span>
-   <span data-ttu-id="a356f-519">**如果您有許多相關的認可按鈕，請使用分割按鈕來合併它們**。</span><span class="sxs-lookup"><span data-stu-id="a356f-519">**If you have many related commit buttons, consolidate them using split buttons**.</span></span>
-   <span data-ttu-id="a356f-520">**請明確地分隔 [認可] 按鈕 (關閉視窗) 和其他所有命令按鈕 (例如 [Advanced) ]。**</span><span class="sxs-lookup"><span data-stu-id="a356f-520">**Have a clear separation from commit buttons (which close the window) and all other command buttons (such as Advanced).**</span></span>

<span data-ttu-id="a356f-521">**回應主要指示**</span><span class="sxs-lookup"><span data-stu-id="a356f-521">**Responding to main instructions**</span></span>

-   <span data-ttu-id="a356f-522">**使用對主要指令有特定回應的正面認可按鈕，而不是一般標籤（例如 [確定] 或 [是]/[否]）。**</span><span class="sxs-lookup"><span data-stu-id="a356f-522">**Use positive commit buttons that are specific responses to the main instruction, instead of generic labels such as OK or Yes/No.**</span></span> <span data-ttu-id="a356f-523">使用者應該能夠藉由單獨讀取按鈕文字來瞭解這些選項。</span><span class="sxs-lookup"><span data-stu-id="a356f-523">Users should be able to understand the options by reading the button text alone.</span></span> <span data-ttu-id="a356f-524">**異常：**</span><span class="sxs-lookup"><span data-stu-id="a356f-524">**Exceptions:**</span></span>
    -   <span data-ttu-id="a356f-525">如果對話方塊沒有設定，請使用 [關閉]，例如資訊對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-525">Use Close for dialogs that don't have settings, such as informational dialogs.</span></span> <span data-ttu-id="a356f-526">請勿針對具有設定的對話方塊使用 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="a356f-526">Never use Close for dialogs that have settings.</span></span>
    -   <span data-ttu-id="a356f-527">當「特定」回應仍為泛型時，請使用 [確定]，例如 [儲存]、[選取] 或 [選擇]。</span><span class="sxs-lookup"><span data-stu-id="a356f-527">Use OK when the "specific" responses are still generic, such as Save, Select, or Choose.</span></span> <span data-ttu-id="a356f-528">變更特定設定或設定集合時，請使用 [確定]。</span><span class="sxs-lookup"><span data-stu-id="a356f-528">Use OK when changing a specific setting or a collection of settings.</span></span>
    -   <span data-ttu-id="a356f-529">**針對沒有主要指示的舊版對話方塊，您可以使用一般標籤，例如 [確定]。**</span><span class="sxs-lookup"><span data-stu-id="a356f-529">**For legacy dialog boxes without a main instruction, you can use generic labels such as OK.**</span></span> <span data-ttu-id="a356f-530">這類對話方塊通常不是為了執行特定工作而設計，因此無法執行特定的回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-530">Often such dialog boxes aren't designed to perform a specific task, preventing more specific responses.</span></span>
    -   <span data-ttu-id="a356f-531">某些工作需要更多考慮，並謹慎閱讀使用者，以做出明智的決策。</span><span class="sxs-lookup"><span data-stu-id="a356f-531">Certain tasks require more thought and careful reading for users to make informed decisions.</span></span> <span data-ttu-id="a356f-532">這通常是 [確認](mess-confirm.md)的情況。</span><span class="sxs-lookup"><span data-stu-id="a356f-532">This is usually the case with [confirmations](mess-confirm.md).</span></span> <span data-ttu-id="a356f-533">**在這種情況下，您可以刻意使用一般認可按鈕標籤來強制使用者讀取主要指示，並防止惟恐的決策。**</span><span class="sxs-lookup"><span data-stu-id="a356f-533">**In such cases, you can purposely use generic commit button labels to force users to read the main instructions and prevent hasty decisions.**</span></span>

        <span data-ttu-id="a356f-534">**正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-534">**Correct:**</span></span>

        ![具有 [是] 和 [否] 按鈕之訊息的螢幕擷取畫面](images/win-dialog-box-image26.png)

        <span data-ttu-id="a356f-536">在此範例中，使用 [是]/[否] 認可按鈕會強制使用者至少讀取主要指令。</span><span class="sxs-lookup"><span data-stu-id="a356f-536">In this example, using Yes/No commit buttons forces users to at least read the main instruction.</span></span>

-   <span data-ttu-id="a356f-537">**或者，您也可以將 "" 當然 "這個字新增至正面的認可按鈕標籤，以表示對話方塊顯示不會繼續的原因** ，而使用者應該先仔細閱讀對話方塊，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="a356f-537">**Alternatively, you can add the word "anyway" to the positive commit button label to indicate that the dialog box presents a reason not to proceed** and that users should read the dialog carefully before proceeding.</span></span>

    <span data-ttu-id="a356f-538">**正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-538">**Correct:**</span></span>

    ![<span data-ttu-id="a356f-539">[郵件和卸載] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-539">screen shot of message and uninstall anyway button</span></span> ](images/win-dialog-box-image27.png)

    <span data-ttu-id="a356f-540">在此範例中，「仍」會新增至認可按鈕標籤，表示使用者應謹慎進行。</span><span class="sxs-lookup"><span data-stu-id="a356f-540">In this example, "anyway" is added to the commit button label to indicate that users should proceed carefully.</span></span>

-   <span data-ttu-id="a356f-541">**針對負認可按鈕使用 [取消] 或 [關閉]，而不是對主要指令的特定回應。**</span><span class="sxs-lookup"><span data-stu-id="a356f-541">**Use Cancel or Close for negative commit buttons instead of specific responses to the main instruction.**</span></span> <span data-ttu-id="a356f-542">使用者通常會發現他們在看到對話方塊之後，他們不想要執行一項工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-542">Quite often users realize that they don't want to perform a task once they see a dialog box.</span></span> <span data-ttu-id="a356f-543">如果取消或關閉已重新標記為特定回應，則使用者必須仔細讀取所有認可按鈕，以決定如何取消。</span><span class="sxs-lookup"><span data-stu-id="a356f-543">If Cancel or Close were relabeled to specific responses, users would have to carefully read all the commit buttons to determine how to cancel.</span></span> <span data-ttu-id="a356f-544">**以一致的方式標記 [取消] 和 [關閉]，可讓您輕鬆尋找。異常：**</span><span class="sxs-lookup"><span data-stu-id="a356f-544">**Labeling Cancel and Close consistently makes them easy to find.Exceptions:**</span></span>
    -   <span data-ttu-id="a356f-545">**請勿使用 [是]/[取消]。**</span><span class="sxs-lookup"><span data-stu-id="a356f-545">**Don't use Yes/Cancel.**</span></span> <span data-ttu-id="a356f-546">一律使用 Yes/No 做為配對。</span><span class="sxs-lookup"><span data-stu-id="a356f-546">Always use Yes/No as a pair.</span></span>
    -   <span data-ttu-id="a356f-547">**當取消不明確時，請使用特定的回應。**</span><span class="sxs-lookup"><span data-stu-id="a356f-547">**Use a specific response when Cancel is ambiguous.**</span></span>
-   <span data-ttu-id="a356f-548">**請勿將一般標籤與內容區域中的文字對應至其特定意義。**</span><span class="sxs-lookup"><span data-stu-id="a356f-548">**Don't map generic labels to their specific meaning with text in the content area.**</span></span> <span data-ttu-id="a356f-549">相反地，使用特定的認可按鈕標籤，或使用連結的問題對話方塊（如果標籤很長）。</span><span class="sxs-lookup"><span data-stu-id="a356f-549">Instead, use specific commit button labels, or a question dialog using links if the labels are lengthy.</span></span>

    <span data-ttu-id="a356f-550">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-550">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-551">不清楚使用按鈕之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-551">screen shot of message with unclear use of buttons</span></span> ](images/win-dialog-box-image28.png)

    <span data-ttu-id="a356f-552">在此範例中，[確定] 對應到 [繼續]，[取消] 會對應到 [保持在] 頁面上。</span><span class="sxs-lookup"><span data-stu-id="a356f-552">In this example, OK is mapped to Continue, Cancel is mapped to Remain on Page.</span></span>

<span data-ttu-id="a356f-553">**是，沒有按鈕**</span><span class="sxs-lookup"><span data-stu-id="a356f-553">**Yes and No buttons**</span></span>

-   <span data-ttu-id="a356f-554">**偏好對 Yes 和 No 按鈕的特定回應。**</span><span class="sxs-lookup"><span data-stu-id="a356f-554">**Prefer specific responses to Yes and No buttons.**</span></span> <span data-ttu-id="a356f-555">雖然使用 [是] 和 [否] 並沒有任何問題，但可以更快速地瞭解特定的回應，進而做出有效率的決策。</span><span class="sxs-lookup"><span data-stu-id="a356f-555">While there's nothing wrong with using Yes and No, specific responses can be understood more quickly, resulting in efficient decision making.</span></span> <span data-ttu-id="a356f-556">不過， [確認](mess-confirm.md) 通常會有 [是] 和 [否] 按鈕，讓 [使用者在回應之前，](mess-confirm.md) 提供確認。</span><span class="sxs-lookup"><span data-stu-id="a356f-556">However, [confirmations](mess-confirm.md) usually have Yes and No buttons to make users give the confirmation [some thought](mess-confirm.md) before responding.</span></span>
-   <span data-ttu-id="a356f-557">**請使用 [是] 和 [無] 按鈕來回應是或沒有任何問題。**</span><span class="sxs-lookup"><span data-stu-id="a356f-557">**Use Yes and No buttons only to respond to yes or no questions.**</span></span> <span data-ttu-id="a356f-558">主要指示應以「是」或「無」問題的方式表示。</span><span class="sxs-lookup"><span data-stu-id="a356f-558">The main instruction should be naturally expressed as a yes or no question.</span></span> <span data-ttu-id="a356f-559">請勿使用 [確定] 並取消 [是] 或 [否]。</span><span class="sxs-lookup"><span data-stu-id="a356f-559">Never use OK and Cancel for yes or no questions.</span></span>

    <span data-ttu-id="a356f-560">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-560">**Incorrect:**</span></span>

    ![顯示具有 [確定] 之訊息的螢幕擷取畫面，表示沒有問題。](images/win-dialog-box-image29.png)

    <span data-ttu-id="a356f-562">**正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-562">**Correct:**</span></span>

    ![<span data-ttu-id="a356f-563">具有相同問題之 [是] 的訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-563">screen shot of message with yes for same question</span></span> ](images/win-dialog-box-image30.png)

    <span data-ttu-id="a356f-564">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="a356f-564">**Better:**</span></span>

    ![<span data-ttu-id="a356f-565">具有執行相同問題之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-565">screen shot of message with run for same question</span></span> ](images/win-dialog-box-image31.png)

    <span data-ttu-id="a356f-566">在這些範例中，[是] 和 [否] 都是良好的回應，而且沒有問題，但特定的回應更好。</span><span class="sxs-lookup"><span data-stu-id="a356f-566">In these examples, Yes and No are good responses to yes and no questions, but specific responses are even better.</span></span>

-   <span data-ttu-id="a356f-567">**如果有特定片語的認可按鈕很長或更難使用，請考慮將主要指令措辭視為是或否。**</span><span class="sxs-lookup"><span data-stu-id="a356f-567">**Consider phrasing the main instruction as a yes or no question if commit buttons with specific phrasing turn out to be long or awkward.**</span></span> <span data-ttu-id="a356f-568">或者，您可以使用命令連結來取得較長的回應 (五個字或更多) 至主要指令。</span><span class="sxs-lookup"><span data-stu-id="a356f-568">Alternatively, you can use command links for longer responses (five words or more) to the main instruction.</span></span>

    <span data-ttu-id="a356f-569">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-569">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-570">具有冗長按鈕標籤之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-570">screen shot of message with wordy button labels</span></span> ](images/win-dialog-box-image32.png)

    <span data-ttu-id="a356f-571">**正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-571">**Correct:**</span></span>

    ![<span data-ttu-id="a356f-572">具有 [是]/[否] 按鈕標籤之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-572">screen shot of message with yes/no button labels</span></span> ](images/win-dialog-box-image33.png)

    <span data-ttu-id="a356f-573">錯誤範例中的特定措辭太長，所以正確的範例會使用 Yes 和 No。</span><span class="sxs-lookup"><span data-stu-id="a356f-573">The specific phrasing in the incorrect example is too long, so the correct example uses Yes and No.</span></span>

-   <span data-ttu-id="a356f-574">**如果沒有回應的意義不清楚，請不要使用 [是] 和 [否] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-574">**Don't use Yes and No buttons if the meaning of the No response is unclear.**</span></span> <span data-ttu-id="a356f-575">若是如此，請改用特定回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-575">If so, use specific responses instead.</span></span>

<span data-ttu-id="a356f-576">**確定按鈕**</span><span class="sxs-lookup"><span data-stu-id="a356f-576">**OK buttons**</span></span>

-   <span data-ttu-id="a356f-577">**在強制回應對話方塊中，按一下 [確定] 表示套用值、執行工作，然後關閉視窗。**</span><span class="sxs-lookup"><span data-stu-id="a356f-577">**In modal dialogs, clicking OK means apply the values, perform the task, and close the window.**</span></span>
-   <span data-ttu-id="a356f-578">**請勿使用 [確定] 按鈕來回應問題。**</span><span class="sxs-lookup"><span data-stu-id="a356f-578">**Don't use OK buttons to respond to questions.**</span></span>
-   <span data-ttu-id="a356f-579">**請勿將存取金鑰指派給 [確定]，因為 Enter 是預設按鈕的存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="a356f-579">**Don't assign access keys to OK, because Enter is the access key for the default button.**</span></span> <span data-ttu-id="a356f-580">這麼做可讓您更輕鬆地指派其他存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-580">Doing so makes the other access keys easier to assign.</span></span>
-   <span data-ttu-id="a356f-581">**正確地標示 [確定] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-581">**Label OK buttons correctly.**</span></span> <span data-ttu-id="a356f-582">[確定] 按鈕應標示為 [確定]，不是 [確定] 或 [確定]。</span><span class="sxs-lookup"><span data-stu-id="a356f-582">The OK button should be labeled OK, not Ok or Okay.</span></span>
-   <span data-ttu-id="a356f-583">**請勿使用 [確定] 按鈕來取得錯誤或警告。**</span><span class="sxs-lookup"><span data-stu-id="a356f-583">**Don't use OK buttons for errors or warnings.**</span></span> <span data-ttu-id="a356f-584">問題永遠沒問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-584">Problems are never OK.</span></span> <span data-ttu-id="a356f-585">請改用 Close。</span><span class="sxs-lookup"><span data-stu-id="a356f-585">Use Close instead.</span></span>

    <span data-ttu-id="a356f-586">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-586">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-587">具有 [確定] 按鈕之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-587">screen shot of message with ok button</span></span> ](images/win-dialog-box-image34.png)

    <span data-ttu-id="a356f-588">在此範例中，應該使用 Close 而不是 OK。</span><span class="sxs-lookup"><span data-stu-id="a356f-588">In this example, Close should be used instead of OK.</span></span>

-   <span data-ttu-id="a356f-589">**請勿在非強制回應對話方塊中使用 [確定] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-589">**Don't use OK buttons in modeless dialog boxes.**</span></span> <span data-ttu-id="a356f-590">非強制回應對話方塊應使用工作特定的認可按鈕 (例如，尋找) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-590">Rather, modeless dialogs should use task-specific commit buttons (for example, Find).</span></span> <span data-ttu-id="a356f-591">不過，某些非強制回應對話方塊只需要 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-591">However, some modeless dialog boxes require only a Close button.</span></span>

<span data-ttu-id="a356f-592">**取消按鈕**</span><span class="sxs-lookup"><span data-stu-id="a356f-592">**Cancel buttons**</span></span>

-   <span data-ttu-id="a356f-593">**按一下 [取消] 表示放棄所有變更、取消工作、關閉視窗，然後將環境傳回至先前的狀態，而不會產生副作用。**</span><span class="sxs-lookup"><span data-stu-id="a356f-593">**Clicking Cancel means abandon all changes, cancel the task, close the window, and return the environment to its previous state, leaving no side effect.**</span></span> <span data-ttu-id="a356f-594">針對嵌套選擇對話方塊，在 [擁有者選擇] 對話方塊中按一下 [取消] 表示也會放棄擁有選擇對話方塊所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a356f-594">For nested choice dialog boxes, clicking Cancel in the owner choice dialog means any changes made by owned choice dialogs are also abandoned.</span></span>
-   <span data-ttu-id="a356f-595">**提供 [取消] 按鈕，讓使用者明確放棄變更。**</span><span class="sxs-lookup"><span data-stu-id="a356f-595">**Provide a Cancel button to let users explicitly abandon changes.**</span></span> <span data-ttu-id="a356f-596">對話方塊需要明確的結束點。</span><span class="sxs-lookup"><span data-stu-id="a356f-596">Dialog boxes need a clear exit point.</span></span> <span data-ttu-id="a356f-597">不要依賴使用者尋找標題列上的 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-597">Don't depend on users finding the Close button on the title bar.</span></span>

    -   <span data-ttu-id="a356f-598">**例外狀況：** 請勿在沒有設定的情況下提供對話方塊的 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-598">**Exception:** Don't provide a Cancel button for dialog boxes without settings.</span></span> <span data-ttu-id="a356f-599">在此情況下，[確定] 和 [關閉] 按鈕的效果與 [取消] 相同。</span><span class="sxs-lookup"><span data-stu-id="a356f-599">The OK and Close buttons have the same effect as Cancel in this case.</span></span>

    <span data-ttu-id="a356f-600">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-600">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-601">只有 [確定] 按鈕的 [訊息] 螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-601">screen shot of message with ok button only</span></span> ](images/win-dialog-box-image35.png)

    <span data-ttu-id="a356f-602">在此範例中，只有標題列上的 [關閉] 按鈕，讓它看起來好像使用者沒有選擇。</span><span class="sxs-lookup"><span data-stu-id="a356f-602">In this example, having only a Close button on the title bar makes it appear as though users don't have a choice.</span></span>

-   <span data-ttu-id="a356f-603">**請勿使用 [取消] 按鈕來回應問題。**</span><span class="sxs-lookup"><span data-stu-id="a356f-603">**Don't use Cancel buttons to respond to questions.**</span></span>

    <span data-ttu-id="a356f-604">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-604">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-605">訊息的螢幕擷取畫面，[確定]-沒有問題</span><span class="sxs-lookup"><span data-stu-id="a356f-605">screen shot of message with ok for yes-no question</span></span> ](images/win-dialog-box-image36.png)

    <span data-ttu-id="a356f-606">在此範例中，[確定] 和 [取消] 不正確地用來回應是或沒有問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-606">In this example, OK and Cancel are incorrectly used to respond to a Yes or No question.</span></span>

-   <span data-ttu-id="a356f-607">**請勿將存取金鑰指派給取消，因為 Esc 是存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="a356f-607">**Don't assign access keys to Cancel, because Esc is the access key.**</span></span> <span data-ttu-id="a356f-608">這麼做可讓您更輕鬆地指派其他存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-608">Doing so makes the other access keys easier to assign.</span></span>
-   <span data-ttu-id="a356f-609">**請勿使用非強制回應對話方塊中的 [取消] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-609">**Don't use Cancel buttons in modeless dialog boxes.**</span></span> <span data-ttu-id="a356f-610">相反地，請改用 Close。</span><span class="sxs-lookup"><span data-stu-id="a356f-610">Rather, use Close instead.</span></span>
-   <span data-ttu-id="a356f-611">**請勿停用 [取消] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-611">**Don't disable the Cancel button.**</span></span> <span data-ttu-id="a356f-612">使用者應該一律能夠取消對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-612">Users should always be able to cancel dialog boxes.</span></span>
    -   <span data-ttu-id="a356f-613">**例外狀況：** 如果有一段期間無法取消作業，您可以停用 [進度] 對話方塊中的 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-613">**Exception:** You may disable the Cancel button in a progress dialog if there is a period during which the operation can't be cancelled.</span></span> <span data-ttu-id="a356f-614">不過，更好的解決方法是將這類作業設計成永遠可取消。</span><span class="sxs-lookup"><span data-stu-id="a356f-614">However, a better solution is to design such operations to always be cancelable.</span></span>

<span data-ttu-id="a356f-615">**關閉按鈕**</span><span class="sxs-lookup"><span data-stu-id="a356f-615">**Close buttons**</span></span>

-   <span data-ttu-id="a356f-616">**使用非強制回應對話方塊的 [關閉] 按鈕，以及無法取消的強制回應對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-616">**Use Close buttons for modeless dialog boxes, as well as modal dialogs that cannot be cancelled.**</span></span>
-   <span data-ttu-id="a356f-617">**按一下 [關閉] 表示關閉對話方塊視窗，並留下任何現有的副作用。**</span><span class="sxs-lookup"><span data-stu-id="a356f-617">**Clicking Close means close the dialog box window, leaving any existing side effects.**</span></span> <span data-ttu-id="a356f-618">請勿使用完成，因為它不是命令式結構。</span><span class="sxs-lookup"><span data-stu-id="a356f-618">Don't use Done, because it isn't an imperative construction.</span></span> <span data-ttu-id="a356f-619">針對 [嵌套選擇] 對話方塊，按一下 [擁有者選擇] 對話方塊中的 [關閉]，表示保留所擁有選擇對話方塊所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a356f-619">For nested choice dialog boxes, clicking Close in the owner choice dialog means any changes made by owned choice dialogs are preserved.</span></span>
-   <span data-ttu-id="a356f-620">**在對話方塊主體中放置明確的 [關閉] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-620">**Put an explicit Close button in the dialog box body.**</span></span> <span data-ttu-id="a356f-621">對話方塊需要明確的結束點。</span><span class="sxs-lookup"><span data-stu-id="a356f-621">Dialog boxes need a clear exit point.</span></span> <span data-ttu-id="a356f-622">不要依賴使用者尋找標題列上的 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-622">Don't depend on users finding the Close button on the title bar.</span></span>
-   <span data-ttu-id="a356f-623">**請確定標題列上的 [關閉] 按鈕與 [取消] 或 [關閉] 具有相同的效果。**</span><span class="sxs-lookup"><span data-stu-id="a356f-623">**Make sure the Close button on the title bar has the same effect as Cancel or Close.**</span></span>
-   <span data-ttu-id="a356f-624">**請勿指派便捷鍵來關閉，因為 Esc 是存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="a356f-624">**Don't assign access keys to Close, because Esc is its the access key.**</span></span> <span data-ttu-id="a356f-625">這麼做可讓您更輕鬆地指派其他存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-625">Doing so makes the other access keys easier to assign.</span></span>

<span data-ttu-id="a356f-626">**套用按鈕**</span><span class="sxs-lookup"><span data-stu-id="a356f-626">**Apply buttons**</span></span>

-   <span data-ttu-id="a356f-627">**請勿在不是屬性工作表或控制項面板的對話方塊中使用 [套用] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-627">**Don't use Apply buttons in dialog boxes that aren't property sheets or control panels.**</span></span> <span data-ttu-id="a356f-628">[套用] 按鈕表示套用暫止的變更，但讓視窗保持開啟。</span><span class="sxs-lookup"><span data-stu-id="a356f-628">The Apply button means apply the pending changes, but leave the window open.</span></span> <span data-ttu-id="a356f-629">這麼做可讓使用者在關閉視窗之前評估變更。</span><span class="sxs-lookup"><span data-stu-id="a356f-629">Doing so allows users to evaluate the changes before closing the window.</span></span> <span data-ttu-id="a356f-630">不過，只有屬性工作表和控制台才有此需求。</span><span class="sxs-lookup"><span data-stu-id="a356f-630">However, only property sheet and control panels have this need.</span></span>

    <span data-ttu-id="a356f-631">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-631">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-632">具有 [套用] 按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-632">screen shot of dialog box with apply button</span></span> ](images/win-dialog-box-image37.png)

    <span data-ttu-id="a356f-633">在此範例中，選擇對話方塊不必要，有 [套用] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-633">In this example, a choice dialog needlessly has an Apply button.</span></span>

<span data-ttu-id="a356f-634">**間接對話方塊的認可按鈕**</span><span class="sxs-lookup"><span data-stu-id="a356f-634">**Commit buttons for indirect dialog boxes**</span></span>

<span data-ttu-id="a356f-635">**注意：** 間接對話方塊會顯示在內容之外，可能是因為工作的間接結果，或是系統或背景進程發生問題的結果。</span><span class="sxs-lookup"><span data-stu-id="a356f-635">**Note:** Indirect dialog boxes are displayed out of context, either as an indirect result of a task or the result of a problem with a system or background process.</span></span> <span data-ttu-id="a356f-636">若為間接對話，[取消] 按鈕會是不明確的，因為它可能表示取消對話方塊或取消整個工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-636">For indirect dialogs, the Cancel button is ambiguous because it could mean cancel the dialog or cancel the entire task.</span></span>

-   <span data-ttu-id="a356f-637">**如果使用者需要取消對話方塊和工作，請提供認可按鈕來進行這兩項作業。**</span><span class="sxs-lookup"><span data-stu-id="a356f-637">**If users need to both cancel the dialog box and the task, give commit buttons to do both.**</span></span> <span data-ttu-id="a356f-638">將取消對話方塊的按鈕標示為主要指示的負值回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-638">Label the button that cancels the dialog box with a negative response to the main instruction.</span></span> <span data-ttu-id="a356f-639">為取消整個工作的按鈕加上標籤。</span><span class="sxs-lookup"><span data-stu-id="a356f-639">Label the button that cancels the entire task with Cancel.</span></span> <span data-ttu-id="a356f-640">使用 [取消] 可讓對話方塊在許多內容中使用。</span><span class="sxs-lookup"><span data-stu-id="a356f-640">Using Cancel allows the dialog box to be used in many contexts.</span></span>

    <span data-ttu-id="a356f-641">**正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-641">**Correct:**</span></span>

    ![<span data-ttu-id="a356f-642">具有儲存/不儲存之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-642">screen shot of dialog box with save/don't save</span></span> ](images/win-dialog-box-image38.png)

    <span data-ttu-id="a356f-643">在此範例中，當尚未儲存圖形時，Windows Paint 會將此對話方塊顯示為新的或結束命令的結果。</span><span class="sxs-lookup"><span data-stu-id="a356f-643">In this example, this dialog box is displayed by Windows Paint as the result of a New or Exit command when the graphic hasn't been saved.</span></span> <span data-ttu-id="a356f-644">請勿儲存並關閉對話方塊而不儲存，而取消會取消新的或結束命令。</span><span class="sxs-lookup"><span data-stu-id="a356f-644">Don't Save closes the dialog without saving, whereas Cancel cancels the New or Exit command.</span></span>

    <span data-ttu-id="a356f-645">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-645">**Incorrect:**</span></span>

    ![<span data-ttu-id="a356f-646">具有 [是]/[否] 按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-646">screen shot of dialog box with yes/no buttons</span></span> ](images/win-dialog-box-image39.png)

    <span data-ttu-id="a356f-647">在此範例中，無法取消工作 (關閉會導致顯示此對話方塊的 Office 快捷方式列) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-647">In this example, there is no way to cancel the task (closing Office Shortcut Bar) that led to displaying this dialog box.</span></span> <span data-ttu-id="a356f-648">這個對話方塊需要 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-648">This dialog box needs a Cancel button.</span></span>

-   <span data-ttu-id="a356f-649">**如果使用者只需要取消對話方塊，而不是工作，請使用具有特定、負回應的按鈕來回應主要指示，** 而且沒有 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-649">**If users just need to cancel the dialog but not the task, use a button with a specific, negative response to the main instruction,** and don't have a Cancel button.</span></span>

    ![<span data-ttu-id="a356f-650">具有執行/不執行之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-650">screen shot of dialog box with run/don't run</span></span> ](images/win-dialog-box-image24.png)

    <span data-ttu-id="a356f-651">在此範例中，當流覽至安裝 ActiveX 控制項的網頁時，會間接顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-651">In this example, this dialog box is displayed indirectly as the result of navigating to a Web page that installs an ActiveX control.</span></span> <span data-ttu-id="a356f-652">在這裡使用 [取消] 會不明確，因此會改用 [不要執行]。</span><span class="sxs-lookup"><span data-stu-id="a356f-652">Using Cancel would be ambiguous here, so Don't run is used instead.</span></span>

<span data-ttu-id="a356f-653">如需詳細資訊和範例，請參閱 [命令按鈕](ctrl-command-buttons.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-653">For more information and examples, see [Command Buttons](ctrl-command-buttons.md).</span></span>

### <a name="command-links"></a><span data-ttu-id="a356f-654">命令連結</span><span class="sxs-lookup"><span data-stu-id="a356f-654">Command links</span></span>

-   <span data-ttu-id="a356f-655">**使用命令連結，而非命令按鈕或選項按鈕和 [確定] 按鈕的組合，來呈現一組冗長的命令。**</span><span class="sxs-lookup"><span data-stu-id="a356f-655">**Present a set of lengthy commands using command links, instead of command buttons or a combination of radio buttons and an OK button.**</span></span> <span data-ttu-id="a356f-656">這樣做可讓使用者只需按一下就能回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-656">Doing so allows users to respond with a single click.</span></span> <span data-ttu-id="a356f-657">不過，此方法只適用于單一問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-657">However, this approach works only for a single question.</span></span>
-   <span data-ttu-id="a356f-658">**先顯示最常使用的命令連結。**</span><span class="sxs-lookup"><span data-stu-id="a356f-658">**Present the most commonly used command links first.**</span></span> <span data-ttu-id="a356f-659">產生的順序大致上應該遵循使用的可能性，但也有邏輯流程。</span><span class="sxs-lookup"><span data-stu-id="a356f-659">The resulting order should roughly follow the likelihood of use, but also have a logical flow.</span></span>
    -   <span data-ttu-id="a356f-660">**例外狀況：** 導致執行所有工作的命令連結應先放置。</span><span class="sxs-lookup"><span data-stu-id="a356f-660">**Exception:** Command links that result in doing everything should be placed first.</span></span>
-   <span data-ttu-id="a356f-661">如果命令連結需要進一步的說明，請 **提供補充說明。**</span><span class="sxs-lookup"><span data-stu-id="a356f-661">If a command link requires further explanation, **provide a supplemental explanation.**</span></span> <span data-ttu-id="a356f-662">補充說明說明使用者可能會想要選擇命令的原因，或如果選擇命令會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="a356f-662">Supplemental explanations describe why users might want to choose the command, or what happens if the command is chosen.</span></span>
-   <span data-ttu-id="a356f-663">**請勿使用冗長重述命令連結的補充說明。**</span><span class="sxs-lookup"><span data-stu-id="a356f-663">**Don't use supplemental explanations that are wordy restatements of the command link.**</span></span> <span data-ttu-id="a356f-664">只有當您無法讓命令連結一目了然時，才使用補充說明。</span><span class="sxs-lookup"><span data-stu-id="a356f-664">Use a supplemental explanation only when you can't make a command link self-explanatory.</span></span> <span data-ttu-id="a356f-665">提供一個命令連結的補充說明，並不表示您必須為所有命令提供它們。</span><span class="sxs-lookup"><span data-stu-id="a356f-665">Providing a supplemental explanation for one command link doesn't mean that you have to provide them for all commands.</span></span>

![<span data-ttu-id="a356f-666">具有文字注意選項之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-666">screen shot of dialog box with text noting options</span></span> ](images/win-dialog-box-image40.png)

<span data-ttu-id="a356f-667">在此範例中，補充說明說明其中一個選項的含意。</span><span class="sxs-lookup"><span data-stu-id="a356f-667">In this example, the supplemental explanation describes the implications of one of the options.</span></span>

-   <span data-ttu-id="a356f-668">**使用以動詞開頭的片語，不含結束標點符號。**</span><span class="sxs-lookup"><span data-stu-id="a356f-668">**Use phrases that start with a verb, without ending punctuation.**</span></span>
-   <span data-ttu-id="a356f-669">**如果是強烈建議的命令，請考慮將「 (建議的) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="a356f-669">**If a command is strongly recommended, consider adding "(recommended)" to the label.**</span></span> <span data-ttu-id="a356f-670">請務必新增至連結標籤，而不是補充說明。</span><span class="sxs-lookup"><span data-stu-id="a356f-670">Be sure to add to the link label, not the supplemental explanation.</span></span>
-   <span data-ttu-id="a356f-671">**如果命令僅供 advanced 使用者使用，請考慮將「 (advanced) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="a356f-671">**If a command is intended only for advanced users, consider adding "(advanced)" to the label.**</span></span> <span data-ttu-id="a356f-672">請務必新增至連結標籤，而不是補充說明。</span><span class="sxs-lookup"><span data-stu-id="a356f-672">Be sure to add to the link label, not the supplemental explanation.</span></span>
-   <span data-ttu-id="a356f-673">**一律提供明確的 [取消] 按鈕**。</span><span class="sxs-lookup"><span data-stu-id="a356f-673">**Always provide an explicit Cancel button**.</span></span> <span data-ttu-id="a356f-674">請勿將命令連結用於此用途。</span><span class="sxs-lookup"><span data-stu-id="a356f-674">Don't use a command link for this purpose.</span></span>

<span data-ttu-id="a356f-675">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-675">**Incorrect:**</span></span>

![<span data-ttu-id="a356f-676">[不結束] 連結之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-676">screen shot of dialog box with don't exit link</span></span> ](images/win-dialog-box-image41.png)

<span data-ttu-id="a356f-677">在此範例中，對話方塊會使用命令連結，而不是 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-677">In this example, the dialog box uses a command link instead of a Cancel button.</span></span>

<span data-ttu-id="a356f-678">如需詳細資訊和範例，請參閱 [命令連結](ctrl-command-links.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-678">For more information and examples, see [Command Links](ctrl-command-links.md).</span></span>

### <a name="dont-show-this-item-again"></a><span data-ttu-id="a356f-679">不要顯示此</span><span class="sxs-lookup"><span data-stu-id="a356f-679">Don't show this</span></span> <item> <span data-ttu-id="a356f-680">再次</span><span class="sxs-lookup"><span data-stu-id="a356f-680">again</span></span>

-   <span data-ttu-id="a356f-681">**<item>如果沒有更好的替代方案，請考慮使用 [不要再顯示這個選項] 選項，讓使用者隱藏週期性對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-681">**Consider using a Don't show this <item> again option to allow users to suppress a recurring dialog box, only if there isn't a better alternative.**</span></span> <span data-ttu-id="a356f-682">最好的方式是在使用者真的需要時顯示對話方塊，或直接將它排除（如果沒有的話）。</span><span class="sxs-lookup"><span data-stu-id="a356f-682">It is better always to show the dialog if users really need it, or simply eliminate it if they don't.</span></span>
-   <span data-ttu-id="a356f-683">**使用這個特定的措辭取代 <item> 為特定的專案。**</span><span class="sxs-lookup"><span data-stu-id="a356f-683">**Use this specific phrasing replace <item> with the specific item.**</span></span> <span data-ttu-id="a356f-684">例如，不要再顯示此提醒。</span><span class="sxs-lookup"><span data-stu-id="a356f-684">For example, Don't show this reminder again.</span></span> <span data-ttu-id="a356f-685">在一般情況下參考對話方塊時，請使用 [不要再顯示此訊息]。</span><span class="sxs-lookup"><span data-stu-id="a356f-685">When referring to a dialog box in general, use Don't show this message again.</span></span>
-   <span data-ttu-id="a356f-686">藉由在選項下新增下列句子，**清楚地指出使用者輸入將用於未來預設值**：未來將會使用您的選取專案。</span><span class="sxs-lookup"><span data-stu-id="a356f-686">**Clearly indicate when user input will be used for future default values** by adding the following sentence under the option: Your selections will be used by default in the future.</span></span>
-   <span data-ttu-id="a356f-687">**預設不會選取此選項。如果對話方塊真的只應顯示一次，請在不詢問的情況下進行。**</span><span class="sxs-lookup"><span data-stu-id="a356f-687">**Don't select the option by default. If the dialog box really should be displayed only once, do so without asking.**</span></span> <span data-ttu-id="a356f-688">請勿使用這個選項來因應使用者，請確定預設行為不會令人討厭。</span><span class="sxs-lookup"><span data-stu-id="a356f-688">Don't use this option as an excuse to annoy users make sure the default behavior isn't annoying.</span></span>

<span data-ttu-id="a356f-689">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-689">**Incorrect:**</span></span>

![<span data-ttu-id="a356f-690">訊息的螢幕擷取畫面，詢問不必要的問題</span><span class="sxs-lookup"><span data-stu-id="a356f-690">screen shot of message asking unnecessary question</span></span> ](images/win-dialog-box-image42.png)

<span data-ttu-id="a356f-691">在此範例中，訊息只會顯示一次。</span><span class="sxs-lookup"><span data-stu-id="a356f-691">In this example, the message should just be displayed once.</span></span> <span data-ttu-id="a356f-692">不需要詢問。</span><span class="sxs-lookup"><span data-stu-id="a356f-692">No need to ask.</span></span>

-   <span data-ttu-id="a356f-693">**讓設定以每個使用者為基礎來保存。**</span><span class="sxs-lookup"><span data-stu-id="a356f-693">**Make the setting persist on a per-user basis.**</span></span>
-   <span data-ttu-id="a356f-694">**如果使用者選取選項，然後按一下 [取消]，此選項就會生效。**</span><span class="sxs-lookup"><span data-stu-id="a356f-694">**If users select the option and click Cancel, this option does take effect.**</span></span> <span data-ttu-id="a356f-695">這項設定是中繼選項，因此它不會遵循不留下副作用的標準取消行為。</span><span class="sxs-lookup"><span data-stu-id="a356f-695">This setting is a meta-option, so it doesn't follow the standard Cancel behavior of leaving no side effect.</span></span> <span data-ttu-id="a356f-696">請注意，如果使用者不想要在未來看到對話方塊，很有可能會想要取消它。</span><span class="sxs-lookup"><span data-stu-id="a356f-696">Note that if users don't want to see the dialog in the future, most likely they want to cancel it as well.</span></span>
-   <span data-ttu-id="a356f-697">如果使用者可能需要還原這些對話方塊，請在程式的 [選項] 對話方塊中提供 [ **還原訊息** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="a356f-697">If users may need to restore these dialog boxes, provide a **Restore messages** command in the program's Options dialog box.</span></span>

### <a name="ask-me-later"></a><span data-ttu-id="a356f-698">稍後詢問我</span><span class="sxs-lookup"><span data-stu-id="a356f-698">Ask me later</span></span>

-   <span data-ttu-id="a356f-699">只有在下列情況下，才提供此選項來關閉對話方塊：</span><span class="sxs-lookup"><span data-stu-id="a356f-699">Provide this option to dismiss a dialog box only when:</span></span>
    -   <span data-ttu-id="a356f-700">**對話方塊是間接的**，因此使用者可能會專注于另一項工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-700">**The dialog box is indirect**, so users are likely to be focused on another task.</span></span>
    -   <span data-ttu-id="a356f-701">**使用者必須回應但不能立即** 進行，以便他們繼續工作。</span><span class="sxs-lookup"><span data-stu-id="a356f-701">**Users must respond but not immediately**, so they can continue with their work.</span></span>
    -   <span data-ttu-id="a356f-702">**問題需要足夠的想法或努力** ，讓使用者可以在有更多時間時做出更好的決策。</span><span class="sxs-lookup"><span data-stu-id="a356f-702">**The question requires sufficient thought or effort** such that users might make better decisions if given more time.</span></span>
    -   <span data-ttu-id="a356f-703">**對話方塊或選項稍後會自動顯示** (，讓使用者在稍後) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-703">**The dialog box or option will be presented automatically later** (so that users really are asked later).</span></span>
-   <span data-ttu-id="a356f-704">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-704">**Incorrect:**</span></span>
-   ![<span data-ttu-id="a356f-705">具有 [稍後詢問我] 選項之 [訊息的螢幕擷取畫面] 選項</span><span class="sxs-lookup"><span data-stu-id="a356f-705">screen shot of message with ask me later option</span></span> ](images/win-dialog-box-image43.png)
-   <span data-ttu-id="a356f-706">在此範例中，問題很簡單，只要新增 [稍後詢問我] 選項就會讓它變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="a356f-706">In this example, the question is simple enough that adding an Ask me later option only complicates it.</span></span>
-   <span data-ttu-id="a356f-707">否則，會預期使用者現在會回應，但可讓他們以 [取消] 或 [關閉] 正常關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-707">Otherwise, expect users to respond now, but allow them to close the dialog box normally with either Cancel or Close.</span></span> <span data-ttu-id="a356f-708">正確使用時，此選項應該很罕見。</span><span class="sxs-lookup"><span data-stu-id="a356f-708">When used properly, this option should be rare.</span></span>

### <a name="morefewer"></a><span data-ttu-id="a356f-709">更多/較少</span><span class="sxs-lookup"><span data-stu-id="a356f-709">More/Fewer</span></span>

-   <span data-ttu-id="a356f-710">**使用 [更多]/[漸進式洩漏] 按鈕來顯示或隱藏目標使用者通常不需要的 advanced 或罕見選項、命令或詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="a356f-710">**Use More/Fewer progressive disclosure buttons to show or hide advanced or rarely used options, commands, or details that target users typically don't need.**</span></span> <span data-ttu-id="a356f-711">這麼做可簡化一般使用方式的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-711">Doing so simplifies the dialog box for typical usage.</span></span> <span data-ttu-id="a356f-712">請勿隱藏常用的選項、命令或資訊，因為使用者可能找不到這些選項、命令或資訊。</span><span class="sxs-lookup"><span data-stu-id="a356f-712">Don't hide commonly used options, commands, or information because users might not find them.</span></span>

![<span data-ttu-id="a356f-713">具有 [其他選項] 按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-713">screen shot of dialog box with more options button</span></span> ](images/win-dialog-box-image24.png)

<span data-ttu-id="a356f-714">在此範例中，預設會隱藏少用的選項。</span><span class="sxs-lookup"><span data-stu-id="a356f-714">In this example, rarely used options are hidden by default.</span></span>

-   <span data-ttu-id="a356f-715">**除非真的有更多詳細資料可顯示，否則請不要使用更多/較少的控制項。**</span><span class="sxs-lookup"><span data-stu-id="a356f-715">**Don't use More/Fewer controls unless there really is more detail to show.**</span></span> <span data-ttu-id="a356f-716">請勿只以不同的格式重新聲明相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="a356f-716">Don't just restate the same information in a different format.</span></span>
-   <span data-ttu-id="a356f-717">**請勿使用更多/較少的控制項來顯示說明。**</span><span class="sxs-lookup"><span data-stu-id="a356f-717">**Don't use More/Fewer controls to show Help.**</span></span> <span data-ttu-id="a356f-718">請改用說明連結或註腳。</span><span class="sxs-lookup"><span data-stu-id="a356f-718">Use Help links or footnotes instead.</span></span>
-   <span data-ttu-id="a356f-719">**使用工作對話方塊時，請避免合併更多/較少的控制項，且不要 <item> 再次顯示。**</span><span class="sxs-lookup"><span data-stu-id="a356f-719">**With task dialogs, avoid combining More/Fewer controls with Don't show this <item> again.**</span></span> <span data-ttu-id="a356f-720">這種組合有一種麻煩的外觀。</span><span class="sxs-lookup"><span data-stu-id="a356f-720">This combination has an awkward appearance.</span></span>
-   <span data-ttu-id="a356f-721">如需標籤指導方針，請參閱 [漸進式洩漏](ctrl-progressive-disclosure-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-721">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="footnotes"></a><span data-ttu-id="a356f-722">註腳</span><span class="sxs-lookup"><span data-stu-id="a356f-722">Footnotes</span></span>

-   <span data-ttu-id="a356f-723">**使用註腳來取得對對話方塊用途不重要的資訊，但使用者可能會覺得有助於做出決策。**</span><span class="sxs-lookup"><span data-stu-id="a356f-723">**Use footnotes for information that's not essential to a dialog box's purpose, but that users may find helpful in making decisions.**</span></span> <span data-ttu-id="a356f-724">大部分的使用者都應該能夠略過註腳，並且仍在回應對話方塊時做出明智的決策。</span><span class="sxs-lookup"><span data-stu-id="a356f-724">Most users should be able to skip footnotes and still make informed decisions in their response to the dialog box.</span></span>

![<span data-ttu-id="a356f-725">含有澄清註腳之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-725">screen shot of dialog box with clarifying footnote</span></span> ](images/win-dialog-box-image44.png)

<span data-ttu-id="a356f-726">在此範例中，註腳資訊是補充項，不是必要的。</span><span class="sxs-lookup"><span data-stu-id="a356f-726">In this example, the footnote information is supplemental, not essential.</span></span>

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a><span data-ttu-id="a356f-727">停用或移除控制項與提供錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="a356f-727">Disabling or removing controls vs. giving error messages</span></span>

-   <span data-ttu-id="a356f-728">當控制項未套用至目前的內容時，請考慮下列選項：</span><span class="sxs-lookup"><span data-stu-id="a356f-728">When a control doesn't apply in the current context, consider the following options:</span></span>
    -   <span data-ttu-id="a356f-729">**當使用者無法啟用控制項時，請移除該控制項，否則使用者不會預期它會套用，而且其狀態不會經常變更。**</span><span class="sxs-lookup"><span data-stu-id="a356f-729">**Remove the control when there is no way for users to enable it, or users don't expect it to apply and its state doesn't change frequently.**</span></span> <span data-ttu-id="a356f-730">這麼做可簡化對話方塊，使用者也不會錯過。</span><span class="sxs-lookup"><span data-stu-id="a356f-730">Doing so simplifies the dialog box, and users won't miss it.</span></span> <span data-ttu-id="a356f-731">具有控制項的出現和經常消失很討厭。</span><span class="sxs-lookup"><span data-stu-id="a356f-731">Having a control appear and disappear frequently is annoying.</span></span>
    -   <span data-ttu-id="a356f-732">**當使用者預期應用程式會經常套用或其狀態變更時，請停用該控制項，而且使用者可以輕鬆地推算控制項停用的原因。**</span><span class="sxs-lookup"><span data-stu-id="a356f-732">**Disable the control when users expect it to apply or its state changes frequently, and users can easily deduce why the control is disabled.**</span></span> <span data-ttu-id="a356f-733">如果有單一的空白文字方塊需要任何輸入，則很容易推算的範例會停用認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-733">An example of easy deduction is disabling a commit button when there is a single, empty text box that requires any input.</span></span> <span data-ttu-id="a356f-734">您可以使用 [氣球](ctrl-balloons.md) 來顯示非關鍵性的使用者輸入問題，以及文字方塊和可編輯的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="a356f-734">You can use [balloons](ctrl-balloons.md) to display non-critical user input problems with text boxes and editable drop-down lists.</span></span> <span data-ttu-id="a356f-735">但是，如果無法使用氣球來說明問題，或是牽涉到多個控制項，則推算將不再很簡單。</span><span class="sxs-lookup"><span data-stu-id="a356f-735">However, if the problem can't be explained with a balloon or involves multiple controls, the deduction would no longer be easy.</span></span>
    -   <span data-ttu-id="a356f-736">**否則，請讓控制項保持啟用狀態，但使用錯誤訊息時，請提供錯誤訊息。**</span><span class="sxs-lookup"><span data-stu-id="a356f-736">**Otherwise, leave the control enabled, but give an error message when it is used incorrectly.**</span></span> <span data-ttu-id="a356f-737">在此情況下停用會讓使用者難以瞭解控制項的停用原因。</span><span class="sxs-lookup"><span data-stu-id="a356f-737">Disabling in this case would make it difficult for users to understand why the control is disabled.</span></span> <span data-ttu-id="a356f-738">使用者會被迫透過實驗和 deductive 邏輯來判斷問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-738">Users would be forced to determine the problem through experimentation and deductive logic.</span></span> <span data-ttu-id="a356f-739">最好是提供實用的錯誤訊息，以明確地說明問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-739">It's better just to provide a helpful error message to explain the problem explicitly.</span></span>
-   <span data-ttu-id="a356f-740">**秘訣：** 如果您不確定是否應該停用控制項或提供錯誤訊息，請從撰寫您可能提供的錯誤訊息開始。</span><span class="sxs-lookup"><span data-stu-id="a356f-740">**Tip:** If you aren't sure whether you should disable a control or give an error message, start by composing the error message that you might give.</span></span> <span data-ttu-id="a356f-741">如果錯誤訊息包含目標使用者無法快速推算的實用資訊，請讓控制項保持啟用並提供錯誤。</span><span class="sxs-lookup"><span data-stu-id="a356f-741">If the error message contains helpful information that target users aren't likely to quickly deduce, leave the control enabled and give the error.</span></span> <span data-ttu-id="a356f-742">否則，請停用控制項。</span><span class="sxs-lookup"><span data-stu-id="a356f-742">Otherwise, disable the control.</span></span>
-   <span data-ttu-id="a356f-743">**如果您停用控制項，也會停用所有相關聯的控制項**，例如其標籤、補充說明或命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-743">**If you disable a control, also disable all associated controls**, such as its label, supplemental explanations, or command buttons.</span></span> <span data-ttu-id="a356f-744">不過，請勿停用其 [群組方塊](ctrl-group-boxes.md)、群組標籤或群組說明（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a356f-744">However, don't disable its [group boxes](ctrl-group-boxes.md), group label, or group explanation if there are any.</span></span>

![<span data-ttu-id="a356f-745">具有暗灰色控制項之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-745">screen shot of dialog box with dimmed controls</span></span> ](images/win-dialog-box-image45.png)

<span data-ttu-id="a356f-746">在此範例中，已停用的文字方塊標籤也會停用，但其群組標籤和群組說明則否。</span><span class="sxs-lookup"><span data-stu-id="a356f-746">In this example, the disabled text box labels are also disabled, but their group label and group explanation are not.</span></span>

### <a name="required-input"></a><span data-ttu-id="a356f-747">必要輸入</span><span class="sxs-lookup"><span data-stu-id="a356f-747">Required input</span></span>

-   <span data-ttu-id="a356f-748">若要指出使用者必須在控制項中提供資訊，請考慮下列選項：</span><span class="sxs-lookup"><span data-stu-id="a356f-748">To indicate that users must provide information in a control, consider the following options:</span></span>
    -   <span data-ttu-id="a356f-749">**請勿指出任何問題，但會處理遺失的必要輸入，並顯示錯誤訊息。**</span><span class="sxs-lookup"><span data-stu-id="a356f-749">**Don't indicate anything, but handle missing required input with error messages.**</span></span> <span data-ttu-id="a356f-750">如果大部分的輸入都是選擇性的，或是使用者不太可能略過控制項，因而讓錯誤訊息的數目保持不變，這種方法會減少雜亂的情況。</span><span class="sxs-lookup"><span data-stu-id="a356f-750">This approach reduces clutter and works well if most input is optional or users aren't likely to skip controls, thus keeping the number of error messages low.</span></span>
    -   <span data-ttu-id="a356f-751">**使用標籤開頭的星號表示必要輸入。**</span><span class="sxs-lookup"><span data-stu-id="a356f-751">**Indicate required input using an asterisk at the beginning of the label.**</span></span> <span data-ttu-id="a356f-752">使用下列其中一項解說星號：</span><span class="sxs-lookup"><span data-stu-id="a356f-752">Explain the asterisk using either:</span></span>

        -   <span data-ttu-id="a356f-753">內容區域底部的註腳，指出 \* 必要的輸入。</span><span class="sxs-lookup"><span data-stu-id="a356f-753">A footnote at the bottom of the content area that says \* Required input.</span></span>
        -   <span data-ttu-id="a356f-754">星號上指出必要輸入的工具提示。</span><span class="sxs-lookup"><span data-stu-id="a356f-754">A tooltip on the asterisk that says Required input.</span></span>

        <span data-ttu-id="a356f-755">如果沒有許多必要的控制項，這種方法就很好用，但如果大部分的控制項都需要，則會很不良。</span><span class="sxs-lookup"><span data-stu-id="a356f-755">This approach works well if there aren't many required controls, but poorly if most controls are required.</span></span>

        ![<span data-ttu-id="a356f-756">包含星號之文字方塊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-756">screen shot of text box labels with asterisks</span></span> ](images/win-dialog-box-image46.png)

        <span data-ttu-id="a356f-757">在此範例中，星號會用來指出所需的輸入。</span><span class="sxs-lookup"><span data-stu-id="a356f-757">In this example, asterisks are used to indicate required input.</span></span>

    -   <span data-ttu-id="a356f-758">**如果所有控制項都需要輸入，請在內容區域頂端的適當位置，「需要所有輸入」狀態。**</span><span class="sxs-lookup"><span data-stu-id="a356f-758">**If all controls require input, state "All input required" at an appropriate place at the top of the content area.**</span></span> <span data-ttu-id="a356f-759">這種方法可減少此特定案例的雜亂情形。</span><span class="sxs-lookup"><span data-stu-id="a356f-759">This approach reduces clutter for this specific case.</span></span>
    -   <span data-ttu-id="a356f-760">**使用標籤之後的 " (選擇性) " 表示選擇性輸入。**</span><span class="sxs-lookup"><span data-stu-id="a356f-760">**Indicate optional inputs with "(optional)" after the label.**</span></span> <span data-ttu-id="a356f-761">如果需要大部分的輸入，這種方法就很好用，但不太可能。</span><span class="sxs-lookup"><span data-stu-id="a356f-761">This approach works well if most input is required, but poorly otherwise.</span></span>

-   <span data-ttu-id="a356f-762">**為求一致，請嘗試使用相同的方法來表示整個程式中所需的輸入。**</span><span class="sxs-lookup"><span data-stu-id="a356f-762">**For consistency, try to use the same method to indicate required input throughout your program.**</span></span> <span data-ttu-id="a356f-763">具體來說，請視需要指定必要或選擇性的輸入，但請避免在同一個程式中使用這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="a356f-763">Specifically, indicate either required or optional input as needed, but avoid using both within the same program.</span></span>

### <a name="error-handling"></a><span data-ttu-id="a356f-764">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="a356f-764">Error handling</span></span>

-   <span data-ttu-id="a356f-765">使用受限制為有效使用者輸入的控制項來防止錯誤。</span><span class="sxs-lookup"><span data-stu-id="a356f-765">Prevent errors by using controls that are constrained to valid user input.</span></span> <span data-ttu-id="a356f-766">您也可以藉由提供合理的預設值來協助減少錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="a356f-766">You can also help reduce the number of errors by providing reasonable default values.</span></span>
-   <span data-ttu-id="a356f-767">請儘快驗證使用者輸入，並盡可能將錯誤顯示為最接近輸入點。</span><span class="sxs-lookup"><span data-stu-id="a356f-767">Validate user input as soon as possible, and show errors as closely to the point of input as possible.</span></span>
-   <span data-ttu-id="a356f-768">**針對使用者輸入問題，使用非強制回應錯誤處理 (就地錯誤或氣球) 。**</span><span class="sxs-lookup"><span data-stu-id="a356f-768">**Use modeless error handling (in-place errors or balloons) for user input problems.**</span></span>
    -   <span data-ttu-id="a356f-769">**在文字方塊中或在文字方塊失去焦點之後，于文字方塊中偵測到非關鍵性、單一點使用者輸入問題時，請使用球標。**</span><span class="sxs-lookup"><span data-stu-id="a356f-769">**Use balloons for non-critical, single-point user input problems detected while in a text box or immediately after a text box loses focus.**</span></span> <span data-ttu-id="a356f-770">氣球不需要可用的螢幕空間或顯示就地訊息所需的動態配置。</span><span class="sxs-lookup"><span data-stu-id="a356f-770">Balloons don't require available screen space or the dynamic layout that is required to display in-place messages.</span></span> <span data-ttu-id="a356f-771">一次只顯示一個氣球。</span><span class="sxs-lookup"><span data-stu-id="a356f-771">Display only a single balloon at a time.</span></span> <span data-ttu-id="a356f-772">因為此問題並不重要，所以不需要任何錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="a356f-772">Because the problem isn't critical, no error icon is necessary.</span></span> <span data-ttu-id="a356f-773">當您按下、解決問題或在超時後，就會離開氣球。</span><span class="sxs-lookup"><span data-stu-id="a356f-773">Balloons go away when clicked, when the problem is resolved, or after a timeout.</span></span>

        ![<span data-ttu-id="a356f-774">「不正確的字元」訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-774">screen shot of 'incorrect character' message</span></span> ](images/win-dialog-box-image47.png)

        <span data-ttu-id="a356f-775">在此範例中，氣球表示輸入問題仍然存在於控制項中。</span><span class="sxs-lookup"><span data-stu-id="a356f-775">In this example, a balloon indicates an input problem while still in the control.</span></span>

-   <span data-ttu-id="a356f-776">**使用就地錯誤偵測延遲的錯誤偵測**，通常是按一下 [認可] 按鈕找到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a356f-776">**Use in-place errors for delayed error detection**, usually errors found by clicking a commit button.</span></span> <span data-ttu-id="a356f-777"> (不會在立即認可的設定中使用就地錯誤。 ) 一次可能會有多個就地錯誤。</span><span class="sxs-lookup"><span data-stu-id="a356f-777">(Don't use in-place errors for settings that are immediately committed.) There can be multiple in-place errors at a time.</span></span> <span data-ttu-id="a356f-778">使用一般文字和16x16 圖元錯誤圖示，盡可能將它們直接放在問題旁。</span><span class="sxs-lookup"><span data-stu-id="a356f-778">Use normal text and a 16x16 pixel error icon, placing them directly next to the problem whenever possible.</span></span> <span data-ttu-id="a356f-779">除非使用者認可，且找不到任何其他錯誤，否則就地錯誤不會消失。</span><span class="sxs-lookup"><span data-stu-id="a356f-779">In-place errors don't go away unless the user commits and no other errors are found.</span></span>

    ![<span data-ttu-id="a356f-780">有兩個錯誤訊息之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-780">screen shot of dialog box with two error messages</span></span> ](images/win-dialog-box-image48.png)

    <span data-ttu-id="a356f-781">在此範例中，按一下 [認可] 按鈕時，會使用就地錯誤來進行找到。</span><span class="sxs-lookup"><span data-stu-id="a356f-781">In this example, an in-place error is used for an error found by clicking the commit button.</span></span>

-   <span data-ttu-id="a356f-782">針對其他所有問題（包括牽涉到多個控制項的錯誤），以及按一下 [認可] 按鈕時所發現的非內容或非輸入錯誤 **，使用 (工作對話方塊或消息) 框的模式錯誤處理**。</span><span class="sxs-lookup"><span data-stu-id="a356f-782">**Use modal error handling (task dialogs or message boxes) for all other problems,** including errors that involve multiple controls, or are non-contextual or non-input errors found by clicking a commit button.</span></span>
-   <span data-ttu-id="a356f-783">**當發現並報告輸入問題時，請將輸入焦點設定為具有不正確資料的第一個控制項。**</span><span class="sxs-lookup"><span data-stu-id="a356f-783">**When an input problem is found and reported, set input focus to the first control with the incorrect data.**</span></span> <span data-ttu-id="a356f-784">必要時，將控制項滾動至 view。</span><span class="sxs-lookup"><span data-stu-id="a356f-784">Scroll the control into view if necessary.</span></span>

<span data-ttu-id="a356f-785">如需詳細資訊和範例，請參閱 [錯誤訊息](mess-error.md) 和 [批註](ctrl-balloons.md)提示。</span><span class="sxs-lookup"><span data-stu-id="a356f-785">For more information and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

### <a name="help"></a><span data-ttu-id="a356f-786">Help</span><span class="sxs-lookup"><span data-stu-id="a356f-786">Help</span></span>

-   <span data-ttu-id="a356f-787">提供使用者協助時，請考慮下列選項 (依照其喜好設定) 順序列出：</span><span class="sxs-lookup"><span data-stu-id="a356f-787">When providing user assistance, consider the following options (listed in their order of preference):</span></span>
    -   <span data-ttu-id="a356f-788">提供互動式控制項自理解標籤。</span><span class="sxs-lookup"><span data-stu-id="a356f-788">Give interactive controls self-explanatory labels.</span></span> <span data-ttu-id="a356f-789">使用者比較有可能讀取互動式控制項上的標籤，而不是任何其他文字。</span><span class="sxs-lookup"><span data-stu-id="a356f-789">Users are more likely to read the labels on interactive controls than any other text.</span></span>
    -   <span data-ttu-id="a356f-790">使用 [靜態文字標籤](text-ui.md)提供內容中的說明。</span><span class="sxs-lookup"><span data-stu-id="a356f-790">Provide in-context explanations using [static text labels](text-ui.md).</span></span>
    -   <span data-ttu-id="a356f-791">提供特定說明主題的特定說明連結。</span><span class="sxs-lookup"><span data-stu-id="a356f-791">Provide a specific Help link to a relevant Help topic.</span></span>
-   <span data-ttu-id="a356f-792">**在對話方塊的內容區域底部找出說明連結。**</span><span class="sxs-lookup"><span data-stu-id="a356f-792">**Locate Help links at the bottom of the content area of the dialog box.**</span></span> <span data-ttu-id="a356f-793">如果對話方塊有註腳，而且說明連結與其相關，請將 [說明] 連結放在註腳內。</span><span class="sxs-lookup"><span data-stu-id="a356f-793">If the dialog box has a footnote and the Help link is related to it, place the Help link within the footnote.</span></span>

    ![<span data-ttu-id="a356f-794">具有說明連結之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-794">screen shot of dialog box with help link</span></span> ](images/win-dialog-box-image40.png)

    <span data-ttu-id="a356f-795">在此範例中，[說明] 連結會套用至整個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-795">In this example, the Help link applies to the entire dialog.</span></span>

    -   <span data-ttu-id="a356f-796">**例外狀況：** 如果對話方塊有數個不同的設定群組，其中有個別的說明主題 (可能在群組方塊) 內，請找出群組底部的 [說明] 連結。</span><span class="sxs-lookup"><span data-stu-id="a356f-796">**Exception:** If a dialog box has several distinct groups of settings that have separate Help topics (perhaps within group boxes), locate the Help links at the bottom of the groups.</span></span>

-   <span data-ttu-id="a356f-797">**請勿使用一般或模糊的說明主題連結或一般説明按鈕。**</span><span class="sxs-lookup"><span data-stu-id="a356f-797">**Don't use general or vague Help topic links or generic Help buttons.**</span></span> <span data-ttu-id="a356f-798">使用者通常會忽略一般說明。</span><span class="sxs-lookup"><span data-stu-id="a356f-798">Users often ignore generic Help.</span></span>

<span data-ttu-id="a356f-799">如需詳細資訊和範例， [請參閱說明](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-799">For more information and examples, see [Help](winenv-help.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="a356f-800">預設值</span><span class="sxs-lookup"><span data-stu-id="a356f-800">Default values</span></span>

-   <span data-ttu-id="a356f-801">在每個對話方塊中包含預設的 [認可] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a356f-801">Include a default commit button on every dialog box.</span></span>
-   <span data-ttu-id="a356f-802">針對問題對話方塊：</span><span class="sxs-lookup"><span data-stu-id="a356f-802">For question dialogs:</span></span>
    -   <span data-ttu-id="a356f-803">**選取最安全的 (，以防止遺失資料或系統存取) ，最安全的回應是預設值。**</span><span class="sxs-lookup"><span data-stu-id="a356f-803">**Select the safest (to prevent loss of data or system access), most secure response to be the default.**</span></span> <span data-ttu-id="a356f-804">如果安全性和安全性不是因素，請選取最有可能或方便的回應。</span><span class="sxs-lookup"><span data-stu-id="a356f-804">If safety and security aren't factors, select the most likely or convenient response.</span></span>
        -   <span data-ttu-id="a356f-805">**例外狀況：** 除非有簡單、明顯的方法可復原命令，否則請勿將破壞性回應設為預設值。</span><span class="sxs-lookup"><span data-stu-id="a356f-805">**Exception:** Don't make a destructive response the default unless there is an easy, obvious way to undo the command.</span></span>
-   <span data-ttu-id="a356f-806">針對選擇對話方塊：</span><span class="sxs-lookup"><span data-stu-id="a356f-806">For choice dialogs:</span></span>
    -   <span data-ttu-id="a356f-807">針對初始預設值，請 **選取最安全的 (，以防止遺失資料或系統存取) 以及每個控制項最安全的值。**</span><span class="sxs-lookup"><span data-stu-id="a356f-807">For the initial default values, **select the safest (to prevent loss of data or system access) and most secure values for each control.**</span></span> <span data-ttu-id="a356f-808">如果安全性和安全性不是因素，請選取最有可能或方便的選項。</span><span class="sxs-lookup"><span data-stu-id="a356f-808">If safety and security aren't factors, select the most likely or convenient options.</span></span>
    -   <span data-ttu-id="a356f-809">針對後續的預設值，請重新 **選取先前選取的選項（如果這些值可能會重複），這樣做就是安全且安全的。**</span><span class="sxs-lookup"><span data-stu-id="a356f-809">For the subsequent default values, **reselect the previously selected options if those values are likely to be repeated, and doing so is safe and secure.**</span></span> <span data-ttu-id="a356f-810">否則，請選取初始預設值。</span><span class="sxs-lookup"><span data-stu-id="a356f-810">Otherwise, select the initial default values.</span></span>

![<span data-ttu-id="a356f-811">[列印] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-811">screen shot of print dialog box</span></span> ](images/win-dialog-box-image49.png)

<span data-ttu-id="a356f-812">在此範例中，使用者最有可能選擇與上次相同的列印設定。</span><span class="sxs-lookup"><span data-stu-id="a356f-812">In this example, users are most likely to choose the same printing settings as they did last time.</span></span> <span data-ttu-id="a356f-813">不過，所需的複本數目可能會變更，因此這項設定不會問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-813">However, the number of copies desired is likely to change, so this setting isn't reselected.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="a356f-814">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="a356f-814">Recommended sizing and spacing</span></span>

-   <span data-ttu-id="a356f-815">**支援 800 x 600 圖元的最小 Windows Vista 螢幕解析度。**</span><span class="sxs-lookup"><span data-stu-id="a356f-815">**Support the minimum Windows Vista screen resolution of 800 x 600 pixels.**</span></span> <span data-ttu-id="a356f-816">您可以使用 1024 x 768 圖元的螢幕解析度，針對可調整大小的視窗優化版面配置。</span><span class="sxs-lookup"><span data-stu-id="a356f-816">Layouts may be optimized for resizable windows using a screen resolution of 1024 x 768 pixels.</span></span>
-   <span data-ttu-id="a356f-817">**請盡可能使用可調整大小的視窗，以避免捲軸和截斷的資料。**</span><span class="sxs-lookup"><span data-stu-id="a356f-817">**Use resizable windows whenever practical to avoid scroll bars and truncated data.**</span></span> <span data-ttu-id="a356f-818">具有動態內容和清單的 windows，從可調整大小的視窗獲益最大。</span><span class="sxs-lookup"><span data-stu-id="a356f-818">Windows with dynamic content and lists benefit the most from resizable windows.</span></span>
-   <span data-ttu-id="a356f-819">**固定大小的 windows 必須是完全可見且大小調整，才能納入工作區域中。**</span><span class="sxs-lookup"><span data-stu-id="a356f-819">**Fixed-sized windows must be entirely visible and sized to fit within the work area.**</span></span>
-   <span data-ttu-id="a356f-820">**可調整大小的視窗可能已針對較高的解析度進行優化，但在顯示時視需要調整為實際螢幕解析度的大小。**</span><span class="sxs-lookup"><span data-stu-id="a356f-820">**Resizable windows may be optimized for higher resolutions, but sized down as needed at display time to the actual screen resolution.**</span></span>
-   <span data-ttu-id="a356f-821">**選擇適合其內容的預設視窗大小。**</span><span class="sxs-lookup"><span data-stu-id="a356f-821">**Choose a default window size appropriate for its contents.**</span></span> <span data-ttu-id="a356f-822">如果您可以有效地使用空間，請不要害怕使用較大的初始視窗大小。</span><span class="sxs-lookup"><span data-stu-id="a356f-822">Don't be afraid to use larger initial window sizes if you can use the space effectively.</span></span>

## <a name="text"></a><span data-ttu-id="a356f-823">Text</span><span class="sxs-lookup"><span data-stu-id="a356f-823">Text</span></span>

### <a name="general"></a><span data-ttu-id="a356f-824">一般</span><span class="sxs-lookup"><span data-stu-id="a356f-824">General</span></span>

-   <span data-ttu-id="a356f-825">**移除多餘的文字。**</span><span class="sxs-lookup"><span data-stu-id="a356f-825">**Remove redundant text.**</span></span> <span data-ttu-id="a356f-826">在標題、主要指示、補充指示、內容區域、命令連結和認可按鈕中尋找重複的文字。</span><span class="sxs-lookup"><span data-stu-id="a356f-826">Look for redundant text in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="a356f-827">一般而言，請在指示和互動式控制項中保留完整文字，然後從其他位置移除任何多餘的。</span><span class="sxs-lookup"><span data-stu-id="a356f-827">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="a356f-828">**使用正片語。**</span><span class="sxs-lookup"><span data-stu-id="a356f-828">**Use positive phrasing.**</span></span> <span data-ttu-id="a356f-829">對使用者來說，可以更輕鬆地理解正面片語。</span><span class="sxs-lookup"><span data-stu-id="a356f-829">Positive phrasing is easier for users to understand.</span></span>

<span data-ttu-id="a356f-830">**正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-830">**Correct:**</span></span>

<span data-ttu-id="a356f-831">要啟用檔案和印表機共用嗎？</span><span class="sxs-lookup"><span data-stu-id="a356f-831">Do you want to enable file and printer sharing?</span></span>

<span data-ttu-id="a356f-832">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="a356f-832">**Incorrect:**</span></span>

<span data-ttu-id="a356f-833">您要停用檔案和印表機共用嗎？</span><span class="sxs-lookup"><span data-stu-id="a356f-833">Do you want to disable file and printer sharing?</span></span>

<span data-ttu-id="a356f-834">不過，片語必須符合相關聯的命令，即使命令有負面片語;例如，使用 disable 來確認 Disable 命令。</span><span class="sxs-lookup"><span data-stu-id="a356f-834">However, phrasing must match the associated command, even if the command is negatively phrased; so, for example, use disable to confirm a Disable command.</span></span>

-   <span data-ttu-id="a356f-835">**如有必要，請使用 "window" 這個字來表示對話方塊本身。**</span><span class="sxs-lookup"><span data-stu-id="a356f-835">**If necessary, use the word "window" to refer to the dialog box itself.**</span></span>
-   <span data-ttu-id="a356f-836">**使用第二個人 ( 「您/您」的 ) ，告訴使用者要** 在主要指示和內容區域中執行的動作。</span><span class="sxs-lookup"><span data-stu-id="a356f-836">**Use the second person ("you/your") to tell users what to do** in the main instruction and content area.</span></span> <span data-ttu-id="a356f-837">通常會隱含第二個人。</span><span class="sxs-lookup"><span data-stu-id="a356f-837">Often the second person is implied.</span></span>

<span data-ttu-id="a356f-838">**範例：**</span><span class="sxs-lookup"><span data-stu-id="a356f-838">**Examples:**</span></span>

<span data-ttu-id="a356f-839">選擇您要列印的圖片</span><span class="sxs-lookup"><span data-stu-id="a356f-839">Choose the pictures you want to print</span></span>

<span data-ttu-id="a356f-840">選擇帳戶</span><span class="sxs-lookup"><span data-stu-id="a356f-840">Choose an account</span></span>

-   <span data-ttu-id="a356f-841">**使用第一個 person ( "I/me/my" ) 讓使用者告訴程式要** 在內容區域中回應主要指令的控制項。</span><span class="sxs-lookup"><span data-stu-id="a356f-841">**Use the first person ("I/me/my") to let users tell the program what to do** in controls in the content area that respond to the main instruction.</span></span>

<span data-ttu-id="a356f-842">**範例：** 列印相機上的相片。</span><span class="sxs-lookup"><span data-stu-id="a356f-842">**Example:** Print the photos on my camera.</span></span>

### <a name="dialog-box-titles"></a><span data-ttu-id="a356f-843">對話方塊標題</span><span class="sxs-lookup"><span data-stu-id="a356f-843">Dialog box titles</span></span>

-   <span data-ttu-id="a356f-844">**使用標題來識別對話方塊來源的命令、功能或程式。**</span><span class="sxs-lookup"><span data-stu-id="a356f-844">**Use the title to identify the command, feature, or program where a dialog box came from.**</span></span>
    -   <span data-ttu-id="a356f-845">如果對話方塊是使用者起始的，請使用命令或功能名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="a356f-845">If dialog is user initiated, identify it using the command or feature name.</span></span> <span data-ttu-id="a356f-846">**異常：**</span><span class="sxs-lookup"><span data-stu-id="a356f-846">**Exceptions:**</span></span>
        -   <span data-ttu-id="a356f-847">如果有許多不同的命令顯示對話方塊，請考慮改為使用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a356f-847">If a dialog box is displayed by many different commands, consider using the program name instead.</span></span>
        -   <span data-ttu-id="a356f-848">如果該標題在主要指示中是多餘的，請改為使用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a356f-848">If that title would be redundant with the main instruction, use the program name instead.</span></span>
    -   <span data-ttu-id="a356f-849">如果是程式或系統起始的 (，因此不在內容) 中，請使用程式或功能名稱提供內容來識別。</span><span class="sxs-lookup"><span data-stu-id="a356f-849">If it is program or system initiated (and therefore out of context), identify it using the program or feature name to give context.</span></span>
    -   <span data-ttu-id="a356f-850">請勿使用標題來說明在主要指令用途的對話方塊中要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="a356f-850">Don't use the title to explain what to do in the dialog that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="a356f-851">使用命令名稱的確切命令名稱，但如果有的話，請不要包含省略號。</span><span class="sxs-lookup"><span data-stu-id="a356f-851">Use the exact command name for command-based names, but don't include the ellipsis if there is one.</span></span> <span data-ttu-id="a356f-852">如有需要，您可以包含命令的功能表標題，以撰寫良好的標題。</span><span class="sxs-lookup"><span data-stu-id="a356f-852">You can include the command's menu title if necessary to compose a good title.</span></span> <span data-ttu-id="a356f-853">範例：物件 .。。命令在 [插入] 功能表中，使用標題插入物件。</span><span class="sxs-lookup"><span data-stu-id="a356f-853">Example: for an Object... command in an Insert menu, use the title Insert Object.</span></span>
-   <span data-ttu-id="a356f-854">**如果工作列上出現非強制回應對話方塊，請先將區分的資訊先放在工作列上，以優化工作列上顯示的標題** 。</span><span class="sxs-lookup"><span data-stu-id="a356f-854">**If a modeless dialog box appears on the taskbar, optimize the title for display on the taskbar** by concisely placing the distinguishing information first.</span></span> <span data-ttu-id="a356f-855">範例：「66% 完成」和「3個提醒」。</span><span class="sxs-lookup"><span data-stu-id="a356f-855">Examples: "66% Complete," and "3 Reminders."</span></span>
-   <span data-ttu-id="a356f-856">**請勿在標題中包含 "dialog" 或 "進度" 單字。**</span><span class="sxs-lookup"><span data-stu-id="a356f-856">**Don't include the words "dialog" or "progress" in the title.**</span></span> <span data-ttu-id="a356f-857">這是隱含的，而不是讓使用者能夠更輕鬆地進行掃描。</span><span class="sxs-lookup"><span data-stu-id="a356f-857">This is implied, and leaving it off makes it easier for users to scan.</span></span>
-   <span data-ttu-id="a356f-858">使用 [標題樣式的大小寫](glossary.md)，但不含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="a356f-858">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="a356f-859">主要指示</span><span class="sxs-lookup"><span data-stu-id="a356f-859">Main instructions</span></span>

-   <span data-ttu-id="a356f-860">**使用主要指令來清楚解說對話方塊中的動作。**</span><span class="sxs-lookup"><span data-stu-id="a356f-860">**Use the main instruction to explain concisely what to do in the dialog.**</span></span> <span data-ttu-id="a356f-861">指令應該是特定的語句、命令式方向或問題。</span><span class="sxs-lookup"><span data-stu-id="a356f-861">The instruction should be a specific statement, imperative direction, or question.</span></span> <span data-ttu-id="a356f-862">良好的指示會使用對話方塊來傳達使用者的目標，而不是單純專注于操作它的機制。</span><span class="sxs-lookup"><span data-stu-id="a356f-862">Good instructions communicate the user's objective with the dialog rather than focusing purely on the mechanics of manipulating it.</span></span>
-   <span data-ttu-id="a356f-863">**當您唯一可以說的是顯而易見的時候，請省略 main 指令。**</span><span class="sxs-lookup"><span data-stu-id="a356f-863">**Omit the main instruction when the only thing you can say is obvious.**</span></span> <span data-ttu-id="a356f-864">在這種情況下，對話方塊的內容很容易理解。</span><span class="sxs-lookup"><span data-stu-id="a356f-864">In such cases, the content of the dialog box is self-explanatory.</span></span> <span data-ttu-id="a356f-865">例如，[檔案開啟] 和 [檔案儲存] 通用對話方塊不需要主要指示，因為它們的內容和設計會讓它們的目的變得很明顯。</span><span class="sxs-lookup"><span data-stu-id="a356f-865">For example, the File Open and File Save common dialogs don't need a main instruction because their context and design make their purpose obvious.</span></span>
-   <span data-ttu-id="a356f-866">**省略重新聲明主要指令的控制項標籤。**</span><span class="sxs-lookup"><span data-stu-id="a356f-866">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="a356f-867">在此情況下，主要指令會採用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-867">In this case, the main instruction takes the access key.</span></span>

<span data-ttu-id="a356f-868">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="a356f-868">**Acceptable:**</span></span>

![<span data-ttu-id="a356f-869">具有重複標籤的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-869">screen shot of text box with redundant label</span></span> ](images/win-dialog-box-image50.png)

<span data-ttu-id="a356f-870">在此範例中，文字方塊標籤只是主要指令的重述。</span><span class="sxs-lookup"><span data-stu-id="a356f-870">In this example, the text box label is just a restatement of the main instruction.</span></span>

<span data-ttu-id="a356f-871">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="a356f-871">**Better:**</span></span>

![<span data-ttu-id="a356f-872">具有一個標籤之相同文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="a356f-872">screen shot of same text box with one label</span></span> ](images/win-dialog-box-image51.png)

<span data-ttu-id="a356f-873">在此範例中，會移除多餘的標籤，所以主要指令會取得存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-873">In this example, the redundant label is removed, so the main instruction takes the access key.</span></span>

-   <span data-ttu-id="a356f-874">**請務必只使用單一的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="a356f-874">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="a356f-875">削減主要指示以瞭解基本資訊。</span><span class="sxs-lookup"><span data-stu-id="a356f-875">Pare the main instruction down to the essential information.</span></span> <span data-ttu-id="a356f-876">如果您必須進一步說明，請使用補充指示。</span><span class="sxs-lookup"><span data-stu-id="a356f-876">If you must explain anything more, use supplemental instruction.</span></span>
-   <span data-ttu-id="a356f-877">**盡可能使用特定動詞。**</span><span class="sxs-lookup"><span data-stu-id="a356f-877">**Use specific verbs whenever possible.**</span></span> <span data-ttu-id="a356f-878">特定動詞 (範例： [連接]、[儲存]、[安裝) 比一般使用者更有意義， (範例：設定、管理、設定) 。</span><span class="sxs-lookup"><span data-stu-id="a356f-878">Specific verbs (examples: connect, save, install) are more meaningful to users than generic ones (examples: configure, manage, set).</span></span>
-   <span data-ttu-id="a356f-879">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-879">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="a356f-880">**如果指令是語句，則不包含最後句號。**</span><span class="sxs-lookup"><span data-stu-id="a356f-880">**Don't include final periods if the instruction is a statement.**</span></span> <span data-ttu-id="a356f-881">如果指令是問題，請包含最後一個問號。</span><span class="sxs-lookup"><span data-stu-id="a356f-881">If the instruction is a question, include a final question mark.</span></span>
-   <span data-ttu-id="a356f-882">在 **[進度] 對話方塊中，使用現在片語來簡短說明進行中的作業，** 並以省略號結尾。</span><span class="sxs-lookup"><span data-stu-id="a356f-882">**For progress dialogs, use a gerund phrase briefly explaining the operation in progress,** ending with an ellipsis.</span></span> <span data-ttu-id="a356f-883">範例：列印您的圖片 .。。</span><span class="sxs-lookup"><span data-stu-id="a356f-883">Example: Printing your pictures...</span></span>
-   <span data-ttu-id="a356f-884">**秘訣：** 您可以藉由想像您對朋友的看法來評估主要指示。</span><span class="sxs-lookup"><span data-stu-id="a356f-884">**Tip:** You can evaluate a main instruction by imagining what you would say to a friend.</span></span> <span data-ttu-id="a356f-885">如果回應主要指示的非自然、無用或麻煩，請重新修改指令。</span><span class="sxs-lookup"><span data-stu-id="a356f-885">If responding with the main instruction would be unnatural, unhelpful, or awkward, rework the instruction.</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="a356f-886">補充指示</span><span class="sxs-lookup"><span data-stu-id="a356f-886">Supplemental instructions</span></span>

-   <span data-ttu-id="a356f-887">**必要時，請使用選擇性的補充指示，以提供有助於瞭解或使用頁面的其他資訊。**</span><span class="sxs-lookup"><span data-stu-id="a356f-887">**When necessary, use an optional supplemental instruction to present additional information helpful to understanding or using the page.**</span></span> <span data-ttu-id="a356f-888">您可以提供更詳細的資訊並定義術語。</span><span class="sxs-lookup"><span data-stu-id="a356f-888">You can provide more detailed information and define terminology.</span></span>
-   <span data-ttu-id="a356f-889">**如果對話方塊的外觀是 [程式] 或 [系統起始 (]，因此不在內容) 中，請使用補充指示來說明對話方塊出現的原因。**</span><span class="sxs-lookup"><span data-stu-id="a356f-889">**If the appearance of the dialog box is program or system initiated (and therefore out of context), use the supplemental instruction to explain why the dialog has appeared.**</span></span> <span data-ttu-id="a356f-890">針對這類對話方塊，內容通常並不明顯。</span><span class="sxs-lookup"><span data-stu-id="a356f-890">For such dialogs, the context is usually not obvious.</span></span>
-   <span data-ttu-id="a356f-891">**請勿以稍微不同的用語重複主要指令。**</span><span class="sxs-lookup"><span data-stu-id="a356f-891">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="a356f-892">相反地，如果沒有其他要新增的指令，請省略補充指令。</span><span class="sxs-lookup"><span data-stu-id="a356f-892">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="a356f-893">使用完整句子、句子樣式的大小寫和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="a356f-893">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="command-links"></a><span data-ttu-id="a356f-894">命令連結</span><span class="sxs-lookup"><span data-stu-id="a356f-894">Command links</span></span>

-   <span data-ttu-id="a356f-895">**選擇清楚的連結文字，以明確地傳達和區分命令連結的用途。**</span><span class="sxs-lookup"><span data-stu-id="a356f-895">**Choose concise link text that clearly communicates and differentiates what the command link does.**</span></span> <span data-ttu-id="a356f-896">它應該是一目了然的，且對應至主要指令。</span><span class="sxs-lookup"><span data-stu-id="a356f-896">It should be self-explanatory and correspond to the main instruction.</span></span> <span data-ttu-id="a356f-897">使用者不應該需要找出連結真正的意義，或與其他連結有何不同。</span><span class="sxs-lookup"><span data-stu-id="a356f-897">Users shouldn't have to figure out what the link really means or how it differs from other links.</span></span>
-   <span data-ttu-id="a356f-898">**一律使用動詞命令來啟動命令連結。**</span><span class="sxs-lookup"><span data-stu-id="a356f-898">**Always start command links with a verb.**</span></span>
-   <span data-ttu-id="a356f-899">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="a356f-899">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="a356f-900">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="a356f-900">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="a356f-901">**如有必要，請使用完整的句子和結束標點符號來提供任何進一步的說明。**</span><span class="sxs-lookup"><span data-stu-id="a356f-901">**If necessary, provide any further explanation using complete sentences and ending punctuation.**</span></span> <span data-ttu-id="a356f-902">不過，只有在必要時才新增這類說明，因為一個命令連結需要一個命令連結的說明。</span><span class="sxs-lookup"><span data-stu-id="a356f-902">However, add such explanations only when needed don't add explanations to all command links just because one command link needs one.</span></span>

<span data-ttu-id="a356f-903">如需詳細資訊和範例，請參閱 [命令連結](ctrl-command-links.md) 指導方針。</span><span class="sxs-lookup"><span data-stu-id="a356f-903">For more information and examples, see [Command Link](ctrl-command-links.md) guidelines.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="a356f-904">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="a356f-904">Commit buttons</span></span>

-   <span data-ttu-id="a356f-905">**使用適當的特定認可按鈕標籤，並回應主要指令。**</span><span class="sxs-lookup"><span data-stu-id="a356f-905">**Use specific commit button labels that make sense on their own and are a response to the main instruction.**</span></span> <span data-ttu-id="a356f-906">在理想的情況下，使用者不需要讀取任何其他人來瞭解標籤。</span><span class="sxs-lookup"><span data-stu-id="a356f-906">Ideally users shouldn't have to read anything else to understand the label.</span></span> <span data-ttu-id="a356f-907">使用者比靜態文字更可能讀取命令按鈕標籤。</span><span class="sxs-lookup"><span data-stu-id="a356f-907">Users are far more likely to read command button labels than static text.</span></span>
-   <span data-ttu-id="a356f-908">**使用動詞啟動認可按鈕標籤。例外狀況是 [確定]、[是] 和 [否]。**</span><span class="sxs-lookup"><span data-stu-id="a356f-908">**Start commit button labels with a verb. Exceptions are OK, Yes, and No.**</span></span>
-   <span data-ttu-id="a356f-909">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="a356f-909">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="a356f-910">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="a356f-910">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="a356f-911">指派唯一的 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="a356f-911">Assign a unique [access key](glossary.md).</span></span>
    -   <span data-ttu-id="a356f-912">**例外狀況：** 請勿將存取金鑰指派給 [確定] 和 [取消] 按鈕，因為 Enter 和 Esc 是其存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-912">**Exception:** Don't assign access keys to OK and Cancel buttons because Enter and Esc are their access keys.</span></span> <span data-ttu-id="a356f-913">這麼做可讓您更輕鬆地指派其他存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a356f-913">Doing so makes the other access keys easier to assign.</span></span>

## <a name="documentation"></a><span data-ttu-id="a356f-914">文件</span><span class="sxs-lookup"><span data-stu-id="a356f-914">Documentation</span></span>

<span data-ttu-id="a356f-915">參考對話方塊時：</span><span class="sxs-lookup"><span data-stu-id="a356f-915">When referring to dialog boxes:</span></span>

-   <span data-ttu-id="a356f-916">在程式設計和其他技術檔中，請將對話方塊稱為對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-916">In programming and other technical documentation, refer to dialog boxes as dialog boxes.</span></span> <span data-ttu-id="a356f-917">在其他地方，依標題參考對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-917">Everywhere else, refer to dialog boxes by their title.</span></span> <span data-ttu-id="a356f-918">如果隱藏標題列，請使用 main 指令參考對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a356f-918">If the title bar is hidden, refer to the dialog using the main instruction.</span></span>
-   <span data-ttu-id="a356f-919">如果您必須在一般情況下參考對話方塊，請在使用者檔中使用 [視窗]。</span><span class="sxs-lookup"><span data-stu-id="a356f-919">If you must refer to a dialog box in general, use window in user documentation.</span></span> <span data-ttu-id="a356f-920">您可以參考簡單的問題對話方塊或確認為訊息。</span><span class="sxs-lookup"><span data-stu-id="a356f-920">You can refer to a simple question dialog or confirmation as a message.</span></span>
-   <span data-ttu-id="a356f-921">使用確切的標題或主要指令文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="a356f-921">Use the exact title or main instruction text, including its capitalization.</span></span>
-   <span data-ttu-id="a356f-922">可能的話，請使用粗體文字來格式化標題。</span><span class="sxs-lookup"><span data-stu-id="a356f-922">When possible, format the title using bold text.</span></span> <span data-ttu-id="a356f-923">否則，請只在必要時才將標題放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="a356f-923">Otherwise, put the title in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="a356f-924">範例：在 **Windows 安全性** 中，按一下 [ **更多選項**]。</span><span class="sxs-lookup"><span data-stu-id="a356f-924">Example: In **Windows Security**, click **More Options**.</span></span>

