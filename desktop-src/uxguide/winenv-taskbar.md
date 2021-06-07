---
title: 工作列
description: 工作列是顯示在桌面上的程式存取點。 透過新的 Windows 7 工作列功能，使用者可以直接從工作列提供命令、存取資源，以及查看程式狀態。
ms.assetid: c00e558a-313f-4741-a4b2-7d738f4544fa
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3e549e665f0200a448144ddf7202b258e88ff26
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443389"
---
# <a name="taskbar"></a><span data-ttu-id="5132c-104">工作列</span><span class="sxs-lookup"><span data-stu-id="5132c-104">Taskbar</span></span>

> [!NOTE]
> <span data-ttu-id="5132c-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="5132c-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="5132c-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="5132c-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="5132c-107">工作列是顯示在桌面上的程式存取點。</span><span class="sxs-lookup"><span data-stu-id="5132c-107">The taskbar is the access point for programs displayed on the desktop.</span></span> <span data-ttu-id="5132c-108">透過新的 Windows 7 工作列功能，使用者可以直接從工作列提供命令、存取資源，以及查看程式狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-108">With the new Windows 7 taskbar features, users can give commands, access resources, and view program status directly from the taskbar.</span></span>

<span data-ttu-id="5132c-109">工作列是顯示在桌面上的程式存取點，即使程式最小化也是如此。</span><span class="sxs-lookup"><span data-stu-id="5132c-109">The taskbar is the access point for programs displayed on the desktop, even if the program is minimized.</span></span> <span data-ttu-id="5132c-110">這類程式稱為有桌上型電腦存在。</span><span class="sxs-lookup"><span data-stu-id="5132c-110">Such programs are said to have desktop presence.</span></span> <span data-ttu-id="5132c-111">使用工作列時，使用者可以在桌面上查看開啟的主要視窗和特定的次要視窗，而且可以在兩者之間快速切換。</span><span class="sxs-lookup"><span data-stu-id="5132c-111">With the taskbar, users can view the open primary windows and certain secondary windows on the desktop, and can quickly switch between them.</span></span>

![<span data-ttu-id="5132c-112">工作列的螢幕擷取畫面，其中包含已叫用的功能</span><span class="sxs-lookup"><span data-stu-id="5132c-112">screen shot of taskbar with features called out</span></span> ](images/winenv-taskbar-image1.png)

<span data-ttu-id="5132c-113">Microsoft Windows 工作列。</span><span class="sxs-lookup"><span data-stu-id="5132c-113">The Microsoft Windows taskbar.</span></span>

<span data-ttu-id="5132c-114">工作列上的控制項稱為工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="5132c-114">The controls on the taskbar are referred to as taskbar buttons.</span></span> <span data-ttu-id="5132c-115">當程式建立主視窗 (或具有特定特性的次要視窗) 時，Windows 會為該視窗新增工作列按鈕，並在該視窗關閉時將其移除。</span><span class="sxs-lookup"><span data-stu-id="5132c-115">When a program creates a primary window (or a secondary window with certain characteristics), Windows adds a taskbar button for that window and removes it when that window closes.</span></span>

<span data-ttu-id="5132c-116">針對 Windows 7 設計的程式可以利用這些新的工作列按鈕功能：</span><span class="sxs-lookup"><span data-stu-id="5132c-116">Programs designed for Windows 7 can take advantage of these new taskbar button features:</span></span>

-   <span data-ttu-id="5132c-117">快速入門清單可讓您快速存取常用的目的地 (例如檔案、資料夾和連結) 和命令，可透過從程式的工作列按鈕存取的內容功能表，以及 [開始] 功能表專案，即使程式目前不在執行中也一樣。</span><span class="sxs-lookup"><span data-stu-id="5132c-117">Jump Lists provide quick access to frequently used destinations (like files, folders, and links) and commands through a context menu accessible from the program's taskbar button and Start menu item even if the program isn't currently running.</span></span>
-   <span data-ttu-id="5132c-118">縮圖工具列可讓您快速存取特定視窗常用的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-118">Thumbnail toolbars provide quick access to frequently used commands for a particular window.</span></span> <span data-ttu-id="5132c-119">縮圖工具列會顯示在工作列按鈕的縮圖中。</span><span class="sxs-lookup"><span data-stu-id="5132c-119">Thumbnail toolbars appear in the taskbar button's thumbnail.</span></span>
-   <span data-ttu-id="5132c-120">覆迭圖示會顯示程式的工作列按鈕圖示上的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="5132c-120">Overlay icons show change of status on the program's taskbar button icon.</span></span>
-   <span data-ttu-id="5132c-121">進度列會顯示程式的工作列按鈕上長時間執行之工作的進度。</span><span class="sxs-lookup"><span data-stu-id="5132c-121">Progress bars show progress for long-running tasks on the program's taskbar button.</span></span>
-   <span data-ttu-id="5132c-122">子視窗的工作列按鈕可讓使用者使用工作列按鈕縮圖，直接切換到視窗索引標籤、專案視窗、多重文件介面 (MDI) 子視窗和次要視窗。</span><span class="sxs-lookup"><span data-stu-id="5132c-122">Sub-window taskbar buttons allow users to use taskbar button thumbnails to switch directly to window tabs, project windows, multiple-document interface (MDI) child windows, and secondary windows.</span></span>
-   <span data-ttu-id="5132c-123">釘選的工作列按鈕可讓使用者將程式按鈕釘選到工作列，以提供程式的快速存取權，即使它們沒有執行也一樣。</span><span class="sxs-lookup"><span data-stu-id="5132c-123">Pinned taskbar buttons allow users to pin program buttons to the taskbar to provide quick access to programs even when they aren't running.</span></span>

<span data-ttu-id="5132c-124">技術上來說，工作列會將 [開始] 按鈕的整個橫條橫跨通知區域，不過，工作列較常見的只是指包含工作列按鈕的區域。</span><span class="sxs-lookup"><span data-stu-id="5132c-124">Technically, the taskbar spans the entire bar from the Start button to the notification area; more commonly, however, the taskbar refers only to the area containing the taskbar buttons.</span></span> <span data-ttu-id="5132c-125">針對多個監視設定，只有一個監視器具有工作列，而該監視是預設監視。</span><span class="sxs-lookup"><span data-stu-id="5132c-125">For multiple monitor configurations, only one monitor has a taskbar, and that monitor is the default monitor.</span></span>

