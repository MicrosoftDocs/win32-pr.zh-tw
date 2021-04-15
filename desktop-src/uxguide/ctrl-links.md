---
title: 連結
description: 透過連結，使用者可以流覽至另一個頁面、視窗或說明主題;顯示定義;起始命令;或選擇選項。
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 521f96146de535210d79814b375499ea34399179
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104561792"
---
# <a name="links"></a><span data-ttu-id="40942-103">連結</span><span class="sxs-lookup"><span data-stu-id="40942-103">Links</span></span>

> [!NOTE]
> <span data-ttu-id="40942-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="40942-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="40942-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="40942-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="40942-106">透過 *連結*，使用者可以流覽至另一個頁面、視窗或說明主題;顯示定義;起始命令;或選擇選項。</span><span class="sxs-lookup"><span data-stu-id="40942-106">With a *link*, users can navigate to another page, window, or Help topic; display a definition; initiate a command; or choose an option.</span></span> <span data-ttu-id="40942-107">連結是文字或圖形，表示可以按一下，通常是使用流覽或未造訪的 [連結系統色彩](vis-color.md)來顯示。</span><span class="sxs-lookup"><span data-stu-id="40942-107">A link is text or a graphic that indicates that it can be clicked, typically by being displayed using the visited or unvisited [link system colors](vis-color.md).</span></span> <span data-ttu-id="40942-108">傳統上，連結也會加上底線，但這種方法通常不是必要的，而且不是為了減少視覺效果。</span><span class="sxs-lookup"><span data-stu-id="40942-108">Traditionally, links are underlined as well, but that approach is often unnecessary and falling out of favor to reduce visual clutter.</span></span>

