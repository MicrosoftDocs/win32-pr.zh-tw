---
title: 命令連結
description: 使用命令連結，使用者可以選取單一回應的單一回應，並藉由執行此動作，移至工作中的下一個步驟。
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29031b4456950db6ceff30d75b354dece92c5897
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103696151"
---
# <a name="command-links"></a><span data-ttu-id="4ee3b-103">命令連結</span><span class="sxs-lookup"><span data-stu-id="4ee3b-103">Command Links</span></span>

> [!NOTE]
> <span data-ttu-id="4ee3b-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="4ee3b-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="4ee3b-106">使用命令連結，使用者可以選取單一回應的單一回應，並藉由執行此動作，移至工作中的下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-106">With command links, users select a single response to a main instruction and by doing so, move on to the next step in a task.</span></span>

<span data-ttu-id="4ee3b-107">命令連結具有乾淨、輕量的外觀，可提供描述性標籤，並以標準箭號或自訂圖示顯示，以及選擇性的補充說明。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-107">Command links have a clean, lightweight appearance that allows for descriptive labels, and are displayed with either a standard arrow or custom icon, and an optional supplemental explanation.</span></span>

![<span data-ttu-id="4ee3b-108">一般命令連結對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-108">screen shot of a typical command-link dialog box</span></span> ](images/ctrl-command-links-image1.png)

<span data-ttu-id="4ee3b-109">一組一般的命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-109">A typical set of command links.</span></span>

<span data-ttu-id="4ee3b-110">命令連結與 [選項按鈕](ctrl-radio-buttons.md) 類似，因為它們可用來從一組互斥、相關的選項中進行選取。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-110">Command links are similar to [radio buttons](ctrl-radio-buttons.md) in that they are used to select from a set of mutually exclusive, related choices.</span></span> <span data-ttu-id="4ee3b-111">和選項按鈕一樣，命令連結一律會呈現在集合中，而不會個別顯示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-111">Like radio buttons, command links are always presented in sets, never individually.</span></span> <span data-ttu-id="4ee3b-112">在外觀中，命令連結具有類似于一般 [連結](ctrl-links.md)的輕量外觀，而不需要框架或其他強大的點擊 [affordance](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-112">In appearance, command links have the lightweight appearance similar to regular [links](ctrl-links.md), without a frame or other strong click [affordance](glossary.md).</span></span> <span data-ttu-id="4ee3b-113">命令連結也類似于 [命令按鈕](ctrl-command-buttons.md)，因為它們可以是預設的「命令按鈕」，而且可以有指派的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-113">Command links are also similar to [command buttons](ctrl-command-buttons.md), in that they can be the default "command button" and they can have an access key assigned.</span></span> <span data-ttu-id="4ee3b-114">就像 [認可按鈕](glossary.md)一樣，在按一下按鈕時，會關閉對話方塊的視窗 () 或前進到下一個頁面 (讓嚮導和頁面的流程) 。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-114">Like [commit buttons](glossary.md), on click they either close the window (for dialog boxes) or advance to the next page (for wizards and pages flows).</span></span>

> [!Note]  
> <span data-ttu-id="4ee3b-115">[連結](ctrl-links.md)和[版面](vis-layout.md)配置的相關指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-115">Guidelines related to [links](ctrl-links.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="4ee3b-116">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="4ee3b-116">Is this the right control?</span></span>

<span data-ttu-id="4ee3b-117">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="4ee3b-117">To decide, consider these questions:</span></span>

-   <span data-ttu-id="4ee3b-118">**選項是否會回應主要指示，以及與視窗或頁面的主要用途相關的選項？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-118">**Are the options responses to the main instruction and related to the primary purpose of the window or page?**</span></span> <span data-ttu-id="4ee3b-119">除了流覽至其他頁面之外，使用者是否必須回應以進行其他動作？</span><span class="sxs-lookup"><span data-stu-id="4ee3b-119">Must users respond to them to do something other than just navigating to a different page?</span></span> <span data-ttu-id="4ee3b-120">如果沒有，請使用另一個控制項，例如命令按鈕或連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-120">If not, use another control such as command buttons or links.</span></span> <span data-ttu-id="4ee3b-121">命令連結不適用次要或選擇性選項，或單純導覽。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-121">Command links aren't appropriate for secondary or optional choices, or pure navigation.</span></span>

    ![<span data-ttu-id="4ee3b-122">個人化控制台專案的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-122">screen shot of a personalize control panel item</span></span> ](images/ctrl-command-links-image2.png)

    <span data-ttu-id="4ee3b-123">雖然個人化主控台專案看起來像是使用命令連結，但是這些選項是一般的連結，因為此 [中樞頁面](winenv-ctrl-panels.md) 是用於純導覽。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-123">While the Personalization Control Panel item looks like it is using command links, the options are regular links because this [hub page](winenv-ctrl-panels.md) is for pure navigation.</span></span>

-   <span data-ttu-id="4ee3b-124">**控制項是否可用來從一組互斥的回應中選擇一個回應？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-124">**Is the control used to choose one response from a set of mutually exclusive responses?**</span></span> <span data-ttu-id="4ee3b-125">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-125">If not, use another control.</span></span> <span data-ttu-id="4ee3b-126">若要讓使用者選擇個別的命令，請使用命令按鈕或連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-126">To let users choose individual commands, use command buttons or links.</span></span>
-   <span data-ttu-id="4ee3b-127">**在對話方塊中，按一下控制項會關閉視窗嗎？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-127">**For dialog boxes, does clicking the control close the window?**</span></span> <span data-ttu-id="4ee3b-128">如果沒有，請使用不需要關閉視窗的控制項，例如選項按鈕、命令按鈕或連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-128">If not, use a control that doesn't require closing the window, such as radio buttons, command buttons, or links.</span></span>

    <span data-ttu-id="4ee3b-129">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-129">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-130">[索引標籤式防火牆設定] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-130">screen shot of tabbed firewall settings dialog box</span></span> ](images/ctrl-command-links-image3.png)

    <span data-ttu-id="4ee3b-131">無法在屬性視窗或索引標籤式對話方塊中使用命令連結，因為按一下控制項可關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-131">Command links can't be used in property windows or tabbed dialogs because clicking the control closes the window.</span></span>

-   <span data-ttu-id="4ee3b-132">**針對 [嚮導] 和 [頁面流程]，在沒有承諾的情況下按一下 [前進到下一頁] 嗎？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-132">**For wizards and page flows, does clicking advance to the next page without commitment?**</span></span> <span data-ttu-id="4ee3b-133">請勿使用命令連結來認可工作;請改用認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-133">Don't use command links to commit to a task; use commit buttons instead.</span></span> <span data-ttu-id="4ee3b-134">因為命令連結看起來像是連結，而使用者將連結與頁面流程中的導覽建立關聯，所以連結不適合用于 [認可頁面](glossary.md) ，因為使用者應該一律能夠返回。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-134">Because command links look like links and users associate links with navigation within a page flow, links aren't appropriate for [commit pages](glossary.md) because users should always be able to back out.</span></span>
-   <span data-ttu-id="4ee3b-135">**針對嚮導和頁面流程，是否有其他頁面使用命令連結？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-135">**For wizards and page flows, are other pages using command links?**</span></span> <span data-ttu-id="4ee3b-136">如果是，而且所有其他因素都相等，則偏好使用命令連結以取得頁面之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-136">If so, and all other factors being equal, prefer command links for consistency across pages.</span></span>
-   <span data-ttu-id="4ee3b-137">**介於兩到五之間的回應數目？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-137">**Is the number of responses between two and five?**</span></span> <span data-ttu-id="4ee3b-138">永遠不應該有單一的命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-138">There should never be a single command link.</span></span> <span data-ttu-id="4ee3b-139">因為命令連結是大型控制項，而且使用的螢幕空間與選項數目成正比，所以請將回應的數目維持在五個以下。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-139">Because command links are large controls and the screen space used is proportional to the number of options, keep the number of responses to five or fewer.</span></span> <span data-ttu-id="4ee3b-140">針對六個以上的選項，請使用選項按鈕、一般連結或單一選取 [清單視圖](ctrl-list-views.md)。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-140">For six or more options, use radio buttons, regular links, or a single-selection [list view](ctrl-list-views.md).</span></span>

    ![<span data-ttu-id="4ee3b-141">對話方塊的螢幕擷取畫面，其中包含命令清單</span><span class="sxs-lookup"><span data-stu-id="4ee3b-141">screen shot of dialog box with list of commands</span></span> ](images/ctrl-command-links-image4.png)

    <span data-ttu-id="4ee3b-142">在此範例中，Microsoft Windows 中的 [自動播放] 功能會使用清單視圖。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-142">In this example, the AutoPlay feature in Microsoft Windows uses a list view.</span></span>

-   <span data-ttu-id="4ee3b-143">**選項按鈕和認可按鈕的組合是較佳的選擇嗎？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-143">**Would a combination of radio buttons and a commit button be a better choice?**</span></span> <span data-ttu-id="4ee3b-144">當下列任何條件成立時，選項按鈕是較佳的選擇：</span><span class="sxs-lookup"><span data-stu-id="4ee3b-144">Radio buttons are a better choice when any of the following are true:</span></span>
    -   <span data-ttu-id="4ee3b-145">**有一個強式預設選項，可讓您大部分的使用者選取。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-145">**There is a strong default option that you want most users to select.**</span></span> <span data-ttu-id="4ee3b-146">在使用者習慣按下 [下一步] 接受適當預設值的情況下，使用者比較不可能變更預設選項按鈕，而不是預設的命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-146">Users are less likely to change a default radio button than a default command link especially in a wizard, where users are accustomed to clicking Next to accept appropriate defaults.</span></span> <span data-ttu-id="4ee3b-147">另一方面，如果您想要鼓勵使用者做出明確的選擇，命令連結是比較好的選擇。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-147">On the other hand, command links are a better choice if you want to encourage users to make an explicit choice.</span></span>
    -   <span data-ttu-id="4ee3b-148">**使用者需要與選擇互動 (可能會在進行決策之前查看其他資訊) 。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-148">**Users need to interact with the choices (perhaps to see additional information) before making a decision.**</span></span> <span data-ttu-id="4ee3b-149">例如，選取選項按鈕可能會動態顯示選項的描述。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-149">For example, selecting a radio button might display a description about the option dynamically.</span></span>

        ![<span data-ttu-id="4ee3b-150">具有選項按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-150">screen shot of dialog box with radio buttons</span></span> ](images/ctrl-command-links-image5.png)

        <span data-ttu-id="4ee3b-151">在此範例中，選取選項按鈕會顯示選項的描述。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-151">In this example, selecting a radio button displays a description of the option.</span></span>

    -   <span data-ttu-id="4ee3b-152">**頁面上有次要或相關的選項。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-152">**There are secondary or related options on the page.**</span></span> <span data-ttu-id="4ee3b-153">命令連結傾向于將頁面設為市場，讓您輕鬆地忽略其他所有專案。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-153">Command links tend to dominate the page, making it easy to overlook everything else.</span></span> <span data-ttu-id="4ee3b-154">此外，按一下命令連結之後，就無法選取次要選項。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-154">Furthermore, once a command link is clicked, it's impossible to select secondary options.</span></span>

        <span data-ttu-id="4ee3b-155">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-155">**Incorrect:**</span></span>

        ![<span data-ttu-id="4ee3b-156">具有混合控制項之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-156">screen shot of dialog box with mixed controls</span></span> ](images/ctrl-command-links-image6.png)

        <span data-ttu-id="4ee3b-157">在此範例中，有兩種不同的方式可回應主要指令。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-157">In this example, there are two different ways to respond to the main instruction.</span></span> <span data-ttu-id="4ee3b-158">命令連結不會用於第一個回應，因為很難選取次要選項。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-158">A command link wasn't used for the first response because it would be difficult to select secondary options.</span></span>

        <span data-ttu-id="4ee3b-159">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-159">**Correct:**</span></span>

        ![<span data-ttu-id="4ee3b-160">具有相同控制項之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-160">screen shot of dialog box with same controls</span></span> ](images/ctrl-command-links-image7.png)

        <span data-ttu-id="4ee3b-161">在此範例中，選項按鈕可讓回應變成清楚，並允許使用者選取次要選項。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-161">In this example, radio buttons make the responses clear, while allowing users to select secondary options.</span></span>

-   <span data-ttu-id="4ee3b-162">**在對話方塊中，一組認可按鈕是否是較佳的選擇？**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-162">**For dialog boxes, would a group of commit buttons be a better choice?**</span></span> <span data-ttu-id="4ee3b-163">當選項需要較長、更清楚的回應和補充說明，但如果有一些簡單的選項，則 [認可] 按鈕群組是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-163">Command links work better when the options require longer, more explanatory responses and supplemental explanations, but a group of commit buttons is a better choice if there are a few simple options.</span></span>

    <span data-ttu-id="4ee3b-164">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-164">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-165">對話方塊的螢幕擷取畫面，其中包含儲存並不儲存</span><span class="sxs-lookup"><span data-stu-id="4ee3b-165">screen shot of dialog box with save and don't save</span></span> ](images/ctrl-command-links-image8.png)

    <span data-ttu-id="4ee3b-166">在此範例中，使用簡單命令的命令連結，會讓對話方塊不必要地複雜。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-166">In this example, using command links for simple commands makes the dialog box unnecessarily complicated.</span></span>

    <span data-ttu-id="4ee3b-167">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-167">**Correct:**</span></span>

    ![顯示具有 [儲存]、[不要儲存] 和 [取消] 認可按鈕之對話方塊的螢幕擷取畫面。](images/ctrl-command-links-image9.png)

    <span data-ttu-id="4ee3b-169">在此範例中，使用簡單的認可按鈕是從點開始。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-169">In this example, using simple commit buttons gets right to the point.</span></span>

    <span data-ttu-id="4ee3b-170">不過，當使用文字來說明認可按鈕時，簡單易懂的命令連結一律是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-170">However, self-explanatory command links are always better choice when text is used to explain commit buttons.</span></span>

    <span data-ttu-id="4ee3b-171">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-171">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-172">具有不必要文字之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-172">screen shot of dialog box with unnecessary text</span></span> ](images/ctrl-command-links-image10.png)

    <span data-ttu-id="4ee3b-173">在此範例中，會使用文字來說明認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-173">In this example, text is used to explain the commit buttons.</span></span>

    <span data-ttu-id="4ee3b-174">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-174">**Correct:**</span></span>

    ![<span data-ttu-id="4ee3b-175">不需要更多文字之標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-175">screen shot of labels that don't need more text</span></span> ](images/ctrl-command-links-image11.png)

    <span data-ttu-id="4ee3b-176">在此範例中，命令連結很容易理解。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-176">In this example, the command links are self-explanatory.</span></span>

> [!Note]  
> <span data-ttu-id="4ee3b-177">命令連結需要 Windows Vista 或更新版本，因此不適用於舊版 Windows。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-177">Command links require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span> <span data-ttu-id="4ee3b-178">您可以使用一般連結來取代。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-178">You can use regular links as a substitute.</span></span>

 

![<span data-ttu-id="4ee3b-179">具有圖示和文字的一般連結螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-179">screen shot of regular links with icons and text</span></span> ](images/ctrl-command-links-image12.png)

<span data-ttu-id="4ee3b-180">在此範例中，會使用包含圖示和補充說明的一般連結來取代 Windows XP 中的命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-180">In this example, regular links with an icon and a supplemental explanation are used as a substitute for command links in Windows XP.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="4ee3b-181">設計概念</span><span class="sxs-lookup"><span data-stu-id="4ee3b-181">Design concepts</span></span>

<span data-ttu-id="4ee3b-182">這是因為命令連結可讓您使用更具描述性的標籤，而選擇性的補充說明並不表示您應該。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-182">Just because command links allow you to use more descriptive labels and optional supplemental explanations doesn't mean you should.</span></span> <span data-ttu-id="4ee3b-183">請考慮下列範例：</span><span class="sxs-lookup"><span data-stu-id="4ee3b-183">Consider the following example:</span></span>

<span data-ttu-id="4ee3b-184">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-184">**Incorrect:**</span></span>

![<span data-ttu-id="4ee3b-185">具有太多文字之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-185">screen shot of dialog box with too much text</span></span> ](images/ctrl-command-links-image13.png)

<span data-ttu-id="4ee3b-186">此對話方塊會嚴重過度通訊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-186">This dialog box is seriously over-communicating.</span></span>

<span data-ttu-id="4ee3b-187">此對話方塊會採取簡單的問題，並不必要地使其與命令連結文字的複雜性。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-187">This dialog box takes a simple question and unnecessarily complicates it with command link text.</span></span> <span data-ttu-id="4ee3b-188">使用者不想要讀取這類簡單問題的所有文字。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-188">Users don't want to read all that text for such simple questions.</span></span>

<span data-ttu-id="4ee3b-189">我們可以套用三個命令連結指導方針，以簡化此對話方塊：</span><span class="sxs-lookup"><span data-stu-id="4ee3b-189">We can simplify this dialog box by applying three command link guidelines:</span></span>

-   <span data-ttu-id="4ee3b-190">**請勿使用屬於命令連結之冗長重述的補充說明。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-190">**Don't use a supplemental explanation that is a wordy restatement of the command link.**</span></span> <span data-ttu-id="4ee3b-191">只有當您無法讓命令連結一目了然時，才使用補充說明。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-191">Use a supplemental explanation only when you can't make a command link self-explanatory.</span></span> <span data-ttu-id="4ee3b-192">提供一個命令連結的補充說明，並不表示您必須為所有命令提供它們。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-192">Providing a supplemental explanation for one command link doesn't mean that you have to provide them for all commands.</span></span>
-   <span data-ttu-id="4ee3b-193">**選取最安全的 (，以防止資料遺失或系統存取) ，而且最安全的回應是預設值。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-193">**Select the safest (to prevent loss of data or system access) and most secure response to be the default.**</span></span> <span data-ttu-id="4ee3b-194">如果安全性和安全性不是因素，請選取最有可能或方便的回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-194">If safety and security aren't factors, select the most likely or convenient response.</span></span>
-   <span data-ttu-id="4ee3b-195">**提供明確的 [取消] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-195">**Provide an explicit Cancel button.**</span></span> <span data-ttu-id="4ee3b-196">請勿將命令連結用於此用途。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-196">Don't use a command link for this purpose.</span></span>

<span data-ttu-id="4ee3b-197">藉由套用這些指導方針，我們可以消除不必要的補充說明、將最方便的回應設為預設值，並提供明確的 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-197">By applying these guidelines, we can eliminate the unnecessary supplemental explanations, make the most convenient response the default, and provide an explicit Cancel button.</span></span>

<span data-ttu-id="4ee3b-198">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-198">**Better:**</span></span>

![<span data-ttu-id="4ee3b-199">具有命令和標籤之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-199">screen shot of dialog box with commands and labels</span></span> ](images/ctrl-command-links-image14.png)

<span data-ttu-id="4ee3b-200">更簡單的命令連結的改進版本。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-200">An improved version with simpler command links.</span></span>

<span data-ttu-id="4ee3b-201">雖然此版本不會明確說明未儲存的部分會被視為遺失，但少數使用者會根據這項資訊來變更其決策，因此這是很好的取捨。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-201">While it's true that this version doesn't explain explicitly that not saving is counted as a loss, few users will change their decision based on this information, making this a good tradeoff.</span></span>

<span data-ttu-id="4ee3b-202">您可以藉由分析命令連結是否甚至是在此案例中使用的正確控制項，來建立更好的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-202">This dialog box could be made even better by analyzing whether or not command links are even the right control to use in this case.</span></span> <span data-ttu-id="4ee3b-203">認可按鈕實際上是較佳的選擇，因為不需要更多的清楚解釋回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-203">Commit buttons are actually a better choice, because longer, more explanatory responses aren't needed.</span></span>

<span data-ttu-id="4ee3b-204">**最好：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-204">**Best:**</span></span>

![<span data-ttu-id="4ee3b-205">具有認可按鈕之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-205">screen shot of dialog box with commit buttons</span></span> ](images/ctrl-command-links-image15.png)

<span data-ttu-id="4ee3b-206">正確的版本會使用認可按鈕來向右取得點。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-206">The correct version uses commit buttons to get right to the point.</span></span>

<span data-ttu-id="4ee3b-207">命令連結有許多優點，但使用 unwisely 時，會導致過度通訊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-207">Command links have many advantages, but when used unwisely they lead to over-communication.</span></span> <span data-ttu-id="4ee3b-208">如果是對話方塊，請考慮使用認可按鈕，只有在認可按鈕未執行作業時，才使用命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-208">For dialog boxes, consider using commit buttons first and use command links only if commit buttons don't do the job well.</span></span>

<span data-ttu-id="4ee3b-209">**適當地使用時，命令連結應可簡化並闡明您的 UI。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-209">**When used appropriately, command links should simplify and clarify your UI.**</span></span> <span data-ttu-id="4ee3b-210">如果結果相反，請回頭回頭看看其他替代方案，並專注于您真正需要傳達的內容。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-210">If the results are the opposite, take a step back, review the alternatives, and focus on what you really need to communicate.</span></span>

<span data-ttu-id="4ee3b-211">**如果您只做一件事 ...** 請勿使用命令連結來進行通訊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-211">**If you do only one thing...** Don't use command links to over-communicate.</span></span> <span data-ttu-id="4ee3b-212">命令連結應可簡化並闡明通訊，而不會讓它變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-212">Command links should simplify and clarify the communication, not make it more complicated.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="4ee3b-213">使用模式</span><span class="sxs-lookup"><span data-stu-id="4ee3b-213">Usage patterns</span></span>

<span data-ttu-id="4ee3b-214">命令連結有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="4ee3b-214">Command links have several usage patterns:</span></span>



|                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee3b-215">**頁面回應** 命令連結可用來回應主要指示，並前進到下一頁。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-215">**Page responses** Command links are used to respond to the main instruction and advance to the next page.</span></span>    | <span data-ttu-id="4ee3b-216">使用此模式時，命令連結會取代 [下一步] 按鈕，但仍會有 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-216">with this pattern, the command links replace the next button, but there is still a cancel button.</span></span><br/><span data-ttu-id="4ee3b-217">頁面回應不表示承諾用量。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-217">Page responses don't imply commitment.</span></span> <span data-ttu-id="4ee3b-218">由於命令連結看起來像是連結，而使用者會將連結與頁面流程內的導覽建立關聯，因此不適合使用 [認可] 頁面的連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-218">because command links look like links and users associate links with navigation within a page flow, links aren't appropriate for commit pages.</span></span> <span data-ttu-id="4ee3b-219">使用者應該一律能夠返回。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-219">users should always be able to back out.</span></span> <br/> ![顯示 [連線到網際網路] 對話方塊的螢幕擷取畫面，其中包含 [無線]、[寬頻 (PPPoE) ] 和 [撥號] 命令連結。](images/ctrl-command-links-image16.png)<br/><span data-ttu-id="4ee3b-221">在此範例中，命令連結是用來提供主要指令的描述性回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-221">In this example, command links are used to give descriptive responses to the main instruction.</span></span> <span data-ttu-id="4ee3b-222">雖然您可以在這裡使用選項按鈕，但命令連結可讓使用者只需按一下就能回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-222">While radio buttons could be used here, command links allow users to respond with a single click.</span></span><br/> |
| <span data-ttu-id="4ee3b-223">**對話方塊回應** 命令連結可用來回應主要指令並關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-223">**Dialog box responses** Command links are used to respond to the main instruction and close the dialog box.</span></span>  | <span data-ttu-id="4ee3b-224">使用此模式時，命令連結會取代認可按鈕 (例如 [確定]) ，但仍有 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-224">with this pattern, the command links replace the commit buttons (such as ok), but there is still a cancel button.</span></span><br/><span data-ttu-id="4ee3b-225">與頁面流程不同的是，在建立對話方塊之後，無法再退出對話方塊型回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-225">Unlike page flows, there is no way to back out of a dialog box-based response once it has been made.</span></span> <span data-ttu-id="4ee3b-226">因此，對話方塊命令連結表示承諾用量。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-226">consequently, dialog box command links imply commitment.</span></span> <br/> ![<span data-ttu-id="4ee3b-227">包含命令連結之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-227">screen shot of dialog box with command links</span></span> ](images/ctrl-command-links-image17.png)<br/><span data-ttu-id="4ee3b-228">在此範例中，命令連結是用來提供主要指令的描述性回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-228">In this example, command links are used to give descriptive responses to the main instruction.</span></span> <span data-ttu-id="4ee3b-229">雖然您可以在這裡使用選項按鈕，但命令連結可讓使用者只需按一下就可以選擇。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-229">While radio buttons could be used here, command links allow users to choose with a single click.</span></span><br/>                                                   |
| <span data-ttu-id="4ee3b-230">**詳細回應** 包含詳細資訊的頁面或對話回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-230">**Detailed responses** A page or dialog response that includes detailed information.</span></span>                          | <span data-ttu-id="4ee3b-231">有時，使用者可能需要更詳細的資訊來選擇其回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-231">on occasion, users may need more detailed information to choose their response.</span></span> <br/> ![<span data-ttu-id="4ee3b-232">[複製檔案] 對話方塊和縮圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-232">screen shot of copy file dialog box and thumbnails</span></span> ](images/ctrl-command-links-image18.png)<br/> <span data-ttu-id="4ee3b-233">在此範例中，會使用詳細的命令連結，讓使用者能夠做出明智的決策。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-233">In this example, detailed command links are used so that users can make informed decisions.</span></span> <span data-ttu-id="4ee3b-234">縮圖和檔案詳細資料可協助使用者決定。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-234">The thumbnails and file details help users decide.</span></span><br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a><span data-ttu-id="4ee3b-235">指導方針</span><span class="sxs-lookup"><span data-stu-id="4ee3b-235">Guidelines</span></span>

### <a name="interaction"></a><span data-ttu-id="4ee3b-236">互動</span><span class="sxs-lookup"><span data-stu-id="4ee3b-236">Interaction</span></span>

-   <span data-ttu-id="4ee3b-237">**如果按一下命令連結的結果不是瞬間，則顯示忙碌指標。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-237">**Display a busy pointer if the result of clicking a command link isn't instantaneous.**</span></span> <span data-ttu-id="4ee3b-238">如果沒有意見反應，使用者可能會認為按一下未發生，然後再按一次。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-238">Without feedback, users might assume that the click didn't happen and click again.</span></span>

### <a name="presentation"></a><span data-ttu-id="4ee3b-239">簡報</span><span class="sxs-lookup"><span data-stu-id="4ee3b-239">Presentation</span></span>

-   <span data-ttu-id="4ee3b-240">**一律在兩個或以上的集合中顯示命令連結。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-240">**Always present command links in a set of two or more.**</span></span> <span data-ttu-id="4ee3b-241">邏輯上，沒有理由要求只有一個答案的問題。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-241">Logically, there is no reason to ask a question that has only one answer.</span></span>

    <span data-ttu-id="4ee3b-242">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-242">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-243">具有一個命令連結之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-243">screen shot of dialog box with one command link</span></span> ](images/ctrl-command-links-image19.png)

    <span data-ttu-id="4ee3b-244">在此範例中，對話方塊會顯示為使用者提供選擇，但只有一個指示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-244">In this example, the dialog box appears to be offering the user a choice, but there is just an instruction.</span></span> <span data-ttu-id="4ee3b-245">這應該是參考對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-245">This should be an informational dialog instead.</span></span>

-   <span data-ttu-id="4ee3b-246">**先顯示最常使用的命令連結。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-246">**Present the most commonly used command links first.**</span></span> <span data-ttu-id="4ee3b-247">產生的順序大致上應該遵循使用的可能性，但也有邏輯流程。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-247">The resulting order should roughly follow the likelihood of use, but also have a logical flow.</span></span>
    -   <span data-ttu-id="4ee3b-248">**例外狀況：** 導致執行所有工作的命令連結應先放置。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-248">**Exception:** Command links that result in doing everything should be placed first.</span></span>
-   <span data-ttu-id="4ee3b-249">**提供明確的 [取消] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-249">**Provide an explicit Cancel button.**</span></span> <span data-ttu-id="4ee3b-250">請勿將命令連結用於此用途。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-250">Don't use a command link for this purpose.</span></span> <span data-ttu-id="4ee3b-251">使用者通常會發現他們不想要執行工作。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-251">Quite often users realize that they don't want to perform a task.</span></span> <span data-ttu-id="4ee3b-252">使用命令連結來取消會要求使用者謹慎地讀取所有命令連結，以判斷哪一個表示取消。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-252">Using a command link to cancel would require users to read all the command links carefully to determine which one means cancel.</span></span> <span data-ttu-id="4ee3b-253">具有明確的 [取消] 按鈕，可讓使用者有效率地取消工作。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-253">Having an explicit Cancel button allows users to cancel a task efficiently.</span></span>

    <span data-ttu-id="4ee3b-254">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-254">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-255">具有 [不要結束] 連結之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-255">screen shot of dialog box with 'don't exit' link</span></span> ](images/ctrl-command-links-image20.png)

    <span data-ttu-id="4ee3b-256">在此範例中，[不要結束命令] 連結應該是 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-256">In this example, the Don't exit command link should be a Cancel button.</span></span>

-   <span data-ttu-id="4ee3b-257">**如果提供明確的 [取消] 按鈕，則會保留單一命令連結，同時提供 [取消] 和 [取消] 按鈕的命令連結。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-257">**If providing an explicit Cancel button leaves a single command link, provide both a command link to cancel and a Cancel button.**</span></span> <span data-ttu-id="4ee3b-258">這麼做可讓使用者清楚知道使用者有選擇。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-258">Doing so makes it clear that users have a choice.</span></span> <span data-ttu-id="4ee3b-259">以與第一個回應不同的方式來說明此命令連結，而不只是「取消」或某些變化。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-259">Phrase this command link in terms of how it differs from the first response, instead of just "Cancel" or some variation.</span></span>

    ![<span data-ttu-id="4ee3b-260">兩個連結和 [取消] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-260">screen shot of two links and a cancel button</span></span> ](images/ctrl-command-links-image21.png)

    <span data-ttu-id="4ee3b-261">在此範例中，第二個命令連結表示使用者有一個選擇，但它的所有工作都是 cancel。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-261">In this example, the second command link indicates that the user has a choice, but all it does is cancel.</span></span> <span data-ttu-id="4ee3b-262">不過，它的片語方式與第一個命令連結不同。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-262">However, it is phrased in terms of how it differs from the first command link.</span></span>

-   <span data-ttu-id="4ee3b-263">**如果您無法將環境回復為先前的狀態，請使用 [關閉] 而不是 [取消]，而不會產生任何副作用。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-263">**Use Close instead of Cancel if you can't return the environment to its previous state, leaving no side effect.**</span></span>
-   <span data-ttu-id="4ee3b-264">**不要顯示已停用的命令連結。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-264">**Don't display disabled command links.**</span></span> <span data-ttu-id="4ee3b-265">如果命令連結未套用至目前的內容，請改為將它移除。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-265">If a command link doesn't apply to the current context, remove it instead.</span></span> <span data-ttu-id="4ee3b-266">如果移除所有未套用的命令連結，請將其保留為單一命令連結、消除視窗或頁面，或在需要明確使用者同意的情況下顯示 [確認](mess-confirm.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-266">If removing all the command links that don't apply leaves a single command link, either eliminate the window or page, or display a [confirmation](mess-confirm.md) if explicit user consent is needed.</span></span>

### <a name="icons"></a><span data-ttu-id="4ee3b-267">圖示</span><span class="sxs-lookup"><span data-stu-id="4ee3b-267">Icons</span></span>

-   <span data-ttu-id="4ee3b-268">**所有命令連結都需要圖示。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-268">**All command links need an icon.**</span></span> <span data-ttu-id="4ee3b-269">圖示可協助使用者區分命令連結與一般連結和使用者介面文字。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-269">The icons help users distinguish command links from regular links and user interface text.</span></span>
-   <span data-ttu-id="4ee3b-270">**只針對命令連結使用箭號圖示。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-270">**Use the arrow icon only for command links.**</span></span> <span data-ttu-id="4ee3b-271">一般連結不應使用箭號圖示，除非在 Windows XP 中用來替代命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-271">Regular links shouldn't use the arrow icon unless they are being used as a substitute for command links in Windows XP.</span></span>
-   <span data-ttu-id="4ee3b-272">**使用「安全防護」圖示來指出回應需要立即提高許可權。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-272">**Use the security shield icon to indicate that a response requires immediate elevation.**</span></span> <span data-ttu-id="4ee3b-273">如需使用安全性保護盾圖示的其他指導方針，請參閱 [使用者帳戶控制](winenv-uac.md)。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-273">For additional guidelines on using the security shield icon, see the [User Account Control](winenv-uac.md).</span></span>
-   <span data-ttu-id="4ee3b-274">**只有在協助使用者以視覺化方式識別並區分選項時，才使用自訂圖示。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-274">**Use custom icons only if they help users visually identify and differentiate the options.**</span></span> <span data-ttu-id="4ee3b-275">如果無法立即辨識或有意義，請不要使用自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-275">Don't use custom icons if they aren't immediately recognizable or meaningful.</span></span>

    <span data-ttu-id="4ee3b-276">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-276">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-277">使用自訂圖示的兩個命令連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-277">screen shot of two command links with custom icons</span></span> ](images/ctrl-command-links-image22.png)

    <span data-ttu-id="4ee3b-278">在此範例中，自訂圖示無法立即辨識。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-278">In this example, the custom icons aren't immediately recognizable.</span></span>

-   <span data-ttu-id="4ee3b-279">**若為自訂圖示，請使用16x16 或32x32 圖元圖示。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-279">**For custom icons, use 16x16 or 32x32 pixel icons.**</span></span> <span data-ttu-id="4ee3b-280">如果有足夠的空間，請使用較大的圖示，這些圖示會從較大的大小以視覺化方式受益。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-280">Use the larger icons if there is sufficient space and they benefit visually from the larger size.</span></span> <span data-ttu-id="4ee3b-281">如果您需要安全性防護罩，請使用32x32 或48x48 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-281">If you need security shield overlays, use 32x32 or 48x48 pixel icons.</span></span>

    ![<span data-ttu-id="4ee3b-282">具有圖示的三個命令連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-282">screen shot of three command links with icons</span></span> ](images/ctrl-command-links-image23.png)

    <span data-ttu-id="4ee3b-283">這個範例會使用32x32 圖元的自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-283">This example uses 32x32 pixel custom icons.</span></span>

    ![<span data-ttu-id="4ee3b-284">具有較大圖示的兩個命令連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-284">screen shot of two command links with larger icons</span></span> ](images/ctrl-command-links-image24.png)

    <span data-ttu-id="4ee3b-285">此範例會使用48x48 圖元自訂圖示，並加上安全性防護罩。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-285">This example uses 48x48 pixel custom icons, with a security shield overlay.</span></span>

-   <span data-ttu-id="4ee3b-286">**避免混合自訂圖示與視窗或頁面上的標準箭號圖示。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-286">**Avoid mixing custom icons with the standard arrow icon on a window or a page.**</span></span> <span data-ttu-id="4ee3b-287">如果您在介面上使用自訂圖示，請嘗試使用所有自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-287">If you use a custom icon on a surface, try to use all custom icons.</span></span> <span data-ttu-id="4ee3b-288">不過，偏好使用標準箭號圖示來進行無意義的自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-288">However, prefer the standard arrow icon over meaningless custom icons.</span></span>

### <a name="default-values"></a><span data-ttu-id="4ee3b-289">預設值</span><span class="sxs-lookup"><span data-stu-id="4ee3b-289">Default values</span></span>

-   <span data-ttu-id="4ee3b-290">**選取最安全的 (，以防止資料遺失或系統存取) ，而且最安全的回應是預設值。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-290">**Select the safest (to prevent loss of data or system access) and most secure response to be the default.**</span></span> <span data-ttu-id="4ee3b-291">如果安全性和安全性不是因素，請選取最有可能或方便的回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-291">If safety and security aren't factors, select the most likely or convenient response.</span></span>
-   <span data-ttu-id="4ee3b-292">**在可行的情況下，請將第一個回應設為預設選項** ，因為使用者通常會預期，除非該順序不是邏輯的。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-292">**When practical, make the first response the default option** because users often expect that unless that order isn't logical.</span></span>
-   <span data-ttu-id="4ee3b-293">在對話方塊中，除非有簡單的方法可復原動作，否則請 **不要將破壞性動作設為預設的命令連結**。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-293">**For dialog boxes, don't make a destructive action the default command link** unless there is an easy way to undo the action.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="4ee3b-294">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="4ee3b-294">Recommended sizing and spacing</span></span>

![<span data-ttu-id="4ee3b-295">命令連結大小和間距的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-295">screen shot of command-link sizing and spacing</span></span> ](images/ctrl-command-links-image25.png)

## <a name="labels"></a><span data-ttu-id="4ee3b-296">標籤</span><span class="sxs-lookup"><span data-stu-id="4ee3b-296">Labels</span></span>

> [!Note]  
> <span data-ttu-id="4ee3b-297">因為命令連結會回應主要指令，所以您應該先製作 [良好的主要指示](text-ui.md) ，再決定其回應。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-297">Because command links are responses to a main instruction, you should craft a [good main instruction](text-ui.md) before determining its responses.</span></span>

 

<span data-ttu-id="4ee3b-298">**命令連結標籤**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-298">**Command link labels**</span></span>

-   <span data-ttu-id="4ee3b-299">**選擇明確通訊的精確標籤，並區分命令連結的用途。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-299">**Choose a concise label that clearly communicates and differentiates what the command link does.**</span></span> <span data-ttu-id="4ee3b-300">它應該是一目了然的，且對應至主要指令。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-300">It should be self-explanatory and correspond to the main instruction.</span></span> <span data-ttu-id="4ee3b-301">將標籤的焦點放在回應之間的差異。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-301">Focus the labels on the differences among the responses.</span></span> <span data-ttu-id="4ee3b-302">使用者不需要知道命令連結真正的意義，或與其他命令連結的不同之處。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-302">Users shouldn't have to figure out what the command link really means or how it differs from other command links.</span></span>

    <span data-ttu-id="4ee3b-303">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-303">**Incorrect:**</span></span>

    ![<span data-ttu-id="4ee3b-304">重複命令連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-304">screen shot of a redundant command link</span></span> ](images/ctrl-command-links-image26.png)

    <span data-ttu-id="4ee3b-305">在此範例中，第二個和第三個回應之間有何差異？</span><span class="sxs-lookup"><span data-stu-id="4ee3b-305">In this example, what is the difference between the second and third responses?</span></span> <span data-ttu-id="4ee3b-306">你很高興沒有 [取消] 按鈕嗎？</span><span class="sxs-lookup"><span data-stu-id="4ee3b-306">Aren't you glad there's a Cancel button?</span></span>

-   <span data-ttu-id="4ee3b-307">**專注命令連結標籤，協助使用者做出正確的決策。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-307">**Focus command link labels on helping users make the right decision.**</span></span> <span data-ttu-id="4ee3b-308">省略不會影響選擇的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-308">Omit details that don't affect the choice.</span></span> <span data-ttu-id="4ee3b-309">標籤不需要是將會發生之情況的完整規格。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-309">The labels don't have to be a complete specification of what will happen.</span></span>
-   <span data-ttu-id="4ee3b-310">**使用動詞命令來啟動命令連結。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-310">**Start command links with a verb.**</span></span> <span data-ttu-id="4ee3b-311">不過，請不要使用 click，因為標籤應該傳達命令連結的功能，而不是它的運作方式。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-311">Don't use click, however, because the label should communicate what the command link does, not how it works.</span></span>
    -   <span data-ttu-id="4ee3b-312">**例外狀況：** 如果所有命令連結的開頭都是相同的動詞或片語，請刪除多餘的動詞或片語。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-312">**Exception:** If all the command links begin with the same verb or phrase, eliminate the redundant verb or phrase.</span></span>
-   <span data-ttu-id="4ee3b-313">一般情況下，請 **使用正** 片語 (提供可執行某些動作的選項) 。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-313">In general, **use positive phrasing** (providing a choice to do something).</span></span> <span data-ttu-id="4ee3b-314">負措辭 (如果讓標籤變得更容易瞭解，就可以選擇不執行某些動作) 。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-314">Negative phrasing (providing a choice not to do something) is acceptable if it makes the labels easier to understand.</span></span>
-   <span data-ttu-id="4ee3b-315">**使用平行措辭和單行標籤。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-315">**Use parallel phrasing and single line labels.**</span></span> <span data-ttu-id="4ee3b-316">長標籤不建議讀取，也不需要。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-316">Long labels discourage reading and shouldn't be necessary.</span></span> <span data-ttu-id="4ee3b-317">此外，您也可以在檔中更輕鬆地參考中等大小的標籤。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-317">Also, moderately sized labels are easier to refer to in documentation.</span></span>
-   <span data-ttu-id="4ee3b-318">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-318">**Use sentence-style capitalization.**</span></span>
-   <span data-ttu-id="4ee3b-319">**除非標籤是問題，否則請勿使用結尾標點符號。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-319">**Don't use ending punctuation unless the label is a question.**</span></span>
-   <span data-ttu-id="4ee3b-320">**指派唯一的存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-320">**Assign a unique access key.**</span></span> <span data-ttu-id="4ee3b-321">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-321">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="4ee3b-322">**請勿使用省略號。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-322">**Don't use ellipses.**</span></span> <span data-ttu-id="4ee3b-323">省略號表示執行動作可能需要更多的資訊。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-323">Ellipses mean that more information might be needed to perform the action.</span></span> <span data-ttu-id="4ee3b-324">正確使用的命令連結不需要省略號，因為它們具有立即的作用。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-324">Properly used command links don't need ellipses because they have an immediate effect.</span></span>
-   <span data-ttu-id="4ee3b-325">**如果強烈建議回應，請將「 (建議的) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-325">**If a response is strongly recommended, add "(recommended)" to the label.**</span></span> <span data-ttu-id="4ee3b-326">請務必新增至標籤，而不是補充說明。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-326">Be sure to add to the label, not the supplemental explanation.</span></span>
-   <span data-ttu-id="4ee3b-327">**如果回應僅供 advanced 使用者使用，請考慮將「 (advanced) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-327">**If a response is intended only for advanced users, consider adding "(advanced)" to the label.**</span></span> <span data-ttu-id="4ee3b-328">請務必新增至標籤，而不是補充說明。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-328">Be sure to add to the label, not the supplemental explanation.</span></span>

<span data-ttu-id="4ee3b-329">**秘訣：** 您可以藉由想像 friend 指出的主要指示，並以命令連結回應，來評估命令連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-329">**Tip:** You can evaluate command links by imagining that a friend stated the main instruction, and you responded with the command links.</span></span> <span data-ttu-id="4ee3b-330">如果回應命令連結會非自然或麻煩，請修改命令連結，也可能是主要指令。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-330">If responding with the command links would be unnatural or awkward, revise the command links and possibly the main instruction.</span></span>

<span data-ttu-id="4ee3b-331">**補充說明**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-331">**Supplemental explanations**</span></span>

-   <span data-ttu-id="4ee3b-332">如果命令連結需要進一步的說明，請 **提供補充說明**。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-332">If a command link requires further explanation, **provide a supplemental explanation**.</span></span> <span data-ttu-id="4ee3b-333">補充說明說明為何使用者可能會想要選擇回應，或在選擇回應時所發生的情況。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-333">Supplemental explanations describe why users might want to choose a response or what happens if a response is chosen.</span></span>

    ![<span data-ttu-id="4ee3b-334">描述選項結果之文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4ee3b-334">screen shot of text describing results of option</span></span> ](images/ctrl-command-links-image27.png)

    <span data-ttu-id="4ee3b-335">在此範例中，補充說明會描述選項的含意。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-335">In this example, the supplemental explanation describes the implications of the option.</span></span>

-   <span data-ttu-id="4ee3b-336">**請勿使用冗長重述命令連結的補充說明。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-336">**Don't use a supplemental explanation that is wordy restatement of the command link.**</span></span> <span data-ttu-id="4ee3b-337">只有當您無法讓命令連結一目了然時，才使用補充說明。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-337">Use a supplemental explanation only when you can't make a command link self-explanatory.</span></span> <span data-ttu-id="4ee3b-338">提供一個命令連結的補充說明，並不表示您必須提供這些連結。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-338">Providing a supplemental explanation for one command link doesn't mean that you have to provide them for all.</span></span>
-   <span data-ttu-id="4ee3b-339">**專注補充說明，協助使用者做出正確的決策。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-339">**Focus supplemental explanations on helping users make the right decision.**</span></span> <span data-ttu-id="4ee3b-340">省略不會影響選擇的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-340">Omit details that don't affect the choice.</span></span> <span data-ttu-id="4ee3b-341">補充說明不一定是將會發生什麼事的完整規格。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-341">The supplemental explanations don't have to be a complete specification of what will happen.</span></span>
-   <span data-ttu-id="4ee3b-342">**使用平行措辭和最多三行文字。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-342">**Use parallel phrasing and at most three lines of text.**</span></span> <span data-ttu-id="4ee3b-343">詳細的補充說明不一定需要閱讀。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-343">Long supplemental explanations discourage reading and shouldn't be necessary.</span></span>
-   <span data-ttu-id="4ee3b-344">**使用完整的句子和結束標點符號。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-344">**Use complete sentences and ending punctuation.**</span></span>

<span data-ttu-id="4ee3b-345">**命令連結群組標籤**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-345">**Command link group labels**</span></span>

-   <span data-ttu-id="4ee3b-346">**請勿使用群組標籤。**</span><span class="sxs-lookup"><span data-stu-id="4ee3b-346">**Don't use group labels.**</span></span> <span data-ttu-id="4ee3b-347">主要指示可作為命令連結的群組標籤。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-347">Main instructions act as the group label for command links.</span></span>

## <a name="documentation"></a><span data-ttu-id="4ee3b-348">文件</span><span class="sxs-lookup"><span data-stu-id="4ee3b-348">Documentation</span></span>

<span data-ttu-id="4ee3b-349">參考命令連結時：</span><span class="sxs-lookup"><span data-stu-id="4ee3b-349">When referring to command links:</span></span>

-   <span data-ttu-id="4ee3b-350">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-350">Use the exact label text, including its capitalization, but don't include the access key underscore.</span></span>
-   <span data-ttu-id="4ee3b-351">如果標籤包含物件名稱，請省略物件名稱或使用預留位置文字。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-351">If the label includes an object name, either omit the object name or use placeholder text.</span></span>
-   <span data-ttu-id="4ee3b-352">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-352">To describe the user interaction, use click.</span></span>
-   <span data-ttu-id="4ee3b-353">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-353">When possible, format the label using bold text.</span></span> <span data-ttu-id="4ee3b-354">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-354">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="4ee3b-355">**範例：** 若要複製圖片，請按一下 [ **複製並取代**]。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-355">**Examples:** To copy the picture, click **Copy and Replace**.</span></span>

<span data-ttu-id="4ee3b-356">按一下 **[重設網路介面卡**]。</span><span class="sxs-lookup"><span data-stu-id="4ee3b-356">Click **Reset the network adapter**.</span></span> <span data-ttu-id="4ee3b-357">針對標示為「重設網路介面卡 *配接器名稱*」的命令連結， (。 ) </span><span class="sxs-lookup"><span data-stu-id="4ee3b-357">(For a command link labeled "Reset the network adaptor *adaptor name*".)</span></span>

 

