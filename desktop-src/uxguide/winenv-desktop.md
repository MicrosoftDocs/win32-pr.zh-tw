---
title: 桌面
description: 桌面是其程式的使用者工作區。 它無法提升您對程式或其品牌的認知。 請勿濫用。
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 159be01b1058eac99c30b83534b7a9eafd9c4eb4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104027629"
---
# <a name="desktop"></a><span data-ttu-id="9d07b-105">桌面</span><span class="sxs-lookup"><span data-stu-id="9d07b-105">Desktop</span></span>

> [!NOTE]
> <span data-ttu-id="9d07b-106">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="9d07b-106">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="9d07b-107">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="9d07b-107">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="9d07b-108">桌面是其程式的使用者工作區。</span><span class="sxs-lookup"><span data-stu-id="9d07b-108">The desktop is the user's work area for their programs.</span></span> <span data-ttu-id="9d07b-109">它無法提升您對程式或其品牌的認知。</span><span class="sxs-lookup"><span data-stu-id="9d07b-109">It's not a way to promote awareness of your program or its brand.</span></span> <span data-ttu-id="9d07b-110">不要濫用！</span><span class="sxs-lookup"><span data-stu-id="9d07b-110">Don't abuse it!</span></span>

<span data-ttu-id="9d07b-111">桌上型電腦是 Microsoft Windows 所提供的螢幕上的工作區，類似于實體桌面。</span><span class="sxs-lookup"><span data-stu-id="9d07b-111">The desktop is the onscreen work area provided by Microsoft Windows, analogous to a physical desktop.</span></span> <span data-ttu-id="9d07b-112">它是由 [工作區](glossary.md) 和 [工作列](winenv-taskbar.md)所組成。</span><span class="sxs-lookup"><span data-stu-id="9d07b-112">It consists of a [work area](glossary.md) and [taskbar](winenv-taskbar.md).</span></span> <span data-ttu-id="9d07b-113">工作區域可以橫跨多個監視器。</span><span class="sxs-lookup"><span data-stu-id="9d07b-113">The work area may span multiple monitors.</span></span>

![<span data-ttu-id="9d07b-114">一般 windows 桌面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="9d07b-114">screen shot of a typical windows desktop</span></span> ](images/winenv-desktop-image1.png)

<span data-ttu-id="9d07b-115">一般的 Windows 桌面。</span><span class="sxs-lookup"><span data-stu-id="9d07b-115">A typical Windows desktop.</span></span>

<span data-ttu-id="9d07b-116">作用中的監視器是使用中的程式正在執行的監視器。</span><span class="sxs-lookup"><span data-stu-id="9d07b-116">The active monitor is the monitor where the active program is running.</span></span> <span data-ttu-id="9d07b-117">預設監視器是具有 [開始] 功能表、工作列和通知區域的監視器。</span><span class="sxs-lookup"><span data-stu-id="9d07b-117">The default monitor is the one with the Start menu, taskbar, and notification area.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="9d07b-118">設計概念</span><span class="sxs-lookup"><span data-stu-id="9d07b-118">Design concepts</span></span>

<span data-ttu-id="9d07b-119">Windows 桌面具有下列程式存取點：</span><span class="sxs-lookup"><span data-stu-id="9d07b-119">The Windows desktop has the following program access points:</span></span>

-   <span data-ttu-id="9d07b-120">**工作區。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-120">**Work area.**</span></span> <span data-ttu-id="9d07b-121">使用者可以執行其工作的螢幕區域，以及儲存程式、檔和其快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9d07b-121">The onscreen area where users can perform their work, as well as store programs, documents, and their shortcuts.</span></span> <span data-ttu-id="9d07b-122">雖然在技術上，桌面包含工作列，但在大部分的情況下，它只會參考工作區域。</span><span class="sxs-lookup"><span data-stu-id="9d07b-122">While technically the desktop includes the taskbar, in most contexts it refers just to the work area.</span></span>
-   <span data-ttu-id="9d07b-123">**[開始] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-123">**Start button.**</span></span> <span data-ttu-id="9d07b-124">所有程式和特殊 Windows 的存取點都將 (檔、圖片、音樂、遊戲、電腦主控台) 、使用「最近使用的」清單來快速存取最近使用的程式和檔。</span><span class="sxs-lookup"><span data-stu-id="9d07b-124">The access point for all programs and special Windows places (Documents, Pictures, Music, Games, Computer, Control Panel), with "most recently used" lists for quick access to recently used programs and documents.</span></span>
-   <span data-ttu-id="9d07b-125">**快速啟動。已從 Windows 7 移除。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-125">**Quick Launch. Removed from Windows 7.**</span></span> <span data-ttu-id="9d07b-126">使用者選取之程式的直接存取點。</span><span class="sxs-lookup"><span data-stu-id="9d07b-126">A direct access point for programs selected by the user.</span></span>
-   <span data-ttu-id="9d07b-127">**任務。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-127">**Taskbar.**</span></span> <span data-ttu-id="9d07b-128">執行具有桌上型電腦狀態之程式的存取點。</span><span class="sxs-lookup"><span data-stu-id="9d07b-128">The access point for running programs that have desktop presence.</span></span> <span data-ttu-id="9d07b-129">雖然在技術上，工作列橫跨 [開始] 按鈕到通知區域的整個橫條，但是在大部分的內容中，工作列都指的是介於中間的區域，其中包含工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="9d07b-129">While technically the taskbar spans the entire bar from the Start button to the notification area, in most contexts taskbar refers to the area in between, containing the taskbar buttons.</span></span> <span data-ttu-id="9d07b-130">此區域有時稱為 taskband。</span><span class="sxs-lookup"><span data-stu-id="9d07b-130">This area is sometimes referred to as the taskband.</span></span>
-   <span data-ttu-id="9d07b-131">**Deskbands.不建議使用。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-131">**Deskbands. Not recommended.**</span></span> <span data-ttu-id="9d07b-132">最小化功能、長時間執行的程式，例如語言列。</span><span class="sxs-lookup"><span data-stu-id="9d07b-132">Minimized functional, long-running programs, such as the Language Bar.</span></span> <span data-ttu-id="9d07b-133">最小化至 deskbands 的程式不會在最小化時顯示工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="9d07b-133">Programs that minimize to deskbands don't display taskbar buttons when minimized.</span></span>
-   <span data-ttu-id="9d07b-134">**通知區域。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-134">**Notification area.**</span></span> <span data-ttu-id="9d07b-135">通知和狀態的短期來源，以及不存在於桌面上的系統和程式相關功能的存取點。</span><span class="sxs-lookup"><span data-stu-id="9d07b-135">A short-term source for notifications and status, as well as an access point for system- and program-related features that have no presence on the desktop.</span></span>