<span data-ttu-id="40942-109">當使用者將滑鼠停留在連結上時，連結文字會顯示為加上底線的 (如果尚未) ，且指標圖形變更為 [手](inter-mouse.md)。</span><span class="sxs-lookup"><span data-stu-id="40942-109">When users hover over a link, the link text appears as underlined (if it wasn't already) and the pointer shape changes to a [hand](inter-mouse.md).</span></span>

<span data-ttu-id="40942-110">文字連結是最輕量的加權可點擊控制項，通常用來減少設計的視覺複雜度。</span><span class="sxs-lookup"><span data-stu-id="40942-110">A text link is the lightest weight clickable control, and is often used to reduce the visual complexity of a design.</span></span>

> [!Note]  
> <span data-ttu-id="40942-111">與 [命令連結](ctrl-command-links.md) 和 [版面](vis-layout.md) 配置相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="40942-111">Guidelines related to [command links](ctrl-command-links.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="40942-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="40942-112">Is this the right control?</span></span>

<span data-ttu-id="40942-113">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="40942-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="40942-114">**這是用來流覽至另一個頁面、視窗或說明主題的連結;顯示定義;起始命令;或選擇一個選項？**</span><span class="sxs-lookup"><span data-stu-id="40942-114">**Is the link used to navigate to another page, window, or Help topic; display a definition; initiate a command; or choose an option?**</span></span> <span data-ttu-id="40942-115">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="40942-115">If not, use another control.</span></span>
-   <span data-ttu-id="40942-116">**命令按鈕是否是較佳的選擇？**</span><span class="sxs-lookup"><span data-stu-id="40942-116">**Would a command button be a better choice?**</span></span> <span data-ttu-id="40942-117">如果有下列情況，請使用 [命令按鈕](ctrl-command-buttons.md) ：</span><span class="sxs-lookup"><span data-stu-id="40942-117">Use a [command button](ctrl-command-buttons.md) if:</span></span>
    -   <span data-ttu-id="40942-118">控制項會起始立即動作（包括顯示視窗），而該命令會與視窗的主要用途相關。</span><span class="sxs-lookup"><span data-stu-id="40942-118">The control initiates an immediate action, including displaying a window, and that command relates to the primary purpose of the window.</span></span>
    -   <span data-ttu-id="40942-119">即使是針對次要命令，也會顯示一個視窗，以收集輸入或進行選擇。</span><span class="sxs-lookup"><span data-stu-id="40942-119">A window is displayed to gather input or making choices, even if for a secondary command.</span></span>
    -   <span data-ttu-id="40942-120">標籤很短，由四個或更少的字組所組成，因此可避免冗長的長按鈕外觀。</span><span class="sxs-lookup"><span data-stu-id="40942-120">The label is short, consisting of four or fewer words, thus avoiding the awkward appearance of long buttons.</span></span>
    -   <span data-ttu-id="40942-121">此命令不是內嵌的。</span><span class="sxs-lookup"><span data-stu-id="40942-121">The command is not inline.</span></span>
    -   <span data-ttu-id="40942-122">控制項會出現在其他相關命令按鈕的群組中。</span><span class="sxs-lookup"><span data-stu-id="40942-122">The control appears within a group of other related command buttons.</span></span>
    -   <span data-ttu-id="40942-123">動作具有破壞性或無法復原。</span><span class="sxs-lookup"><span data-stu-id="40942-123">The action is destructive or irreversible.</span></span> <span data-ttu-id="40942-124">因為使用者會將連結與導覽 (以及將) 的功能建立關聯，所以連結不適合具有明顯後果的命令。</span><span class="sxs-lookup"><span data-stu-id="40942-124">Because users associate links with navigation (and the ability to back out), links aren't appropriate for commands with significant consequences.</span></span>
    -   <span data-ttu-id="40942-125">同樣地，在「 [嚮導](win-wizards.md) 」或「工作 [流程](glossary.md)」中，此命令代表承諾用量。</span><span class="sxs-lookup"><span data-stu-id="40942-125">Similarly, in a [wizard](win-wizards.md) or [task flow](glossary.md), the command represents commitment.</span></span> <span data-ttu-id="40942-126">在這類視窗中，命令按鈕會建議承諾，而連結建議您流覽至下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="40942-126">In such windows, command buttons suggest commitment whereas links suggest navigating to the next step.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="40942-127">設計概念</span><span class="sxs-lookup"><span data-stu-id="40942-127">Design concepts</span></span>

<span data-ttu-id="40942-128">**讓連結可辨識**</span><span class="sxs-lookup"><span data-stu-id="40942-128">**Making links recognizable**</span></span>

<span data-ttu-id="40942-129">連結缺乏 [affordance](glossary.md)，這表示 **其視覺屬性不建議其使用方式** ，而且只能透過經驗理解。</span><span class="sxs-lookup"><span data-stu-id="40942-129">Links lack [affordance](glossary.md), which means **their visual properties don't suggest how they are used** and are understood only through experience.</span></span> <span data-ttu-id="40942-130">沒有底線和連結系統色彩的連結會顯示為一般文字;確定其行為的唯一方法是從其呈現方式、其內容，或將指標放在其上。</span><span class="sxs-lookup"><span data-stu-id="40942-130">Links without an underline and link system colors appear as normal text; the only way to ascertain their behavior is from their presentation, their context, or by positioning the pointer over them.</span></span>

<span data-ttu-id="40942-131">令人驚訝的是，這種缺乏 affordance 的動機通常是使用連結的動機，因為它們顯得很輕量，因此降低了設計的視覺複雜度。</span><span class="sxs-lookup"><span data-stu-id="40942-131">Surprisingly, this lack of affordance is often a motivation for using links because they appear so lightweight, thereby reducing the visual complexity of a design.</span></span> <span data-ttu-id="40942-132">連結會消除由其他控制項使用的 [命令按鈕](ctrl-command-buttons.md) 和框線所使用的視覺效果繁重框架。</span><span class="sxs-lookup"><span data-stu-id="40942-132">Links eliminate the visually heavy frame used by [command buttons](ctrl-command-buttons.md) and border used by other controls.</span></span> <span data-ttu-id="40942-133">例如，雖然您可能會使用命令按鈕讓主要命令變得很明顯，但您可以選擇次要命令的連結來將它們反加重。</span><span class="sxs-lookup"><span data-stu-id="40942-133">For example, while you might use command buttons to make primary commands obvious, you might choose links for secondary commands to de-emphasize them.</span></span>

<span data-ttu-id="40942-134">然後挑戰是要保留足夠的視覺線索，讓使用者可以辨識這些連結。</span><span class="sxs-lookup"><span data-stu-id="40942-134">The challenge is then to keep enough visual clues so users can recognize the links.</span></span> <span data-ttu-id="40942-135">基本的指導方針是， **使用者必須能夠透過視覺化檢查來辨識連結，他們不應將其暫留在物件上，或按一下以判斷它是否為連結**。</span><span class="sxs-lookup"><span data-stu-id="40942-135">The fundamental guideline is **users must be able to recognize links by visual inspection alone they shouldn't have to hover over an object or click it to determine if it is a link**.</span></span>

<span data-ttu-id="40942-136">如果連結使用 [連結系統色彩](vis-color.md) 和至少一個下列的視覺線索，則使用者可以單獨辨識視覺檢查的連結：</span><span class="sxs-lookup"><span data-stu-id="40942-136">Users can recognize a link by visual inspection alone if the link uses the [link system colors](vis-color.md) and at least one of the following visual clues:</span></span>

-   <span data-ttu-id="40942-137">加上底線的文字。</span><span class="sxs-lookup"><span data-stu-id="40942-137">Underlined text.</span></span>
-   <span data-ttu-id="40942-138">圖形或專案符號，例如具有 [圖示連結](#usage-patterns) 模式的文字。</span><span class="sxs-lookup"><span data-stu-id="40942-138">A graphic or bullet, such as with the [text with icon link](#usage-patterns) pattern.</span></span>
-   <span data-ttu-id="40942-139">在標準導覽、選項或命令位置內放置，例如視窗的 [內容區域](glossary.md) ，或是在巡覽列、功能表列、工具列或頁尾中。</span><span class="sxs-lookup"><span data-stu-id="40942-139">Placement within a standard navigation, option, or command location, such as the [content area](glossary.md) of a window, or in a navigation bar, menu bar, toolbar, or page footer.</span></span>

<span data-ttu-id="40942-140">使用者也可以使用下列視覺線索來辨識視覺化檢查的連結，但這些線索本身並不足夠：</span><span class="sxs-lookup"><span data-stu-id="40942-140">Users can also recognize a link by visual inspection with the following visual clues, but these clues aren't sufficient by themselves:</span></span>

-   <span data-ttu-id="40942-141">建議按一下的文字，例如顯示、列印、複製或刪除等命令式動詞命令開始的命令。</span><span class="sxs-lookup"><span data-stu-id="40942-141">Text that suggests clicking, such as a command starting with an imperative verb like Show, Print, Copy, or Delete.</span></span>
-   <span data-ttu-id="40942-142">在一般文字區塊內放置。</span><span class="sxs-lookup"><span data-stu-id="40942-142">Placement within a block of normal text.</span></span>

<span data-ttu-id="40942-143">當然，使用者隨時都可以透過滑鼠停留或按一下的方式來判斷連結。</span><span class="sxs-lookup"><span data-stu-id="40942-143">Of course, users can always determine a link through interaction either hovering or clicking.</span></span> <span data-ttu-id="40942-144">如果任何重要工作都不需要探索連結，您可以消除這類連結。</span><span class="sxs-lookup"><span data-stu-id="40942-144">If discovery of a link isn't required for any significant tasks, you can de-emphasize such links.</span></span>

![<span data-ttu-id="40942-145">黑色背景上灰色標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-145">screen shot of gray labels on black background</span></span> ](images/ctrl-links-image1.png)

<span data-ttu-id="40942-146">在此範例中，請洽詢美國、使用條款、商標和隱私權聲明。</span><span class="sxs-lookup"><span data-stu-id="40942-146">In this example, Contact Us, Terms of Use, Trademarks, and Privacy Statement are links.</span></span> <span data-ttu-id="40942-147">因為任何重要的工作都不需要它們，所以會刻意將它們取消強調。</span><span class="sxs-lookup"><span data-stu-id="40942-147">They are intentionally de-emphasized because they aren't required for any important tasks.</span></span> <span data-ttu-id="40942-148">唯一的線索是連結滑鼠指標，並放在視窗底部的標準導覽區域中，以顯示滑鼠指標。</span><span class="sxs-lookup"><span data-stu-id="40942-148">The only clues that they are links are that they have a mouse pointer on hover and are positioned in a standard navigation area at the bottom of the window.</span></span>

<span data-ttu-id="40942-149">**建立特定、相關且可預測的連結**</span><span class="sxs-lookup"><span data-stu-id="40942-149">**Making links specific, relevant, and predictable**</span></span>

<span data-ttu-id="40942-150">連結文字應該指出按一下連結的結果。</span><span class="sxs-lookup"><span data-stu-id="40942-150">Link text should indicate the result of clicking on the link.</span></span>

<span data-ttu-id="40942-151">特定連結比一般連結更吸引使用者，所以請 **使用連結標籤，提供有關按一下連結之結果的特定描述性資訊**。</span><span class="sxs-lookup"><span data-stu-id="40942-151">Specific links are more compelling to users than general links, so **use link labels that give specific descriptive information about the result of clicking on the link**.</span></span> <span data-ttu-id="40942-152">不過，請確定您的連結文字不太明確，因為它會誤導並防止適當的使用。</span><span class="sxs-lookup"><span data-stu-id="40942-152">However, make sure that your link text isn't so specific that it is misleading and discourages proper use.</span></span>

<span data-ttu-id="40942-153">精簡的連結可能會比詳細資訊連結更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="40942-153">Concise links are more likely to be read than verbose links.</span></span> <span data-ttu-id="40942-154">**消除不必要的文字和詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="40942-154">**Eliminate unnecessary text and detail.**</span></span> <span data-ttu-id="40942-155">連結標籤不需要完整的。</span><span class="sxs-lookup"><span data-stu-id="40942-155">Link labels don't have to be comprehensive.</span></span>

<span data-ttu-id="40942-156">若要評估您的連結文字：</span><span class="sxs-lookup"><span data-stu-id="40942-156">To evaluate your link text:</span></span>

-   <span data-ttu-id="40942-157">請確定連結文字反映連結所支援的案例。</span><span class="sxs-lookup"><span data-stu-id="40942-157">Make sure the link text reflects the scenarios that the link supports.</span></span>
-   <span data-ttu-id="40942-158">請確定連結的結果是可預測的。</span><span class="sxs-lookup"><span data-stu-id="40942-158">Make sure the results of the link are predictable.</span></span> <span data-ttu-id="40942-159">結果不應驚訝的使用者。</span><span class="sxs-lookup"><span data-stu-id="40942-159">Users shouldn't be surprised by the results.</span></span>

<span data-ttu-id="40942-160">**如果您只進行兩件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="40942-160">**If you do only two things...**</span></span>

1. <span data-ttu-id="40942-161">讓視覺檢查單獨找到連結。</span><span class="sxs-lookup"><span data-stu-id="40942-161">Make links discoverable by visual inspection alone.</span></span> <span data-ttu-id="40942-162">使用者不需要與您的程式互動，即可找到連結。</span><span class="sxs-lookup"><span data-stu-id="40942-162">Users shouldn't have to interact with your program to find links.</span></span>

2. <span data-ttu-id="40942-163">使用連結，提供有關點選連結之結果的特定描述性資訊，視需要使用最多文字。</span><span class="sxs-lookup"><span data-stu-id="40942-163">Use links that give specific descriptive information about the result of clicking on the link, using as much text as necessary.</span></span> <span data-ttu-id="40942-164">使用者應該能夠精確地預測連結文字的連結結果， [以及選用的](ctrl-tooltips-and-infotips.md)提示。</span><span class="sxs-lookup"><span data-stu-id="40942-164">Users should be able to accurately predict the result of a link from its link text and optional [infotip](ctrl-tooltips-and-infotips.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="40942-165">使用模式</span><span class="sxs-lookup"><span data-stu-id="40942-165">Usage patterns</span></span>

<span data-ttu-id="40942-166">連結有數種功能模式：</span><span class="sxs-lookup"><span data-stu-id="40942-166">Links have several functional patterns:</span></span>



|                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40942-167">**導覽連結**</span><span class="sxs-lookup"><span data-stu-id="40942-167">**Navigation links**</span></span><br/> <span data-ttu-id="40942-168">用來流覽至另一個頁面或視窗的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-168">A link used to navigate to another page or window.</span></span> <br/>                                                      | <span data-ttu-id="40942-169">當您在瀏覽器視窗或嚮導中，按一下連結會流覽至另一個頁面;或顯示新的視窗。</span><span class="sxs-lookup"><span data-stu-id="40942-169">Clicking the link navigates inplace to another page, as in a browser window or wizard; or displays a new window.</span></span> <span data-ttu-id="40942-170">相較于工作連結，流覽不會起始工作，而是直接流覽至另一個位置或繼續進行中的工作。</span><span class="sxs-lookup"><span data-stu-id="40942-170">In contrast to task links, the navigation doesn't initiate a task but simply navigates to another place or proceeds with a task already in progress.</span></span> <span data-ttu-id="40942-171">由於使用者隨時都可以返回，因此導覽暗示了安全性。</span><span class="sxs-lookup"><span data-stu-id="40942-171">Navigation implies safety because the user can always go back.</span></span><br/> <span data-ttu-id="40942-172">新聞頭條新聞</span><span class="sxs-lookup"><span data-stu-id="40942-172">News headlines</span></span><br/> <span data-ttu-id="40942-173">在此範例中，按一下連結會流覽至 [新聞頭條新聞] 頁面。</span><span class="sxs-lookup"><span data-stu-id="40942-173">In this example, clicking the link navigates to the News headlines page.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="40942-174">**工作連結**</span><span class="sxs-lookup"><span data-stu-id="40942-174">**Task links**</span></span><br/> <span data-ttu-id="40942-175">用來起始新命令的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-175">A link used to initiate a new command.</span></span> <br/>                                                                        | <span data-ttu-id="40942-176">按一下連結可立即執行命令，或顯示對話方塊或頁面來收集更多輸入。</span><span class="sxs-lookup"><span data-stu-id="40942-176">Clicking the link either performs a command immediately, or displays a dialog box or page to gather more input.</span></span> <span data-ttu-id="40942-177">相對於導覽連結，工作連結會起始新的工作，而不是繼續進行現有的工作。</span><span class="sxs-lookup"><span data-stu-id="40942-177">In contrast to navigation links, task links initiate a new task instead of continuing with an existing task.</span></span> <span data-ttu-id="40942-178">工作不表示 safetyusers 無法使用 Back 命令還原為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="40942-178">Tasks don't imply safetyusers can't revert to the previous state with a Back command.</span></span> <span data-ttu-id="40942-179">系統會呼叫工作連結，以防止與 [命令連結](ctrl-command-links.md)混淆。</span><span class="sxs-lookup"><span data-stu-id="40942-179">Task links are so called to prevent confusion with [command links](ctrl-command-links.md).</span></span> <br/> <span data-ttu-id="40942-180">登入</span><span class="sxs-lookup"><span data-stu-id="40942-180">Login</span></span><br/> <span data-ttu-id="40942-181">在此範例中，按一下連結會起始登入命令。</span><span class="sxs-lookup"><span data-stu-id="40942-181">In this example, clicking the link initiates a login command.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="40942-182">**說明連結**</span><span class="sxs-lookup"><span data-stu-id="40942-182">**Help links**</span></span><br/> <span data-ttu-id="40942-183">用來顯示說明主題的文字連結。</span><span class="sxs-lookup"><span data-stu-id="40942-183">A text link used to display a Help topic.</span></span> <br/>                                                                     | <span data-ttu-id="40942-184">按一下該連結會在另一個視窗中顯示說明文章。</span><span class="sxs-lookup"><span data-stu-id="40942-184">Clicking the link displays a Help article in a separate window.</span></span><br/> <span data-ttu-id="40942-185">什麼是強式密碼？</span><span class="sxs-lookup"><span data-stu-id="40942-185">What is a strong password?</span></span><br/> <span data-ttu-id="40942-186">在此範例中，按一下連結會顯示具有指定主題的說明視窗。</span><span class="sxs-lookup"><span data-stu-id="40942-186">In this example, clicking the link displays a Help window with the given topic.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="40942-187">**定義連結**</span><span class="sxs-lookup"><span data-stu-id="40942-187">**Definition links**</span></span><br/> <span data-ttu-id="40942-188">當使用者按一下或停留在連結上時，用來顯示資訊提示中定義的文字連結。</span><span class="sxs-lookup"><span data-stu-id="40942-188">a text link used to display a definition in an infotip when the user clicks on or hovers over the link.</span></span> <br/> | <span data-ttu-id="40942-189">此模式適用于定義您的使用者可能不知道的詞彙，而不會增加螢幕雜亂。</span><span class="sxs-lookup"><span data-stu-id="40942-189">this pattern is useful for defining terms that may not be known to your users without adding screen clutter.</span></span><br/> ![<span data-ttu-id="40942-190">滑鼠停留時顯示的提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-190">screen shot of infotip displayed by mouse hover</span></span> ](images/ctrl-links-image2.png)<br/> <span data-ttu-id="40942-191">在此範例中，會顯示 [提示] 定義。</span><span class="sxs-lookup"><span data-stu-id="40942-191">In this example, the infotip definition is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="40942-192">**功能表連結**</span><span class="sxs-lookup"><span data-stu-id="40942-192">**Menu links**</span></span><br/> <span data-ttu-id="40942-193">一組用來建立功能表的工作連結。</span><span class="sxs-lookup"><span data-stu-id="40942-193">a set of task links used to create a menu.</span></span> <br/>                                                                    | <span data-ttu-id="40942-194">因為功能表的內容會指出一組連結，所以文字通常不會加上底線， (除了停留) 之外，可能不會使用連結系統色彩。</span><span class="sxs-lookup"><span data-stu-id="40942-194">because the context of the menu indicates a set of links, the text is usually not underlined (except on hover) and might not use the link system colors.</span></span><br/> ![<span data-ttu-id="40942-195">一組連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-195">screen shot of a set of links</span></span> ](images/ctrl-links-image3.png)<br/> <span data-ttu-id="40942-196">在此範例中，一組連結會建立功能表。</span><span class="sxs-lookup"><span data-stu-id="40942-196">In this example, a set of links creates a menu.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="40942-197">**選項連結**</span><span class="sxs-lookup"><span data-stu-id="40942-197">**Option links**</span></span><br/> <span data-ttu-id="40942-198">選取的選項或其預留位置，其中按一下連結會叫用命令來變更該選項。</span><span class="sxs-lookup"><span data-stu-id="40942-198">a selected option or its placeholder, where clicking the link invokes a command to change that option.</span></span><br/>       | <span data-ttu-id="40942-199">不同于一般文字連結，此連結會變更其文字，以反映目前選取的選項，而且一律會使用未連結的連結色彩來繪製。</span><span class="sxs-lookup"><span data-stu-id="40942-199">unlike regular text links, the link changes its text to reflect the currently selected option and is always drawn using the unvisited link color.</span></span> <br/> ![<span data-ttu-id="40942-200">outlook 規則 wizard 中的規則螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-200">screen shot of a rule in outlook rules wizard</span></span> ](images/ctrl-links-image4.png)<br/> <span data-ttu-id="40942-201">左邊的範例會顯示 [microsoft outlook 規則] 嚮導中包含預留位置選項的規則。</span><span class="sxs-lookup"><span data-stu-id="40942-201">the example on the left shows a rule from the microsoft outlook rules wizard with placeholder options.</span></span> <span data-ttu-id="40942-202">當使用者按一下連結並選取某些選項之後，右邊的範例會更新連結文字以顯示結果。</span><span class="sxs-lookup"><span data-stu-id="40942-202">after users click the links and select some options, the right-hand example updates the link text to show the results.</span></span><br/> <span data-ttu-id="40942-203">如果選項具有變數格式，則使用選項連結特別適用。</span><span class="sxs-lookup"><span data-stu-id="40942-203">using option links is particularly suitable if the options have a variable format.</span></span> <br/> ![<span data-ttu-id="40942-204">規則嚮導中已修改規則的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-204">screen shot of a modified rule in the rules wizard</span></span> ](images/ctrl-links-image5.png)<br/> <span data-ttu-id="40942-205">右側的範例顯示 outlook 規則具有變數格式。</span><span class="sxs-lookup"><span data-stu-id="40942-205">the example on the right shows that outlook rules have a variable format.</span></span> <br/> ![<span data-ttu-id="40942-206">文字變更為下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-206">screen shot of how text changes to drop-down list</span></span> ](images/ctrl-links-image6.png)<br/> <span data-ttu-id="40942-207">左邊的範例顯示選項連結。</span><span class="sxs-lookup"><span data-stu-id="40942-207">The example on the left shows an option link.</span></span> <span data-ttu-id="40942-208">當選取時，它會變成下拉式清單，如右側所示。</span><span class="sxs-lookup"><span data-stu-id="40942-208">It becomes a drop-down list when selected, as shown on the right.</span></span><br/> |



 

<span data-ttu-id="40942-209">連結也有數種展示模式：</span><span class="sxs-lookup"><span data-stu-id="40942-209">Links also have several presentation patterns:</span></span>



|                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40942-210">**純文字連結**</span><span class="sxs-lookup"><span data-stu-id="40942-210">**Plain text links**</span></span><br/> <span data-ttu-id="40942-211">只包含文字。</span><span class="sxs-lookup"><span data-stu-id="40942-211">consist only of text.</span></span> <br/>                                      | <span data-ttu-id="40942-212">這份簡報最有彈性，因為它可以在任何地方使用，包括 [內嵌](glossary.md)在內。</span><span class="sxs-lookup"><span data-stu-id="40942-212">this presentation is the most flexible because it can be used anywhere, including [inline](glossary.md).</span></span><br/> <span data-ttu-id="40942-213">![藍色連結文字的螢幕擷取畫面 ](images/ctrl-links-image7.png)</span><span class="sxs-lookup"><span data-stu-id="40942-213">![screen shot of blue link text ](images/ctrl-links-image7.png)</span></span><br/> <span data-ttu-id="40942-214">在此範例中，文字色彩清楚地識別內嵌連結。</span><span class="sxs-lookup"><span data-stu-id="40942-214">In this example, the text color clearly identifies an inline link.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="40942-215">**具有圖示連結的文字**</span><span class="sxs-lookup"><span data-stu-id="40942-215">**Text with icon links**</span></span><br/> <span data-ttu-id="40942-216">具有上述圖示的文字，表示其功能。</span><span class="sxs-lookup"><span data-stu-id="40942-216">text with a preceding icon that indicates its function.</span></span><br/> | <span data-ttu-id="40942-217">因為圖形提供了更多的連結視覺指示，所以更容易辨識成連結，而不是純文字連結（未加上底線）。</span><span class="sxs-lookup"><span data-stu-id="40942-217">because the graphic provides an additional visual indication of a link, it is easier to recognize as a link than a plain text link that isn't underlined.</span></span> <span data-ttu-id="40942-218">此模式通常會使用16x16 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="40942-218">this pattern typically uses a 16x16 pixel icon.</span></span><br/> ![<span data-ttu-id="40942-219">具有圖示的四個連結清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-219">screen shot of list of four links with icons</span></span> ](images/ctrl-links-image8.png)<br/> <span data-ttu-id="40942-220">在此範例中，圖示會提供連結的其他視覺指示。</span><span class="sxs-lookup"><span data-stu-id="40942-220">in this example, the icons provide an additional visual indication of a link.</span></span><br/> ![<span data-ttu-id="40942-221">使用小型三角形的 play 命令螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-221">screen shot of play command with small triangle</span></span> ](images/ctrl-links-image9.png)<br/> <span data-ttu-id="40942-222">在此範例中，標準三角形播放符號表示此文字是命令。</span><span class="sxs-lookup"><span data-stu-id="40942-222">In this example, the standard triangular Play symbol indicates that this text is a command.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="40942-223">**僅限圖形連結**</span><span class="sxs-lookup"><span data-stu-id="40942-223">**Graphics-only links**</span></span><br/> <span data-ttu-id="40942-224">只包含圖形。</span><span class="sxs-lookup"><span data-stu-id="40942-224">consist only of a graphic.</span></span><br/>                               | <span data-ttu-id="40942-225">如果缺少文字連結，則不會有連結色彩或底線來表示連結。</span><span class="sxs-lookup"><span data-stu-id="40942-225">given the lack of a text link, there is no link color or underline to indicate the link.</span></span> <span data-ttu-id="40942-226">這些連結會依據圖形設計來建議按一下，或是在圖形中建議使用者按一下時，建議採取動作的文字。</span><span class="sxs-lookup"><span data-stu-id="40942-226">these links depend on either the graphic design to suggest clicking, or text within the graphic that suggests an action when users click.</span></span> <span data-ttu-id="40942-227">僅限圖形的連結有時候會有滑鼠停留效果以表示連結。</span><span class="sxs-lookup"><span data-stu-id="40942-227">graphic-only links sometimes have a mouse over effect to indicate the link.</span></span> <span data-ttu-id="40942-228">這種方法有助於，但無法單獨透過視覺化檢查來探索。</span><span class="sxs-lookup"><span data-stu-id="40942-228">this approach helps, but isn't discoverable by visual inspection alone.</span></span><br/> <span data-ttu-id="40942-229">![具有連結的圖示螢幕擷取畫面-選取滑鼠指標 ](images/ctrl-links-image10.png)</span><span class="sxs-lookup"><span data-stu-id="40942-229">![screen shot of icon with link-select mouse pointer ](images/ctrl-links-image10.png)</span></span><br/> <span data-ttu-id="40942-230">在此範例中，不會單獨搜尋視覺檢查的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-230">In this example, the link isn't discoverable by visual inspection alone.</span></span><br/> <span data-ttu-id="40942-231">**由於其潛在的辨識和當地語系化問題，因此不建議使用僅限圖形的連結，做為執行工作的唯一方法。**</span><span class="sxs-lookup"><span data-stu-id="40942-231">**Due to their potential recognition and localization problems, graphics-only links are not recommended as the only way to perform a task.**</span></span> <br/> |



 

## <a name="guidelines"></a><span data-ttu-id="40942-232">指導方針</span><span class="sxs-lookup"><span data-stu-id="40942-232">Guidelines</span></span>

### <a name="interaction"></a><span data-ttu-id="40942-233">互動</span><span class="sxs-lookup"><span data-stu-id="40942-233">Interaction</span></span>

-   <span data-ttu-id="40942-234">**如果按一下連結的結果不是瞬間，則顯示忙碌指標。**</span><span class="sxs-lookup"><span data-stu-id="40942-234">**Display a busy pointer if the result of clicking a link isn't instantaneous.**</span></span> <span data-ttu-id="40942-235">如果沒有意見反應，使用者可能會認為按一下未發生，然後再按一次。</span><span class="sxs-lookup"><span data-stu-id="40942-235">Without feedback, users might assume that the click didn't happen and click again.</span></span>

### <a name="color"></a><span data-ttu-id="40942-236">Color</span><span class="sxs-lookup"><span data-stu-id="40942-236">Color</span></span>

-   <span data-ttu-id="40942-237">**使用主題或連結系統色彩來取得已造訪和未造訪的連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-237">**Use the theme or link system colors for visited and unvisited links.**</span></span> <span data-ttu-id="40942-238">這些色彩的意義在所有程式中都是一致的。</span><span class="sxs-lookup"><span data-stu-id="40942-238">The meaning of these colors is consistent across all programs.</span></span> <span data-ttu-id="40942-239">如果基於任何原因，使用者不喜歡這些色彩 (可能是因為) 的協助工具原因，他們可以自行變更。</span><span class="sxs-lookup"><span data-stu-id="40942-239">If for any reason users don't like these colors (perhaps for accessibility reasons), they can change them themselves.</span></span>
-   <span data-ttu-id="40942-240">**針對流覽連結，使用不同的色彩來流覽和未造訪的連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-240">**For navigation links, use different colors for visited and unvisited links.**</span></span> <span data-ttu-id="40942-241">在程式實例的持續時間內，只保留流覽過之連結的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="40942-241">Keep the history of visited links only for the duration of the program instance.</span></span> <span data-ttu-id="40942-242">流覽的色彩很重要，可指出使用者的所在位置，防止他們不慎重複地重新使用相同的頁面。</span><span class="sxs-lookup"><span data-stu-id="40942-242">The visited color is important to indicate where users have already been, preventing them from unintentionally revisiting the same pages repeatedly.</span></span>
-   <span data-ttu-id="40942-243">**針對其他類型的連結，請勿使用流覽過的連結色彩。**</span><span class="sxs-lookup"><span data-stu-id="40942-243">**For other types of links, don't use the visited link color.**</span></span> <span data-ttu-id="40942-244">例如，找不到足夠的值來識別「造訪的」命令。</span><span class="sxs-lookup"><span data-stu-id="40942-244">There isn't sufficient value in identifying "visited" commands, for example.</span></span>
-   <span data-ttu-id="40942-245">**請勿將不是連結的文字色彩，因為使用者可能會假設它是連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-245">**Don't color text that isn't a link because users may assume that it is a link.**</span></span> <span data-ttu-id="40942-246">使用粗體或灰色陰影，您也可以使用彩色文字。</span><span class="sxs-lookup"><span data-stu-id="40942-246">Use bold or a shade of gray where you'd otherwise use colored text.</span></span>
-   <span data-ttu-id="40942-247">**例外** 狀況：如果所有連結都已加上底線，或放在標準導覽或命令位置內，您可以使用彩色文字。</span><span class="sxs-lookup"><span data-stu-id="40942-247">**Exception**: You can use colored text if all links are either underlined or placed within standard navigation or command locations.</span></span>

    <span data-ttu-id="40942-248">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-248">**Incorrect:**</span></span>

    ![<span data-ttu-id="40942-249">具有藍色文字之電源計劃訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-249">screen shot of power-plan message with blue text</span></span> ](images/ctrl-links-image11.png)

    <span data-ttu-id="40942-250">在此範例中，藍色文字不正確地用於不是連結的文字。</span><span class="sxs-lookup"><span data-stu-id="40942-250">In this example, blue text is incorrectly used for text that isn't a link.</span></span>

-   <span data-ttu-id="40942-251">**使用與連結色彩對比的背景色彩。**</span><span class="sxs-lookup"><span data-stu-id="40942-251">**Use background colors that contrast with the link colors.**</span></span> <span data-ttu-id="40942-252">[視窗系統色彩](vis-color.md)一律是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="40942-252">The [window system color](vis-color.md) is always a good choice.</span></span>

    <span data-ttu-id="40942-253">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-253">**Incorrect:**</span></span>

    ![<span data-ttu-id="40942-254">藍色背景上藍色連結文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-254">screen shot of blue link text on blue background</span></span> ](images/ctrl-links-image12.png)

    <span data-ttu-id="40942-255">在此範例中，背景色彩會提供與連結色彩不佳的對比。</span><span class="sxs-lookup"><span data-stu-id="40942-255">In this example, the background color provides poor contrast with the link color.</span></span>

### <a name="underlining"></a><span data-ttu-id="40942-256">強調</span><span class="sxs-lookup"><span data-stu-id="40942-256">Underlining</span></span>

-   <span data-ttu-id="40942-257">**針對執行主要工作所需的連結，請提供視覺線索，讓使用者可以單獨辨識視覺檢查的連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-257">**For links that are necessary to perform a primary task, provide visual clues so that users can recognize links by visual inspection alone.**</span></span> <span data-ttu-id="40942-258">這些線索包括底線、圖形或專案符號，以及標準連結位置。</span><span class="sxs-lookup"><span data-stu-id="40942-258">These clues include underlining, graphics or bullets, and standard link locations.</span></span> <span data-ttu-id="40942-259">使用者不應該將滑鼠停留在物件上，或嘗試按一下它來判斷它是否為連結。</span><span class="sxs-lookup"><span data-stu-id="40942-259">Users shouldn't have to hover over an object or attempt to click on it to determine if it is a link.</span></span> <span data-ttu-id="40942-260">如果連結不清楚其內容，請使用加底線的文字。</span><span class="sxs-lookup"><span data-stu-id="40942-260">Use underlined text if the link isn't obvious from its context.</span></span>
-   <span data-ttu-id="40942-261">**請勿將不是連結的文字加上底線，因為使用者可能會假設它是連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-261">**Don't underline text that isn't a link because users may assume that it is a link.**</span></span> <span data-ttu-id="40942-262">請使用斜體，否則您會使用加底線的文字。</span><span class="sxs-lookup"><span data-stu-id="40942-262">Use italics where you'd otherwise use underlined text.</span></span> <span data-ttu-id="40942-263">只保留連結的底線。</span><span class="sxs-lookup"><span data-stu-id="40942-263">Reserve underlining only for links.</span></span>
-   <span data-ttu-id="40942-264">**列印時，請勿列印底線或連結色彩。**</span><span class="sxs-lookup"><span data-stu-id="40942-264">**When printing, don't print underlines or link colors.**</span></span> <span data-ttu-id="40942-265">列印的連結沒有任何值，而且可能會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="40942-265">Printed links have no value and are potentially confusing.</span></span>

### <a name="text-with-icon-links"></a><span data-ttu-id="40942-266">具有圖示連結的文字</span><span class="sxs-lookup"><span data-stu-id="40942-266">Text with icon links</span></span>

-   <span data-ttu-id="40942-267">**只針對命令連結使用箭號圖示。**</span><span class="sxs-lookup"><span data-stu-id="40942-267">**Use the arrow icon only for command links.**</span></span> <span data-ttu-id="40942-268">一般連結不應使用箭號圖示，除非在 Windows XP 中用來替代 [命令連結](ctrl-command-links.md) 。</span><span class="sxs-lookup"><span data-stu-id="40942-268">Regular links shouldn't use the arrow icon unless they are being used as a substitute for [command links](ctrl-command-links.md) in Windows XP.</span></span>
-   <span data-ttu-id="40942-269">**將圖示放在文字的左邊。**</span><span class="sxs-lookup"><span data-stu-id="40942-269">**Place the icon to the left of the text.**</span></span> <span data-ttu-id="40942-270">圖示需要以視覺化方式導向文字。</span><span class="sxs-lookup"><span data-stu-id="40942-270">The icon needs to lead into the text visually.</span></span>

<span data-ttu-id="40942-271">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-271">**Correct:**</span></span>

![<span data-ttu-id="40942-272">文字前面圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-272">screen shot of icon preceding text</span></span> ](images/ctrl-links-image13.png)

<span data-ttu-id="40942-273">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-273">**Incorrect:**</span></span>

![<span data-ttu-id="40942-274">下列文字圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-274">screen shot of icon following text</span></span> ](images/ctrl-links-image14.png)

<span data-ttu-id="40942-275">在不正確的範例中，圖示不會導致文字。</span><span class="sxs-lookup"><span data-stu-id="40942-275">In the incorrect example, the icon doesn't lead into the text.</span></span>

-   <span data-ttu-id="40942-276">**將按一下圖示的結果設為與按一下文字相同的結果。**</span><span class="sxs-lookup"><span data-stu-id="40942-276">**Make the result of clicking the icon the same as clicking the text.**</span></span> <span data-ttu-id="40942-277">否則會導致非預期且混淆。</span><span class="sxs-lookup"><span data-stu-id="40942-277">Doing otherwise would be unexpected and confusing.</span></span>

### <a name="graphics-only-links"></a><span data-ttu-id="40942-278">僅限圖形連結</span><span class="sxs-lookup"><span data-stu-id="40942-278">Graphics-only links</span></span>

-   <span data-ttu-id="40942-279">**請勿使用僅限圖形的連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-279">**Don't use graphics-only links.**</span></span> <span data-ttu-id="40942-280">使用者難度將其辨識為連結以及圖形內的任何文字 (用來指出按一下) 建立當地語系化問題時的動作。</span><span class="sxs-lookup"><span data-stu-id="40942-280">Users have difficultly recognizing them as links and any text within the graphic (used to indicate their action when clicked) creates a localization problem.</span></span>

### <a name="navigation-links"></a><span data-ttu-id="40942-281">導覽連結</span><span class="sxs-lookup"><span data-stu-id="40942-281">Navigation links</span></span>

-   <span data-ttu-id="40942-282">**請確定流覽連結不需要承諾用量。**</span><span class="sxs-lookup"><span data-stu-id="40942-282">**Make sure navigation links don't require commitment.**</span></span> <span data-ttu-id="40942-283">使用者應該一律能夠回到初始狀態，方法是使用 [上一頁] 進行就地流覽或 [取消] 以關閉新的視窗。</span><span class="sxs-lookup"><span data-stu-id="40942-283">Users should always be able to return to the initial state, either by using Back for inplace navigation or Cancel to close a new window.</span></span>
-   <span data-ttu-id="40942-284">**連結至特定內容，而不是一般內容。**</span><span class="sxs-lookup"><span data-stu-id="40942-284">**Link to specific content rather than general content.**</span></span> <span data-ttu-id="40942-285">例如，最好連結至檔的相關區段，而不是連結到一開始。</span><span class="sxs-lookup"><span data-stu-id="40942-285">For example, it is better to link to the relevant section of a document than to link to the beginning.</span></span>
-   <span data-ttu-id="40942-286">**只有在連結的材質相關、實用且不重複時，才使用連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-286">**Use a link only if the linked material is relevant, helpful, and not redundant.**</span></span> <span data-ttu-id="40942-287">您可以使用導覽連結中的 [使用擋板]，而不使用它們。</span><span class="sxs-lookup"><span data-stu-id="40942-287">Use restraint in navigation links don't use them just because you can.</span></span>
-   <span data-ttu-id="40942-288">**如果連結流覽至外部網站，請在 [提示] 中放入 URL，** 讓使用者可以判斷連結的目標。</span><span class="sxs-lookup"><span data-stu-id="40942-288">**If a link navigates to an external site, put the URL in the infotip** so that users can determine the target of the link.</span></span>
-   <span data-ttu-id="40942-289">**只連結第一次出現的連結文字。**</span><span class="sxs-lookup"><span data-stu-id="40942-289">**Link only the first occurrence of the link text.**</span></span> <span data-ttu-id="40942-290">多餘的連結是不必要的，而且可能會使文字難以讀取。</span><span class="sxs-lookup"><span data-stu-id="40942-290">Redundant links are unnecessary and can make text difficult to read.</span></span>

    <span data-ttu-id="40942-291">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-291">**Correct:**</span></span>

    <span data-ttu-id="40942-292">[圖片] 資料夾可讓您輕鬆分享圖片。</span><span class="sxs-lookup"><span data-stu-id="40942-292">The Pictures folder makes sharing your pictures easy.</span></span> <span data-ttu-id="40942-293">您可以使用圖片中的工作，以電子郵件傳送圖片，或在網路上的安全私人位置發佈圖片。</span><span class="sxs-lookup"><span data-stu-id="40942-293">You can use the tasks in Pictures to send your pictures in e-mail or publish them in a secure, private location on the Web.</span></span> <span data-ttu-id="40942-294">您也可以直接從 [圖片] 資料夾列印圖片。</span><span class="sxs-lookup"><span data-stu-id="40942-294">You can also print your pictures directly from the Pictures folder.</span></span>

    <span data-ttu-id="40942-295">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-295">**Incorrect:**</span></span>

    <span data-ttu-id="40942-296">[圖片] 資料夾可讓您輕鬆分享圖片。</span><span class="sxs-lookup"><span data-stu-id="40942-296">The Pictures folder makes sharing your pictures easy.</span></span> <span data-ttu-id="40942-297">您可以使用圖片中的工作，以電子郵件傳送圖片，或在網路上的安全私人位置發佈圖片。</span><span class="sxs-lookup"><span data-stu-id="40942-297">You can use the tasks in Pictures to send your pictures in e-mail or publish them in a secure, private location on the Web.</span></span> <span data-ttu-id="40942-298">您也可以直接從 [圖片] 資料夾列印圖片。</span><span class="sxs-lookup"><span data-stu-id="40942-298">You can also print your pictures directly from the Pictures folder.</span></span>

    <span data-ttu-id="40942-299">在正確的範例中，只會連結第一個出現的相關文字。</span><span class="sxs-lookup"><span data-stu-id="40942-299">In the correct example, only the first occurrence of the relevant text is linked.</span></span>

    <span data-ttu-id="40942-300">**異常：**</span><span class="sxs-lookup"><span data-stu-id="40942-300">**Exceptions:**</span></span>

    -   <span data-ttu-id="40942-301">**如果指令有連結，請將連結放在指令中。**</span><span class="sxs-lookup"><span data-stu-id="40942-301">**If an instruction has a link, put the link in the instruction.**</span></span>

        <span data-ttu-id="40942-302">使用強式密碼非常重要。</span><span class="sxs-lookup"><span data-stu-id="40942-302">Using strong passwords is very important.</span></span> <span data-ttu-id="40942-303">如需詳細資訊，請參閱＜增強式密碼＞。</span><span class="sxs-lookup"><span data-stu-id="40942-303">For more information, see Strong Passwords.</span></span>

        <span data-ttu-id="40942-304">在此範例中，連結是在指令中，而不是第一次出現。</span><span class="sxs-lookup"><span data-stu-id="40942-304">In this example, the link is in the instruction instead of the first occurrence.</span></span>

    -   <span data-ttu-id="40942-305">**如果與第一個位置相距較早的位置，則連結至之後的位置。**</span><span class="sxs-lookup"><span data-stu-id="40942-305">**Link to later occurrences if they are far away from the first.**</span></span> <span data-ttu-id="40942-306">例如，您可以在說明主題內的不同區段中，連結重複的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-306">For example, you can link redundantly in different sections within a Help topic.</span></span>

### <a name="task-links"></a><span data-ttu-id="40942-307">工作連結</span><span class="sxs-lookup"><span data-stu-id="40942-307">Task links</span></span>

-   <span data-ttu-id="40942-308">**針對不具破壞性或可輕易還原的命令使用工作連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-308">**Use task links for commands that aren't destructive or are easily reversible.**</span></span> <span data-ttu-id="40942-309">因為使用者會將連結與導覽 (以及將) 的功能建立關聯，所以連結不適合具有明顯後果的命令。</span><span class="sxs-lookup"><span data-stu-id="40942-309">Because users associate links with navigation (and the ability to back out), links aren't appropriate for commands with significant consequences.</span></span> <span data-ttu-id="40942-310">顯示對話方塊或確認的命令是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="40942-310">Commands that display a dialog box or a confirmation are a good choice.</span></span>

    <span data-ttu-id="40942-311">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-311">**Correct:**</span></span>

    <span data-ttu-id="40942-312">開始</span><span class="sxs-lookup"><span data-stu-id="40942-312">Start</span></span>

    <span data-ttu-id="40942-313">Stop</span><span class="sxs-lookup"><span data-stu-id="40942-313">Stop</span></span>

    <span data-ttu-id="40942-314">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-314">**Incorrect:**</span></span>

    <span data-ttu-id="40942-315">刪除檔案</span><span class="sxs-lookup"><span data-stu-id="40942-315">Delete file</span></span>

    <span data-ttu-id="40942-316">在不正確的範例中，命令是破壞性的。</span><span class="sxs-lookup"><span data-stu-id="40942-316">In the incorrect example, the command is destructive.</span></span>

### <a name="menu-links"></a><span data-ttu-id="40942-317">功能表連結</span><span class="sxs-lookup"><span data-stu-id="40942-317">Menu links</span></span>

-   <span data-ttu-id="40942-318">**將相關的導覽和工作連結分組到功能表中。**</span><span class="sxs-lookup"><span data-stu-id="40942-318">**Group related navigation and task links into menus.**</span></span> <span data-ttu-id="40942-319">在標準導覽或命令位置內放置相關連結的功能表，可讓您更輕鬆地尋找和瞭解連結，而不是個別放置的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-319">A menu of related links placed within a standard navigation or command location makes it easier to find and understand the links than when they're placed separately.</span></span>
-   <span data-ttu-id="40942-320">**針對選取專案相依的功能表，移除不適用的功能表連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-320">**For selection-dependent menus, remove menu links that don't apply.**</span></span> <span data-ttu-id="40942-321">請勿停用它們。</span><span class="sxs-lookup"><span data-stu-id="40942-321">Don't disable them.</span></span> <span data-ttu-id="40942-322">這樣做會消除雜亂，使用者不會錯過需要選取的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-322">Doing so eliminates clutter and users won't miss links that require selection.</span></span>
-   <span data-ttu-id="40942-323">**針對與選取無關的功能表，停用不適用的功能表連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-323">**For selection-independent menus, disable menu links that don't apply.**</span></span> <span data-ttu-id="40942-324">請勿移除它們。</span><span class="sxs-lookup"><span data-stu-id="40942-324">Don't remove them.</span></span> <span data-ttu-id="40942-325">這樣做會讓功能表變得更穩定，並讓您更容易找到這些連結。</span><span class="sxs-lookup"><span data-stu-id="40942-325">Doing so makes the menus more stable and such links easier to find.</span></span>

    ![<span data-ttu-id="40942-326">具有暗灰色功能表命令之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-326">screen shot of dialog box with dimmed menu command</span></span> ](images/ctrl-links-image15.png)

    <span data-ttu-id="40942-327">在此範例中，Windows Update 正在執行更新，所以會停用 [檢查更新] 命令，而不會移除。</span><span class="sxs-lookup"><span data-stu-id="40942-327">In this example from Windows Update, an update is being performed, so the Check for updates command is disabled rather than removed.</span></span>

### <a name="link-infotips"></a><span data-ttu-id="40942-328">連結提示</span><span class="sxs-lookup"><span data-stu-id="40942-328">Link infotips</span></span>

-   <span data-ttu-id="40942-329">如果連結需要進一步說明，請在 **個別的文字控制項或提示中提供補充說明中的說明** [，但](ctrl-tooltips-and-infotips.md)不能同時提供兩者。</span><span class="sxs-lookup"><span data-stu-id="40942-329">If a link requires further explanation, **provide the explanation in either a supplemental explanation in a separate text control or an** [infotip](ctrl-tooltips-and-infotips.md), but not both.</span></span> <span data-ttu-id="40942-330">使用完整的句子和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-330">Use complete sentences and ending punctuation.</span></span> <span data-ttu-id="40942-331">如果文字相同，就不需要提供兩者，如果文字不同，則會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="40942-331">Providing both is unnecessary if the text is the same, and confusing if the text is different.</span></span>

    ![<span data-ttu-id="40942-332">具有補充文字之連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-332">screen shot of link with supplemental text</span></span> ](images/ctrl-links-image16.png)

    <span data-ttu-id="40942-333">在此範例中，補充說明會提供連結的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="40942-333">In this example, a supplemental explanation provides further information about the link.</span></span>

    ![<span data-ttu-id="40942-334">連結提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-334">screen shot of link with infotip</span></span> ](images/ctrl-links-image17.png)

    <span data-ttu-id="40942-335">在此範例中，資訊提示會提供進一步的資訊。</span><span class="sxs-lookup"><span data-stu-id="40942-335">In this example, an infotip provides further information.</span></span>

-   <span data-ttu-id="40942-336">**請勿提供只是連結文字重述的提示。**</span><span class="sxs-lookup"><span data-stu-id="40942-336">**Don't provide an infotip that is merely a restatement of the link text.**</span></span>

    <span data-ttu-id="40942-337">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-337">**Incorrect:**</span></span>

    ![<span data-ttu-id="40942-338">具有重複提示的連結螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-338">screen shot of link with redundant infotip</span></span> ](images/ctrl-links-image18.png)

    <span data-ttu-id="40942-339">在此範例中，提示會造成使用者 repetitiveness 的風險令人困擾。</span><span class="sxs-lookup"><span data-stu-id="40942-339">In this example, the infotip risks annoying users by its repetitiveness.</span></span>

## <a name="text"></a><span data-ttu-id="40942-340">Text</span><span class="sxs-lookup"><span data-stu-id="40942-340">Text</span></span>

-   <span data-ttu-id="40942-341">請勿指派 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="40942-341">Don't assign an [access key](glossary.md).</span></span> <span data-ttu-id="40942-342">使用 Tab 鍵存取連結。</span><span class="sxs-lookup"><span data-stu-id="40942-342">Links are accessed using the Tab key.</span></span>
-   <span data-ttu-id="40942-343">**使用連結，提供有關點選連結之結果的特定描述性資訊**，視需要使用最多文字。</span><span class="sxs-lookup"><span data-stu-id="40942-343">**Use links that give specific descriptive information about the result of clicking on the link**, using as much text as necessary.</span></span> <span data-ttu-id="40942-344">連結文字應該指出按一下連結的結果。</span><span class="sxs-lookup"><span data-stu-id="40942-344">The link text should indicate the result of clicking on the link.</span></span> <span data-ttu-id="40942-345">**使用者應該能夠精確地預測連結文字的連結結果，以及選用的提示。**</span><span class="sxs-lookup"><span data-stu-id="40942-345">**Users should be able to accurately predict the result of a link from its link text and optional infotip.**</span></span>

    <span data-ttu-id="40942-346">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-346">**Incorrect:**</span></span>

    ![<span data-ttu-id="40942-347">安全性注意事項警告連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="40942-347">screen shot of a security notice warning link</span></span> ](images/ctrl-links-image19.png)

    <span data-ttu-id="40942-348">在此範例中，即使連結顯得很重要，但其標籤過於一般。</span><span class="sxs-lookup"><span data-stu-id="40942-348">In this example, even though the link appears important, its label is too general.</span></span> <span data-ttu-id="40942-349">使用者更有可能按一下更明確的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-349">Users are more likely to click a more specific link.</span></span>

-   <span data-ttu-id="40942-350">內嵌連結：</span><span class="sxs-lookup"><span data-stu-id="40942-350">For inline links:</span></span>
    -   <span data-ttu-id="40942-351">保留文字的大小寫和標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-351">Preserve the capitalization and punctuation of the text.</span></span>
    -   <span data-ttu-id="40942-352">除非文字是問題，否則請勿在連結中包含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-352">Don't include ending punctuation in the link unless the text is a question.</span></span>
    -   <span data-ttu-id="40942-353">連結文字最相關的部分，然後選擇夠大的連結文字，以便輕鬆地按一下。</span><span class="sxs-lookup"><span data-stu-id="40942-353">Link on the most relevant part of the text and choose link text that is large enough to be easy to click.</span></span>

        <span data-ttu-id="40942-354">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-354">**Correct:**</span></span>

        <span data-ttu-id="40942-355">前往新聞群組。</span><span class="sxs-lookup"><span data-stu-id="40942-355">Go to a newsgroup.</span></span>

        <span data-ttu-id="40942-356">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-356">**Incorrect:**</span></span>

        <span data-ttu-id="40942-357">前往新聞群組。</span><span class="sxs-lookup"><span data-stu-id="40942-357">Go to a newsgroup.</span></span>

        <span data-ttu-id="40942-358">在這些範例中，"Go" 不是文字中最相關的部分，而且也不夠大，無法進行良好的點擊目標，而是「新聞群組」。</span><span class="sxs-lookup"><span data-stu-id="40942-358">In these examples, "Go" isn't the most relevant part of the text and it isn't large enough to make a good click target, whereas "newsgroup" is.</span></span>

    -   <span data-ttu-id="40942-359">**避免在彼此旁放置兩個不同的內嵌連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-359">**Avoid putting two different inline links next to each other.**</span></span> <span data-ttu-id="40942-360">使用者可能會認為它們是單一連結。</span><span class="sxs-lookup"><span data-stu-id="40942-360">Users are likely to believe they are a single link.</span></span>

        <span data-ttu-id="40942-361">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-361">**Incorrect:**</span></span>

        <span data-ttu-id="40942-362">如需詳細資訊，請參閱 UX 指導方針。</span><span class="sxs-lookup"><span data-stu-id="40942-362">For more information, see UX guidelines.</span></span>

        <span data-ttu-id="40942-363">在此範例中，"UX" 和 "方針" 是兩個不同的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-363">In this example, "UX" and "guidelines" are two different links.</span></span>

-   <span data-ttu-id="40942-364">針對獨立連結 (不是內嵌) ：</span><span class="sxs-lookup"><span data-stu-id="40942-364">For independent links (not inline):</span></span>
    -   <span data-ttu-id="40942-365">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="40942-365">Use [sentence-style capitalization](glossary.md).</span></span>
    -   <span data-ttu-id="40942-366">除非連結是問題，否則請勿使用結尾標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-366">Don't use ending punctuation unless the link is a question.</span></span>
    -   <span data-ttu-id="40942-367">使用所有文字作為連結。</span><span class="sxs-lookup"><span data-stu-id="40942-367">Use all the text as the link.</span></span>
-   <span data-ttu-id="40942-368">使用與螢幕上的其他連結清楚區別的連結。</span><span class="sxs-lookup"><span data-stu-id="40942-368">Use links that are clearly differentiated from the other links on the screen.</span></span> <span data-ttu-id="40942-369">使用者應該能夠準確地預測和區分連結目標。</span><span class="sxs-lookup"><span data-stu-id="40942-369">Users should be able to accurately predict and differentiate between link targets.</span></span>

    <span data-ttu-id="40942-370">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-370">**Incorrect:**</span></span>

    <span data-ttu-id="40942-371">尋找防毒軟體</span><span class="sxs-lookup"><span data-stu-id="40942-371">Find antivirus software</span></span>

    <span data-ttu-id="40942-372">取得防毒軟體</span><span class="sxs-lookup"><span data-stu-id="40942-372">Get antivirus software</span></span>

    <span data-ttu-id="40942-373">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-373">**Correct:**</span></span>

    <span data-ttu-id="40942-374">如何知道是否已安裝防毒軟體</span><span class="sxs-lookup"><span data-stu-id="40942-374">How to know if antivirus software is installed</span></span>

    <span data-ttu-id="40942-375">安裝防毒軟體</span><span class="sxs-lookup"><span data-stu-id="40942-375">Install antivirus software</span></span>

    <span data-ttu-id="40942-376">在不正確的範例中，這兩個連結之間的差異並不清楚。</span><span class="sxs-lookup"><span data-stu-id="40942-376">In the incorrect example, the distinction between the two links is unclear.</span></span>

-   <span data-ttu-id="40942-377">不要在連結文字上按一下或按一下這裡。</span><span class="sxs-lookup"><span data-stu-id="40942-377">Don't add Click or Click here to the link text.</span></span> <span data-ttu-id="40942-378">這並不是必要的，因為連結表示按一下。</span><span class="sxs-lookup"><span data-stu-id="40942-378">It isn't necessary because a link implies clicking.</span></span> <span data-ttu-id="40942-379">此外，請按一下這裡，並在畫面讀取器讀取時，單獨傳達沒有連結的資訊。</span><span class="sxs-lookup"><span data-stu-id="40942-379">Also, Click here and here alone convey no information about the link when read by a screen reader.</span></span>

    <span data-ttu-id="40942-380">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-380">**Incorrect:**</span></span>

    <span data-ttu-id="40942-381">按一下這裡以取得說明。</span><span class="sxs-lookup"><span data-stu-id="40942-381">Click here for description.</span></span>

    <span data-ttu-id="40942-382">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-382">**Correct:**</span></span>

    <span data-ttu-id="40942-383">Description</span><span class="sxs-lookup"><span data-stu-id="40942-383">Description</span></span>

    <span data-ttu-id="40942-384">在不正確的範例中，「按一下這裡」就不需要說出，也不會傳達連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="40942-384">In the incorrect examples, "click here" goes without saying and conveys no information about the link.</span></span>

<span data-ttu-id="40942-385">**導覽連結**</span><span class="sxs-lookup"><span data-stu-id="40942-385">**Navigation links**</span></span>

-   <span data-ttu-id="40942-386">**以名詞開始連結，並清楚地描述按一下連結的位置。**</span><span class="sxs-lookup"><span data-stu-id="40942-386">**Start the link with a noun and clearly describe where clicking the link will go.**</span></span> <span data-ttu-id="40942-387">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-387">Don't use ending punctuation.</span></span> <span data-ttu-id="40942-388">有時，您可能需要使用動詞來啟動導覽連結，但不要使用會再次出現連結的動詞，例如 View、Open 或 Go 的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="40942-388">On occasion you may need to start navigation links with a verb, but don't use verbs that reiterate navigation that is already implied by the fact of linking, such as View, Open, or Go to.</span></span>
-   <span data-ttu-id="40942-389">**如果流覽至網頁，而您希望目標使用者重新叫用 URL 並將它輸入瀏覽器中，請將導覽連結顯示為 URL。**</span><span class="sxs-lookup"><span data-stu-id="40942-389">**Present a navigation link as a URL if it navigates to a Web page and you expect the target users to recall the URL and type it into a browser.**</span></span> <span data-ttu-id="40942-390">可能的話，請將這類 Url 設計成簡短且容易記住。</span><span class="sxs-lookup"><span data-stu-id="40942-390">If possible, design such URLs to be short and easy to remember.</span></span>
-   <span data-ttu-id="40942-391">**如果連結中包含的網站 URL 是以 "www" 開頭，請省略 HTTPs://通訊協定名稱並使用小寫文字。**</span><span class="sxs-lookup"><span data-stu-id="40942-391">**If the link includes a URL to a Web site starting with "www," omit the https:// protocol name and use lowercase text.**</span></span>

    <span data-ttu-id="40942-392">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-392">**Incorrect:**</span></span>

    https://www.microsoft.com

    `www.microsoft.com`

    <span data-ttu-id="40942-393">**正確：**</span><span class="sxs-lookup"><span data-stu-id="40942-393">**Correct:**</span></span>

    <span data-ttu-id="40942-394">microsoft.com</span><span class="sxs-lookup"><span data-stu-id="40942-394">microsoft.com</span></span>

    <span data-ttu-id="40942-395">在不正確的範例中，"HTTPs://" 和 "www" go 不需要說。</span><span class="sxs-lookup"><span data-stu-id="40942-395">In the incorrect examples, the "https://" and "www" go without saying.</span></span>

<span data-ttu-id="40942-396">**工作連結**</span><span class="sxs-lookup"><span data-stu-id="40942-396">**Task links**</span></span>

-   <span data-ttu-id="40942-397">**使用命令式動詞來啟動連結，並清楚地描述連結所執行的工作。**</span><span class="sxs-lookup"><span data-stu-id="40942-397">**Start the link with an imperative verb and clearly describe the task that the link performs.**</span></span> <span data-ttu-id="40942-398">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-398">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="40942-399">**如果命令需要額外的資訊，請以省略號結束連結 (包括成功完成的確認) 。**</span><span class="sxs-lookup"><span data-stu-id="40942-399">**End the link with an ellipsis if the command needs additional information (including a confirmation) for successful completion.**</span></span> <span data-ttu-id="40942-400">當工作成功完成時，請不要使用省略號。只有在需要額外資訊才能執行工作時，才會顯示另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="40942-400">Don't use an ellipsis when the successful completion of the task is to display another window only when additional information is needed to perform the task.</span></span>

    <span data-ttu-id="40942-401">列印...</span><span class="sxs-lookup"><span data-stu-id="40942-401">Print...</span></span>

    <span data-ttu-id="40942-402">在此範例中，Print .。。命令連結會顯示 [列印] 對話方塊，以收集詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="40942-402">In this example, the Print... command link displays a Print dialog box to gather more information.</span></span>

    <span data-ttu-id="40942-403">列印</span><span class="sxs-lookup"><span data-stu-id="40942-403">Print</span></span>

    <span data-ttu-id="40942-404">相反地，在此範例中，列印命令連結會將檔的單一複本列印到預設印表機，而不需要進一步的使用者互動。</span><span class="sxs-lookup"><span data-stu-id="40942-404">By contrast, in this example a Print command link prints a single copy of a document to the default printer without any further user interaction.</span></span>

    <span data-ttu-id="40942-405">**適當地使用省略號很重要，表示使用者可以在執行工作之前進行進一步的選擇，或完全取消工作**。</span><span class="sxs-lookup"><span data-stu-id="40942-405">**Proper use of ellipses is important to indicate that users can make further choices before performing the task, or can cancel the task entirely**.</span></span> <span data-ttu-id="40942-406">省略號提供的視覺提示可讓使用者探索您的軟體，而不需要擔心。</span><span class="sxs-lookup"><span data-stu-id="40942-406">The visual cue offered by an ellipsis allows users to explore your software without fear.</span></span>

-   <span data-ttu-id="40942-407">**如有必要，請結束具有 "now" 的工作連結，以區別其與導覽連結。**</span><span class="sxs-lookup"><span data-stu-id="40942-407">**If necessary, end a task link with "now" to distinguish it from a navigation link.**</span></span>

    <span data-ttu-id="40942-408">下載檔案</span><span class="sxs-lookup"><span data-stu-id="40942-408">Download files</span></span>

    <span data-ttu-id="40942-409">立即下載檔案</span><span class="sxs-lookup"><span data-stu-id="40942-409">Download files now</span></span>

    <span data-ttu-id="40942-410">在此範例中，「下載檔案」會流覽至下載檔案的頁面，而「立即下載檔案」實際上會執行命令。</span><span class="sxs-lookup"><span data-stu-id="40942-410">In this example, "Download files" navigates to a page for downloading files, whereas "Download files now" actually performs the command.</span></span>

<span data-ttu-id="40942-411">**說明連結**</span><span class="sxs-lookup"><span data-stu-id="40942-411">**Help links**</span></span>

<span data-ttu-id="40942-412">如需指導方針與範例， [請參閱說明](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="40942-412">For guidelines and examples, see [Help](winenv-help.md).</span></span>

<span data-ttu-id="40942-413">**連結提示**</span><span class="sxs-lookup"><span data-stu-id="40942-413">**Link infotips**</span></span>

-   <span data-ttu-id="40942-414">使用完整句子和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="40942-414">Use full sentences and ending punctuation.</span></span>

<span data-ttu-id="40942-415">如需詳細的指導方針與範例，請參閱 [工具提示和提示](ctrl-tooltips-and-infotips.md)。</span><span class="sxs-lookup"><span data-stu-id="40942-415">For more guidelines and examples, see [Tooltips and Infotips](ctrl-tooltips-and-infotips.md).</span></span>

## <a name="documentation"></a><span data-ttu-id="40942-416">文件</span><span class="sxs-lookup"><span data-stu-id="40942-416">Documentation</span></span>

<span data-ttu-id="40942-417">參考連結時：</span><span class="sxs-lookup"><span data-stu-id="40942-417">When referring to links:</span></span>

-   <span data-ttu-id="40942-418">使用確切的連結文字，包括其大小寫，但不包含省略號。</span><span class="sxs-lookup"><span data-stu-id="40942-418">Use the exact link text, including its capitalization, but don't include the ellipsis.</span></span>
-   <span data-ttu-id="40942-419">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="40942-419">To describe user interaction, use click.</span></span>
-   <span data-ttu-id="40942-420">可能的話，請使用粗體文字來設定連結文字的格式。</span><span class="sxs-lookup"><span data-stu-id="40942-420">When possible, format the link text using bold text.</span></span> <span data-ttu-id="40942-421">否則，請只在必要時才將連結文字放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="40942-421">Otherwise, put the link text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="40942-422">範例：若要開始掃描，請按一下 [ **掃描電腦**]。</span><span class="sxs-lookup"><span data-stu-id="40942-422">Example: To start the scan, click **Scan a computer**.</span></span>

 

