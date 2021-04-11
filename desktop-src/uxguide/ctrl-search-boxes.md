---
title: 搜尋方塊
description: 使用搜尋方塊，使用者可以藉由篩選或反白顯示相符專案，快速找出一組大型資料中的特定物件或文字。
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103945574"
---
# <a name="search-boxes"></a><span data-ttu-id="98599-103">搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="98599-103">Search Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="98599-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="98599-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="98599-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="98599-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="98599-106">使用搜尋方塊，使用者可以藉由篩選或反白顯示相符專案，快速找出一組大型資料中的特定物件或文字。</span><span class="sxs-lookup"><span data-stu-id="98599-106">With a Search box, users can quickly locate specific objects or text within a large set of data by filtering or highlighting matches.</span></span> <span data-ttu-id="98599-107">沒有標準的搜尋控制項，但您應該努力讓程式的搜尋功能與 Windows 的功能保持一致。</span><span class="sxs-lookup"><span data-stu-id="98599-107">There is no standard search control, but you should strive to make your program's search features consistent with those of Windows.</span></span>

<span data-ttu-id="98599-108">搜尋的類型有兩種：</span><span class="sxs-lookup"><span data-stu-id="98599-108">There are two types of searches:</span></span>

-   <span data-ttu-id="98599-109">立即 **搜尋**，結果會立即顯示為使用者類型。</span><span class="sxs-lookup"><span data-stu-id="98599-109">**Instant search**, where the results are displayed immediately as the user types.</span></span> <span data-ttu-id="98599-110">不需要按一下按鈕，因此放大鏡搜尋符號會顯示為圖形，而不是按鈕。</span><span class="sxs-lookup"><span data-stu-id="98599-110">No button needs to be clicked, so the magnifying glass search symbol is shown as a graphic, not a button.</span></span>

    ![顯示即時搜尋方塊的螢幕擷取畫面，其中包含指向搜尋方塊的 [提示] 標注，以及指向放大鏡圖形的 [搜尋符號] 標注。](images/ctrl-search-boxes-image1.png)

    <span data-ttu-id="98599-112">使用立即搜尋的一般搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-112">A typical Search box using Instant search.</span></span> <span data-ttu-id="98599-113">每次擊鍵時都會自動執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-113">Search is automatically executed on every keystroke.</span></span>

-   <span data-ttu-id="98599-114">**一般搜尋**，在使用者按一下 [搜尋] 按鈕時執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-114">**Regular search**, where a search is performed when the user clicks the search button.</span></span> <span data-ttu-id="98599-115">放大鏡搜尋符號會顯示在按鈕上。</span><span class="sxs-lookup"><span data-stu-id="98599-115">The magnifying glass search symbol is shown on a button.</span></span>

    ![<span data-ttu-id="98599-116">一般搜尋方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="98599-116">screen shot of a regular search box</span></span> ](images/ctrl-search-boxes-image2.png)

    <span data-ttu-id="98599-117">使用一般搜尋的一般搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-117">A typical Search box using regular search.</span></span> <span data-ttu-id="98599-118">使用者按一下按鈕來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-118">Users click a button to perform the search.</span></span>

    <span data-ttu-id="98599-119">您可以為您的使用者提供一種或兩種搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="98599-119">You can provide either or both kinds of search options for your users.</span></span>

## <a name="is-this-the-right-control"></a><span data-ttu-id="98599-120">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="98599-120">Is this the right control?</span></span>

<span data-ttu-id="98599-121">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="98599-121">To decide, consider these questions:</span></span>