![<span data-ttu-id="9d07b-136">[開始] 按鈕、工作列、縮圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="9d07b-136">screen shot of start button, taskbar, thumbnail</span></span> ](images/winenv-desktop-image2.png)

<span data-ttu-id="9d07b-137">Windows 桌面存取點包含 [開始] 按鈕、工作列和通知區域。</span><span class="sxs-lookup"><span data-stu-id="9d07b-137">The Windows desktop access points include the Start button, taskbar, and notification area.</span></span> <span data-ttu-id="9d07b-138">請注意工作列按鈕的縮圖功能。</span><span class="sxs-lookup"><span data-stu-id="9d07b-138">Note the thumbnail feature of the taskbar button.</span></span>

<span data-ttu-id="9d07b-139">**Windows 桌面是受限的共用資源，是使用者進入 Windows 的進入點。讓使用者保持控制。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-139">**The Windows desktop is a limited, shared resource that is the user's entry point to Windows. Leave users in control.**</span></span> <span data-ttu-id="9d07b-140">您應以預期的方式使用其區域，任何其他使用方式都應視為濫用。</span><span class="sxs-lookup"><span data-stu-id="9d07b-140">You should use its areas as intended—any other usage should be considered an abuse.</span></span> <span data-ttu-id="9d07b-141">絕對不要將它們視為提升您的程式或其 [品牌](exper-branding.md)認知的方式。</span><span class="sxs-lookup"><span data-stu-id="9d07b-141">Never view them as ways to promote awareness of your program or its [brand](exper-branding.md).</span></span>

<span data-ttu-id="9d07b-142">在 Windows 7 中，原始設備製造商 (Oem) 和獨立硬體廠商 (Ihv) 可以使用 Device Stage 來設計電腦和裝置的自訂、品牌化 UI，而不會讓使用者的桌上型電腦變得雜亂。</span><span class="sxs-lookup"><span data-stu-id="9d07b-142">For Windows 7, Original Equipment Manufacturers (OEMs) and Independent Hardware Vendors (IHVs) can use Device Stage to design a customized, branded UI for the computer and devices, without cluttering users' desktops.</span></span> <span data-ttu-id="9d07b-143">尤其是 Oem 可以使用 Device Stage PC，來提供自訂程式、服務供應專案及支援的功能。</span><span class="sxs-lookup"><span data-stu-id="9d07b-143">OEMs in particular can use Device Stage PC to feature custom programs, service offerings, and support.</span></span> <span data-ttu-id="9d07b-144">如需詳細資訊，請參閱 [Microsoft 裝置體驗開發工具組](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx)。</span><span class="sxs-lookup"><span data-stu-id="9d07b-144">For more information, see the [Microsoft Device Experience Development Kit](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).</span></span>

<span data-ttu-id="9d07b-145">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-145">**If you do only one thing...**</span></span>

-   <span data-ttu-id="9d07b-146">不要濫用桌面，讓使用者保持掌控。</span><span class="sxs-lookup"><span data-stu-id="9d07b-146">Don't abuse the desktop—keep users in control.</span></span> <span data-ttu-id="9d07b-147">如果您的目標使用者可能經常使用您的程式，請在安裝期間提供選項，將快捷方式放在桌面上（預設為未選取）。</span><span class="sxs-lookup"><span data-stu-id="9d07b-147">If your target users are likely to use your program frequently, provide an option during setup to put a shortcut on the desktop, unselected by default.</span></span>