<span data-ttu-id="5132c-126">**注意：** 與 [桌面](winenv-desktop.md)、 [通知區域](winenv-notification.md)和 [視窗管理](win-window-mgt.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="5132c-126">**Note:** Guidelines related to [desktop](winenv-desktop.md), [notification area](winenv-notification.md), and [window management](win-window-mgt.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="5132c-127">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="5132c-127">Is this the right user interface?</span></span>

<span data-ttu-id="5132c-128">針對 Windows 7 設計的程式可以利用這些工作列按鈕功能。</span><span class="sxs-lookup"><span data-stu-id="5132c-128">Programs designed for Windows 7 can take advantage of these taskbar button features.</span></span> <span data-ttu-id="5132c-129">請詢問自己下列重要問題，以判斷是否要使用它們：</span><span class="sxs-lookup"><span data-stu-id="5132c-129">Ask yourself the following key questions to determine whether or not to use them:</span></span>

<span data-ttu-id="5132c-130">**跳躍清單**</span><span class="sxs-lookup"><span data-stu-id="5132c-130">**Jump Lists**</span></span>

-   <span data-ttu-id="5132c-131">**使用者通常需要使用您的程式啟動新工作嗎？**</span><span class="sxs-lookup"><span data-stu-id="5132c-131">**Do users often need to start new tasks using your program?**</span></span> <span data-ttu-id="5132c-132">如果是的話，請考慮提供捷徑清單。</span><span class="sxs-lookup"><span data-stu-id="5132c-132">If so, consider providing a Jump List.</span></span> <span data-ttu-id="5132c-133">雖然跳躍清單可以用於其他用途，但大部分案例都牽涉到開始新的工作。</span><span class="sxs-lookup"><span data-stu-id="5132c-133">While Jump Lists can be used for other purposes, most scenarios involve starting a new task.</span></span>
-   <span data-ttu-id="5132c-134">**使用者通常需要存取最近或經常使用的檔案、資料夾、連結或其他資源？**</span><span class="sxs-lookup"><span data-stu-id="5132c-134">**Do users often need to access recently or frequently used files, folders, links, or other resources?**</span></span> <span data-ttu-id="5132c-135">如果是的話，請考慮提供捷徑清單來存取這些有用的資源。</span><span class="sxs-lookup"><span data-stu-id="5132c-135">If so, consider providing a Jump List to access these useful resources.</span></span>

    ![<span data-ttu-id="5132c-136">使用 internet explorer 跳躍清單的工作列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-136">screen shot of taskbar with internet explorer jump list</span></span> ](images/winenv-taskbar-image2.png)

    <span data-ttu-id="5132c-137">在此範例中，Windows Internet Explorer 會使用捷徑清單來呈現經常造訪的頁面。</span><span class="sxs-lookup"><span data-stu-id="5132c-137">In this example, Windows Internet Explorer uses a Jump List to present frequently visited pages.</span></span>

-   <span data-ttu-id="5132c-138">**當您使用其他程式時，即使您的程式未執行，使用者是否經常需要快速存取少量的程式命令？**</span><span class="sxs-lookup"><span data-stu-id="5132c-138">**Do users often need quick access to a small number of your program's commands while using other programs, even if your program isn't running?**</span></span> <span data-ttu-id="5132c-139">如果是的話，請考慮使用這些常用的命令來提供捷徑清單。</span><span class="sxs-lookup"><span data-stu-id="5132c-139">If so, consider providing a Jump List with these frequently used commands.</span></span> <span data-ttu-id="5132c-140">即使您的程式未執行，這些命令也必須正常運作，且必須套用至整個程式，而不是特定的視窗。</span><span class="sxs-lookup"><span data-stu-id="5132c-140">These commands must work even if your program isn't running, and must apply to the entire program, not a specific window.</span></span> <span data-ttu-id="5132c-141">或者，請考慮提供適用于特定視窗之命令的縮圖工具列。</span><span class="sxs-lookup"><span data-stu-id="5132c-141">As an alternative, consider providing a thumbnail toolbar for commands that apply to a specific window.</span></span>

    ![<span data-ttu-id="5132c-142">具有粘滯便箋跳躍清單的工作列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-142">screen shot of taskbar with sticky notes jump list</span></span> ](images/winenv-taskbar-image3.png)

    <span data-ttu-id="5132c-143">在此範例中，自黏便箋配件可讓使用者在使用其他程式時快速建立新的附注。</span><span class="sxs-lookup"><span data-stu-id="5132c-143">In this example, the Sticky Notes accessory allows users to create a new note quickly while using other programs.</span></span>

-   <span data-ttu-id="5132c-144">**您是否正在升級新的、單一用途或難以尋找的功能？**</span><span class="sxs-lookup"><span data-stu-id="5132c-144">**Are you promoting new, single use, or hard to find features?**</span></span> <span data-ttu-id="5132c-145">如果是，請勿使用跳躍清單，因為它們不是用於此用途。</span><span class="sxs-lookup"><span data-stu-id="5132c-145">If so, don't use Jump Lists because they aren't intended for this purpose.</span></span> <span data-ttu-id="5132c-146">請改為直接在程式中改善這類命令的可探索性。</span><span class="sxs-lookup"><span data-stu-id="5132c-146">Instead, improve the discoverability of such commands directly in the program.</span></span>

<span data-ttu-id="5132c-147">**縮圖工具列**</span><span class="sxs-lookup"><span data-stu-id="5132c-147">**Thumbnail toolbars**</span></span>

<span data-ttu-id="5132c-148">是否適用下列所有條件？</span><span class="sxs-lookup"><span data-stu-id="5132c-148">Do all of the following conditions apply?</span></span>

-   <span data-ttu-id="5132c-149">**命令是否適用于特定的視窗？**</span><span class="sxs-lookup"><span data-stu-id="5132c-149">**Do the commands apply to a specific window?**</span></span> <span data-ttu-id="5132c-150">縮圖工具列適用于適用于現有工作的命令，而捷徑清單命令則用於啟動新的工作。</span><span class="sxs-lookup"><span data-stu-id="5132c-150">Thumbnail toolbars are for commands that apply to existing tasks, whereas Jump List commands are for starting new tasks.</span></span>
-   <span data-ttu-id="5132c-151">**使用其他程式時，使用者是否需要快速與執行中的工作互動？**</span><span class="sxs-lookup"><span data-stu-id="5132c-151">**Do users need to interact with a running task quickly while using other programs?**</span></span> <span data-ttu-id="5132c-152">如果是，縮圖工具列是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="5132c-152">If so, thumbnail toolbars are a good choice.</span></span> <span data-ttu-id="5132c-153">縮圖工具列最多可顯示7個命令，但通常偏好最多五個命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-153">Thumbnail toolbars can present a maximum of seven commands, but a maximum of five commands is generally preferred.</span></span>
-   <span data-ttu-id="5132c-154">**命令是否立即進行？**</span><span class="sxs-lookup"><span data-stu-id="5132c-154">**Are the commands immediate?**</span></span> <span data-ttu-id="5132c-155">也就是說，他們不需要額外的輸入嗎？</span><span class="sxs-lookup"><span data-stu-id="5132c-155">That is, do they not require additional input?</span></span> <span data-ttu-id="5132c-156">縮圖工具列必須要有立即的命令才能有效率，而跳躍清單更適合需要額外輸入的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-156">Thumbnail toolbars need to have immediate commands to be efficient, whereas Jump Lists work better with commands that require additional input.</span></span>

    <span data-ttu-id="5132c-157">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-157">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-158">具有重迭視窗的工作列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-158">screen shot of taskbar with overlapping windows</span></span> ](images/winenv-taskbar-image4.png)

    <span data-ttu-id="5132c-159">需要額外輸入的命令不適用於縮圖工具列。</span><span class="sxs-lookup"><span data-stu-id="5132c-159">Commands that require additional input don't work well on thumbnail toolbars.</span></span>

-   <span data-ttu-id="5132c-160">**命令是否 direct？**</span><span class="sxs-lookup"><span data-stu-id="5132c-160">**Are the commands direct?**</span></span> <span data-ttu-id="5132c-161">也就是說，使用者只要按一下，就可以與他們互動嗎？</span><span class="sxs-lookup"><span data-stu-id="5132c-161">That is, can users interact with them using a single click?</span></span> <span data-ttu-id="5132c-162">工具列必須有直接命令才能有效率。</span><span class="sxs-lookup"><span data-stu-id="5132c-162">Toolbars need to have direct commands to be efficient.</span></span>
-   <span data-ttu-id="5132c-163">**命令是否適當地以圖示表示？**</span><span class="sxs-lookup"><span data-stu-id="5132c-163">**Are the commands well represented by icons?**</span></span> <span data-ttu-id="5132c-164">縮圖工具列命令會使用不是文字標籤的圖示來呈現，而捷徑清單的命令則會以文字標籤表示。</span><span class="sxs-lookup"><span data-stu-id="5132c-164">Thumbnail toolbar commands are presented using icons not text labels, whereas Jump List commands are represented by text labels.</span></span>

    <span data-ttu-id="5132c-165">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-165">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-166">具有圖示的縮圖命令螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-166">screen shot of thumbnail command with icon</span></span> ](images/winenv-taskbar-image5.png)

    <span data-ttu-id="5132c-167">在此範例中，命令未妥善地以圖示表示。</span><span class="sxs-lookup"><span data-stu-id="5132c-167">In this example, the command isn't well represented by icons.</span></span>

<span data-ttu-id="5132c-168">**重迭圖示**</span><span class="sxs-lookup"><span data-stu-id="5132c-168">**Overlay icons**</span></span>

-   <span data-ttu-id="5132c-169">**程式是否有「桌面存在」？**</span><span class="sxs-lookup"><span data-stu-id="5132c-169">**Does the program have "desktop presence"?**</span></span> <span data-ttu-id="5132c-170">如果沒有，請改用通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-170">If not, use a notification area icon instead.</span></span> <span data-ttu-id="5132c-171">若是如此，請考慮使用覆迭圖示，而不是在針對 Windows 7 設計之程式的通知區域圖標上放置狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-171">If so, consider using an overlay icon instead of putting status on the notification area icon for programs designed for Windows 7.</span></span> <span data-ttu-id="5132c-172">這麼做可確保在) 使用大型圖示時，圖示一律會顯示 (，並將該程式的狀態合併到一個位置。</span><span class="sxs-lookup"><span data-stu-id="5132c-172">Doing so ensures that the icon will always be visible (when large icons are used), and consolidates the program with its status in one place.</span></span>
-   <span data-ttu-id="5132c-173">**覆迭圖示是否會暫時顯示，以顯示狀態的變更？**</span><span class="sxs-lookup"><span data-stu-id="5132c-173">**Is the overlay icon displayed temporarily to show a change of status?**</span></span> <span data-ttu-id="5132c-174">如果是的話，視下列因素而定，重迭圖示可能會適當：</span><span class="sxs-lookup"><span data-stu-id="5132c-174">If so, an overlay icon may be appropriate, depending on the following factors:</span></span>
    -   <span data-ttu-id="5132c-175">**使用其他程式時，狀態是否有用且相關？**</span><span class="sxs-lookup"><span data-stu-id="5132c-175">**Is the status useful and relevant while using other programs?**</span></span> <span data-ttu-id="5132c-176">如果沒有，請在程式的 [ [狀態列](ctrl-status-bars.md) ] 或 [其他程式狀態] 區域中顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="5132c-176">If not, display the information in the program's [status bars](ctrl-status-bars.md) or other program status area.</span></span>

        ![<span data-ttu-id="5132c-177">internet explorer 視窗狀態列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-177">screen shot of internet explorer window status bar</span></span> ](images/winenv-taskbar-image7.png)

        <span data-ttu-id="5132c-178">在此範例中，會使用狀態列，因為在使用其他程式時，狀態不會很有用。</span><span class="sxs-lookup"><span data-stu-id="5132c-178">In this example, the status bar is used because the status isn't useful when using other programs.</span></span>

    -   <span data-ttu-id="5132c-179">**狀態是否顯示進度？**</span><span class="sxs-lookup"><span data-stu-id="5132c-179">**Is the status showing progress?**</span></span> <span data-ttu-id="5132c-180">若是如此，請改用工作列按鈕的進度列。</span><span class="sxs-lookup"><span data-stu-id="5132c-180">If so, use a taskbar button progress bar instead.</span></span>
    -   <span data-ttu-id="5132c-181">**狀態是否危急？是否需要立即採取動作？**</span><span class="sxs-lookup"><span data-stu-id="5132c-181">**Is the status critical? Is immediate action required?**</span></span> <span data-ttu-id="5132c-182">如果是的話，請以需要注意的方式來顯示資訊，而且無法輕易地忽略，例如 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="5132c-182">If so, display the information in a way that demands attention and cannot be easily ignored, such as a [dialog box](win-dialog-box.md).</span></span>

<span data-ttu-id="5132c-183">**進度列**</span><span class="sxs-lookup"><span data-stu-id="5132c-183">**Progress bars**</span></span>

-   <span data-ttu-id="5132c-184">**使用其他程式時，進度回饋是否有用且相關？**</span><span class="sxs-lookup"><span data-stu-id="5132c-184">**Is the progress feedback useful and relevant while using other programs?**</span></span> <span data-ttu-id="5132c-185">也就是說，使用者可能會在使用其他程式時監視進度，並變更其行為？</span><span class="sxs-lookup"><span data-stu-id="5132c-185">That is, are users likely to monitor the progress while using other programs, and change their behavior as a result?</span></span> <span data-ttu-id="5132c-186">這類有用且相關的狀態通常會使用無狀態的進度對話方塊或專用的進度頁面來顯示，但不會顯示在狀態列上的忙碌指標、活動指標或進度列。</span><span class="sxs-lookup"><span data-stu-id="5132c-186">Such useful and relevant status is usually displayed using a modeless progress dialog box or a dedicated progress page, but not with a busy pointer, activity indicator, or progress bar on a status bar.</span></span> <span data-ttu-id="5132c-187">如果在使用其他程式時狀態不實用，只要直接在程式中顯示進度意見反應。</span><span class="sxs-lookup"><span data-stu-id="5132c-187">If the status isn't useful when using other programs, just display the progress feedback directly in the program itself.</span></span>

    <span data-ttu-id="5132c-188">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-188">**Correct:**</span></span>

    ![<span data-ttu-id="5132c-189">具有進度列之 [複製] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-189">screen shot of copy dialog box with progress bar</span></span> ](images/winenv-taskbar-image8.png)

    <span data-ttu-id="5132c-190">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-190">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-191">工作列按鈕上進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-191">screen shot of progress bar on taskbar button</span></span> ](images/winenv-taskbar-image9.png)

    <span data-ttu-id="5132c-192">在不正確的範例中，工作列按鈕的進度列不太實用。</span><span class="sxs-lookup"><span data-stu-id="5132c-192">In the incorrect example, the taskbar button progress bar isn't very useful.</span></span>

-   <span data-ttu-id="5132c-193">**工作是否連續？**</span><span class="sxs-lookup"><span data-stu-id="5132c-193">**Is the task continuous?**</span></span> <span data-ttu-id="5132c-194">如果工作從未完成，就不需要顯示其進度。</span><span class="sxs-lookup"><span data-stu-id="5132c-194">If the task never completes, there's no need to show its progress.</span></span> <span data-ttu-id="5132c-195">連續工作的範例包括使用者不會起始的防毒軟體掃描，以及檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="5132c-195">Examples of continuous tasks include antivirus scans that aren't initiated by users, and file indexing.</span></span>

    <span data-ttu-id="5132c-196">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-196">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-197">連續工作的進度圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-197">screen shot of progress icon of a continuous task</span></span> ](images/winenv-taskbar-image10.png)

    <span data-ttu-id="5132c-198">在此範例中，連續工作不需要顯示進度。</span><span class="sxs-lookup"><span data-stu-id="5132c-198">In this example, a continuous task doesn't need to show progress.</span></span>

<span data-ttu-id="5132c-199">**子視窗工作列**</span><span class="sxs-lookup"><span data-stu-id="5132c-199">**Sub-window taskbars**</span></span>

-   <span data-ttu-id="5132c-200">**您的程式是否包含使用者通常想要直接切換的索引標籤、專案視窗、MDI 子視窗或次要視窗？**</span><span class="sxs-lookup"><span data-stu-id="5132c-200">**Does your program contain tabs, project windows, MDI child windows, or secondary windows that users would often want to switch to directly?**</span></span> <span data-ttu-id="5132c-201">如果是這樣，則可以適當地提供這些 windows 的工作列按鈕縮圖。</span><span class="sxs-lookup"><span data-stu-id="5132c-201">If so, giving these windows their own taskbar button thumbnails may be appropriate.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="5132c-202">設計概念</span><span class="sxs-lookup"><span data-stu-id="5132c-202">Design concepts</span></span>

### <a name="using-jump-lists-and-thumbnail-toolbars-effectively"></a><span data-ttu-id="5132c-203">有效使用跳躍清單和縮圖工具列</span><span class="sxs-lookup"><span data-stu-id="5132c-203">Using Jump Lists and thumbnail toolbars effectively</span></span>

<span data-ttu-id="5132c-204">跳躍清單和縮圖工具列可協助使用者更有效率地存取資源和執行命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-204">Jump Lists and thumbnail toolbars help users access resources and perform commands more efficiently.</span></span> <span data-ttu-id="5132c-205">不過，在設計您的程式如何支援這些功能時，並不會提高授與的效率。</span><span class="sxs-lookup"><span data-stu-id="5132c-205">However, when designing how your program supports these features, don't take improved efficiency for granted.</span></span> <span data-ttu-id="5132c-206">如果使用者無法準確預測哪些功能具有所需的命令，或他們必須檢查多個位置，則最終使用者將會感到挫折並停止使用這些功能。</span><span class="sxs-lookup"><span data-stu-id="5132c-206">If users can't accurately predict which feature has the command they need, or they have to check multiple places, eventually users will become frustrated and stop using these features.</span></span>

<span data-ttu-id="5132c-207">當快捷方式清單和縮圖工具列是：</span><span class="sxs-lookup"><span data-stu-id="5132c-207">Jump Lists and thumbnail toolbars work together most effectively when they are:</span></span>

-   <span data-ttu-id="5132c-208">**清楚區別。**</span><span class="sxs-lookup"><span data-stu-id="5132c-208">**Clearly differentiated.**</span></span> <span data-ttu-id="5132c-209">使用者知道何時要尋找捷徑清單中的目的地或命令，以及何時查看縮圖工具列。</span><span class="sxs-lookup"><span data-stu-id="5132c-209">Users know when to look for a destination or command in a Jump List, and when to look in a thumbnail toolbar.</span></span> <span data-ttu-id="5132c-210">每個都有明確的用途，因此使用者很少會混淆兩者的內容。</span><span class="sxs-lookup"><span data-stu-id="5132c-210">There is a clear purpose for each, so users rarely confuse the contents of the two.</span></span> <span data-ttu-id="5132c-211">一般而言，會使用跳躍清單來啟動新的工作，而縮圖工具列會在使用其他程式時用來與執行中的工作進行互動。</span><span class="sxs-lookup"><span data-stu-id="5132c-211">Generally, Jump Lists are used to start new tasks, whereas thumbnail toolbars are used to interact with running tasks while using other programs.</span></span>
-   <span data-ttu-id="5132c-212">**有用。**</span><span class="sxs-lookup"><span data-stu-id="5132c-212">**Useful.**</span></span> <span data-ttu-id="5132c-213">提供的目的地和命令是使用者所需的。</span><span class="sxs-lookup"><span data-stu-id="5132c-213">The destinations and commands offered are the ones that users need.</span></span> <span data-ttu-id="5132c-214">如果使用者不太可能需要任何東西，就不會包含它。</span><span class="sxs-lookup"><span data-stu-id="5132c-214">If users aren't likely to need something, it isn't included.</span></span> <span data-ttu-id="5132c-215">如果不需要，請不要使用專案數目上限。</span><span class="sxs-lookup"><span data-stu-id="5132c-215">Don't use the maximum number of items if they aren't needed.</span></span>
-   <span data-ttu-id="5132c-216">**預測。**</span><span class="sxs-lookup"><span data-stu-id="5132c-216">**Predictable.**</span></span> <span data-ttu-id="5132c-217">提供的目的地和命令是使用者預期要尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="5132c-217">The destinations and commands offered are the ones that users expect to find.</span></span> <span data-ttu-id="5132c-218">使用者很少需要查看一個以上的位置。</span><span class="sxs-lookup"><span data-stu-id="5132c-218">Users rarely have to look in more than one place.</span></span>
-   <span data-ttu-id="5132c-219">**妥善整理。**</span><span class="sxs-lookup"><span data-stu-id="5132c-219">**Well organized.**</span></span> <span data-ttu-id="5132c-220">使用者可以找到他們想要快速尋找的內容。</span><span class="sxs-lookup"><span data-stu-id="5132c-220">Users are able to find what they are looking for quickly.</span></span> <span data-ttu-id="5132c-221">它們使用描述性但簡潔的標籤，以及適合辨識的適當圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-221">They use descriptive yet concise labels, and suitable icons to aid recognition.</span></span>

<span data-ttu-id="5132c-222">請務必進行使用者研究，以確定您有正確的許可權。</span><span class="sxs-lookup"><span data-stu-id="5132c-222">Be sure to do user research to make sure you've got it right.</span></span> <span data-ttu-id="5132c-223">如果您最後發現您無法設計可達成這些目標的跳躍清單和縮圖工具列，請考慮只提供其中一項。</span><span class="sxs-lookup"><span data-stu-id="5132c-223">If you ultimately find that you can't design Jump Lists and thumbnail toolbars together that achieve these goals, consider providing only one of them.</span></span> <span data-ttu-id="5132c-224">最好要有一個可預測的方式來提供命令，而不是兩個混淆的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-224">It's better to have one predictable way to give commands than two confusing ones.</span></span>

## <a name="guidelines"></a><span data-ttu-id="5132c-225">指導方針</span><span class="sxs-lookup"><span data-stu-id="5132c-225">Guidelines</span></span>

### <a name="taskbar-buttons"></a><span data-ttu-id="5132c-226">工作列按鈕</span><span class="sxs-lookup"><span data-stu-id="5132c-226">Taskbar buttons</span></span>

-   <span data-ttu-id="5132c-227">**使用工作列按鈕縮圖) ，讓下列視窗類型出現在 Windows 7 的工作列 (：**</span><span class="sxs-lookup"><span data-stu-id="5132c-227">**Make the following window types appear on the taskbar (for Windows 7, by using a taskbar button thumbnail):**</span></span>
    -   <span data-ttu-id="5132c-228">包含沒有擁有者之對話方塊的主要 windows () </span><span class="sxs-lookup"><span data-stu-id="5132c-228">Primary windows (which includes dialog boxes without owners)</span></span>
    -   <span data-ttu-id="5132c-229">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="5132c-229">Property sheets</span></span>
    -   <span data-ttu-id="5132c-230">非模式進度對話方塊</span><span class="sxs-lookup"><span data-stu-id="5132c-230">Modeless progress dialog boxes</span></span>
    -   <span data-ttu-id="5132c-231">精靈</span><span class="sxs-lookup"><span data-stu-id="5132c-231">Wizards</span></span>
-   <span data-ttu-id="5132c-232">**若為 Windows 7，請使用工作列按鈕縮圖，將下列視窗類型與啟動的主視窗工作列按鈕分組。**</span><span class="sxs-lookup"><span data-stu-id="5132c-232">**For Windows 7, use taskbar button thumbnails to group the following window types with the primary window taskbar button it was launched from.**</span></span> <span data-ttu-id="5132c-233">每個程式都 (具體來說，每個程式都可以被視為個別的程式) 應該有一個工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="5132c-233">Each program (specifically, each program perceived as a separate program) should have a single taskbar button.</span></span>

    -   <span data-ttu-id="5132c-234">次要視窗</span><span class="sxs-lookup"><span data-stu-id="5132c-234">Secondary windows</span></span>
    -   <span data-ttu-id="5132c-235">工作區索引標籤</span><span class="sxs-lookup"><span data-stu-id="5132c-235">Workspace tabs</span></span>
    -   <span data-ttu-id="5132c-236">Project 視窗</span><span class="sxs-lookup"><span data-stu-id="5132c-236">Project windows</span></span>
    -   <span data-ttu-id="5132c-237">MDI 子視窗</span><span class="sxs-lookup"><span data-stu-id="5132c-237">MDI child windows</span></span>

    <span data-ttu-id="5132c-238">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-238">**Correct:**</span></span>

    ![<span data-ttu-id="5132c-239">windows explorer 和進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-239">screen shot of windows explorer and progress bar</span></span> ](images/winenv-taskbar-image11.png)

    <span data-ttu-id="5132c-240">在此範例中，次要視窗會以其主視窗的工作列按鈕分組。</span><span class="sxs-lookup"><span data-stu-id="5132c-240">In this example, a secondary window is grouped with its primary window's taskbar button.</span></span>

    <span data-ttu-id="5132c-241">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-241">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-242">windows explorer 和控制台的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-242">screen shot of windows explorer and control panel</span></span> ](images/winenv-taskbar-image12.png)

    <span data-ttu-id="5132c-243">在此範例中，主控台的群組 Windows 檔案總管不正確。</span><span class="sxs-lookup"><span data-stu-id="5132c-243">In this example, Control Panel is incorrectly grouped with Windows Explorer.</span></span> <span data-ttu-id="5132c-244">使用者將這些視為個別的程式。</span><span class="sxs-lookup"><span data-stu-id="5132c-244">Users perceive these as separate programs.</span></span>

    <span data-ttu-id="5132c-245">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-245">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-246">程式、進度列和工作列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-246">screen shot of program, progress bar, and a taskbar</span></span> ](images/winenv-taskbar-image13.png)

    <span data-ttu-id="5132c-247">在此範例中，Windows 備份錯誤地針對單一程式使用兩個工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="5132c-247">In this example, Windows Backup incorrectly uses two taskbar buttons for a single program.</span></span>

-   <span data-ttu-id="5132c-248">**還原主視窗也應還原其所有的次要視窗，** 即使這些次要視窗有自己的工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="5132c-248">**Restoring a primary window should also restore all its secondary windows,** even if those secondary windows have their own taskbar buttons.</span></span> <span data-ttu-id="5132c-249">還原時，請將次要視窗放在主視窗的最上層。</span><span class="sxs-lookup"><span data-stu-id="5132c-249">When restoring, place secondary windows on top of the primary window.</span></span>
-   <span data-ttu-id="5132c-250">**若是 Windows 7，通常有桌上型電腦的程式可能會暫時顯示工作列按鈕來顯示狀態。**</span><span class="sxs-lookup"><span data-stu-id="5132c-250">**For Windows 7, programs that normally have desktop presence may temporarily display a taskbar button to show status.**</span></span> <span data-ttu-id="5132c-251">只有當您的程式通常會顯示在桌面上，而且使用者經常與其互動時，才需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="5132c-251">Do so only if your program is normally displayed on the desktop and users frequently interact with it.</span></span> <span data-ttu-id="5132c-252">通常在沒有桌上型電腦的情況下執行的程式應該改為使用其通知區域圖示，即使它可能不會一直顯示也一樣。</span><span class="sxs-lookup"><span data-stu-id="5132c-252">A program that normally runs without desktop presence should use its notification area icon instead, even though it might not always be visible.</span></span>

    <span data-ttu-id="5132c-253">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-253">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-254">windows 同步中心工作列按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-254">screen shot of windows sync center taskbar button</span></span> ](images/winenv-taskbar-image14.png)

    <span data-ttu-id="5132c-255">在此範例中，Windows 同步中心不正確地使用暫存工作列按鈕來顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-255">In this example, Windows Sync Center incorrectly uses a temporary taskbar button to display status.</span></span> <span data-ttu-id="5132c-256">它應該改用其通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-256">It should use its notification area icon instead.</span></span>

### <a name="icons"></a><span data-ttu-id="5132c-257">圖示</span><span class="sxs-lookup"><span data-stu-id="5132c-257">Icons</span></span>

-   <span data-ttu-id="5132c-258">**將您的程式圖示設計成在工作列上看起來很棒。**</span><span class="sxs-lookup"><span data-stu-id="5132c-258">**Design your program icon to look great on the taskbar.**</span></span> <span data-ttu-id="5132c-259">確定它有意義，並反映其功能和您的品牌。</span><span class="sxs-lookup"><span data-stu-id="5132c-259">Ensure it is meaningful, and reflects its function and your brand.</span></span> <span data-ttu-id="5132c-260">使其成為相異的，使其成為特殊的，並確保其在所有圖示大小中都能妥善呈現。</span><span class="sxs-lookup"><span data-stu-id="5132c-260">Make it distinct, make it special, and ensure it renders well in all icon sizes.</span></span> <span data-ttu-id="5132c-261">花時間取得正確的時間。</span><span class="sxs-lookup"><span data-stu-id="5132c-261">Spend the time necessary to get it right.</span></span> <span data-ttu-id="5132c-262">遵循 [Aero 樣式的圖示指導方針](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="5132c-262">Follow the [Aero-style icon guidelines](vis-icons.md).</span></span>
-   <span data-ttu-id="5132c-263">**如果您的程式使用重迭圖示，請設計您的程式基底圖示來妥善處理重迭。**</span><span class="sxs-lookup"><span data-stu-id="5132c-263">**If your program uses overlay icons, design your program's base icon to handle overlays well.**</span></span> <span data-ttu-id="5132c-264">重迭圖示會顯示在右下角，因此請設計圖示，讓該區域可以遮蔽。</span><span class="sxs-lookup"><span data-stu-id="5132c-264">Overlay icons are displayed in the lower right corner, so design the icon so that area can be obscured.</span></span>

    ![<span data-ttu-id="5132c-265">圖示和右下角重迭的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-265">screen shot of icons and with lower-right overlay</span></span> ](images/winenv-taskbar-image15.png)

    <span data-ttu-id="5132c-266">在此範例中，程式的工作列按鈕圖示在右下方區域中沒有重要的資訊。</span><span class="sxs-lookup"><span data-stu-id="5132c-266">In this example, the program's taskbar button icon doesn't have important information in the lower right area.</span></span>

-   <span data-ttu-id="5132c-267">**請勿在程式的基底圖示中使用** 覆迭，不論您的程式是否使用重迭圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-267">**Don't use overlays in your program's base icon,** whether your program uses overlay icons or not.</span></span> <span data-ttu-id="5132c-268">在基底圖示中使用覆迭將會造成混淆，因為使用者必須找出它沒有通訊的狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-268">Using an overlay in the base icon will be confusing because users will have to figure out that it's not communicating status.</span></span>

    <span data-ttu-id="5132c-269">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-269">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-270">具有重迭基底圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-270">screen shot of base icon with overlay</span></span> ](images/winenv-taskbar-image16.png)

    <span data-ttu-id="5132c-271">在此範例中，程式的基底圖示看起來像是顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-271">In this example, the program's base icon looks like it is showing status.</span></span>

<span data-ttu-id="5132c-272">如需一般圖示指導方針和範例，請參閱 [圖示](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="5132c-272">For general icon guidelines and examples, see [Icons](vis-icons.md).</span></span>

### <a name="overlay-icons"></a><span data-ttu-id="5132c-273">重迭圖示</span><span class="sxs-lookup"><span data-stu-id="5132c-273">Overlay icons</span></span>

-   <span data-ttu-id="5132c-274">**使用重迭圖示來指出僅有用且相關的狀態。**</span><span class="sxs-lookup"><span data-stu-id="5132c-274">**Use overlay icons to indicate useful and relevant status only.**</span></span> <span data-ttu-id="5132c-275">請考慮將重迭圖示顯示為使用者的工作可能會中斷，因此狀態變更必須足以應付可能的中斷。</span><span class="sxs-lookup"><span data-stu-id="5132c-275">Consider the display of an overlay icon to be a potential interruption of the user's work, so the status change must be important enough to merit a potential interruption.</span></span>

    <span data-ttu-id="5132c-276">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-276">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-277">三個重迭圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-277">screen shot of three overlay icons</span></span> ](images/winenv-taskbar-image17.png)

    <span data-ttu-id="5132c-278">在這些範例中，覆迭圖示的重要性不足以應付可能的中斷。</span><span class="sxs-lookup"><span data-stu-id="5132c-278">In these examples, the overlay icon isn't important enough to merit a potential interruption.</span></span>

-   <span data-ttu-id="5132c-279">**使用重迭圖示來暫存狀態。**</span><span class="sxs-lookup"><span data-stu-id="5132c-279">**Use overlay icons for temporary status.**</span></span> <span data-ttu-id="5132c-280">如果不斷顯示，重迭圖示會遺失其值，因此一般程式狀態不應顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-280">The overlay icons lose their value if displayed constantly, so normal program status should not show an icon.</span></span> <span data-ttu-id="5132c-281">當圖示為時，請移除覆迭圖示：</span><span class="sxs-lookup"><span data-stu-id="5132c-281">Remove the overlay icon when the icon:</span></span>

    -   <span data-ttu-id="5132c-282">**是否有問題：** 解決問題後，請移除圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-282">**Is for a problem:** Remove the icon once the problem has been resolved.</span></span>
    -   <span data-ttu-id="5132c-283">**警示：有一些新功能：** 當使用者啟用程式之後，請移除圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-283">**Alerts that something is new:** Remove the icon once the user has activated the program.</span></span>

    <span data-ttu-id="5132c-284">**例外狀況：** 如果使用者一律需要知道其狀態，您的程式可能會經常顯示重迭圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-284">**Exception:** Your program can constantly display an overlay icon if users always need to know its status.</span></span>

    ![<span data-ttu-id="5132c-285">具有重迭圖示的 live messenger 螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-285">screen shot of live messenger with overlay icon</span></span> ](images/winenv-taskbar-image18.png)

    <span data-ttu-id="5132c-286">在此範例中，Windows Live Messenger 一律會顯示重迭圖示，讓使用者一律可以檢查其回報的狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-286">In this example, Windows Live Messenger always displays an overlay icon so that users can always check their reported presence.</span></span>

-   <span data-ttu-id="5132c-287">**請勿顯示圖示來指出問題已獲得解決。**</span><span class="sxs-lookup"><span data-stu-id="5132c-287">**Don't display an icon to indicate that a problem has been solved.**</span></span> <span data-ttu-id="5132c-288">相反地，只要移除任何先前表示有問題的圖示即可。</span><span class="sxs-lookup"><span data-stu-id="5132c-288">Instead, simply remove any previous icon indicating a problem.</span></span> <span data-ttu-id="5132c-289">假設使用者通常會預期您的程式會在沒有問題的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="5132c-289">Assume that users normally expect your program to run without problems.</span></span>
-   <span data-ttu-id="5132c-290">**顯示重迭圖示或通知區域圖示，但不能同時顯示兩者。**</span><span class="sxs-lookup"><span data-stu-id="5132c-290">**Display either overlay icons or notification area icons, but never both.**</span></span> <span data-ttu-id="5132c-291">您的程式可能會支援這兩種機制來提供回溯相容性，但如果您的程式使用重迭圖示來顯示狀態，則它也不應該使用通知區域圖示來取得狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-291">Your program may support both mechanisms for backward compatibility, but if your program displays status using overlay icons, it shouldn't also use notification area icons for status.</span></span>

    <span data-ttu-id="5132c-292">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-292">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-293">顯示圖示兩次的工作列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-293">screen shot of taskbar with icon displayed twice</span></span> ](images/winenv-taskbar-image19.png)

    <span data-ttu-id="5132c-294">在此範例中，新的郵件圖示會重複顯示。</span><span class="sxs-lookup"><span data-stu-id="5132c-294">In this example, the new mail icon is displayed redundantly.</span></span>

-   <span data-ttu-id="5132c-295">**請勿快閃工作列按鈕，以吸引狀態變更。**</span><span class="sxs-lookup"><span data-stu-id="5132c-295">**Don't flash the taskbar button to draw attention to a status change.**</span></span> <span data-ttu-id="5132c-296">這麼做會造成太雜亂的情況。</span><span class="sxs-lookup"><span data-stu-id="5132c-296">Doing so would be too distracting.</span></span> <span data-ttu-id="5132c-297">讓使用者自行探索重迭圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-297">Let users discover overlay icons on their own.</span></span>
-   <span data-ttu-id="5132c-298">**偏好使用標準重迭圖示來指出狀態或狀態變更。**</span><span class="sxs-lookup"><span data-stu-id="5132c-298">**Prefer standard overlay icons to indicate status or status changes.**</span></span> <span data-ttu-id="5132c-299">使用這些標準重迭圖示：</span><span class="sxs-lookup"><span data-stu-id="5132c-299">Use these standard overlay icons:</span></span> 

    | <span data-ttu-id="5132c-300">重疊</span><span class="sxs-lookup"><span data-stu-id="5132c-300">Overlay</span></span> | <span data-ttu-id="5132c-301">狀態</span><span class="sxs-lookup"><span data-stu-id="5132c-301">Status</span></span> |
    |---------------------------------------------------------------------------------------------------|----------------------------------|
    | ![<span data-ttu-id="5132c-302">小型警告圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-302">screen shot of small warning icon</span></span> ](images/winenv-taskbar-image20.png)<br/>               | <span data-ttu-id="5132c-303">警告</span><span class="sxs-lookup"><span data-stu-id="5132c-303">Warning</span></span><br/>               |
    | ![<span data-ttu-id="5132c-304">小錯誤圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-304">screen shot of small error icon</span></span> ](images/winenv-taskbar-image21.png)<br/>                 | <span data-ttu-id="5132c-305">錯誤</span><span class="sxs-lookup"><span data-stu-id="5132c-305">Error</span></span><br/>                 |
    | ![<span data-ttu-id="5132c-306">小型停用/中斷連線圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-306">screen shot of small disabled/disconnected icon</span></span> ](images/winenv-taskbar-image22.png)<br/> | <span data-ttu-id="5132c-307">已停用/已中斷連線</span><span class="sxs-lookup"><span data-stu-id="5132c-307">Disabled/Disconnected</span></span><br/> |
    | ![<span data-ttu-id="5132c-308">小型封鎖/離線圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-308">screen shot of small blocked/offline icon</span></span> ](images/winenv-taskbar-image23.png)<br/>       | <span data-ttu-id="5132c-309">封鎖/離線</span><span class="sxs-lookup"><span data-stu-id="5132c-309">Blocked/Offline</span></span><br/>       |

    

     

-   <span data-ttu-id="5132c-310">**針對自訂覆迭圖示，選擇容易辨識的設計。**</span><span class="sxs-lookup"><span data-stu-id="5132c-310">**For custom overlay icons, choose an easily recognizable design.**</span></span> <span data-ttu-id="5132c-311">使用高品質的16x16 圖元、完整色彩圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-311">Use high-quality 16x16 pixel, full color icons.</span></span> <span data-ttu-id="5132c-312">偏好在正方形或矩形形狀圖示上具有特殊輪廓的圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-312">Prefer icons with distinctive outlines over square or rectangular shaped icons.</span></span> <span data-ttu-id="5132c-313">也套用其他 [Aero 樣式的圖示指導方針](vis-icons.md) 。</span><span class="sxs-lookup"><span data-stu-id="5132c-313">Apply the other [Aero-style icon guidelines](vis-icons.md) as well.</span></span>
-   <span data-ttu-id="5132c-314">**讓自訂覆迭圖示的設計更簡單。**</span><span class="sxs-lookup"><span data-stu-id="5132c-314">**Keep the design of custom overlay icons simple.**</span></span> <span data-ttu-id="5132c-315">請勿嘗試傳達複雜、不熟悉或抽象的想法。</span><span class="sxs-lookup"><span data-stu-id="5132c-315">Don't try to communicate complex, unfamiliar, or abstract ideas.</span></span> <span data-ttu-id="5132c-316">如果您不能想像出合適的自訂圖示，請在適當的情況下改用標準圖示錯誤或警告圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-316">If you can't think of a suitable custom icon, use a standard icon error or warning icon instead when appropriate.</span></span> <span data-ttu-id="5132c-317">這些圖示可以有效地用來傳達許多類型的狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-317">These icons can be used effectively to communicate many types of status.</span></span>
-   <span data-ttu-id="5132c-318">**請勿變更太頻繁的狀態。**</span><span class="sxs-lookup"><span data-stu-id="5132c-318">**Don't change status too frequently.**</span></span> <span data-ttu-id="5132c-319">重迭圖示不應該出現雜訊、不穩定或需要注意。</span><span class="sxs-lookup"><span data-stu-id="5132c-319">Overlay icons shouldn't appear noisy, unstable, or demand attention.</span></span> <span data-ttu-id="5132c-320">眼睛對周邊周邊領域的變化很敏感，因此狀態變更必須很微妙。</span><span class="sxs-lookup"><span data-stu-id="5132c-320">The eye is sensitive to changes in the peripheral field of vision, so status changes need to be subtle.</span></span>
    -   <span data-ttu-id="5132c-321">**請勿快速變更圖示。**</span><span class="sxs-lookup"><span data-stu-id="5132c-321">**Don't change the icon rapidly.**</span></span> <span data-ttu-id="5132c-322">如果基礎狀態快速變更，請讓圖示反映高階狀態。</span><span class="sxs-lookup"><span data-stu-id="5132c-322">If underlying status is changing rapidly, have the icon reflect high-level status.</span></span>

        <span data-ttu-id="5132c-323">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-323">**Incorrect:**</span></span>

        ![<span data-ttu-id="5132c-324">兩種狀態中重迭圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-324">screen shot of overlay icon in two states</span></span> ](images/winenv-taskbar-image24.png)

        <span data-ttu-id="5132c-325">在此範例中，快速變更的重迭圖示會要求注意。</span><span class="sxs-lookup"><span data-stu-id="5132c-325">In this example, the rapidly changing overlay icon demands attention.</span></span>

    -   <span data-ttu-id="5132c-326">**請勿使用動畫。**</span><span class="sxs-lookup"><span data-stu-id="5132c-326">**Don't use animations.**</span></span> <span data-ttu-id="5132c-327">這麼做會造成太雜亂的事情。</span><span class="sxs-lookup"><span data-stu-id="5132c-327">Doing so is too distracting.</span></span>
    -   <span data-ttu-id="5132c-328">**請勿將圖示閃爍。**</span><span class="sxs-lookup"><span data-stu-id="5132c-328">**Don't flash the icon.**</span></span> <span data-ttu-id="5132c-329">這麼做會造成太雜亂的事情。</span><span class="sxs-lookup"><span data-stu-id="5132c-329">Doing so is too distracting.</span></span> <span data-ttu-id="5132c-330">如果事件需要立即注意，請改用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5132c-330">If an event requires immediate attention, use a dialog box instead.</span></span> <span data-ttu-id="5132c-331">如果事件另需要注意，請使用通知。</span><span class="sxs-lookup"><span data-stu-id="5132c-331">If the event otherwise needs attention, use a notification.</span></span>

### <a name="taskbar-button-flashing"></a><span data-ttu-id="5132c-332">工作列按鈕閃爍</span><span class="sxs-lookup"><span data-stu-id="5132c-332">Taskbar button flashing</span></span>

-   <span data-ttu-id="5132c-333">**請謹慎地使用工作列按鈕來要求使用者立即注意，讓執行中的工作持續進行。**</span><span class="sxs-lookup"><span data-stu-id="5132c-333">**Use taskbar button flashing sparingly to demand the user's immediate attention to keep an ongoing task running.**</span></span> <span data-ttu-id="5132c-334">當工作列按鈕閃爍時，使用者很難專注，因此假設他們會中斷其執行的動作，使其停止。</span><span class="sxs-lookup"><span data-stu-id="5132c-334">It's hard for users to concentrate while a taskbar button is flashing, so assume that they will interrupt what they are doing to make it stop.</span></span> <span data-ttu-id="5132c-335">雖然閃爍工作列按鈕的效果比竊取輸入焦點還好，但閃爍的工作列按鈕仍會有很大的干擾。</span><span class="sxs-lookup"><span data-stu-id="5132c-335">While flashing a taskbar button is better than stealing input focus, flashing taskbar buttons are still very intrusive.</span></span> <span data-ttu-id="5132c-336">請確定中斷已對齊，例如，表示使用者需要在關閉視窗之前儲存資料。</span><span class="sxs-lookup"><span data-stu-id="5132c-336">Make sure the interruption is justified, such as to indicate that the user needs to save data before closing a window.</span></span> <span data-ttu-id="5132c-337">非使用中的程式很少需要立即採取行動。</span><span class="sxs-lookup"><span data-stu-id="5132c-337">Inactive programs should rarely require immediate action.</span></span> <span data-ttu-id="5132c-338">如果使用者唯一要做的事是啟動程式、讀取訊息，或查看狀態變更，請不要閃爍工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="5132c-338">Don't flash the taskbar button if the only thing the user has to do is activate the program, read a message, or see a change in status.</span></span>
-   <span data-ttu-id="5132c-339">**如果不需要立即採取行動，請考慮下列替代方案：**</span><span class="sxs-lookup"><span data-stu-id="5132c-339">**If immediate action isn't required, consider these alternatives:**</span></span>
    -   <span data-ttu-id="5132c-340">使用 [動作成功通知](mess-notif.md) ，表示工作已完成。</span><span class="sxs-lookup"><span data-stu-id="5132c-340">Use an [action success notification](mess-notif.md) to indicate that a task has completed.</span></span>
    -   <span data-ttu-id="5132c-341">不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="5132c-341">Do nothing.</span></span> <span data-ttu-id="5132c-342">等到使用者下一次啟動程式時，才等待使用者參與問題。</span><span class="sxs-lookup"><span data-stu-id="5132c-342">Just wait for users to attend to the issue the next time they activate the program.</span></span> <span data-ttu-id="5132c-343">這通常是最佳選擇。</span><span class="sxs-lookup"><span data-stu-id="5132c-343">This is often the best choice.</span></span>
-   <span data-ttu-id="5132c-344">**如果非使用中的程式需要立即注意，請快閃其工作列按鈕以強調顯示並將其醒目提示。**</span><span class="sxs-lookup"><span data-stu-id="5132c-344">**If an inactive program requires immediate attention, flash its taskbar button to draw attention and leave it highlighted.**</span></span> <span data-ttu-id="5132c-345">請勿執行任何動作：請勿還原或啟用視窗，也不會播放任何音效效果。</span><span class="sxs-lookup"><span data-stu-id="5132c-345">Don't do anything else: don't restore or activate the window and don't play any sound effects.</span></span> <span data-ttu-id="5132c-346">相反地，請考慮使用者的視窗狀態選擇，並讓使用者在準備就緒時啟動視窗。</span><span class="sxs-lookup"><span data-stu-id="5132c-346">Instead, respect the user's window state selection and let the user activate the window when ready.</span></span>
-   <span data-ttu-id="5132c-347">**針對具有工作列按鈕的次要視窗，請將其按鈕閃爍，而不是主視窗的工作列按鈕。**</span><span class="sxs-lookup"><span data-stu-id="5132c-347">**For secondary windows that have a taskbar button, flash its button instead of the primary window's taskbar button.**</span></span> <span data-ttu-id="5132c-348">這麼做可讓使用者直接參與視窗。</span><span class="sxs-lookup"><span data-stu-id="5132c-348">Doing so allows users to attend to the window directly.</span></span>
-   <span data-ttu-id="5132c-349">**針對沒有工作列按鈕的次要視窗，請將主視窗的工作列按鈕閃爍，然後將次要視窗放在該程式的所有其他視窗之上。**</span><span class="sxs-lookup"><span data-stu-id="5132c-349">**For secondary windows that don't have a taskbar button, flash the primary window's taskbar button and bring the secondary window on top of all the other windows for that program.**</span></span> <span data-ttu-id="5132c-350">需要注意的次要視窗必須是最上層的，以確保使用者看見它們。</span><span class="sxs-lookup"><span data-stu-id="5132c-350">Secondary windows that require attention must be topmost to ensure that users see them.</span></span>
-   <span data-ttu-id="5132c-351">**一次只針對一個視窗快閃一個工作列按鈕。**</span><span class="sxs-lookup"><span data-stu-id="5132c-351">**Flash only one taskbar button for one window at a time.**</span></span> <span data-ttu-id="5132c-352">不需要閃爍一個以上的按鈕，也不會造成太大的干擾。</span><span class="sxs-lookup"><span data-stu-id="5132c-352">Flashing more than one button is unnecessary and too distracting.</span></span>
-   <span data-ttu-id="5132c-353">**當程式變成使用中狀態時，移除工作列按鈕醒目提示。**</span><span class="sxs-lookup"><span data-stu-id="5132c-353">**Remove the taskbar button highlight once the program becomes active.**</span></span>
-   <span data-ttu-id="5132c-354">**當程式變成使用中狀態時，請確定有明顯的東西。**</span><span class="sxs-lookup"><span data-stu-id="5132c-354">**When the program becomes active, make sure there is something obvious to do.**</span></span> <span data-ttu-id="5132c-355">一般來說，這個目標是藉由顯示詢問問題或起始動作的對話方塊來完成。</span><span class="sxs-lookup"><span data-stu-id="5132c-355">Typically, this objective is accomplished by displaying a dialog box that asks a question or initiates an action.</span></span>

### <a name="quick-launch-shortcuts"></a><span data-ttu-id="5132c-356">快速啟動快速鍵</span><span class="sxs-lookup"><span data-stu-id="5132c-356">Quick Launch shortcuts</span></span>

-   <span data-ttu-id="5132c-357">**只有當使用者加入宣告時，才將程式快捷方式放在快速啟動區域中。**</span><span class="sxs-lookup"><span data-stu-id="5132c-357">**Put program shortcuts in the Quick Launch area only if users opt in.**</span></span> <span data-ttu-id="5132c-358">因為快速啟動已從 Windows 7 移除，所以針對 Windows 7 設計的程式不應將程式快捷方式新增至快速啟動區域，或提供選項來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="5132c-358">Because Quick Launch was removed from Windows 7, programs designed for Windows 7 shouldn't add program shortcuts to the Quick Launch area or provide options to do so.</span></span>

### <a name="jump-lists"></a><span data-ttu-id="5132c-359">跳躍清單</span><span class="sxs-lookup"><span data-stu-id="5132c-359">Jump Lists</span></span>

<span data-ttu-id="5132c-360">**設計**</span><span class="sxs-lookup"><span data-stu-id="5132c-360">**Design**</span></span>

-   <span data-ttu-id="5132c-361">**設計跳躍清單來滿足使用者日常工作的目標。**</span><span class="sxs-lookup"><span data-stu-id="5132c-361">**Design Jump Lists to satisfy your users' goals for their everyday tasks.**</span></span> <span data-ttu-id="5132c-362">考量：</span><span class="sxs-lookup"><span data-stu-id="5132c-362">Consider:</span></span>
    -   <span data-ttu-id="5132c-363">**您的程式用途。**</span><span class="sxs-lookup"><span data-stu-id="5132c-363">**Your program's purpose.**</span></span> <span data-ttu-id="5132c-364">請思考下一步最可能的使用者。</span><span class="sxs-lookup"><span data-stu-id="5132c-364">Think about what users are most likely to do next.</span></span> <span data-ttu-id="5132c-365">針對檔建立程式，使用者可能會回到最近使用的檔。</span><span class="sxs-lookup"><span data-stu-id="5132c-365">For document creation programs, users are likely to return to recently used documents.</span></span> <span data-ttu-id="5132c-366">針對顯示現有內容的程式，使用者可能會想要存取經常使用的資源。</span><span class="sxs-lookup"><span data-stu-id="5132c-366">For programs that show existing content, users may want access to resources they use frequently.</span></span> <span data-ttu-id="5132c-367">針對其他程式，使用者可能會執行他們之前未完成的工作，例如讀取新郵件、觀看新的影片，或查看其下一個會議。</span><span class="sxs-lookup"><span data-stu-id="5132c-367">For other programs, users might be likely to do tasks they haven't done before, such as read new messages, watch new videos, or check their next meeting.</span></span>
    -   <span data-ttu-id="5132c-368">**使用者最在意的資訊。**</span><span class="sxs-lookup"><span data-stu-id="5132c-368">**What users care about most.**</span></span> <span data-ttu-id="5132c-369">考慮使用者為何會使用捷徑清單而不是其他方法。</span><span class="sxs-lookup"><span data-stu-id="5132c-369">Think about why users would use the Jump List instead of other means.</span></span> <span data-ttu-id="5132c-370">例如，使用者很可能會在意明確識別為重要 (的目的地，例如，使用者放在其連結列或我的最愛中的網址，或輸入) 的網路位址。</span><span class="sxs-lookup"><span data-stu-id="5132c-370">For example, users are more likely to care about destinations they explicitly identified as important (such as Web addresses users placed on their links bar or in Favorites, or typed in).</span></span> <span data-ttu-id="5132c-371">他們比較不可能在意間接取得或只需要進行一些工作 (例如透過重新導向流覽的 Web 位址，或按一下 [連結]) 。</span><span class="sxs-lookup"><span data-stu-id="5132c-371">They are less likely to care about those obtained indirectly or with little effort (such as Web addresses visited through redirection or by clicking links).</span></span>

        <span data-ttu-id="5132c-372">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-372">**Correct:**</span></span>

        ![<span data-ttu-id="5132c-373">具有一個目標連結的快捷方式清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-373">screen shot of jump list with one link to a target</span></span> ](images/winenv-taskbar-image25.png)

        <span data-ttu-id="5132c-374">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-374">**Incorrect:**</span></span>

        ![<span data-ttu-id="5132c-375">具有目標五個連結的跳躍清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-375">screen shot of jump list with five links to target</span></span> ](images/winenv-taskbar-image26.png)

        <span data-ttu-id="5132c-376">在不正確的範例中，捷徑清單包含使用者不太可能在意的許多目的地。</span><span class="sxs-lookup"><span data-stu-id="5132c-376">In the incorrect example, the Jump List contains many destinations that users aren't likely to care about.</span></span>

-   <span data-ttu-id="5132c-377">**不要讓目的地太細微。**</span><span class="sxs-lookup"><span data-stu-id="5132c-377">**Don't make destinations too granular.**</span></span> <span data-ttu-id="5132c-378">將目的地設為窄且特定可能會導致重複，有數種方式可移至相同的位置。</span><span class="sxs-lookup"><span data-stu-id="5132c-378">Making destinations too narrow and specific can result in redundancy, with several ways to go to the same place.</span></span> <span data-ttu-id="5132c-379">例如，不要列出個別網頁，而是改為列出最上層首頁;而不是列出歌曲、列出專輯。</span><span class="sxs-lookup"><span data-stu-id="5132c-379">For example, instead of listing individual Web pages, list top-level home pages instead; instead of listing songs, list albums.</span></span>

    <span data-ttu-id="5132c-380">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-380">**Correct:**</span></span>

    ![<span data-ttu-id="5132c-381">依群組組織的快捷方式清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-381">screen shot of jump list organized by groups</span></span> ](images/winenv-taskbar-image27.png)

    <span data-ttu-id="5132c-382">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-382">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-383">按歌曲組織之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-383">screen shot of jump list organized by songs</span></span> ](images/winenv-taskbar-image28.png)

    <span data-ttu-id="5132c-384">在不正確的範例中，列出捷徑清單中的歌曲將會填入單一專輯。</span><span class="sxs-lookup"><span data-stu-id="5132c-384">In the incorrect example, listing songs in a Jump List will fill it with a single album.</span></span>

-   <span data-ttu-id="5132c-385">**如果您不需要，請不要填滿所有可用的捷徑清單位置。**</span><span class="sxs-lookup"><span data-stu-id="5132c-385">**Don't fill all the available Jump List slots if you don't need to.**</span></span> <span data-ttu-id="5132c-386">如果您的程式只有三個有用的專案，請將焦點放在最有用的專案捷徑清單內容，僅提供三個專案。</span><span class="sxs-lookup"><span data-stu-id="5132c-386">Focus Jump List content on the most useful items if your program has only three useful items, provide only three.</span></span> <span data-ttu-id="5132c-387">捷徑清單中的專案越多，尋找任何特定專案所需的工作就越多。</span><span class="sxs-lookup"><span data-stu-id="5132c-387">The more items in a Jump List, the more effort required to find any specific item.</span></span>

    ![<span data-ttu-id="5132c-388">具有一個命令的跳躍清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-388">screen shot of jump list with one command</span></span> ](images/winenv-taskbar-image29.png)

    <span data-ttu-id="5132c-389">在此範例中，自黏便箋的配件會提供單一捷徑清單命令，因為這是必要的。</span><span class="sxs-lookup"><span data-stu-id="5132c-389">In this example, the Sticky Notes accessory provides a single Jump List command, because that's all that is needed.</span></span>

-   <span data-ttu-id="5132c-390">**只有在需要時才提供工具提示，以協助使用者瞭解捷徑清單專案。**</span><span class="sxs-lookup"><span data-stu-id="5132c-390">**Provide tooltips only when needed to help users understand Jump List items.**</span></span> <span data-ttu-id="5132c-391">避免重複的工具提示，因為它們是不必要的干擾。</span><span class="sxs-lookup"><span data-stu-id="5132c-391">Avoid redundant tooltips because they are an unnecessary distraction.</span></span> <span data-ttu-id="5132c-392">如需其他工具提示方針，請參閱 [工具提示和提示](ctrl-tooltips-and-infotips.md)。</span><span class="sxs-lookup"><span data-stu-id="5132c-392">For more tooltip guidelines, see [Tooltips and Infotips](ctrl-tooltips-and-infotips.md).</span></span>

    <span data-ttu-id="5132c-393">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-393">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-394">具有多餘工具提示之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-394">screen shot of jump list with redundant tooltip</span></span> ](images/winenv-taskbar-image30.png)

    <span data-ttu-id="5132c-395">在此範例中，捷徑清單工具提示是多餘的。</span><span class="sxs-lookup"><span data-stu-id="5132c-395">In this example, the Jump List tooltip is redundant.</span></span>

<span data-ttu-id="5132c-396">**捷徑清單功能與程式功能的比較**</span><span class="sxs-lookup"><span data-stu-id="5132c-396">**Jump List features vs. program features**</span></span>

-   <span data-ttu-id="5132c-397">**不要讓目的地和命令只能透過跳躍清單使用。**</span><span class="sxs-lookup"><span data-stu-id="5132c-397">**Don't make destinations and commands available only through Jump Lists.**</span></span> <span data-ttu-id="5132c-398">相同的目的地和命令應該可直接從程式本身取得。</span><span class="sxs-lookup"><span data-stu-id="5132c-398">The same destinations and commands should be available directly from the program itself.</span></span>
-   <span data-ttu-id="5132c-399">**針對命令的目的地和標籤使用一致的名稱。**</span><span class="sxs-lookup"><span data-stu-id="5132c-399">**Use consistent names for destinations and labels for commands.**</span></span> <span data-ttu-id="5132c-400">捷徑清單專案應標示為與直接從程式存取的對等專案相同。</span><span class="sxs-lookup"><span data-stu-id="5132c-400">Jump List items should be labeled the same as the equivalent items accessed directly from the program.</span></span>
-   <span data-ttu-id="5132c-401">**即使程式未執行，也可讓程式處理目的地和命令。**</span><span class="sxs-lookup"><span data-stu-id="5132c-401">**Enable your program to handle destinations and commands even when the program isn't running.**</span></span> <span data-ttu-id="5132c-402">這麼做是為了提供一致、可靠且方便的體驗。</span><span class="sxs-lookup"><span data-stu-id="5132c-402">Doing so is necessary for a consistent, dependable, and convenient experience.</span></span>

<span data-ttu-id="5132c-403">**分組**</span><span class="sxs-lookup"><span data-stu-id="5132c-403">**Grouping**</span></span>

-   <span data-ttu-id="5132c-404">**至少提供一個和最多三個群組。**</span><span class="sxs-lookup"><span data-stu-id="5132c-404">**Provide at least one and at most three groups.**</span></span> <span data-ttu-id="5132c-405">捷徑清單的專案一律會分組以標示其用途。</span><span class="sxs-lookup"><span data-stu-id="5132c-405">Jump List items are always grouped to label their purpose.</span></span> <span data-ttu-id="5132c-406">擁有三個以上的群組，可讓專案更難找到。</span><span class="sxs-lookup"><span data-stu-id="5132c-406">Having more than three groups makes items harder to find.</span></span>
-   <span data-ttu-id="5132c-407">**適當時，請使用標準組名。**</span><span class="sxs-lookup"><span data-stu-id="5132c-407">**Use standard group names when appropriate.**</span></span> <span data-ttu-id="5132c-408">標準組名對於使用者來說很熟悉且更容易瞭解。</span><span class="sxs-lookup"><span data-stu-id="5132c-408">Standard group names are familiar and easier for users to understand.</span></span>

    <span data-ttu-id="5132c-409">命令會被指定工作組名（由 Windows 指派），因此無法變更。</span><span class="sxs-lookup"><span data-stu-id="5132c-409">Commands are given the Tasks group name, which is assigned by Windows and therefore can't be changed.</span></span>

    <span data-ttu-id="5132c-410">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-410">**Correct:**</span></span>

    ![<span data-ttu-id="5132c-411">最近的組名之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-411">screen shot of jump list with recent group name</span></span> ](images/winenv-taskbar-image31.png)

    <span data-ttu-id="5132c-412">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-412">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-413">具有歷程記錄組名之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-413">screen shot of jump list with history group name</span></span> ](images/winenv-taskbar-image32.png)

    <span data-ttu-id="5132c-414">最新的組名是比較好的組名，因為它很熟悉，而且歷程記錄和最近的差異不值得進行。</span><span class="sxs-lookup"><span data-stu-id="5132c-414">Recent is the better group name because it is familiar, and the subtle distinction between history and recent isn't worth making.</span></span>

<span data-ttu-id="5132c-415">**命令**</span><span class="sxs-lookup"><span data-stu-id="5132c-415">**Commands**</span></span>

-   <span data-ttu-id="5132c-416">**提供一組固定的命令，無論程式執行狀態、目前檔或目前的使用者。**</span><span class="sxs-lookup"><span data-stu-id="5132c-416">**Provide a fixed set of commands regardless of program running state, current document, or current user.**</span></span> <span data-ttu-id="5132c-417">命令應該套用至整個程式，而不是特定的視窗或檔。</span><span class="sxs-lookup"><span data-stu-id="5132c-417">The commands should apply to the entire program, not to a specific window or document.</span></span> <span data-ttu-id="5132c-418">這麼做是為了提供一致、可靠且方便的體驗。</span><span class="sxs-lookup"><span data-stu-id="5132c-418">Doing so is necessary for a consistent, dependable, and convenient experience.</span></span> <span data-ttu-id="5132c-419">命令不應移除或停用。</span><span class="sxs-lookup"><span data-stu-id="5132c-419">Commands shouldn't be removed or disabled.</span></span>

    <span data-ttu-id="5132c-420">**例外狀況：** 當下列情況時，您可以替代或移除命令：</span><span class="sxs-lookup"><span data-stu-id="5132c-420">**Exceptions:** You may substitute or remove commands when:</span></span>

    -   <span data-ttu-id="5132c-421">只要一個命令永遠適用，一組互斥的命令就會共用單一命令位置。</span><span class="sxs-lookup"><span data-stu-id="5132c-421">A set of mutually exclusive commands share a single command slot, as long as one command always applies.</span></span>
    -   <span data-ttu-id="5132c-422">在使用特定功能之前，命令不會套用，只要在其他情況下一律套用命令即可。</span><span class="sxs-lookup"><span data-stu-id="5132c-422">Commands don't apply until specific features have been used, as long as the commands otherwise always apply.</span></span>

    <span data-ttu-id="5132c-423">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-423">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-424">具有列印工作之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-424">screen shot of jump list with print task</span></span> ](images/winenv-taskbar-image33.png)

    <span data-ttu-id="5132c-425">在此範例中，Print 不是理想的捷徑清單命令，因為它相依于目前的檔。</span><span class="sxs-lookup"><span data-stu-id="5132c-425">In this example, Print isn't a good Jump List command because it depends on the current document.</span></span>

    <span data-ttu-id="5132c-426">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-426">**Correct:**</span></span>

    ![<span data-ttu-id="5132c-427">登入和登出的跳躍清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-427">screen shot of jump list with sign-in and sign-out</span></span> ](images/winenv-taskbar-image34.png)

    <span data-ttu-id="5132c-428">在此範例中，登入和登出都是互斥的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-428">In this example, Sign in and Sign out are mutually exclusive commands.</span></span> <span data-ttu-id="5132c-429">此外，也會使用分隔符號來分組相關的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-429">Also, separators are used to group related commands.</span></span>

-   <span data-ttu-id="5132c-430">**適當時，請使用下列標準命令標籤。**</span><span class="sxs-lookup"><span data-stu-id="5132c-430">**Use the following standard command labels when appropriate.**</span></span> <span data-ttu-id="5132c-431">標準命令標籤可讓使用者更容易瞭解。</span><span class="sxs-lookup"><span data-stu-id="5132c-431">Standard command labels are easier for users to understand.</span></span>
-   <span data-ttu-id="5132c-432">**以邏輯順序顯示命令。**</span><span class="sxs-lookup"><span data-stu-id="5132c-432">**Present the commands in a logical order.**</span></span> <span data-ttu-id="5132c-433">一般訂單包括依使用頻率或使用順序。</span><span class="sxs-lookup"><span data-stu-id="5132c-433">Common orders include by frequency of use or order of use.</span></span> <span data-ttu-id="5132c-434">將高度相關的命令放在彼此旁邊。</span><span class="sxs-lookup"><span data-stu-id="5132c-434">Place highly related commands next to each other.</span></span> <span data-ttu-id="5132c-435">在 [工作] 群組中，視需要在相關命令群組之間放置分隔符號。</span><span class="sxs-lookup"><span data-stu-id="5132c-435">Within the Tasks group, put separators between groups of related commands as needed.</span></span>
-   <span data-ttu-id="5132c-436">**請勿提供用來開啟或關閉程式的命令。**</span><span class="sxs-lookup"><span data-stu-id="5132c-436">**Don't provide commands for opening or closing the program.**</span></span> <span data-ttu-id="5132c-437">這些命令都內建在所有跳躍清單中。</span><span class="sxs-lookup"><span data-stu-id="5132c-437">These commands are built into all Jump Lists.</span></span>

<span data-ttu-id="5132c-438">**命令圖示**</span><span class="sxs-lookup"><span data-stu-id="5132c-438">**Command icons**</span></span>

-   <span data-ttu-id="5132c-439">在 **[工作] 群組內，只有在可協助使用者瞭解、辨識或區分命令** 時，特別是在程式中使用的命令已建立圖示時，才提供命令圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-439">**Within the Tasks group, provide a command icon only when it helps users understand, recognize, or differentiate commands,** especially when there is an established icon for the command used within the program.</span></span>

    -   <span data-ttu-id="5132c-440">**例外狀況：** 如果您的程式使用兩個目的地 (一律會有圖示) 和命令，請考慮為所有命令提供圖示（如果沒有這麼做）。</span><span class="sxs-lookup"><span data-stu-id="5132c-440">**Exception:** If your program uses both destinations (which always have icons) and commands, consider providing icons for all commands if not doing so would look awkward.</span></span>

    <span data-ttu-id="5132c-441">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-441">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-442">跳躍清單不一致使用圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-442">screen shot of jump list inconsistent use of icons</span></span> ](images/winenv-taskbar-image35.png)

    <span data-ttu-id="5132c-443">在此範例中，Internet Explorer 應該提供所有命令的圖示，以避免出現麻煩的外觀。</span><span class="sxs-lookup"><span data-stu-id="5132c-443">In this example, Internet Explorer should provide icons for all commands to avoid an awkward appearance.</span></span>

<span data-ttu-id="5132c-444">**目的地**</span><span class="sxs-lookup"><span data-stu-id="5132c-444">**Destinations**</span></span>

-   <span data-ttu-id="5132c-445">**提供目前使用者專屬的一組動態目的地，但不受程式執行狀態或目前檔的影響。**</span><span class="sxs-lookup"><span data-stu-id="5132c-445">**Provide a dynamic set of destinations that are specific to the current user, but independent of the program running state or current document.**</span></span> <span data-ttu-id="5132c-446">如先前所述，請確定其符合您的程式目的、使用者最在意的專案，以及具有適當的明確程度。</span><span class="sxs-lookup"><span data-stu-id="5132c-446">As mentioned previously, make sure they fit your program's purpose, are what users care about the most, and have the right level of specificity.</span></span>
-   <span data-ttu-id="5132c-447">**適用時，請使用「自動」目的地清單。**</span><span class="sxs-lookup"><span data-stu-id="5132c-447">**When suitable, use an "automatic" destination list.**</span></span> <span data-ttu-id="5132c-448">自動目的地是由 Windows 管理，但您的程式會控制傳遞的特定目的地。</span><span class="sxs-lookup"><span data-stu-id="5132c-448">Automatic destinations are managed by Windows, but your program controls the specific destinations that are passed on.</span></span>
    -   <span data-ttu-id="5132c-449">請考慮使用最新的檔建立程式，使用者可能會回到最近使用的目的地。</span><span class="sxs-lookup"><span data-stu-id="5132c-449">Consider using Recent for document creation programs where users are likely to return to recently used destinations.</span></span>

        ![<span data-ttu-id="5132c-450">具有「最近」組名之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-450">screen shot of jump list with 'recent' group name</span></span> ](images/winenv-taskbar-image36.png)

        <span data-ttu-id="5132c-451">在此範例中，Windows 記事本使用最近的目的地。</span><span class="sxs-lookup"><span data-stu-id="5132c-451">In this example, Windows Notepad uses Recent destinations.</span></span>

    -   <span data-ttu-id="5132c-452">請考慮經常在顯示現有內容的程式中使用，使用者可能會在其中返回經常使用的專案。</span><span class="sxs-lookup"><span data-stu-id="5132c-452">Consider using Frequent for programs that show existing content, where users are likely to return to items that they use often.</span></span> <span data-ttu-id="5132c-453">頻繁的目的地會依頻率順序排序，最常優先。</span><span class="sxs-lookup"><span data-stu-id="5132c-453">Frequent destinations are sorted in order of frequency, most frequent first.</span></span>

        ![<span data-ttu-id="5132c-454">常用組名的快捷方式清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-454">screen shot of jump list with frequent group name</span></span> ](images/winenv-taskbar-image37.png)

        <span data-ttu-id="5132c-455">在此範例中，Windows 檔案總管會使用頻繁的目的地。</span><span class="sxs-lookup"><span data-stu-id="5132c-455">In this example, Windows Explorer uses Frequent destinations.</span></span>

    -   <span data-ttu-id="5132c-456">如果最近會導致許多無用的目的地，請經常使用。</span><span class="sxs-lookup"><span data-stu-id="5132c-456">Use Frequent if Recent would result in many useless destinations.</span></span> <span data-ttu-id="5132c-457">當使用者移至許多不同的目的地，但不太可能會傳回很少使用的目的地時，經常會有更穩定的清單，以及更好的選擇。</span><span class="sxs-lookup"><span data-stu-id="5132c-457">Frequent lists are more stable, and the better choice when users go to many different destinations, but aren't likely to return to rarely used ones.</span></span>

        <span data-ttu-id="5132c-458">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-458">**Incorrect:**</span></span>

        ![<span data-ttu-id="5132c-459">含有數個最近專案的快捷方式清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-459">screen shot of jump list with several recent items</span></span> ](images/winenv-taskbar-image38.png)

        <span data-ttu-id="5132c-460">在 Windows Internet Explorer 中使用 [最近] 會導致許多無用的目的地。</span><span class="sxs-lookup"><span data-stu-id="5132c-460">Using Recent in Windows Internet Explorer would result in many useless destinations.</span></span>

    -   <span data-ttu-id="5132c-461">如果 [最近] 或 [頻繁] 是相當適合的選項，請使用 [最近]，因為這種方法可讓使用者更容易瞭解並可預測。</span><span class="sxs-lookup"><span data-stu-id="5132c-461">If Recent or Frequent are equally suitable choices, use Recent because that approach is easier for users to understand and is more predictable.</span></span>
    -   <span data-ttu-id="5132c-462">如果使用 [最近]，而程式在 [檔案] 功能表中有對等專案，請以相同的順序讓清單具有相同的內容。</span><span class="sxs-lookup"><span data-stu-id="5132c-462">If using Recent, and the program has an equivalent in the File menu, make the lists have the same contents in the same order.</span></span> <span data-ttu-id="5132c-463">對使用者而言，這些應該會顯示為相同的清單。</span><span class="sxs-lookup"><span data-stu-id="5132c-463">To users, these should appear to be the same lists.</span></span>

-   <span data-ttu-id="5132c-464">**必要時，請使用自訂目的地清單。**</span><span class="sxs-lookup"><span data-stu-id="5132c-464">**When necessary, use a custom destination list.**</span></span> <span data-ttu-id="5132c-465">您的程式可以完全掌控自訂目的地清單的內容和排序次序，因此可以根據任何因素來建立清單。</span><span class="sxs-lookup"><span data-stu-id="5132c-465">Your program has complete control over a custom destination list's contents and sort order, and therefore can base the list on any factors.</span></span>
    -   <span data-ttu-id="5132c-466">如果適合，請建立最新或經常的自訂版本，但自動管理不適合您的程式。</span><span class="sxs-lookup"><span data-stu-id="5132c-466">Create custom versions of Recent or Frequent if those are suitable, but the automatic management doesn't work well for your program.</span></span> <span data-ttu-id="5132c-467">例如，您的程式可能需要追蹤開啟檔案命令以外的各種因素。</span><span class="sxs-lookup"><span data-stu-id="5132c-467">For example, your program may need to track a variety of factors beyond open file commands.</span></span> <span data-ttu-id="5132c-468">在此情況下，請使用相同名稱 (最近的) 和排序次序，因為使用者不會察覺到差異。</span><span class="sxs-lookup"><span data-stu-id="5132c-468">In this case, use the same name (Recent or Frequent) and sort order because users won't be aware of the difference.</span></span>
    -   <span data-ttu-id="5132c-469">否則，請使用不同類型的目的地，以進一步滿足您的使用者目標。</span><span class="sxs-lookup"><span data-stu-id="5132c-469">Otherwise, use a different type of destination to better satisfy your user's goals.</span></span> <span data-ttu-id="5132c-470">這些清單通常可協助使用者執行他們之前未完成的工作，例如讀取新郵件、觀看新影片，或檢查其下一個會議。</span><span class="sxs-lookup"><span data-stu-id="5132c-470">Often, these lists help users perform tasks that they haven't done before, such as read new messages, watch new videos, or check their next meeting.</span></span>

        ![<span data-ttu-id="5132c-471">具有「新增」組名之跳躍清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-471">screen shot of jump list with 'new' group name</span></span> ](images/winenv-taskbar-image39.png)

        <span data-ttu-id="5132c-472">在此範例中，Windows Media Center 會列出使用者尚未看到的最近錄製的節目。</span><span class="sxs-lookup"><span data-stu-id="5132c-472">In this example, Windows Media Center lists the recently recorded shows that the user hasn't seen yet.</span></span>

    -   <span data-ttu-id="5132c-473">選擇對應至使用者的清單之精神模型的排序次序。</span><span class="sxs-lookup"><span data-stu-id="5132c-473">Choose a sort order that corresponds to the user's mental model of the list.</span></span> <span data-ttu-id="5132c-474">例如，待辦事項樣式清單會先列出下一件事。</span><span class="sxs-lookup"><span data-stu-id="5132c-474">For example, a to-do style list would have the next thing to do listed first.</span></span> <span data-ttu-id="5132c-475">如果沒有明確的精神模型，請依字母順序排序目的地清單。</span><span class="sxs-lookup"><span data-stu-id="5132c-475">If there is no clear mental model, sort the destination list in alphabetical order.</span></span>

-   <span data-ttu-id="5132c-476">**請勿使用多個目的地清單來提供相同資料的不同觀點。**</span><span class="sxs-lookup"><span data-stu-id="5132c-476">**Don't use multiple destination lists that give different views of the same data.**</span></span> <span data-ttu-id="5132c-477">相反地，多個目的地清單應該有最不同的資料，以支援不同的案例。</span><span class="sxs-lookup"><span data-stu-id="5132c-477">Rather, multiple destination lists should have mostly different data to support difference scenarios.</span></span> <span data-ttu-id="5132c-478">例如，您可以提供最新清單或常用清單，但不能同時提供兩者。</span><span class="sxs-lookup"><span data-stu-id="5132c-478">For example, you can provide a Recent list or a Frequent list, but not both.</span></span> <span data-ttu-id="5132c-479">如果有重迭的專案，這麼做會很浪費，但如果移除重迭的專案，就會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="5132c-479">Doing so is wasteful if overlapping items are present, but confusing if overlapping items are removed.</span></span>

    <span data-ttu-id="5132c-480">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-480">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-481">重複群組專案的快捷方式清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-481">screen shot of jump list with repeated group items</span></span> ](images/winenv-taskbar-image40.png)

    <span data-ttu-id="5132c-482">在此範例中，為相同的目的地提供不同的觀點，會造成浪費。</span><span class="sxs-lookup"><span data-stu-id="5132c-482">In this example, providing different views of the same destinations is wasteful.</span></span>

    <span data-ttu-id="5132c-483">**正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-483">**Correct:**</span></span>

    ![<span data-ttu-id="5132c-484">具有妥善組織之工作的快捷方式清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-484">screen shot of jump list with well organized tasks</span></span> ](images/winenv-taskbar-image41.png)

    <span data-ttu-id="5132c-485">在此範例中，目的地清單針對不同的工作具有不同的資料。</span><span class="sxs-lookup"><span data-stu-id="5132c-485">In this example, the destination lists have different data for different tasks.</span></span>

-   <span data-ttu-id="5132c-486">**如果您的程式有可清除隱私權資料的命令，也請清除目的地清單。**</span><span class="sxs-lookup"><span data-stu-id="5132c-486">**If your program has a command to clear data for privacy, clear the Destinations lists as well.**</span></span> <span data-ttu-id="5132c-487">目的地清單可能包含機密資料。</span><span class="sxs-lookup"><span data-stu-id="5132c-487">Destination lists may contain sensitive data.</span></span>

### <a name="thumbnail-toolbars"></a><span data-ttu-id="5132c-488">縮圖工具列</span><span class="sxs-lookup"><span data-stu-id="5132c-488">Thumbnail toolbars</span></span>

<span data-ttu-id="5132c-489">**互動**</span><span class="sxs-lookup"><span data-stu-id="5132c-489">**Interaction**</span></span>

-   <span data-ttu-id="5132c-490">**提供最多七個最重要、最常使用的命令，以套用至縮圖中顯示的視窗。**</span><span class="sxs-lookup"><span data-stu-id="5132c-490">**Provide up to seven of the most important, frequently used commands that apply to the window shown in the thumbnail.**</span></span> <span data-ttu-id="5132c-491">如果您的程式只有三個重要且常用的命令，請務必提供最多的命令，只提供三個。</span><span class="sxs-lookup"><span data-stu-id="5132c-491">Don't feel obligated to provide as many commands as you can if your program has only three important, frequently used commands, provide only three.</span></span>

    <span data-ttu-id="5132c-492">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-492">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-493">具有太多命令的工具列螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-493">screen shot of toolbar with too many commands</span></span> ](images/winenv-taskbar-image42.png)

    <span data-ttu-id="5132c-494">在此範例中，縮圖工具列有不重要的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-494">In this example, the thumbnail toolbar has commands that aren't important.</span></span>

-   <span data-ttu-id="5132c-495">**使用直接和立即的命令。**</span><span class="sxs-lookup"><span data-stu-id="5132c-495">**Use commands that are direct and immediate.**</span></span> <span data-ttu-id="5132c-496">這些命令應該會立即生效，按一下命令不應該顯示下拉式功能表或對話方塊以進行更多輸入。</span><span class="sxs-lookup"><span data-stu-id="5132c-496">These commands should have an immediate effect clicking the command should not display a drop-down menu or dialog box for more input.</span></span>

    <span data-ttu-id="5132c-497">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-497">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-498">具有下拉式功能表的縮圖螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-498">screen shot of thumbnail with drop-down menu</span></span> ](images/winenv-taskbar-image43.png)

    <span data-ttu-id="5132c-499">縮圖工具列命令必須立即生效。</span><span class="sxs-lookup"><span data-stu-id="5132c-499">Thumbnail toolbar commands must have an immediate effect.</span></span>

-   <span data-ttu-id="5132c-500">**停用未套用至目前內容的命令，或直接導致錯誤的命令。**</span><span class="sxs-lookup"><span data-stu-id="5132c-500">**Disable commands that don't apply to the current context, or that would directly result in an error.**</span></span> <span data-ttu-id="5132c-501">請勿隱藏這類命令，因為這樣做會使工具列呈現不穩定。</span><span class="sxs-lookup"><span data-stu-id="5132c-501">Don't hide such commands because doing so makes the toolbar presentation unstable.</span></span>
-   <span data-ttu-id="5132c-502">**如果使用者按一下命令可能會檢查結果，或立即按一下另一個命令，請勿關閉縮圖。**</span><span class="sxs-lookup"><span data-stu-id="5132c-502">**Don't dismiss the thumbnail when users click a command if they are likely to review the results or immediately click another command.**</span></span> <span data-ttu-id="5132c-503">移除指出使用者現在已完成的命令縮圖，例如使用顯示其他視窗的命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-503">Remove the thumbnail for commands that indicate that the user is finished for now, such as with commands that display other windows.</span></span>

    ![<span data-ttu-id="5132c-504">使用命令的 media player 縮圖螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-504">screen shot of media player thumbnail with command</span></span> ](images/winenv-taskbar-image44.png)

    <span data-ttu-id="5132c-505">在此範例中，按一下 Windows Media Player 中的 [下一步] 會繼續顯示縮圖，因為使用者可能會想要提供其他命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-505">In this example, clicking Next in Windows Media Player continues to display the thumbnail because users might want to give other commands.</span></span>

    ![<span data-ttu-id="5132c-506">具有聊天圖示的縮圖螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="5132c-506">screen shot of thumbnail with chat icon</span></span> ](images/winenv-taskbar-image45.png)

    <span data-ttu-id="5132c-507">在此範例中，按一下 Windows Live Messenger 的聊天會關閉縮圖，因為使用者最有可能傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="5132c-507">In this example, clicking Chat in Windows Live Messenger dismisses the thumbnail because users are most likely to send a message.</span></span>

<span data-ttu-id="5132c-508">**展示**</span><span class="sxs-lookup"><span data-stu-id="5132c-508">**Presentation**</span></span>

-   <span data-ttu-id="5132c-509">**請確定縮圖工具列圖示符合 Aero 樣式圖示的指導方針。**</span><span class="sxs-lookup"><span data-stu-id="5132c-509">**Make sure thumbnail toolbar icons conform to the Aero-style icon guidelines.**</span></span> <span data-ttu-id="5132c-510">針對每個命令，提供高品質的16x16、20x20 和24x24 圖元、完整色彩圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-510">For each command, provide high-quality 16x16, 20x20, and 24x24 pixel, full color icons.</span></span> <span data-ttu-id="5132c-511">較大的版本會在高 DPI 的顯示模式中使用。</span><span class="sxs-lookup"><span data-stu-id="5132c-511">The larger versions are used in high-dpi display modes.</span></span>
-   <span data-ttu-id="5132c-512">**請確定在一般和暫留狀態中，工具列背景色彩清楚看到圖示。**</span><span class="sxs-lookup"><span data-stu-id="5132c-512">**Make sure the icons are clearly visible against the toolbar background color in both normal and hover states.**</span></span> <span data-ttu-id="5132c-513">一律在內容和高對比模式中評估圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-513">Always evaluate icons in context and in the high-contrast modes.</span></span>
-   <span data-ttu-id="5132c-514">**選擇清楚傳達其效果的命令圖示設計。**</span><span class="sxs-lookup"><span data-stu-id="5132c-514">**Choose command icon designs that clearly communicate their effect.**</span></span> <span data-ttu-id="5132c-515">設計完善的命令圖示一目了然，可協助使用者有效率地尋找及瞭解命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-515">Well-designed command icons are self-explanatory to help users find and understand commands efficiently.</span></span>
-   <span data-ttu-id="5132c-516">**選擇可辨識且可辨別的圖示。**</span><span class="sxs-lookup"><span data-stu-id="5132c-516">**Choose icons that are recognizable and distinguishable.**</span></span> <span data-ttu-id="5132c-517">請確定圖示有獨特的圖形和色彩。</span><span class="sxs-lookup"><span data-stu-id="5132c-517">Make sure the icons have distinctive shapes and colors.</span></span> <span data-ttu-id="5132c-518">這麼做可協助使用者快速尋找命令，即使它們不記得圖示符號也一樣。</span><span class="sxs-lookup"><span data-stu-id="5132c-518">Doing so helps users find the commands quickly, even if they don't remember the icon symbol.</span></span> <span data-ttu-id="5132c-519">初次使用之後，使用者應該不需要依賴工具提示來區分命令。</span><span class="sxs-lookup"><span data-stu-id="5132c-519">After initial use, users shouldn't have to rely on tooltips to distinguish between the commands.</span></span>
-   <span data-ttu-id="5132c-520">**提供工具提示以標記每個命令。**</span><span class="sxs-lookup"><span data-stu-id="5132c-520">**Provide a tooltip to label each command.**</span></span> <span data-ttu-id="5132c-521">很好的工具提示會標示所指向的未標記控制項。</span><span class="sxs-lookup"><span data-stu-id="5132c-521">A good tooltip labels the unlabeled control being pointed to.</span></span> <span data-ttu-id="5132c-522">如需指導方針與範例，請參閱 [工具提示和提示](ctrl-tooltips-and-infotips.md)。</span><span class="sxs-lookup"><span data-stu-id="5132c-522">For guidelines and examples, see [Tooltips and Infotips](ctrl-tooltips-and-infotips.md).</span></span>

### <a name="progress-bars"></a><span data-ttu-id="5132c-523">進度列</span><span class="sxs-lookup"><span data-stu-id="5132c-523">Progress bars</span></span>

-   <span data-ttu-id="5132c-524">**遵循一般進度列指導方針，** 包括不重新開機或備份進度，以及使用紅色進度列來指出問題。</span><span class="sxs-lookup"><span data-stu-id="5132c-524">**Follow the general progress bar guidelines,** including not restarting or backing up progress, and using a red progress bar to indicate a problem.</span></span>
-   <span data-ttu-id="5132c-525">**避免使用不定的進度列。**</span><span class="sxs-lookup"><span data-stu-id="5132c-525">**Avoid using indeterminate progress bars.**</span></span> <span data-ttu-id="5132c-526">不定的進度列會顯示活動，而不是進度。</span><span class="sxs-lookup"><span data-stu-id="5132c-526">Indeterminate progress bars show activity, not progress.</span></span> <span data-ttu-id="5132c-527">針對不接受授與活動的罕見情況，保留不定的進度列。</span><span class="sxs-lookup"><span data-stu-id="5132c-527">Reserve indeterminate progress bars for those rare situations where users don't take activity for granted.</span></span>

<span data-ttu-id="5132c-528">如需詳細的指導方針，請參閱 [進度](progress-bars.md)列。</span><span class="sxs-lookup"><span data-stu-id="5132c-528">For more guidelines, see [Progress Bars](progress-bars.md).</span></span>

## <a name="text"></a><span data-ttu-id="5132c-529">Text</span><span class="sxs-lookup"><span data-stu-id="5132c-529">Text</span></span>

### <a name="window-titles"></a><span data-ttu-id="5132c-530">視窗標題</span><span class="sxs-lookup"><span data-stu-id="5132c-530">Window titles</span></span>

<span data-ttu-id="5132c-531">選擇視窗標題時，請考慮標題在工作列上的外觀：</span><span class="sxs-lookup"><span data-stu-id="5132c-531">When choosing window titles, consider the title's appearance on the taskbar:</span></span>

-   <span data-ttu-id="5132c-532">藉由簡潔地先放置區分的資訊，將標題優化以顯示在工作列上。</span><span class="sxs-lookup"><span data-stu-id="5132c-532">Optimize titles for display on the taskbar by concisely placing the distinguishing information first.</span></span>
-   <span data-ttu-id="5132c-533">若為非模式進度對話方塊，請先總結進度。</span><span class="sxs-lookup"><span data-stu-id="5132c-533">For modeless progress dialog boxes, first summarize the progress.</span></span> <span data-ttu-id="5132c-534">範例：「66% 完成」。</span><span class="sxs-lookup"><span data-stu-id="5132c-534">Example: "66% Complete."</span></span>
-   <span data-ttu-id="5132c-535">避免使用截斷的視窗標題。</span><span class="sxs-lookup"><span data-stu-id="5132c-535">Avoid window titles that have awkward truncations.</span></span>

    <span data-ttu-id="5132c-536">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="5132c-536">**Incorrect:**</span></span>

    ![<span data-ttu-id="5132c-537">標題的螢幕擷取畫面，會截斷程式名稱</span><span class="sxs-lookup"><span data-stu-id="5132c-537">screen shot of title that cuts off program name</span></span> ](images/winenv-taskbar-image48.png)

    <span data-ttu-id="5132c-538">在此範例中，截斷的視窗標題會產生不太不幸的結果。</span><span class="sxs-lookup"><span data-stu-id="5132c-538">In this example, the truncated window title has unfortunate results.</span></span>

### <a name="jump-list-commands"></a><span data-ttu-id="5132c-539">捷徑清單命令</span><span class="sxs-lookup"><span data-stu-id="5132c-539">Jump List commands</span></span>

-   <span data-ttu-id="5132c-540">**使用動詞命令開始。**</span><span class="sxs-lookup"><span data-stu-id="5132c-540">**Start commands with a verb.**</span></span>
-   <span data-ttu-id="5132c-541">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="5132c-541">**Use sentence-style capitalization.**</span></span>

<span data-ttu-id="5132c-542">如需更多命令標籤指導方針，請參閱 [功能表](cmd-menus.md)。</span><span class="sxs-lookup"><span data-stu-id="5132c-542">For more command label guidelines, see [Menus](cmd-menus.md).</span></span>

## <a name="documentation"></a><span data-ttu-id="5132c-543">文件</span><span class="sxs-lookup"><span data-stu-id="5132c-543">Documentation</span></span>

<span data-ttu-id="5132c-544">參考工作列時：</span><span class="sxs-lookup"><span data-stu-id="5132c-544">When referring to the taskbar:</span></span>

-   <span data-ttu-id="5132c-545">請參閱整個工具列，將工作列 (為小寫) 中的單一複合字組。</span><span class="sxs-lookup"><span data-stu-id="5132c-545">Refer to the entire bar as the taskbar (a single compound word in lowercase).</span></span>
-   <span data-ttu-id="5132c-546">在工作列上明確地參考專案的標籤，或通常是工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="5132c-546">Refer to items on the taskbar specifically by their label, or generally as taskbar buttons.</span></span>
-   <span data-ttu-id="5132c-547">可能的話，請使用粗體文字來格式化工作列標籤。</span><span class="sxs-lookup"><span data-stu-id="5132c-547">When possible, format the taskbar labels using bold text.</span></span> <span data-ttu-id="5132c-548">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="5132c-548">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>
-   <span data-ttu-id="5132c-549">請參閱覆迭圖示作為工作列按鈕圖示。</span><span class="sxs-lookup"><span data-stu-id="5132c-549">Refer to overlay icons as taskbar button icons.</span></span> <span data-ttu-id="5132c-550">請勿將它們稱為通知，即使其目的是要通知使用者。</span><span class="sxs-lookup"><span data-stu-id="5132c-550">Don't refer to them as notifications, even if their purpose is to notify users.</span></span> <span data-ttu-id="5132c-551">不過，您可以說這些圖示會通知使用者特定事件。</span><span class="sxs-lookup"><span data-stu-id="5132c-551">However, you can say that these icons notify users of specific events.</span></span>

<span data-ttu-id="5132c-552">範例：新的郵件工作列按鈕圖示會通知您新的電子郵件訊息已到達。</span><span class="sxs-lookup"><span data-stu-id="5132c-552">Example: The New Mail taskbar button icon notifies you that a new e-mail message has arrived.</span></span>

 