-   <span data-ttu-id="98599-122">**是否有特定物件難以尋找？**</span><span class="sxs-lookup"><span data-stu-id="98599-122">**Are specific objects difficult to find?**</span></span> <span data-ttu-id="98599-123">發生的時機為：</span><span class="sxs-lookup"><span data-stu-id="98599-123">This can happen when:</span></span>
    -   <span data-ttu-id="98599-124">有許多物件。</span><span class="sxs-lookup"><span data-stu-id="98599-124">There are many objects.</span></span>
    -   <span data-ttu-id="98599-125">物件不是位於單一位置。</span><span class="sxs-lookup"><span data-stu-id="98599-125">The objects aren't located in a single location.</span></span> <span data-ttu-id="98599-126">搜尋特別適用于在樹狀結構中尋找物件。</span><span class="sxs-lookup"><span data-stu-id="98599-126">Search is especially useful for finding objects in trees.</span></span>
    -   <span data-ttu-id="98599-127">搜尋資料很難找到 (例如，中繼資料) 。</span><span class="sxs-lookup"><span data-stu-id="98599-127">The search data is difficult to find (for example, metadata).</span></span>
-   <span data-ttu-id="98599-128">**使用者是否需要尋找檔中的特定文字？**</span><span class="sxs-lookup"><span data-stu-id="98599-128">**Do users need to find specific text within documents?**</span></span>
-   <span data-ttu-id="98599-129">**您的功能是否會在五秒內傳回相關的搜尋結果？**</span><span class="sxs-lookup"><span data-stu-id="98599-129">**Does your feature return relevant search results within five seconds?**</span></span> <span data-ttu-id="98599-130">如果沒有，您可以提供搜尋功能，但會使用替代的設計來提供可見的意見反應，以容納長時間執行的搜尋，例如搜尋對話方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-130">If not, you can provide a search feature, but use an alternative design that gives visible feedback to accommodate long-running searches, such as a search dialog box.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="98599-131">設計概念</span><span class="sxs-lookup"><span data-stu-id="98599-131">Design concepts</span></span>

<span data-ttu-id="98599-132">在許多案例中，搜尋是很重要的第一步：使用者必須先尋找物件才能使用它們。</span><span class="sxs-lookup"><span data-stu-id="98599-132">Searching is a crucial first step in many scenarios: Users must find objects before they can use them.</span></span> <span data-ttu-id="98599-133">使用者會在越來越大的硬碟上儲存越來越多的物件，但是流覽物件無法妥善調整。</span><span class="sxs-lookup"><span data-stu-id="98599-133">Users are saving more and more objects on increasingly larger hard disks, but browsing for objects doesn't scale well.</span></span> <span data-ttu-id="98599-134">搜尋必須是使用者體驗的簡單、一致、可靠的部分。</span><span class="sxs-lookup"><span data-stu-id="98599-134">Search must be a simple, consistent, reliable part of the user experience.</span></span>

<span data-ttu-id="98599-135">Windows 中的搜尋方塊：</span><span class="sxs-lookup"><span data-stu-id="98599-135">Search boxes in Windows:</span></span>

-   <span data-ttu-id="98599-136">是所有 Explorer 視窗的一部分，因此很容易找到和辨識。</span><span class="sxs-lookup"><span data-stu-id="98599-136">Are part of all Explorer windows, so they are easy to find and recognize.</span></span>
-   <span data-ttu-id="98599-137">具有一致的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="98599-137">Have consistent appearance and behavior.</span></span>
-   <span data-ttu-id="98599-138">既有效率又快速，提供立即搜尋模式的即時結果。</span><span class="sxs-lookup"><span data-stu-id="98599-138">Are efficient and fast, giving instant results in Instant search mode.</span></span>

<span data-ttu-id="98599-139">在下列位置中，Windows 會使用搜尋方塊：</span><span class="sxs-lookup"><span data-stu-id="98599-139">A Search box is used in Windows in these places:</span></span>