## <a name="guidelines"></a><span data-ttu-id="9d07b-148">指導方針</span><span class="sxs-lookup"><span data-stu-id="9d07b-148">Guidelines</span></span>

-   <span data-ttu-id="9d07b-149">**如果您的使用者很可能經常使用您的程式，請在安裝期間提供選項，將程式快捷方式放在桌面上。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-149">**If your users are very likely to use your program frequently, provide an option during setup to put a program shortcut on the desktop.**</span></span> <span data-ttu-id="9d07b-150">大部分的程式都不常使用，以保證提供此選項。</span><span class="sxs-lookup"><span data-stu-id="9d07b-150">Most programs won't be used frequently enough to warrant offering this option.</span></span>
-   <span data-ttu-id="9d07b-151">**預設會顯示未選取的選項。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-151">**Present the option unselected by default.**</span></span> <span data-ttu-id="9d07b-152">要求使用者選取此選項很重要，因為在桌上型電腦上不想要的圖示之後，許多使用者都不願意移除它們。</span><span class="sxs-lookup"><span data-stu-id="9d07b-152">Requiring users to select the option is important because once undesired icons are on the desktop, many users are reluctant to remove them.</span></span> <span data-ttu-id="9d07b-153">這可能會導致不必要的桌面雜亂。</span><span class="sxs-lookup"><span data-stu-id="9d07b-153">This can lead to unnecessary desktop clutter.</span></span>
-   <span data-ttu-id="9d07b-154">**如果使用者選取選項，請只提供單一程式快捷方式。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-154">**If users select the option, provide only a single program shortcut.**</span></span> <span data-ttu-id="9d07b-155">如果您的產品是由多個程式所組成，請只提供主要程式的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9d07b-155">If your product consists of multiple programs, provide a shortcut only to the main program.</span></span>
-   <span data-ttu-id="9d07b-156">**只將程式快捷方式放在桌面上。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-156">**Put only program shortcuts on the desktop.**</span></span> <span data-ttu-id="9d07b-157">請勿放置實際的程式或其他類型的檔案。</span><span class="sxs-lookup"><span data-stu-id="9d07b-157">Don't put the actual program or other types of files.</span></span>

    <span data-ttu-id="9d07b-158">**正確：**</span><span class="sxs-lookup"><span data-stu-id="9d07b-158">**Correct:**</span></span>

    ![<span data-ttu-id="9d07b-159">具有箭號重迭之快捷方式圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="9d07b-159">screen shot of shortcut icon with arrow overlay</span></span> ](images/winenv-desktop-image3.png)

    <span data-ttu-id="9d07b-160">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="9d07b-160">**Incorrect:**</span></span>

    ![<span data-ttu-id="9d07b-161">程式圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="9d07b-161">screen shot of program icon</span></span> ](images/winenv-desktop-image4.png)

    <span data-ttu-id="9d07b-162">在不正確的範例中，會將程式（而不是快捷方式）複製到桌面。</span><span class="sxs-lookup"><span data-stu-id="9d07b-162">In the incorrect example, the program, not a shortcut, is copied to the desktop.</span></span>

-   <span data-ttu-id="9d07b-163">**選擇可在不截斷的情況下顯示的標籤。**</span><span class="sxs-lookup"><span data-stu-id="9d07b-163">**Choose a label that can be displayed without truncation.**</span></span> <span data-ttu-id="9d07b-164">使用者不應看見省略號。</span><span class="sxs-lookup"><span data-stu-id="9d07b-164">Users shouldn't see an ellipsis.</span></span>

    <span data-ttu-id="9d07b-165">**正確：**</span><span class="sxs-lookup"><span data-stu-id="9d07b-165">**Correct:**</span></span>

    ![<span data-ttu-id="9d07b-166">具有完整名稱之快捷方式圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="9d07b-166">screen shot of shortcut icon with complete name</span></span> ](images/winenv-desktop-image3.png)

    <span data-ttu-id="9d07b-167">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="9d07b-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="9d07b-168">以截斷名稱顯示快捷方式圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="9d07b-168">screen shot of shortcut icon with truncated name</span></span> ](images/winenv-desktop-image5.png)

    <span data-ttu-id="9d07b-169">在不正確的範例中，程式快捷方式標籤很長，因此會被截斷。</span><span class="sxs-lookup"><span data-stu-id="9d07b-169">In the incorrect example, the program shortcut label is so long that it is truncated.</span></span>

## <a name="documentation"></a><span data-ttu-id="9d07b-170">文件</span><span class="sxs-lookup"><span data-stu-id="9d07b-170">Documentation</span></span>

-   <span data-ttu-id="9d07b-171">參考桌面時，請使用 desktop、uncapitalized。</span><span class="sxs-lookup"><span data-stu-id="9d07b-171">When referring to the desktop, use desktop, uncapitalized.</span></span>
-   <span data-ttu-id="9d07b-172">參考桌面快捷方式時，請使用快捷方式 uncapitalized。</span><span class="sxs-lookup"><span data-stu-id="9d07b-172">When referring to desktop shortcuts, use shortcut, uncapitalized.</span></span>

 

 