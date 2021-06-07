---
title: 連結
description: 透過連結，使用者可以流覽至另一個頁面、視窗或說明主題;顯示定義;起始命令;或選擇選項。
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 161313008612d04b5009942f82f662888d1ffd35
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524253"
---
# <a name="links"></a><span data-ttu-id="804d9-103">連結</span><span class="sxs-lookup"><span data-stu-id="804d9-103">Links</span></span>

> [!NOTE]
> <span data-ttu-id="804d9-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="804d9-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="804d9-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="804d9-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="804d9-106">透過 *連結*，使用者可以流覽至另一個頁面、視窗或說明主題;顯示定義;起始命令;或選擇選項。</span><span class="sxs-lookup"><span data-stu-id="804d9-106">With a *link*, users can navigate to another page, window, or Help topic; display a definition; initiate a command; or choose an option.</span></span> <span data-ttu-id="804d9-107">連結是文字或圖形，表示可以按一下，通常是使用流覽或未造訪的 [連結系統色彩](vis-color.md)來顯示。</span><span class="sxs-lookup"><span data-stu-id="804d9-107">A link is text or a graphic that indicates that it can be clicked, typically by being displayed using the visited or unvisited [link system colors](vis-color.md).</span></span> <span data-ttu-id="804d9-108">傳統上，連結也會加上底線，但這種方法通常不是必要的，而且不是為了減少視覺效果。</span><span class="sxs-lookup"><span data-stu-id="804d9-108">Traditionally, links are underlined as well, but that approach is often unnecessary and falling out of favor to reduce visual clutter.</span></span>