-   <span data-ttu-id="98599-140">總管</span><span class="sxs-lookup"><span data-stu-id="98599-140">Explorers</span></span>
-   <span data-ttu-id="98599-141">體驗 (Microsoft Windows Media Player、Windows 影像中心、Windows Internet Explorer) </span><span class="sxs-lookup"><span data-stu-id="98599-141">Experiences (Microsoft Windows Media Player, Windows Photo Gallery, Windows Internet Explorer)</span></span>
-   <span data-ttu-id="98599-142">[開始] 功能表 (尋找程式和最近使用的檔案) </span><span class="sxs-lookup"><span data-stu-id="98599-142">Start menu (to find programs and recent files)</span></span>
-   <span data-ttu-id="98599-143">主控台首頁] (尋找 [控制台] 專案和工作) </span><span class="sxs-lookup"><span data-stu-id="98599-143">Control Panel home page (to find control panel items and tasks)</span></span>
-   <span data-ttu-id="98599-144">協助 (尋找相關說明主題) </span><span class="sxs-lookup"><span data-stu-id="98599-144">Help (to find relevant Help topics)</span></span>

### <a name="look-and-feel"></a><span data-ttu-id="98599-145">外觀與風格</span><span class="sxs-lookup"><span data-stu-id="98599-145">Look and feel</span></span>

<span data-ttu-id="98599-146">在 Windows 中搜尋的風格，藉由支援立即搜尋來大幅增強。</span><span class="sxs-lookup"><span data-stu-id="98599-146">The feel of Search in Windows is significantly enhanced by supporting Instant search.</span></span> <span data-ttu-id="98599-147">有了立即的結果，讓 Windows 感覺更強大且更直接。</span><span class="sxs-lookup"><span data-stu-id="98599-147">Having instant results makes Windows feel more powerful and direct.</span></span>

<span data-ttu-id="98599-148">在 Windows 檔案總管和應用程式視窗中，如果是增補進入點，則搜尋位於右上角。</span><span class="sxs-lookup"><span data-stu-id="98599-148">In Windows Explorer and application windows, Search is located in the upper-right corner if it is a supplemental entry point.</span></span> <span data-ttu-id="98599-149">在此情況下，當使用者在視窗中找不到想要的內容時，就會尋找搜尋機制。</span><span class="sxs-lookup"><span data-stu-id="98599-149">In this case, users look for a search mechanism when they don't find what they are looking for in the window.</span></span> <span data-ttu-id="98599-150">但是，如果搜尋是主要進入點，則會在視窗的頂端置中。</span><span class="sxs-lookup"><span data-stu-id="98599-150">However, if Search is the primary entry point, it is centered at the top of the window.</span></span>

<span data-ttu-id="98599-151">[搜尋] 按鈕會以視覺化方式連線到搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-151">The Search button is visually connected to a Search box.</span></span> <span data-ttu-id="98599-152">若要將空間最小化，請在搜尋方塊中使用選擇性的 [提示](ctrl-text-boxes.md) ，而不是使用標籤。</span><span class="sxs-lookup"><span data-stu-id="98599-152">To minimize space, an optional [prompt](ctrl-text-boxes.md) is used inside a Search box instead of a label.</span></span> <span data-ttu-id="98599-153">提示可能是指令 (例如，輸入搜尋) 或指出搜尋的範圍 (例如，搜尋) 的圖片。</span><span class="sxs-lookup"><span data-stu-id="98599-153">The prompt may be an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>

![<span data-ttu-id="98599-154">立即搜尋方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="98599-154">screen shot of an instant search box</span></span> ](images/ctrl-search-boxes-image3.png)

<span data-ttu-id="98599-155">如果沒有標籤和個別按鈕，Windows 中的即時搜尋就會有輕量的外觀。</span><span class="sxs-lookup"><span data-stu-id="98599-155">Without labels and separate buttons, Instant search in Windows has a lightweight look.</span></span>

<span data-ttu-id="98599-156">執行成功搜尋會建立搜尋結果的虛擬頁面，並將其新增至後端堆疊和位址列。</span><span class="sxs-lookup"><span data-stu-id="98599-156">Performing a successful search creates a virtual page of the search results and adds it to the Back stack and Address bar.</span></span> <span data-ttu-id="98599-157">使用者有數種方式可還原原始頁面，並清除搜尋方塊，包括按一下 [上一步]、按一下網址列中的原始頁面、按下 Esc 或清除 [搜尋] 方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-157">Users have several ways to restore the original page and clear a Search box, including clicking Back, clicking the original page in the Address bar, pressing Esc, or clearing the Search box.</span></span>

<span data-ttu-id="98599-158">使用者也可以直接清除 [搜尋] 方塊，而不還原上一頁的結果。</span><span class="sxs-lookup"><span data-stu-id="98599-158">Users can also simply clear the Search box without restoring a previous page of results.</span></span> <span data-ttu-id="98599-159">在 [立即搜尋] 模式中，當使用者開始鍵入之後，會出現 [清除] 按鈕;"x" 會取代放大鏡搜尋符號。</span><span class="sxs-lookup"><span data-stu-id="98599-159">In Instant search mode, a clear button appears after the user starts typing; an "x" replaces the magnifying glass search symbol.</span></span> <span data-ttu-id="98599-160">停留時，"x" 會取得按鈕外觀，且可以按一下。</span><span class="sxs-lookup"><span data-stu-id="98599-160">On hover, the "x" gets a button look and can be clicked.</span></span>

![<span data-ttu-id="98599-161">具有 ' x ' 圖示之搜尋方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="98599-161">screen shot of a search box with an 'x' icon</span></span> ](images/ctrl-search-boxes-image4.png)

<span data-ttu-id="98599-162">使用者可以按一下控制項右端的 [x] 來清除搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-162">The user can clear the Search box by clicking "x" at the right end of the control.</span></span>

<span data-ttu-id="98599-163">在一般搜尋模式中，[清除] 按鈕是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="98599-163">In regular search mode, the clear button is optional.</span></span> <span data-ttu-id="98599-164">例如，如果搜尋需要很長的時間才能完成，使用者可能會發現它很有用。</span><span class="sxs-lookup"><span data-stu-id="98599-164">Users may find it useful, for example, if a search is taking a long time to complete.</span></span> <span data-ttu-id="98599-165">使用者可以按一下 "x" 來停止搜尋進行中。</span><span class="sxs-lookup"><span data-stu-id="98599-165">Users can click the "x" to stop the search in progress.</span></span> <span data-ttu-id="98599-166">如果搜尋已完成，使用者可以按一下 "x" 來清除搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-166">If a search has already completed, users can click the "x" to clear the Search box.</span></span>

## <a name="guidelines"></a><span data-ttu-id="98599-167">指導方針</span><span class="sxs-lookup"><span data-stu-id="98599-167">Guidelines</span></span>

### <a name="location"></a><span data-ttu-id="98599-168">Location</span><span class="sxs-lookup"><span data-stu-id="98599-168">Location</span></span>

-   <span data-ttu-id="98599-169">若為應用程式視窗，請在右上角尋找 [搜尋]。</span><span class="sxs-lookup"><span data-stu-id="98599-169">For application windows, locate Search in the upper-right corner.</span></span>
-   <span data-ttu-id="98599-170">若為快顯視窗，請在最適合且方便的地方尋找搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-170">For popup windows, locate Search wherever is most sensible and convenient.</span></span>
-   <span data-ttu-id="98599-171">**例外狀況：** 如果搜尋通常是使用者在視窗 (主要進入點) 的第一件事，請將其置中在視窗的頂端。</span><span class="sxs-lookup"><span data-stu-id="98599-171">**Exception:** If Search is usually the first thing users do in a window (the primary entry point), center it at the top of the window.</span></span>

### <a name="look"></a><span data-ttu-id="98599-172">看</span><span class="sxs-lookup"><span data-stu-id="98599-172">Look</span></span>