<span data-ttu-id="804d9-109">當使用者將滑鼠停留在連結上時，連結文字會顯示為加上底線的 (如果尚未) ，且指標圖形變更為 [手](inter-mouse.md)。</span><span class="sxs-lookup"><span data-stu-id="804d9-109">When users hover over a link, the link text appears as underlined (if it wasn't already) and the pointer shape changes to a [hand](inter-mouse.md).</span></span>

<span data-ttu-id="804d9-110">文字連結是最輕量的加權可點擊控制項，通常用來減少設計的視覺複雜度。</span><span class="sxs-lookup"><span data-stu-id="804d9-110">A text link is the lightest weight clickable control, and is often used to reduce the visual complexity of a design.</span></span>

> [!Note]  
> <span data-ttu-id="804d9-111">與 [命令連結](ctrl-command-links.md) 和 [版面](vis-layout.md) 配置相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="804d9-111">Guidelines related to [command links](ctrl-command-links.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="804d9-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="804d9-112">Is this the right control?</span></span>

<span data-ttu-id="804d9-113">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="804d9-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="804d9-114">**這是用來流覽至另一個頁面、視窗或說明主題的連結;顯示定義;起始命令;或選擇一個選項？**</span><span class="sxs-lookup"><span data-stu-id="804d9-114">**Is the link used to navigate to another page, window, or Help topic; display a definition; initiate a command; or choose an option?**</span></span> <span data-ttu-id="804d9-115">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="804d9-115">If not, use another control.</span></span>
-   <span data-ttu-id="804d9-116">**命令按鈕是否是較佳的選擇？**</span><span class="sxs-lookup"><span data-stu-id="804d9-116">**Would a command button be a better choice?**</span></span> <span data-ttu-id="804d9-117">如果有下列情況，請使用 [命令按鈕](ctrl-command-buttons.md) ：</span><span class="sxs-lookup"><span data-stu-id="804d9-117">Use a [command button](ctrl-command-buttons.md) if:</span></span>
    -   <span data-ttu-id="804d9-118">控制項會起始立即動作（包括顯示視窗），而該命令會與視窗的主要用途相關。</span><span class="sxs-lookup"><span data-stu-id="804d9-118">The control initiates an immediate action, including displaying a window, and that command relates to the primary purpose of the window.</span></span>
    -   <span data-ttu-id="804d9-119">即使是針對次要命令，也會顯示一個視窗，以收集輸入或進行選擇。</span><span class="sxs-lookup"><span data-stu-id="804d9-119">A window is displayed to gather input or making choices, even if for a secondary command.</span></span>
    -   <span data-ttu-id="804d9-120">標籤很短，由四個或更少的字組所組成，因此可避免冗長的長按鈕外觀。</span><span class="sxs-lookup"><span data-stu-id="804d9-120">The label is short, consisting of four or fewer words, thus avoiding the awkward appearance of long buttons.</span></span>
    -   <span data-ttu-id="804d9-121">此命令不是內嵌的。</span><span class="sxs-lookup"><span data-stu-id="804d9-121">The command is not inline.</span></span>
    -   <span data-ttu-id="804d9-122">控制項會出現在其他相關命令按鈕的群組中。</span><span class="sxs-lookup"><span data-stu-id="804d9-122">The control appears within a group of other related command buttons.</span></span>
    -   <span data-ttu-id="804d9-123">動作具有破壞性或無法復原。</span><span class="sxs-lookup"><span data-stu-id="804d9-123">The action is destructive or irreversible.</span></span> <span data-ttu-id="804d9-124">因為使用者會將連結與導覽 (以及將) 的功能建立關聯，所以連結不適合具有明顯後果的命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-124">Because users associate links with navigation (and the ability to back out), links aren't appropriate for commands with significant consequences.</span></span>
    -   <span data-ttu-id="804d9-125">同樣地，在「 [嚮導](win-wizards.md) 」或「工作 [流程](glossary.md)」中，此命令代表承諾用量。</span><span class="sxs-lookup"><span data-stu-id="804d9-125">Similarly, in a [wizard](win-wizards.md) or [task flow](glossary.md), the command represents commitment.</span></span> <span data-ttu-id="804d9-126">在這類視窗中，命令按鈕會建議承諾，而連結建議您流覽至下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="804d9-126">In such windows, command buttons suggest commitment whereas links suggest navigating to the next step.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="804d9-127">設計概念</span><span class="sxs-lookup"><span data-stu-id="804d9-127">Design concepts</span></span>

<span data-ttu-id="804d9-128">**讓連結可辨識**</span><span class="sxs-lookup"><span data-stu-id="804d9-128">**Making links recognizable**</span></span>

<span data-ttu-id="804d9-129">連結缺乏 [affordance](glossary.md)，這表示 **其視覺屬性不建議其使用方式** ，而且只能透過經驗理解。</span><span class="sxs-lookup"><span data-stu-id="804d9-129">Links lack [affordance](glossary.md), which means **their visual properties don't suggest how they are used** and are understood only through experience.</span></span> <span data-ttu-id="804d9-130">沒有底線和連結系統色彩的連結會顯示為一般文字;確定其行為的唯一方法是從其呈現方式、其內容，或將指標放在其上。</span><span class="sxs-lookup"><span data-stu-id="804d9-130">Links without an underline and link system colors appear as normal text; the only way to ascertain their behavior is from their presentation, their context, or by positioning the pointer over them.</span></span>

<span data-ttu-id="804d9-131">令人驚訝的是，這種缺乏 affordance 的動機通常是使用連結的動機，因為它們顯得很輕量，因此降低了設計的視覺複雜度。</span><span class="sxs-lookup"><span data-stu-id="804d9-131">Surprisingly, this lack of affordance is often a motivation for using links because they appear so lightweight, thereby reducing the visual complexity of a design.</span></span> <span data-ttu-id="804d9-132">連結會消除由其他控制項使用的 [命令按鈕](ctrl-command-buttons.md) 和框線所使用的視覺效果繁重框架。</span><span class="sxs-lookup"><span data-stu-id="804d9-132">Links eliminate the visually heavy frame used by [command buttons](ctrl-command-buttons.md) and border used by other controls.</span></span> <span data-ttu-id="804d9-133">例如，雖然您可能會使用命令按鈕讓主要命令變得很明顯，但您可以選擇次要命令的連結來將它們反加重。</span><span class="sxs-lookup"><span data-stu-id="804d9-133">For example, while you might use command buttons to make primary commands obvious, you might choose links for secondary commands to de-emphasize them.</span></span>

<span data-ttu-id="804d9-134">然後挑戰是要保留足夠的視覺線索，讓使用者可以辨識這些連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-134">The challenge is then to keep enough visual clues so users can recognize the links.</span></span> <span data-ttu-id="804d9-135">基本的指導方針是， **使用者必須能夠透過視覺化檢查來辨識連結，他們不應將其暫留在物件上，或按一下以判斷它是否為連結**。</span><span class="sxs-lookup"><span data-stu-id="804d9-135">The fundamental guideline is **users must be able to recognize links by visual inspection alone they shouldn't have to hover over an object or click it to determine if it is a link**.</span></span>

<span data-ttu-id="804d9-136">如果連結使用 [連結系統色彩](vis-color.md) 和至少一個下列的視覺線索，則使用者可以單獨辨識視覺檢查的連結：</span><span class="sxs-lookup"><span data-stu-id="804d9-136">Users can recognize a link by visual inspection alone if the link uses the [link system colors](vis-color.md) and at least one of the following visual clues:</span></span>

-   <span data-ttu-id="804d9-137">加上底線的文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-137">Underlined text.</span></span>
-   <span data-ttu-id="804d9-138">圖形或專案符號，例如具有 [圖示連結](#usage-patterns) 模式的文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-138">A graphic or bullet, such as with the [text with icon link](#usage-patterns) pattern.</span></span>
-   <span data-ttu-id="804d9-139">在標準導覽、選項或命令位置內放置，例如視窗的 [內容區域](glossary.md) ，或是在巡覽列、功能表列、工具列或頁尾中。</span><span class="sxs-lookup"><span data-stu-id="804d9-139">Placement within a standard navigation, option, or command location, such as the [content area](glossary.md) of a window, or in a navigation bar, menu bar, toolbar, or page footer.</span></span>

<span data-ttu-id="804d9-140">使用者也可以使用下列視覺線索來辨識視覺化檢查的連結，但這些線索本身並不足夠：</span><span class="sxs-lookup"><span data-stu-id="804d9-140">Users can also recognize a link by visual inspection with the following visual clues, but these clues aren't sufficient by themselves:</span></span>

-   <span data-ttu-id="804d9-141">建議按一下的文字，例如顯示、列印、複製或刪除等命令式動詞命令開始的命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-141">Text that suggests clicking, such as a command starting with an imperative verb like Show, Print, Copy, or Delete.</span></span>
-   <span data-ttu-id="804d9-142">在一般文字區塊內放置。</span><span class="sxs-lookup"><span data-stu-id="804d9-142">Placement within a block of normal text.</span></span>

<span data-ttu-id="804d9-143">當然，使用者隨時都可以透過滑鼠停留或按一下的方式來判斷連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-143">Of course, users can always determine a link through interaction either hovering or clicking.</span></span> <span data-ttu-id="804d9-144">如果任何重要工作都不需要探索連結，您可以消除這類連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-144">If discovery of a link isn't required for any significant tasks, you can de-emphasize such links.</span></span>

![<span data-ttu-id="804d9-145">黑色背景上灰色標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-145">screen shot of gray labels on black background</span></span> ](images/ctrl-links-image1.png)

<span data-ttu-id="804d9-146">在此範例中，請洽詢美國、使用條款、商標和隱私權聲明。</span><span class="sxs-lookup"><span data-stu-id="804d9-146">In this example, Contact Us, Terms of Use, Trademarks, and Privacy Statement are links.</span></span> <span data-ttu-id="804d9-147">因為任何重要的工作都不需要它們，所以會刻意將它們取消強調。</span><span class="sxs-lookup"><span data-stu-id="804d9-147">They are intentionally de-emphasized because they aren't required for any important tasks.</span></span> <span data-ttu-id="804d9-148">唯一的線索是連結滑鼠指標，並放在視窗底部的標準導覽區域中，以顯示滑鼠指標。</span><span class="sxs-lookup"><span data-stu-id="804d9-148">The only clues that they are links are that they have a mouse pointer on hover and are positioned in a standard navigation area at the bottom of the window.</span></span>

<span data-ttu-id="804d9-149">**建立特定、相關且可預測的連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-149">**Making links specific, relevant, and predictable**</span></span>

<span data-ttu-id="804d9-150">連結文字應該指出按一下連結的結果。</span><span class="sxs-lookup"><span data-stu-id="804d9-150">Link text should indicate the result of clicking on the link.</span></span>

<span data-ttu-id="804d9-151">特定連結比一般連結更吸引使用者，所以請 **使用連結標籤，提供有關按一下連結之結果的特定描述性資訊**。</span><span class="sxs-lookup"><span data-stu-id="804d9-151">Specific links are more compelling to users than general links, so **use link labels that give specific descriptive information about the result of clicking on the link**.</span></span> <span data-ttu-id="804d9-152">不過，請確定您的連結文字不太明確，因為它會誤導並防止適當的使用。</span><span class="sxs-lookup"><span data-stu-id="804d9-152">However, make sure that your link text isn't so specific that it is misleading and discourages proper use.</span></span>

<span data-ttu-id="804d9-153">精簡的連結可能會比詳細資訊連結更容易讀取。</span><span class="sxs-lookup"><span data-stu-id="804d9-153">Concise links are more likely to be read than verbose links.</span></span> <span data-ttu-id="804d9-154">**消除不必要的文字和詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="804d9-154">**Eliminate unnecessary text and detail.**</span></span> <span data-ttu-id="804d9-155">連結標籤不需要完整的。</span><span class="sxs-lookup"><span data-stu-id="804d9-155">Link labels don't have to be comprehensive.</span></span>

<span data-ttu-id="804d9-156">若要評估您的連結文字：</span><span class="sxs-lookup"><span data-stu-id="804d9-156">To evaluate your link text:</span></span>

-   <span data-ttu-id="804d9-157">請確定連結文字反映連結所支援的案例。</span><span class="sxs-lookup"><span data-stu-id="804d9-157">Make sure the link text reflects the scenarios that the link supports.</span></span>
-   <span data-ttu-id="804d9-158">請確定連結的結果是可預測的。</span><span class="sxs-lookup"><span data-stu-id="804d9-158">Make sure the results of the link are predictable.</span></span> <span data-ttu-id="804d9-159">結果不應驚訝的使用者。</span><span class="sxs-lookup"><span data-stu-id="804d9-159">Users shouldn't be surprised by the results.</span></span>

<span data-ttu-id="804d9-160">**如果您只進行兩件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="804d9-160">**If you do only two things...**</span></span>

1. <span data-ttu-id="804d9-161">讓視覺檢查單獨找到連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-161">Make links discoverable by visual inspection alone.</span></span> <span data-ttu-id="804d9-162">使用者不需要與您的程式互動，即可找到連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-162">Users shouldn't have to interact with your program to find links.</span></span>

2. <span data-ttu-id="804d9-163">使用連結，提供有關點選連結之結果的特定描述性資訊，視需要使用最多文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-163">Use links that give specific descriptive information about the result of clicking on the link, using as much text as necessary.</span></span> <span data-ttu-id="804d9-164">使用者應該能夠精確地預測連結文字的連結結果， [以及選用的](ctrl-tooltips-and-infotips.md)提示。</span><span class="sxs-lookup"><span data-stu-id="804d9-164">Users should be able to accurately predict the result of a link from its link text and optional [infotip](ctrl-tooltips-and-infotips.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="804d9-165">使用模式</span><span class="sxs-lookup"><span data-stu-id="804d9-165">Usage patterns</span></span>

<span data-ttu-id="804d9-166">連結有數種功能模式：</span><span class="sxs-lookup"><span data-stu-id="804d9-166">Links have several functional patterns:</span></span>



|    <span data-ttu-id="804d9-167">使用狀況</span><span class="sxs-lookup"><span data-stu-id="804d9-167">Usage</span></span>                  |    <span data-ttu-id="804d9-168">範例</span><span class="sxs-lookup"><span data-stu-id="804d9-168">Example</span></span>   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804d9-169">**導覽連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-169">**Navigation links**</span></span><br/> <span data-ttu-id="804d9-170">用來流覽至另一個頁面或視窗的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-170">A link used to navigate to another page or window.</span></span> <br/>                                                      | <span data-ttu-id="804d9-171">當您在瀏覽器視窗或嚮導中，按一下連結會流覽至另一個頁面;或顯示新的視窗。</span><span class="sxs-lookup"><span data-stu-id="804d9-171">Clicking the link navigates inplace to another page, as in a browser window or wizard; or displays a new window.</span></span> <span data-ttu-id="804d9-172">相較于工作連結，流覽不會起始工作，而是直接流覽至另一個位置或繼續進行中的工作。</span><span class="sxs-lookup"><span data-stu-id="804d9-172">In contrast to task links, the navigation doesn't initiate a task but simply navigates to another place or proceeds with a task already in progress.</span></span> <span data-ttu-id="804d9-173">由於使用者隨時都可以返回，因此導覽暗示了安全性。</span><span class="sxs-lookup"><span data-stu-id="804d9-173">Navigation implies safety because the user can always go back.</span></span><br/> <span data-ttu-id="804d9-174">新聞頭條新聞</span><span class="sxs-lookup"><span data-stu-id="804d9-174">News headlines</span></span><br/> <span data-ttu-id="804d9-175">在此範例中，按一下連結會流覽至 [新聞頭條新聞] 頁面。</span><span class="sxs-lookup"><span data-stu-id="804d9-175">In this example, clicking the link navigates to the News headlines page.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="804d9-176">**工作連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-176">**Task links**</span></span><br/> <span data-ttu-id="804d9-177">用來起始新命令的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-177">A link used to initiate a new command.</span></span> <br/>                                                                        | <span data-ttu-id="804d9-178">按一下連結可立即執行命令，或顯示對話方塊或頁面來收集更多輸入。</span><span class="sxs-lookup"><span data-stu-id="804d9-178">Clicking the link either performs a command immediately, or displays a dialog box or page to gather more input.</span></span> <span data-ttu-id="804d9-179">相對於導覽連結，工作連結會起始新的工作，而不是繼續進行現有的工作。</span><span class="sxs-lookup"><span data-stu-id="804d9-179">In contrast to navigation links, task links initiate a new task instead of continuing with an existing task.</span></span> <span data-ttu-id="804d9-180">工作不表示 safetyusers 無法使用 Back 命令還原為先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="804d9-180">Tasks don't imply safetyusers can't revert to the previous state with a Back command.</span></span> <span data-ttu-id="804d9-181">系統會呼叫工作連結，以防止與 [命令連結](ctrl-command-links.md)混淆。</span><span class="sxs-lookup"><span data-stu-id="804d9-181">Task links are so called to prevent confusion with [command links](ctrl-command-links.md).</span></span> <br/> <span data-ttu-id="804d9-182">登入</span><span class="sxs-lookup"><span data-stu-id="804d9-182">Login</span></span><br/> <span data-ttu-id="804d9-183">在此範例中，按一下連結會起始登入命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-183">In this example, clicking the link initiates a login command.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="804d9-184">**說明連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-184">**Help links**</span></span><br/> <span data-ttu-id="804d9-185">用來顯示說明主題的文字連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-185">A text link used to display a Help topic.</span></span> <br/>                                                                     | <span data-ttu-id="804d9-186">按一下該連結會在另一個視窗中顯示說明文章。</span><span class="sxs-lookup"><span data-stu-id="804d9-186">Clicking the link displays a Help article in a separate window.</span></span><br/> <span data-ttu-id="804d9-187">什麼是強式密碼？</span><span class="sxs-lookup"><span data-stu-id="804d9-187">What is a strong password?</span></span><br/> <span data-ttu-id="804d9-188">在此範例中，按一下連結會顯示具有指定主題的說明視窗。</span><span class="sxs-lookup"><span data-stu-id="804d9-188">In this example, clicking the link displays a Help window with the given topic.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="804d9-189">**定義連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-189">**Definition links**</span></span><br/> <span data-ttu-id="804d9-190">當使用者按一下或停留在連結上時，用來顯示資訊提示中定義的文字連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-190">a text link used to display a definition in an infotip when the user clicks on or hovers over the link.</span></span> <br/> | <span data-ttu-id="804d9-191">此模式適用于定義您的使用者可能不知道的詞彙，而不會增加螢幕雜亂。</span><span class="sxs-lookup"><span data-stu-id="804d9-191">this pattern is useful for defining terms that may not be known to your users without adding screen clutter.</span></span><br/> ![<span data-ttu-id="804d9-192">滑鼠停留時顯示的提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-192">screen shot of infotip displayed by mouse hover</span></span> ](images/ctrl-links-image2.png)<br/> <span data-ttu-id="804d9-193">在此範例中，會顯示 [提示] 定義。</span><span class="sxs-lookup"><span data-stu-id="804d9-193">In this example, the infotip definition is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="804d9-194">**功能表連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-194">**Menu links**</span></span><br/> <span data-ttu-id="804d9-195">一組用來建立功能表的工作連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-195">a set of task links used to create a menu.</span></span> <br/>                                                                    | <span data-ttu-id="804d9-196">因為功能表的內容會指出一組連結，所以文字通常不會加上底線， (除了停留) 之外，可能不會使用連結系統色彩。</span><span class="sxs-lookup"><span data-stu-id="804d9-196">because the context of the menu indicates a set of links, the text is usually not underlined (except on hover) and might not use the link system colors.</span></span><br/> ![<span data-ttu-id="804d9-197">一組連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-197">screen shot of a set of links</span></span> ](images/ctrl-links-image3.png)<br/> <span data-ttu-id="804d9-198">在此範例中，一組連結會建立功能表。</span><span class="sxs-lookup"><span data-stu-id="804d9-198">In this example, a set of links creates a menu.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="804d9-199">**選項連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-199">**Option links**</span></span><br/> <span data-ttu-id="804d9-200">選取的選項或其預留位置，其中按一下連結會叫用命令來變更該選項。</span><span class="sxs-lookup"><span data-stu-id="804d9-200">a selected option or its placeholder, where clicking the link invokes a command to change that option.</span></span><br/>       | <span data-ttu-id="804d9-201">不同于一般文字連結，此連結會變更其文字，以反映目前選取的選項，而且一律會使用未連結的連結色彩來繪製。</span><span class="sxs-lookup"><span data-stu-id="804d9-201">unlike regular text links, the link changes its text to reflect the currently selected option and is always drawn using the unvisited link color.</span></span> <br/> ![<span data-ttu-id="804d9-202">outlook 規則 wizard 中的規則螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-202">screen shot of a rule in outlook rules wizard</span></span> ](images/ctrl-links-image4.png)<br/> <span data-ttu-id="804d9-203">左邊的範例會顯示 [microsoft outlook 規則] 嚮導中包含預留位置選項的規則。</span><span class="sxs-lookup"><span data-stu-id="804d9-203">the example on the left shows a rule from the microsoft outlook rules wizard with placeholder options.</span></span> <span data-ttu-id="804d9-204">當使用者按一下連結並選取某些選項之後，右邊的範例會更新連結文字以顯示結果。</span><span class="sxs-lookup"><span data-stu-id="804d9-204">after users click the links and select some options, the right-hand example updates the link text to show the results.</span></span><br/> <span data-ttu-id="804d9-205">如果選項具有變數格式，則使用選項連結特別適用。</span><span class="sxs-lookup"><span data-stu-id="804d9-205">using option links is particularly suitable if the options have a variable format.</span></span> <br/> ![<span data-ttu-id="804d9-206">規則嚮導中已修改規則的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-206">screen shot of a modified rule in the rules wizard</span></span> ](images/ctrl-links-image5.png)<br/> <span data-ttu-id="804d9-207">右側的範例顯示 outlook 規則具有變數格式。</span><span class="sxs-lookup"><span data-stu-id="804d9-207">the example on the right shows that outlook rules have a variable format.</span></span> <br/> ![<span data-ttu-id="804d9-208">文字變更為下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-208">screen shot of how text changes to drop-down list</span></span> ](images/ctrl-links-image6.png)<br/> <span data-ttu-id="804d9-209">左邊的範例顯示選項連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-209">The example on the left shows an option link.</span></span> <span data-ttu-id="804d9-210">當選取時，它會變成下拉式清單，如右側所示。</span><span class="sxs-lookup"><span data-stu-id="804d9-210">It becomes a drop-down list when selected, as shown on the right.</span></span><br/> |



 

<span data-ttu-id="804d9-211">連結也有數種展示模式：</span><span class="sxs-lookup"><span data-stu-id="804d9-211">Links also have several presentation patterns:</span></span>



|    <span data-ttu-id="804d9-212">使用狀況</span><span class="sxs-lookup"><span data-stu-id="804d9-212">Usage</span></span>                                 |    <span data-ttu-id="804d9-213">範例</span><span class="sxs-lookup"><span data-stu-id="804d9-213">Example</span></span>                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804d9-214">**純文字連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-214">**Plain text links**</span></span><br/> <span data-ttu-id="804d9-215">只包含文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-215">consist only of text.</span></span> <br/>                                      | <span data-ttu-id="804d9-216">這份簡報最有彈性，因為它可以在任何地方使用，包括 [內嵌](glossary.md)在內。</span><span class="sxs-lookup"><span data-stu-id="804d9-216">this presentation is the most flexible because it can be used anywhere, including [inline](glossary.md).</span></span><br/> <span data-ttu-id="804d9-217">![藍色連結文字的螢幕擷取畫面 ](images/ctrl-links-image7.png)</span><span class="sxs-lookup"><span data-stu-id="804d9-217">![screen shot of blue link text ](images/ctrl-links-image7.png)</span></span><br/> <span data-ttu-id="804d9-218">在此範例中，文字色彩清楚地識別內嵌連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-218">In this example, the text color clearly identifies an inline link.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="804d9-219">**具有圖示連結的文字**</span><span class="sxs-lookup"><span data-stu-id="804d9-219">**Text with icon links**</span></span><br/> <span data-ttu-id="804d9-220">具有上述圖示的文字，表示其功能。</span><span class="sxs-lookup"><span data-stu-id="804d9-220">text with a preceding icon that indicates its function.</span></span><br/> | <span data-ttu-id="804d9-221">因為圖形提供了更多的連結視覺指示，所以更容易辨識成連結，而不是純文字連結（未加上底線）。</span><span class="sxs-lookup"><span data-stu-id="804d9-221">because the graphic provides an additional visual indication of a link, it is easier to recognize as a link than a plain text link that isn't underlined.</span></span> <span data-ttu-id="804d9-222">此模式通常會使用16x16 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="804d9-222">this pattern typically uses a 16x16 pixel icon.</span></span><br/> ![<span data-ttu-id="804d9-223">具有圖示的四個連結清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-223">screen shot of list of four links with icons</span></span> ](images/ctrl-links-image8.png)<br/> <span data-ttu-id="804d9-224">在此範例中，圖示會提供連結的其他視覺指示。</span><span class="sxs-lookup"><span data-stu-id="804d9-224">in this example, the icons provide an additional visual indication of a link.</span></span><br/> ![<span data-ttu-id="804d9-225">使用小型三角形的 play 命令螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-225">screen shot of play command with small triangle</span></span> ](images/ctrl-links-image9.png)<br/> <span data-ttu-id="804d9-226">在此範例中，標準三角形播放符號表示此文字是命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-226">In this example, the standard triangular Play symbol indicates that this text is a command.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="804d9-227">**僅限圖形連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-227">**Graphics-only links**</span></span><br/> <span data-ttu-id="804d9-228">只包含圖形。</span><span class="sxs-lookup"><span data-stu-id="804d9-228">consist only of a graphic.</span></span><br/>                               | <span data-ttu-id="804d9-229">如果缺少文字連結，則不會有連結色彩或底線來表示連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-229">given the lack of a text link, there is no link color or underline to indicate the link.</span></span> <span data-ttu-id="804d9-230">這些連結會依據圖形設計來建議按一下，或是在圖形中建議使用者按一下時，建議採取動作的文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-230">these links depend on either the graphic design to suggest clicking, or text within the graphic that suggests an action when users click.</span></span> <span data-ttu-id="804d9-231">僅限圖形的連結有時候會有滑鼠停留效果以表示連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-231">graphic-only links sometimes have a mouse over effect to indicate the link.</span></span> <span data-ttu-id="804d9-232">這種方法有助於，但無法單獨透過視覺化檢查來探索。</span><span class="sxs-lookup"><span data-stu-id="804d9-232">this approach helps, but isn't discoverable by visual inspection alone.</span></span><br/> <span data-ttu-id="804d9-233">![具有連結的圖示螢幕擷取畫面-選取滑鼠指標 ](images/ctrl-links-image10.png)</span><span class="sxs-lookup"><span data-stu-id="804d9-233">![screen shot of icon with link-select mouse pointer ](images/ctrl-links-image10.png)</span></span><br/> <span data-ttu-id="804d9-234">在此範例中，不會單獨搜尋視覺檢查的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-234">In this example, the link isn't discoverable by visual inspection alone.</span></span><br/> <span data-ttu-id="804d9-235">**由於其潛在的辨識和當地語系化問題，因此不建議使用僅限圖形的連結，做為執行工作的唯一方法。**</span><span class="sxs-lookup"><span data-stu-id="804d9-235">**Due to their potential recognition and localization problems, graphics-only links are not recommended as the only way to perform a task.**</span></span> <br/> |



 

## <a name="guidelines"></a><span data-ttu-id="804d9-236">指導方針</span><span class="sxs-lookup"><span data-stu-id="804d9-236">Guidelines</span></span>

### <a name="interaction"></a><span data-ttu-id="804d9-237">互動</span><span class="sxs-lookup"><span data-stu-id="804d9-237">Interaction</span></span>

-   <span data-ttu-id="804d9-238">**如果按一下連結的結果不是瞬間，則顯示忙碌指標。**</span><span class="sxs-lookup"><span data-stu-id="804d9-238">**Display a busy pointer if the result of clicking a link isn't instantaneous.**</span></span> <span data-ttu-id="804d9-239">如果沒有意見反應，使用者可能會認為按一下未發生，然後再按一次。</span><span class="sxs-lookup"><span data-stu-id="804d9-239">Without feedback, users might assume that the click didn't happen and click again.</span></span>

### <a name="color"></a><span data-ttu-id="804d9-240">Color</span><span class="sxs-lookup"><span data-stu-id="804d9-240">Color</span></span>

-   <span data-ttu-id="804d9-241">**使用主題或連結系統色彩來取得已造訪和未造訪的連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-241">**Use the theme or link system colors for visited and unvisited links.**</span></span> <span data-ttu-id="804d9-242">這些色彩的意義在所有程式中都是一致的。</span><span class="sxs-lookup"><span data-stu-id="804d9-242">The meaning of these colors is consistent across all programs.</span></span> <span data-ttu-id="804d9-243">如果基於任何原因，使用者不喜歡這些色彩 (可能是因為) 的協助工具原因，他們可以自行變更。</span><span class="sxs-lookup"><span data-stu-id="804d9-243">If for any reason users don't like these colors (perhaps for accessibility reasons), they can change them themselves.</span></span>
-   <span data-ttu-id="804d9-244">**針對流覽連結，使用不同的色彩來流覽和未造訪的連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-244">**For navigation links, use different colors for visited and unvisited links.**</span></span> <span data-ttu-id="804d9-245">在程式實例的持續時間內，只保留流覽過之連結的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="804d9-245">Keep the history of visited links only for the duration of the program instance.</span></span> <span data-ttu-id="804d9-246">流覽的色彩很重要，可指出使用者的所在位置，防止他們不慎重複地重新使用相同的頁面。</span><span class="sxs-lookup"><span data-stu-id="804d9-246">The visited color is important to indicate where users have already been, preventing them from unintentionally revisiting the same pages repeatedly.</span></span>
-   <span data-ttu-id="804d9-247">**針對其他類型的連結，請勿使用流覽過的連結色彩。**</span><span class="sxs-lookup"><span data-stu-id="804d9-247">**For other types of links, don't use the visited link color.**</span></span> <span data-ttu-id="804d9-248">例如，找不到足夠的值來識別「造訪的」命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-248">There isn't sufficient value in identifying "visited" commands, for example.</span></span>
-   <span data-ttu-id="804d9-249">**請勿將不是連結的文字色彩，因為使用者可能會假設它是連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-249">**Don't color text that isn't a link because users may assume that it is a link.**</span></span> <span data-ttu-id="804d9-250">使用粗體或灰色陰影，您也可以使用彩色文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-250">Use bold or a shade of gray where you'd otherwise use colored text.</span></span>
-   <span data-ttu-id="804d9-251">**例外** 狀況：如果所有連結都已加上底線，或放在標準導覽或命令位置內，您可以使用彩色文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-251">**Exception**: You can use colored text if all links are either underlined or placed within standard navigation or command locations.</span></span>

    <span data-ttu-id="804d9-252">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-252">**Incorrect:**</span></span>

    ![<span data-ttu-id="804d9-253">具有藍色文字之電源計劃訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-253">screen shot of power-plan message with blue text</span></span> ](images/ctrl-links-image11.png)

    <span data-ttu-id="804d9-254">在此範例中，藍色文字不正確地用於不是連結的文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-254">In this example, blue text is incorrectly used for text that isn't a link.</span></span>

-   <span data-ttu-id="804d9-255">**使用與連結色彩對比的背景色彩。**</span><span class="sxs-lookup"><span data-stu-id="804d9-255">**Use background colors that contrast with the link colors.**</span></span> <span data-ttu-id="804d9-256">[視窗系統色彩](vis-color.md)一律是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="804d9-256">The [window system color](vis-color.md) is always a good choice.</span></span>

    <span data-ttu-id="804d9-257">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-257">**Incorrect:**</span></span>

    ![<span data-ttu-id="804d9-258">藍色背景上藍色連結文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-258">screen shot of blue link text on blue background</span></span> ](images/ctrl-links-image12.png)

    <span data-ttu-id="804d9-259">在此範例中，背景色彩會提供與連結色彩不佳的對比。</span><span class="sxs-lookup"><span data-stu-id="804d9-259">In this example, the background color provides poor contrast with the link color.</span></span>

### <a name="underlining"></a><span data-ttu-id="804d9-260">強調</span><span class="sxs-lookup"><span data-stu-id="804d9-260">Underlining</span></span>

-   <span data-ttu-id="804d9-261">**針對執行主要工作所需的連結，請提供視覺線索，讓使用者可以單獨辨識視覺檢查的連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-261">**For links that are necessary to perform a primary task, provide visual clues so that users can recognize links by visual inspection alone.**</span></span> <span data-ttu-id="804d9-262">這些線索包括底線、圖形或專案符號，以及標準連結位置。</span><span class="sxs-lookup"><span data-stu-id="804d9-262">These clues include underlining, graphics or bullets, and standard link locations.</span></span> <span data-ttu-id="804d9-263">使用者不應該將滑鼠停留在物件上，或嘗試按一下它來判斷它是否為連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-263">Users shouldn't have to hover over an object or attempt to click on it to determine if it is a link.</span></span> <span data-ttu-id="804d9-264">如果連結不清楚其內容，請使用加底線的文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-264">Use underlined text if the link isn't obvious from its context.</span></span>
-   <span data-ttu-id="804d9-265">**請勿將不是連結的文字加上底線，因為使用者可能會假設它是連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-265">**Don't underline text that isn't a link because users may assume that it is a link.**</span></span> <span data-ttu-id="804d9-266">請使用斜體，否則您會使用加底線的文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-266">Use italics where you'd otherwise use underlined text.</span></span> <span data-ttu-id="804d9-267">只保留連結的底線。</span><span class="sxs-lookup"><span data-stu-id="804d9-267">Reserve underlining only for links.</span></span>
-   <span data-ttu-id="804d9-268">**列印時，請勿列印底線或連結色彩。**</span><span class="sxs-lookup"><span data-stu-id="804d9-268">**When printing, don't print underlines or link colors.**</span></span> <span data-ttu-id="804d9-269">列印的連結沒有任何值，而且可能會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="804d9-269">Printed links have no value and are potentially confusing.</span></span>

### <a name="text-with-icon-links"></a><span data-ttu-id="804d9-270">具有圖示連結的文字</span><span class="sxs-lookup"><span data-stu-id="804d9-270">Text with icon links</span></span>

-   <span data-ttu-id="804d9-271">**只針對命令連結使用箭號圖示。**</span><span class="sxs-lookup"><span data-stu-id="804d9-271">**Use the arrow icon only for command links.**</span></span> <span data-ttu-id="804d9-272">一般連結不應使用箭號圖示，除非在 Windows XP 中用來替代 [命令連結](ctrl-command-links.md) 。</span><span class="sxs-lookup"><span data-stu-id="804d9-272">Regular links shouldn't use the arrow icon unless they are being used as a substitute for [command links](ctrl-command-links.md) in Windows XP.</span></span>
-   <span data-ttu-id="804d9-273">**將圖示放在文字的左邊。**</span><span class="sxs-lookup"><span data-stu-id="804d9-273">**Place the icon to the left of the text.**</span></span> <span data-ttu-id="804d9-274">圖示需要以視覺化方式導向文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-274">The icon needs to lead into the text visually.</span></span>

<span data-ttu-id="804d9-275">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-275">**Correct:**</span></span>

![<span data-ttu-id="804d9-276">文字前面圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-276">screen shot of icon preceding text</span></span> ](images/ctrl-links-image13.png)

<span data-ttu-id="804d9-277">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-277">**Incorrect:**</span></span>

![<span data-ttu-id="804d9-278">下列文字圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-278">screen shot of icon following text</span></span> ](images/ctrl-links-image14.png)

<span data-ttu-id="804d9-279">在不正確的範例中，圖示不會導致文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-279">In the incorrect example, the icon doesn't lead into the text.</span></span>

-   <span data-ttu-id="804d9-280">**將按一下圖示的結果設為與按一下文字相同的結果。**</span><span class="sxs-lookup"><span data-stu-id="804d9-280">**Make the result of clicking the icon the same as clicking the text.**</span></span> <span data-ttu-id="804d9-281">否則會導致非預期且混淆。</span><span class="sxs-lookup"><span data-stu-id="804d9-281">Doing otherwise would be unexpected and confusing.</span></span>

### <a name="graphics-only-links"></a><span data-ttu-id="804d9-282">僅限圖形連結</span><span class="sxs-lookup"><span data-stu-id="804d9-282">Graphics-only links</span></span>

-   <span data-ttu-id="804d9-283">**請勿使用僅限圖形的連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-283">**Don't use graphics-only links.**</span></span> <span data-ttu-id="804d9-284">使用者難度將其辨識為連結以及圖形內的任何文字 (用來指出按一下) 建立當地語系化問題時的動作。</span><span class="sxs-lookup"><span data-stu-id="804d9-284">Users have difficultly recognizing them as links and any text within the graphic (used to indicate their action when clicked) creates a localization problem.</span></span>

### <a name="navigation-links"></a><span data-ttu-id="804d9-285">導覽連結</span><span class="sxs-lookup"><span data-stu-id="804d9-285">Navigation links</span></span>

-   <span data-ttu-id="804d9-286">**請確定流覽連結不需要承諾用量。**</span><span class="sxs-lookup"><span data-stu-id="804d9-286">**Make sure navigation links don't require commitment.**</span></span> <span data-ttu-id="804d9-287">使用者應該一律能夠回到初始狀態，方法是使用 [上一頁] 進行就地流覽或 [取消] 以關閉新的視窗。</span><span class="sxs-lookup"><span data-stu-id="804d9-287">Users should always be able to return to the initial state, either by using Back for inplace navigation or Cancel to close a new window.</span></span>
-   <span data-ttu-id="804d9-288">**連結至特定內容，而不是一般內容。**</span><span class="sxs-lookup"><span data-stu-id="804d9-288">**Link to specific content rather than general content.**</span></span> <span data-ttu-id="804d9-289">例如，最好連結至檔的相關區段，而不是連結到一開始。</span><span class="sxs-lookup"><span data-stu-id="804d9-289">For example, it is better to link to the relevant section of a document than to link to the beginning.</span></span>
-   <span data-ttu-id="804d9-290">**只有在連結的材質相關、實用且不重複時，才使用連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-290">**Use a link only if the linked material is relevant, helpful, and not redundant.**</span></span> <span data-ttu-id="804d9-291">您可以使用導覽連結中的 [使用擋板]，而不使用它們。</span><span class="sxs-lookup"><span data-stu-id="804d9-291">Use restraint in navigation links don't use them just because you can.</span></span>
-   <span data-ttu-id="804d9-292">**如果連結流覽至外部網站，請在 [提示] 中放入 URL，** 讓使用者可以判斷連結的目標。</span><span class="sxs-lookup"><span data-stu-id="804d9-292">**If a link navigates to an external site, put the URL in the infotip** so that users can determine the target of the link.</span></span>
-   <span data-ttu-id="804d9-293">**只連結第一次出現的連結文字。**</span><span class="sxs-lookup"><span data-stu-id="804d9-293">**Link only the first occurrence of the link text.**</span></span> <span data-ttu-id="804d9-294">多餘的連結是不必要的，而且可能會使文字難以讀取。</span><span class="sxs-lookup"><span data-stu-id="804d9-294">Redundant links are unnecessary and can make text difficult to read.</span></span>

    <span data-ttu-id="804d9-295">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-295">**Correct:**</span></span>

    <span data-ttu-id="804d9-296">[圖片] 資料夾可讓您輕鬆分享圖片。</span><span class="sxs-lookup"><span data-stu-id="804d9-296">The Pictures folder makes sharing your pictures easy.</span></span> <span data-ttu-id="804d9-297">您可以使用圖片中的工作，以電子郵件傳送圖片，或在網路上的安全私人位置發佈圖片。</span><span class="sxs-lookup"><span data-stu-id="804d9-297">You can use the tasks in Pictures to send your pictures in e-mail or publish them in a secure, private location on the Web.</span></span> <span data-ttu-id="804d9-298">您也可以直接從 [圖片] 資料夾列印圖片。</span><span class="sxs-lookup"><span data-stu-id="804d9-298">You can also print your pictures directly from the Pictures folder.</span></span>

    <span data-ttu-id="804d9-299">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-299">**Incorrect:**</span></span>

    <span data-ttu-id="804d9-300">[圖片] 資料夾可讓您輕鬆分享圖片。</span><span class="sxs-lookup"><span data-stu-id="804d9-300">The Pictures folder makes sharing your pictures easy.</span></span> <span data-ttu-id="804d9-301">您可以使用圖片中的工作，以電子郵件傳送圖片，或在網路上的安全私人位置發佈圖片。</span><span class="sxs-lookup"><span data-stu-id="804d9-301">You can use the tasks in Pictures to send your pictures in e-mail or publish them in a secure, private location on the Web.</span></span> <span data-ttu-id="804d9-302">您也可以直接從 [圖片] 資料夾列印圖片。</span><span class="sxs-lookup"><span data-stu-id="804d9-302">You can also print your pictures directly from the Pictures folder.</span></span>

    <span data-ttu-id="804d9-303">在正確的範例中，只會連結第一個出現的相關文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-303">In the correct example, only the first occurrence of the relevant text is linked.</span></span>

    <span data-ttu-id="804d9-304">**異常：**</span><span class="sxs-lookup"><span data-stu-id="804d9-304">**Exceptions:**</span></span>

    -   <span data-ttu-id="804d9-305">**如果指令有連結，請將連結放在指令中。**</span><span class="sxs-lookup"><span data-stu-id="804d9-305">**If an instruction has a link, put the link in the instruction.**</span></span>

        <span data-ttu-id="804d9-306">使用強式密碼非常重要。</span><span class="sxs-lookup"><span data-stu-id="804d9-306">Using strong passwords is very important.</span></span> <span data-ttu-id="804d9-307">如需詳細資訊，請參閱＜增強式密碼＞。</span><span class="sxs-lookup"><span data-stu-id="804d9-307">For more information, see Strong Passwords.</span></span>

        <span data-ttu-id="804d9-308">在此範例中，連結是在指令中，而不是第一次出現。</span><span class="sxs-lookup"><span data-stu-id="804d9-308">In this example, the link is in the instruction instead of the first occurrence.</span></span>

    -   <span data-ttu-id="804d9-309">**如果與第一個位置相距較早的位置，則連結至之後的位置。**</span><span class="sxs-lookup"><span data-stu-id="804d9-309">**Link to later occurrences if they are far away from the first.**</span></span> <span data-ttu-id="804d9-310">例如，您可以在說明主題內的不同區段中，連結重複的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-310">For example, you can link redundantly in different sections within a Help topic.</span></span>

### <a name="task-links"></a><span data-ttu-id="804d9-311">工作連結</span><span class="sxs-lookup"><span data-stu-id="804d9-311">Task links</span></span>

-   <span data-ttu-id="804d9-312">**針對不具破壞性或可輕易還原的命令使用工作連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-312">**Use task links for commands that aren't destructive or are easily reversible.**</span></span> <span data-ttu-id="804d9-313">因為使用者會將連結與導覽 (以及將) 的功能建立關聯，所以連結不適合具有明顯後果的命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-313">Because users associate links with navigation (and the ability to back out), links aren't appropriate for commands with significant consequences.</span></span> <span data-ttu-id="804d9-314">顯示對話方塊或確認的命令是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="804d9-314">Commands that display a dialog box or a confirmation are a good choice.</span></span>

    <span data-ttu-id="804d9-315">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-315">**Correct:**</span></span>

    <span data-ttu-id="804d9-316">開始</span><span class="sxs-lookup"><span data-stu-id="804d9-316">Start</span></span>

    <span data-ttu-id="804d9-317">Stop</span><span class="sxs-lookup"><span data-stu-id="804d9-317">Stop</span></span>

    <span data-ttu-id="804d9-318">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-318">**Incorrect:**</span></span>

    <span data-ttu-id="804d9-319">刪除檔案</span><span class="sxs-lookup"><span data-stu-id="804d9-319">Delete file</span></span>

    <span data-ttu-id="804d9-320">在不正確的範例中，命令是破壞性的。</span><span class="sxs-lookup"><span data-stu-id="804d9-320">In the incorrect example, the command is destructive.</span></span>

### <a name="menu-links"></a><span data-ttu-id="804d9-321">功能表連結</span><span class="sxs-lookup"><span data-stu-id="804d9-321">Menu links</span></span>

-   <span data-ttu-id="804d9-322">**將相關的導覽和工作連結分組到功能表中。**</span><span class="sxs-lookup"><span data-stu-id="804d9-322">**Group related navigation and task links into menus.**</span></span> <span data-ttu-id="804d9-323">在標準導覽或命令位置內放置相關連結的功能表，可讓您更輕鬆地尋找和瞭解連結，而不是個別放置的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-323">A menu of related links placed within a standard navigation or command location makes it easier to find and understand the links than when they're placed separately.</span></span>
-   <span data-ttu-id="804d9-324">**針對選取專案相依的功能表，移除不適用的功能表連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-324">**For selection-dependent menus, remove menu links that don't apply.**</span></span> <span data-ttu-id="804d9-325">請勿停用它們。</span><span class="sxs-lookup"><span data-stu-id="804d9-325">Don't disable them.</span></span> <span data-ttu-id="804d9-326">這樣做會消除雜亂，使用者不會錯過需要選取的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-326">Doing so eliminates clutter and users won't miss links that require selection.</span></span>
-   <span data-ttu-id="804d9-327">**針對與選取無關的功能表，停用不適用的功能表連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-327">**For selection-independent menus, disable menu links that don't apply.**</span></span> <span data-ttu-id="804d9-328">請勿移除它們。</span><span class="sxs-lookup"><span data-stu-id="804d9-328">Don't remove them.</span></span> <span data-ttu-id="804d9-329">這樣做會讓功能表變得更穩定，並讓您更容易找到這些連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-329">Doing so makes the menus more stable and such links easier to find.</span></span>

    ![<span data-ttu-id="804d9-330">具有暗灰色功能表命令之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-330">screen shot of dialog box with dimmed menu command</span></span> ](images/ctrl-links-image15.png)

    <span data-ttu-id="804d9-331">在此範例中，Windows Update 正在執行更新，所以會停用 [檢查更新] 命令，而不會移除。</span><span class="sxs-lookup"><span data-stu-id="804d9-331">In this example from Windows Update, an update is being performed, so the Check for updates command is disabled rather than removed.</span></span>

### <a name="link-infotips"></a><span data-ttu-id="804d9-332">連結提示</span><span class="sxs-lookup"><span data-stu-id="804d9-332">Link infotips</span></span>

-   <span data-ttu-id="804d9-333">如果連結需要進一步說明，請在 **個別的文字控制項或提示中提供補充說明中的說明** [，但](ctrl-tooltips-and-infotips.md)不能同時提供兩者。</span><span class="sxs-lookup"><span data-stu-id="804d9-333">If a link requires further explanation, **provide the explanation in either a supplemental explanation in a separate text control or an** [infotip](ctrl-tooltips-and-infotips.md), but not both.</span></span> <span data-ttu-id="804d9-334">使用完整的句子和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-334">Use complete sentences and ending punctuation.</span></span> <span data-ttu-id="804d9-335">如果文字相同，就不需要提供兩者，如果文字不同，則會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="804d9-335">Providing both is unnecessary if the text is the same, and confusing if the text is different.</span></span>

    ![<span data-ttu-id="804d9-336">具有補充文字之連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-336">screen shot of link with supplemental text</span></span> ](images/ctrl-links-image16.png)

    <span data-ttu-id="804d9-337">在此範例中，補充說明會提供連結的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="804d9-337">In this example, a supplemental explanation provides further information about the link.</span></span>

    ![<span data-ttu-id="804d9-338">連結提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-338">screen shot of link with infotip</span></span> ](images/ctrl-links-image17.png)

    <span data-ttu-id="804d9-339">在此範例中，資訊提示會提供進一步的資訊。</span><span class="sxs-lookup"><span data-stu-id="804d9-339">In this example, an infotip provides further information.</span></span>

-   <span data-ttu-id="804d9-340">**請勿提供只是連結文字重述的提示。**</span><span class="sxs-lookup"><span data-stu-id="804d9-340">**Don't provide an infotip that is merely a restatement of the link text.**</span></span>

    <span data-ttu-id="804d9-341">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-341">**Incorrect:**</span></span>

    ![<span data-ttu-id="804d9-342">具有重複提示的連結螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-342">screen shot of link with redundant infotip</span></span> ](images/ctrl-links-image18.png)

    <span data-ttu-id="804d9-343">在此範例中，提示會造成使用者 repetitiveness 的風險令人困擾。</span><span class="sxs-lookup"><span data-stu-id="804d9-343">In this example, the infotip risks annoying users by its repetitiveness.</span></span>

## <a name="text"></a><span data-ttu-id="804d9-344">Text</span><span class="sxs-lookup"><span data-stu-id="804d9-344">Text</span></span>

-   <span data-ttu-id="804d9-345">請勿指派 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="804d9-345">Don't assign an [access key](glossary.md).</span></span> <span data-ttu-id="804d9-346">使用 Tab 鍵存取連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-346">Links are accessed using the Tab key.</span></span>
-   <span data-ttu-id="804d9-347">**使用連結，提供有關點選連結之結果的特定描述性資訊**，視需要使用最多文字。</span><span class="sxs-lookup"><span data-stu-id="804d9-347">**Use links that give specific descriptive information about the result of clicking on the link**, using as much text as necessary.</span></span> <span data-ttu-id="804d9-348">連結文字應該指出按一下連結的結果。</span><span class="sxs-lookup"><span data-stu-id="804d9-348">The link text should indicate the result of clicking on the link.</span></span> <span data-ttu-id="804d9-349">**使用者應該能夠精確地預測連結文字的連結結果，以及選用的提示。**</span><span class="sxs-lookup"><span data-stu-id="804d9-349">**Users should be able to accurately predict the result of a link from its link text and optional infotip.**</span></span>

    <span data-ttu-id="804d9-350">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-350">**Incorrect:**</span></span>

    ![<span data-ttu-id="804d9-351">安全性注意事項警告連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="804d9-351">screen shot of a security notice warning link</span></span> ](images/ctrl-links-image19.png)

    <span data-ttu-id="804d9-352">在此範例中，即使連結顯得很重要，但其標籤過於一般。</span><span class="sxs-lookup"><span data-stu-id="804d9-352">In this example, even though the link appears important, its label is too general.</span></span> <span data-ttu-id="804d9-353">使用者更有可能按一下更明確的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-353">Users are more likely to click a more specific link.</span></span>

-   <span data-ttu-id="804d9-354">內嵌連結：</span><span class="sxs-lookup"><span data-stu-id="804d9-354">For inline links:</span></span>
    -   <span data-ttu-id="804d9-355">保留文字的大小寫和標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-355">Preserve the capitalization and punctuation of the text.</span></span>
    -   <span data-ttu-id="804d9-356">除非文字是問題，否則請勿在連結中包含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-356">Don't include ending punctuation in the link unless the text is a question.</span></span>
    -   <span data-ttu-id="804d9-357">連結文字最相關的部分，然後選擇夠大的連結文字，以便輕鬆地按一下。</span><span class="sxs-lookup"><span data-stu-id="804d9-357">Link on the most relevant part of the text and choose link text that is large enough to be easy to click.</span></span>

        <span data-ttu-id="804d9-358">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-358">**Correct:**</span></span>

        <span data-ttu-id="804d9-359">前往新聞群組。</span><span class="sxs-lookup"><span data-stu-id="804d9-359">Go to a newsgroup.</span></span>

        <span data-ttu-id="804d9-360">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-360">**Incorrect:**</span></span>

        <span data-ttu-id="804d9-361">前往新聞群組。</span><span class="sxs-lookup"><span data-stu-id="804d9-361">Go to a newsgroup.</span></span>

        <span data-ttu-id="804d9-362">在這些範例中，"Go" 不是文字中最相關的部分，而且也不夠大，無法進行良好的點擊目標，而是「新聞群組」。</span><span class="sxs-lookup"><span data-stu-id="804d9-362">In these examples, "Go" isn't the most relevant part of the text and it isn't large enough to make a good click target, whereas "newsgroup" is.</span></span>

    -   <span data-ttu-id="804d9-363">**避免在彼此旁放置兩個不同的內嵌連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-363">**Avoid putting two different inline links next to each other.**</span></span> <span data-ttu-id="804d9-364">使用者可能會認為它們是單一連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-364">Users are likely to believe they are a single link.</span></span>

        <span data-ttu-id="804d9-365">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-365">**Incorrect:**</span></span>

        <span data-ttu-id="804d9-366">如需詳細資訊，請參閱 UX 指導方針。</span><span class="sxs-lookup"><span data-stu-id="804d9-366">For more information, see UX guidelines.</span></span>

        <span data-ttu-id="804d9-367">在此範例中，"UX" 和 "方針" 是兩個不同的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-367">In this example, "UX" and "guidelines" are two different links.</span></span>

-   <span data-ttu-id="804d9-368">針對獨立連結 (不是內嵌) ：</span><span class="sxs-lookup"><span data-stu-id="804d9-368">For independent links (not inline):</span></span>
    -   <span data-ttu-id="804d9-369">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="804d9-369">Use [sentence-style capitalization](glossary.md).</span></span>
    -   <span data-ttu-id="804d9-370">除非連結是問題，否則請勿使用結尾標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-370">Don't use ending punctuation unless the link is a question.</span></span>
    -   <span data-ttu-id="804d9-371">使用所有文字作為連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-371">Use all the text as the link.</span></span>
-   <span data-ttu-id="804d9-372">使用與螢幕上的其他連結清楚區別的連結。</span><span class="sxs-lookup"><span data-stu-id="804d9-372">Use links that are clearly differentiated from the other links on the screen.</span></span> <span data-ttu-id="804d9-373">使用者應該能夠準確地預測和區分連結目標。</span><span class="sxs-lookup"><span data-stu-id="804d9-373">Users should be able to accurately predict and differentiate between link targets.</span></span>

    <span data-ttu-id="804d9-374">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-374">**Incorrect:**</span></span>

    <span data-ttu-id="804d9-375">尋找防毒軟體</span><span class="sxs-lookup"><span data-stu-id="804d9-375">Find antivirus software</span></span>

    <span data-ttu-id="804d9-376">取得防毒軟體</span><span class="sxs-lookup"><span data-stu-id="804d9-376">Get antivirus software</span></span>

    <span data-ttu-id="804d9-377">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-377">**Correct:**</span></span>

    <span data-ttu-id="804d9-378">如何知道是否已安裝防毒軟體</span><span class="sxs-lookup"><span data-stu-id="804d9-378">How to know if antivirus software is installed</span></span>

    <span data-ttu-id="804d9-379">安裝防毒軟體</span><span class="sxs-lookup"><span data-stu-id="804d9-379">Install antivirus software</span></span>

    <span data-ttu-id="804d9-380">在不正確的範例中，這兩個連結之間的差異並不清楚。</span><span class="sxs-lookup"><span data-stu-id="804d9-380">In the incorrect example, the distinction between the two links is unclear.</span></span>

-   <span data-ttu-id="804d9-381">不要在連結文字上按一下或按一下這裡。</span><span class="sxs-lookup"><span data-stu-id="804d9-381">Don't add Click or Click here to the link text.</span></span> <span data-ttu-id="804d9-382">這並不是必要的，因為連結表示按一下。</span><span class="sxs-lookup"><span data-stu-id="804d9-382">It isn't necessary because a link implies clicking.</span></span> <span data-ttu-id="804d9-383">此外，請按一下這裡，並在畫面讀取器讀取時，單獨傳達沒有連結的資訊。</span><span class="sxs-lookup"><span data-stu-id="804d9-383">Also, Click here and here alone convey no information about the link when read by a screen reader.</span></span>

    <span data-ttu-id="804d9-384">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-384">**Incorrect:**</span></span>

    <span data-ttu-id="804d9-385">按一下這裡以取得說明。</span><span class="sxs-lookup"><span data-stu-id="804d9-385">Click here for description.</span></span>

    <span data-ttu-id="804d9-386">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-386">**Correct:**</span></span>

    <span data-ttu-id="804d9-387">描述</span><span class="sxs-lookup"><span data-stu-id="804d9-387">Description</span></span>

    <span data-ttu-id="804d9-388">在不正確的範例中，「按一下這裡」就不需要說出，也不會傳達連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="804d9-388">In the incorrect examples, "click here" goes without saying and conveys no information about the link.</span></span>

<span data-ttu-id="804d9-389">**導覽連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-389">**Navigation links**</span></span>

-   <span data-ttu-id="804d9-390">**以名詞開始連結，並清楚地描述按一下連結的位置。**</span><span class="sxs-lookup"><span data-stu-id="804d9-390">**Start the link with a noun and clearly describe where clicking the link will go.**</span></span> <span data-ttu-id="804d9-391">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-391">Don't use ending punctuation.</span></span> <span data-ttu-id="804d9-392">有時，您可能需要使用動詞來啟動導覽連結，但不要使用會再次出現連結的動詞，例如 View、Open 或 Go 的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-392">On occasion you may need to start navigation links with a verb, but don't use verbs that reiterate navigation that is already implied by the fact of linking, such as View, Open, or Go to.</span></span>
-   <span data-ttu-id="804d9-393">**如果流覽至網頁，而您希望目標使用者重新叫用 URL 並將它輸入瀏覽器中，請將導覽連結顯示為 URL。**</span><span class="sxs-lookup"><span data-stu-id="804d9-393">**Present a navigation link as a URL if it navigates to a Web page and you expect the target users to recall the URL and type it into a browser.**</span></span> <span data-ttu-id="804d9-394">可能的話，請將這類 Url 設計成簡短且容易記住。</span><span class="sxs-lookup"><span data-stu-id="804d9-394">If possible, design such URLs to be short and easy to remember.</span></span>
-   <span data-ttu-id="804d9-395">**如果連結中包含的網站 URL 是以 "www" 開頭，請省略 HTTPs://通訊協定名稱並使用小寫文字。**</span><span class="sxs-lookup"><span data-stu-id="804d9-395">**If the link includes a URL to a Web site starting with "www," omit the https:// protocol name and use lowercase text.**</span></span>

    <span data-ttu-id="804d9-396">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-396">**Incorrect:**</span></span>

    https://www.microsoft.com

    `www.microsoft.com`

    <span data-ttu-id="804d9-397">**正確：**</span><span class="sxs-lookup"><span data-stu-id="804d9-397">**Correct:**</span></span>

    <span data-ttu-id="804d9-398">microsoft.com</span><span class="sxs-lookup"><span data-stu-id="804d9-398">microsoft.com</span></span>

    <span data-ttu-id="804d9-399">在不正確的範例中，"HTTPs://" 和 "www" go 不需要說。</span><span class="sxs-lookup"><span data-stu-id="804d9-399">In the incorrect examples, the "https://" and "www" go without saying.</span></span>

<span data-ttu-id="804d9-400">**工作連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-400">**Task links**</span></span>

-   <span data-ttu-id="804d9-401">**使用命令式動詞來啟動連結，並清楚地描述連結所執行的工作。**</span><span class="sxs-lookup"><span data-stu-id="804d9-401">**Start the link with an imperative verb and clearly describe the task that the link performs.**</span></span> <span data-ttu-id="804d9-402">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-402">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="804d9-403">**如果命令需要額外的資訊，請以省略號結束連結 (包括成功完成的確認) 。**</span><span class="sxs-lookup"><span data-stu-id="804d9-403">**End the link with an ellipsis if the command needs additional information (including a confirmation) for successful completion.**</span></span> <span data-ttu-id="804d9-404">當工作成功完成時，請不要使用省略號。只有在需要額外資訊才能執行工作時，才會顯示另一個視窗。</span><span class="sxs-lookup"><span data-stu-id="804d9-404">Don't use an ellipsis when the successful completion of the task is to display another window only when additional information is needed to perform the task.</span></span>

    <span data-ttu-id="804d9-405">列印...</span><span class="sxs-lookup"><span data-stu-id="804d9-405">Print...</span></span>

    <span data-ttu-id="804d9-406">在此範例中，Print .。。命令連結會顯示 [列印] 對話方塊，以收集詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="804d9-406">In this example, the Print... command link displays a Print dialog box to gather more information.</span></span>

    <span data-ttu-id="804d9-407">列印</span><span class="sxs-lookup"><span data-stu-id="804d9-407">Print</span></span>

    <span data-ttu-id="804d9-408">相反地，在此範例中，列印命令連結會將檔的單一複本列印到預設印表機，而不需要進一步的使用者互動。</span><span class="sxs-lookup"><span data-stu-id="804d9-408">By contrast, in this example a Print command link prints a single copy of a document to the default printer without any further user interaction.</span></span>

    <span data-ttu-id="804d9-409">**適當地使用省略號很重要，表示使用者可以在執行工作之前進行進一步的選擇，或完全取消工作**。</span><span class="sxs-lookup"><span data-stu-id="804d9-409">**Proper use of ellipses is important to indicate that users can make further choices before performing the task, or can cancel the task entirely**.</span></span> <span data-ttu-id="804d9-410">省略號提供的視覺提示可讓使用者探索您的軟體，而不需要擔心。</span><span class="sxs-lookup"><span data-stu-id="804d9-410">The visual cue offered by an ellipsis allows users to explore your software without fear.</span></span>

-   <span data-ttu-id="804d9-411">**如有必要，請結束具有 "now" 的工作連結，以區別其與導覽連結。**</span><span class="sxs-lookup"><span data-stu-id="804d9-411">**If necessary, end a task link with "now" to distinguish it from a navigation link.**</span></span>

    <span data-ttu-id="804d9-412">下載檔案</span><span class="sxs-lookup"><span data-stu-id="804d9-412">Download files</span></span>

    <span data-ttu-id="804d9-413">立即下載檔案</span><span class="sxs-lookup"><span data-stu-id="804d9-413">Download files now</span></span>

    <span data-ttu-id="804d9-414">在此範例中，「下載檔案」會流覽至下載檔案的頁面，而「立即下載檔案」實際上會執行命令。</span><span class="sxs-lookup"><span data-stu-id="804d9-414">In this example, "Download files" navigates to a page for downloading files, whereas "Download files now" actually performs the command.</span></span>

<span data-ttu-id="804d9-415">**說明連結**</span><span class="sxs-lookup"><span data-stu-id="804d9-415">**Help links**</span></span>

<span data-ttu-id="804d9-416">如需指導方針與範例， [請參閱說明](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="804d9-416">For guidelines and examples, see [Help](winenv-help.md).</span></span>

<span data-ttu-id="804d9-417">**連結提示**</span><span class="sxs-lookup"><span data-stu-id="804d9-417">**Link infotips**</span></span>

-   <span data-ttu-id="804d9-418">使用完整句子和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="804d9-418">Use full sentences and ending punctuation.</span></span>

<span data-ttu-id="804d9-419">如需詳細的指導方針與範例，請參閱 [工具提示和提示](ctrl-tooltips-and-infotips.md)。</span><span class="sxs-lookup"><span data-stu-id="804d9-419">For more guidelines and examples, see [Tooltips and Infotips](ctrl-tooltips-and-infotips.md).</span></span>

## <a name="documentation"></a><span data-ttu-id="804d9-420">文件</span><span class="sxs-lookup"><span data-stu-id="804d9-420">Documentation</span></span>

<span data-ttu-id="804d9-421">參考連結時：</span><span class="sxs-lookup"><span data-stu-id="804d9-421">When referring to links:</span></span>

-   <span data-ttu-id="804d9-422">使用確切的連結文字，包括其大小寫，但不包含省略號。</span><span class="sxs-lookup"><span data-stu-id="804d9-422">Use the exact link text, including its capitalization, but don't include the ellipsis.</span></span>
-   <span data-ttu-id="804d9-423">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="804d9-423">To describe user interaction, use click.</span></span>
-   <span data-ttu-id="804d9-424">可能的話，請使用粗體文字來設定連結文字的格式。</span><span class="sxs-lookup"><span data-stu-id="804d9-424">When possible, format the link text using bold text.</span></span> <span data-ttu-id="804d9-425">否則，請只在必要時才將連結文字放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="804d9-425">Otherwise, put the link text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="804d9-426">範例：若要開始掃描，請按一下 [ **掃描電腦**]。</span><span class="sxs-lookup"><span data-stu-id="804d9-426">Example: To start the scan, click **Scan a computer**.</span></span>

 