-   <span data-ttu-id="98599-173">使用標準搜尋按鈕圖形。</span><span class="sxs-lookup"><span data-stu-id="98599-173">Use the standard search button graphics.</span></span> <span data-ttu-id="98599-174">有三個版本：</span><span class="sxs-lookup"><span data-stu-id="98599-174">There are three versions:</span></span>
    -   <span data-ttu-id="98599-175">**只有在滑鼠停留) 上 (沒有按鈕時，才會顯示放大鏡搜尋符號。**</span><span class="sxs-lookup"><span data-stu-id="98599-175">**Magnifying glass search symbol only (no button on hover).**</span></span> <span data-ttu-id="98599-176">用於立即搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-176">Use for Instant search.</span></span>
    -   <span data-ttu-id="98599-177">**放大鏡搜尋符號與按鈕。**</span><span class="sxs-lookup"><span data-stu-id="98599-177">**Magnifying glass search symbol with button.**</span></span> <span data-ttu-id="98599-178">當您需要按一下按鈕來開始搜尋時，請使用。</span><span class="sxs-lookup"><span data-stu-id="98599-178">Use when button needs to be clicked to start the search.</span></span>
    -   <span data-ttu-id="98599-179">**具有按鈕和下拉箭號的放大鏡搜尋符號。**</span><span class="sxs-lookup"><span data-stu-id="98599-179">**Magnifying glass search symbol with button and drop-down arrow.**</span></span> <span data-ttu-id="98599-180">當使用者可以變更範圍或有其他設定可供使用時，請新增下拉式箭號。</span><span class="sxs-lookup"><span data-stu-id="98599-180">Add a drop-down arrow when users can change the scope or when other settings are available.</span></span>
        -   <span data-ttu-id="98599-181">若為立即搜尋，請只使用下拉式箭號，並在滑鼠停留時顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="98599-181">For Instant search, use a drop-down arrow only, and show a button on hover.</span></span>
        -   <span data-ttu-id="98599-182">針對一般搜尋，請在按鈕上顯示下拉箭號。</span><span class="sxs-lookup"><span data-stu-id="98599-182">For regular search, show the drop-down arrow on a button.</span></span>

![<span data-ttu-id="98599-183">處於不同狀態的即時搜尋方塊圖</span><span class="sxs-lookup"><span data-stu-id="98599-183">figure of instant search boxes in different states</span></span> ](images/ctrl-search-boxes-image5.png)

<span data-ttu-id="98599-184">立即搜尋的視覺規格。</span><span class="sxs-lookup"><span data-stu-id="98599-184">Visual specifications for Instant search.</span></span>

![<span data-ttu-id="98599-185">不同狀態之一般搜尋方塊的圖</span><span class="sxs-lookup"><span data-stu-id="98599-185">figure of regular search boxes in different states</span></span> ](images/ctrl-search-boxes-image6.png)

<span data-ttu-id="98599-186">一般搜尋的視覺規格。</span><span class="sxs-lookup"><span data-stu-id="98599-186">Visual specifications for regular search.</span></span>

-   <span data-ttu-id="98599-187">請勿使用標籤;請改用選用的提示。</span><span class="sxs-lookup"><span data-stu-id="98599-187">Don't use a label; use an optional prompt instead.</span></span> <span data-ttu-id="98599-188">如果使用者傾向于假設搜尋是一般檔案搜尋，請使用提示來提供範圍。</span><span class="sxs-lookup"><span data-stu-id="98599-188">If users tend to assume that the search is a generic file search, use the prompt to give the scope.</span></span> <span data-ttu-id="98599-189">否則，請使用類型來搜尋或類似的簡潔片語。</span><span class="sxs-lookup"><span data-stu-id="98599-189">Otherwise, use Type to search or a similar, concise phrase.</span></span>

    ![<span data-ttu-id="98599-190">[要搜尋的類型] 提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="98599-190">screen shot of 'type to search' prompt</span></span> ](images/ctrl-search-boxes-image7.png)

    ![<span data-ttu-id="98599-191">[搜尋所有小工具] 提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="98599-191">screen shot of 'search all gadgets' prompt</span></span> ](images/ctrl-search-boxes-image8.png)

    <span data-ttu-id="98599-192">在這些範例中，簡短的文字提示可協助使用者使用搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-192">In these examples, brief textual prompts help users work with Search.</span></span>

### <a name="interaction"></a><span data-ttu-id="98599-193">互動</span><span class="sxs-lookup"><span data-stu-id="98599-193">Interaction</span></span>

-   <span data-ttu-id="98599-194">**在輸入焦點上，自動選取任何先前輸入的文字。**</span><span class="sxs-lookup"><span data-stu-id="98599-194">**On input focus, automatically select any previously entered text.**</span></span> <span data-ttu-id="98599-195">這麼做可讓使用者藉由輸入來輸入新的搜尋，或使用方向鍵來定位插入號來修改先前的搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-195">Doing so allows users to enter a new search by typing, or to modify the previous search by positioning the caret using the arrow keys.</span></span>

    ![<span data-ttu-id="98599-196">具有反白顯示文字之搜尋方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="98599-196">screen shot of search box with highlighted text</span></span> ](images/ctrl-search-boxes-image9.png)

    <span data-ttu-id="98599-197">在此範例中，會在輸入焦點上選取先前輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="98599-197">In this example, previously entered text is selected on input focus.</span></span>

-   <span data-ttu-id="98599-198">**將 [搜尋] 方塊的鍵盤快速鍵指派為 Ctrl + E。**</span><span class="sxs-lookup"><span data-stu-id="98599-198">**Assign the keyboard shortcut for the Search box to be Ctrl+E.**</span></span>

### <a name="functionality"></a><span data-ttu-id="98599-199">功能</span><span class="sxs-lookup"><span data-stu-id="98599-199">Functionality</span></span>

-   <span data-ttu-id="98599-200">**盡可能支援立即搜尋。**</span><span class="sxs-lookup"><span data-stu-id="98599-200">**Support Instant search whenever possible.**</span></span> <span data-ttu-id="98599-201">如果有一般搜尋需要額外等候時間的情況，請提供一般和立即搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-201">Provide both regular and Instant searches if there are scenarios where regular searching is worth the extra wait time.</span></span>
-   <span data-ttu-id="98599-202">一般搜尋必須在五秒內傳回相關的結果，而立即搜尋必須在2秒內傳回結果。</span><span class="sxs-lookup"><span data-stu-id="98599-202">Regular searches must return relevant results within five seconds and Instant search must return results within two seconds.</span></span> <span data-ttu-id="98599-203">在此之後，只要程式有回應，而且使用者可以執行其他工作，搜尋就會繼續在較短的時間內填滿較不相關的結果。</span><span class="sxs-lookup"><span data-stu-id="98599-203">After this point, Search may continue to fill in less relevant results over time as long as the program is responsive and users can perform other tasks.</span></span> <span data-ttu-id="98599-204">您可能必須編制搜尋資料的索引，以確保此回應性。</span><span class="sxs-lookup"><span data-stu-id="98599-204">You may have to index your search data to ensure this responsiveness.</span></span>
-   <span data-ttu-id="98599-205">如果您同時提供一般和立即搜尋模式，則即時搜尋結果必須是一般搜尋結果的子集。</span><span class="sxs-lookup"><span data-stu-id="98599-205">If you provide both regular and Instant search modes, the Instant search results must be a subset of the regular search results.</span></span>
-   <span data-ttu-id="98599-206">所有搜尋都是首碼型 (沒有搜尋) 的子字串或尾碼。</span><span class="sxs-lookup"><span data-stu-id="98599-206">All searching is prefix-based (no substring or suffix searching).</span></span> <span data-ttu-id="98599-207">使用尾端萬用字元是選擇性的，不會影響結果。</span><span class="sxs-lookup"><span data-stu-id="98599-207">The use of trailing wildcard characters is optional and doesn't affect the results.</span></span> <span data-ttu-id="98599-208">如果輸入多個單字，請使用或搜尋。</span><span class="sxs-lookup"><span data-stu-id="98599-208">If multiple words are entered, use OR searching.</span></span>
-   <span data-ttu-id="98599-209">成功搜尋會將包含搜尋結果的虛擬頁面新增至後端堆疊和位址列。</span><span class="sxs-lookup"><span data-stu-id="98599-209">A successful search adds a virtual page with the search results to the Back stack and Address bar.</span></span> <span data-ttu-id="98599-210">單一虛擬頁面中有多個搜尋結果，所以按一下 [上一步] 一律會傳回原始頁面。</span><span class="sxs-lookup"><span data-stu-id="98599-210">Multiple searches result in a single virtual page, so clicking Back always returns the original page.</span></span>
-   <span data-ttu-id="98599-211">如果需要調整規模，請依相關性排名搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="98599-211">If necessary for scale, rank the search results by relevance.</span></span>
-   <span data-ttu-id="98599-212">空白搜尋會傳回原始頁面。</span><span class="sxs-lookup"><span data-stu-id="98599-212">A blank search returns the original page.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="98599-213">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="98599-213">Recommended sizing and spacing</span></span>

![<span data-ttu-id="98599-214">立即搜尋方塊調整大小和間距的圖表</span><span class="sxs-lookup"><span data-stu-id="98599-214">figure of instant search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image10.png)

<span data-ttu-id="98599-215">立即搜尋的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="98599-215">Recommended sizing and spacing for Instant search.</span></span>

![<span data-ttu-id="98599-216">標準搜尋方塊調整大小和間距的圖表</span><span class="sxs-lookup"><span data-stu-id="98599-216">figure of regular search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image11.png)

<span data-ttu-id="98599-217">一般搜尋的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="98599-217">Recommended sizing and spacing for regular search.</span></span>

## <a name="text"></a><span data-ttu-id="98599-218">Text</span><span class="sxs-lookup"><span data-stu-id="98599-218">Text</span></span>

-   <span data-ttu-id="98599-219">針對 [搜尋] 方塊中的提示文字，請將其設為指示 (例如，輸入以搜尋) 或指出搜尋的範圍 (例如，搜尋) 的圖片。</span><span class="sxs-lookup"><span data-stu-id="98599-219">For the wording of the prompt in the Search box, either make it an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>
-   <span data-ttu-id="98599-220">提示文字應簡短。</span><span class="sxs-lookup"><span data-stu-id="98599-220">Prompt text should be brief.</span></span> <span data-ttu-id="98599-221">單一單字或簡短片語應已足夠。</span><span class="sxs-lookup"><span data-stu-id="98599-221">A single word or short phrase should suffice.</span></span>
-   <span data-ttu-id="98599-222">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="98599-222">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="98599-223">請勿使用結尾標點符號或省略號。</span><span class="sxs-lookup"><span data-stu-id="98599-223">Don't use ending punctuation or ellipsis.</span></span>

## <a name="documentation"></a><span data-ttu-id="98599-224">文件</span><span class="sxs-lookup"><span data-stu-id="98599-224">Documentation</span></span>

-   <span data-ttu-id="98599-225">請將此控制項稱為搜尋方塊。</span><span class="sxs-lookup"><span data-stu-id="98599-225">Refer to this control as the Search box.</span></span> <span data-ttu-id="98599-226">將第一個單字的初始字母大寫：不要將方塊的初始字母大寫。</span><span class="sxs-lookup"><span data-stu-id="98599-226">Capitalize the initial letter of the first word; don't capitalize the initial letter of box.</span></span>
-   <span data-ttu-id="98599-227">請以立即搜尋和一般搜尋的形式來參考這兩種搜尋類型。</span><span class="sxs-lookup"><span data-stu-id="98599-227">Refer to the two types of search as Instant search and regular search.</span></span> <span data-ttu-id="98599-228">將立即搜尋的初始字母大寫：請勿將一般搜尋的初始字母變成大寫。</span><span class="sxs-lookup"><span data-stu-id="98599-228">Capitalize the initial letter of Instant search; don't capitalize the initial letter of regular search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98599-229">相關主題</span><span class="sxs-lookup"><span data-stu-id="98599-229">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98599-230">詞彙</span><span class="sxs-lookup"><span data-stu-id="98599-230">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 