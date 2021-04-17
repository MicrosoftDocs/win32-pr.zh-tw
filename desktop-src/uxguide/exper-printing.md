---
title: '列印 (設計基本概念) '
description: 列印是使用者在紙張上的體驗。 它很容易忽略，但它是整體使用者體驗的重要部分。
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a98bf29da1169ad43a3b1d16ab52298d62612037
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560988"
---
# <a name="printing-design-basics"></a><span data-ttu-id="18d18-104">列印 (設計基本概念) </span><span class="sxs-lookup"><span data-stu-id="18d18-104">Printing (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="18d18-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="18d18-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="18d18-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="18d18-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="18d18-107">列印是使用者在紙張上的體驗。</span><span class="sxs-lookup"><span data-stu-id="18d18-107">Printing is the user experience on paper.</span></span> <span data-ttu-id="18d18-108">它很容易忽略，但它是整體使用者體驗的重要部分。</span><span class="sxs-lookup"><span data-stu-id="18d18-108">It's easy to overlook, but it is an important part of the overall user experience.</span></span>

<span data-ttu-id="18d18-109">在本文中， *列印* 是指紙上的使用者體驗，其中的輸出會被導向紙張而非螢幕顯示。</span><span class="sxs-lookup"><span data-stu-id="18d18-109">In this article, *printing* refers to the user experience on paper, where output is directed to paper instead of the screen display.</span></span> <span data-ttu-id="18d18-110">*印表機易記的格式* 是指程式可以對螢幕顯示輸出進行的修改，使其更適合用於紙張輸出。</span><span class="sxs-lookup"><span data-stu-id="18d18-110">*Printer-friendly format* refers to modifications the program can make to screen display output that make it more suitable for paper output.</span></span>

<span data-ttu-id="18d18-111">儘管預期的預測會導致「完全紙張辦公室」，但我們現在會盡可能地列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-111">Despite the prediction that computing would result in the "paperless office," surprisingly enough we print now as much as ever.</span></span> <span data-ttu-id="18d18-112">我們發佈了 Microsoft PowerPoint 簡報投影片的硬拷貝，我們會在線上閱讀我們所探索到的文章，但稍後想要更仔細研究，我們會列印試算表中所收到的重要電子郵件或繼續，依此類推。</span><span class="sxs-lookup"><span data-stu-id="18d18-112">We distribute hard copies of Microsoft PowerPoint presentation decks, we print articles we discover online but wish to research more carefully later, we print important e-mails or resumes we have received in electronic form, and so on.</span></span> <span data-ttu-id="18d18-113">雖然在設計使用者介面時很容易忽略列印，但請記住，列印是整體使用者體驗的重要部分。</span><span class="sxs-lookup"><span data-stu-id="18d18-113">While it's easy to overlook printing when designing a user interface, remember that printing is an important part of the overall user experience.</span></span>

<span data-ttu-id="18d18-114">**注意：** 與 [通用對話](win-common-dlg.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="18d18-114">**Note:** Guidelines related to [common dialogs](win-common-dlg.md) are presented in a separate article.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="18d18-115">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="18d18-115">Is this the right user interface?</span></span>

<span data-ttu-id="18d18-116">若要決定您的程式是否需要支援列印，請考慮下列問題：</span><span class="sxs-lookup"><span data-stu-id="18d18-116">To decide if your program needs to support printing, consider these questions:</span></span>

-   <span data-ttu-id="18d18-117">**您所設計的程式類型為何？**</span><span class="sxs-lookup"><span data-stu-id="18d18-117">**What type of program are you designing?**</span></span> <span data-ttu-id="18d18-118">程式類型是適當的列印支援層級的良好指標。</span><span class="sxs-lookup"><span data-stu-id="18d18-118">The program type is a good indicator of the appropriate level of printing support.</span></span> <span data-ttu-id="18d18-119">檔和影像建立、觀賞和流覽程式都需要絕佳的列印支援，而其他類型的程式可能只需要較低的列印支援。</span><span class="sxs-lookup"><span data-stu-id="18d18-119">Document and image creation, viewing, and browsing programs need excellent printing support, whereas other types of programs may only need printing support to a lesser degree.</span></span> <span data-ttu-id="18d18-120">如需程式類型清單的 (，請參閱本文的 [列印模式](#printing-patterns) 一節。 ) </span><span class="sxs-lookup"><span data-stu-id="18d18-120">(For a list of program types, see the [Printing patterns](#printing-patterns) section of this article.)</span></span>
-   <span data-ttu-id="18d18-121">**此程式是否用於可從直接紙張輸出受益的案例？**</span><span class="sxs-lookup"><span data-stu-id="18d18-121">**Is the program used in scenarios that benefit from direct paper output?**</span></span> <span data-ttu-id="18d18-122">如果是這樣，將列印支援新增至您的程式會比要求使用者將資料複製到另一個要列印的程式更方便。</span><span class="sxs-lookup"><span data-stu-id="18d18-122">If so, it's more convenient to add printing support to your program than to require users to copy the data to another program to print.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="18d18-123">設計概念</span><span class="sxs-lookup"><span data-stu-id="18d18-123">Design concepts</span></span>

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a><span data-ttu-id="18d18-124">設計程式以排除不必要的列印</span><span class="sxs-lookup"><span data-stu-id="18d18-124">Design your program to eliminate unnecessary printing</span></span>

<span data-ttu-id="18d18-125">有許多原因會讓使用者列印一些不錯的原因，有些則比較少。</span><span class="sxs-lookup"><span data-stu-id="18d18-125">There are many reasons why users need to print some which are good, some which are less so.</span></span> <span data-ttu-id="18d18-126">使用者應該列印，因為他們需要，而不是因為他們必須這樣做。</span><span class="sxs-lookup"><span data-stu-id="18d18-126">Users should print because they want to, not because they must.</span></span> <span data-ttu-id="18d18-127">要求使用者列印可能是遺失功能的正負號。</span><span class="sxs-lookup"><span data-stu-id="18d18-127">Requiring users to print can be a sign of missing features.</span></span> <span data-ttu-id="18d18-128">例如，在過去的使用者必須列印檔案才能提出批註並建議修訂，但現在使用者可以直接在 Microsoft Word 檔中執行這些工作。</span><span class="sxs-lookup"><span data-stu-id="18d18-128">For example, in the past users had to print documents in order to make comments and suggest revisions, but now users can do these tasks directly within Microsoft Word documents.</span></span> <span data-ttu-id="18d18-129">**請檢查您的程式與列印相關的案例，並確定可能的最大範圍，確定列印的需求是選擇性的，而不是遺失功能的結果。**</span><span class="sxs-lookup"><span data-stu-id="18d18-129">**Review your program's scenarios that involve printing, and to the best extent possible, make sure that the need to print is optional and not the result of missing features.**</span></span>

<span data-ttu-id="18d18-130">也值得記住，節省紙和筆墨等資源是很有説明的，而且長期的組織會節省成本。</span><span class="sxs-lookup"><span data-stu-id="18d18-130">It's also worth remembering that conserving resources like paper and ink is helpful environmentally and saves organizations money in the long run.</span></span>

### <a name="understand-the-differences-between-screen-display-and-print"></a><span data-ttu-id="18d18-131">瞭解螢幕顯示和列印之間的差異</span><span class="sxs-lookup"><span data-stu-id="18d18-131">Understand the differences between screen display and print</span></span>

<span data-ttu-id="18d18-132">雖然顯示器輸出和列印之間有許多相似之處，但也有許多差異。</span><span class="sxs-lookup"><span data-stu-id="18d18-132">While there are many similarities between display output and printing, there are many differences as well.</span></span> <span data-ttu-id="18d18-133">列印輸出：</span><span class="sxs-lookup"><span data-stu-id="18d18-133">Print output:</span></span>

-   <span data-ttu-id="18d18-134">**具有高 DPI。**</span><span class="sxs-lookup"><span data-stu-id="18d18-134">**Has a high dpi.**</span></span> <span data-ttu-id="18d18-135">顯示輸出通常是96或120點（每英寸 (DPI) ），而印表機輸出通常是 600 DPI 或更高。</span><span class="sxs-lookup"><span data-stu-id="18d18-135">Display output is usually at 96 or 120 dots per inch (dpi), whereas printer output is usually at 600 dpi or greater.</span></span>
-   <span data-ttu-id="18d18-136">**有不同的最佳字型。**</span><span class="sxs-lookup"><span data-stu-id="18d18-136">**Has different optimal fonts.**</span></span> <span data-ttu-id="18d18-137">雖然設計完善的字型適用于顯示和列印，但在大量文字的高解析度上，serif 字型比使用 sans serif 字型更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="18d18-137">While well-designed fonts work well for both display and print, serif fonts are more readable at high resolutions for large amounts of text than sans serif fonts.</span></span> <span data-ttu-id="18d18-138">因此，主要用於列印的大量文字應使用 serif 字型，而主要用於顯示的文字則應使用「sans serif」字型。</span><span class="sxs-lookup"><span data-stu-id="18d18-138">Thus, large amounts of text primarily intended for print should use a serif font, whereas text primarily intended for display should use a sans serif font.</span></span> <span data-ttu-id="18d18-139">如需詳細資訊， [請參閱 (](vis-fonts.md) Segoe UI) 的字型。</span><span class="sxs-lookup"><span data-stu-id="18d18-139">For more information, see [Fonts](vis-fonts.md) (Segoe UI).</span></span>
-   <span data-ttu-id="18d18-140">**具有外觀比例。**</span><span class="sxs-lookup"><span data-stu-id="18d18-140">**Has aspect ratio.**</span></span> <span data-ttu-id="18d18-141">顯示器通常 (4:3 或 5:4) 的 [外觀比例](glossary.md) 很低，而列印會使用高外觀比例 (8.5：11或1：以) 的標準頁面大小為基礎的1.4142。</span><span class="sxs-lookup"><span data-stu-id="18d18-141">Display usually has a low [aspect ratio](glossary.md) (4:3 or 5:4), whereas print uses a high aspect ratio (8.5:11 or 1:1.4142 based on the standard page sizes).</span></span> <span data-ttu-id="18d18-142">這是因為直向 [模式](glossary.md) 列印比 [橫向模式](glossary.md)更常見。</span><span class="sxs-lookup"><span data-stu-id="18d18-142">This is because [portrait mode](glossary.md) printing is more common than [landscape mode](glossary.md).</span></span>
-   <span data-ttu-id="18d18-143">**有頁面。**</span><span class="sxs-lookup"><span data-stu-id="18d18-143">**Has pages.**</span></span> <span data-ttu-id="18d18-144">因此，列印輸出：</span><span class="sxs-lookup"><span data-stu-id="18d18-144">Consequently, print output:</span></span>
    -   <span data-ttu-id="18d18-145">具有標準頁面大小。</span><span class="sxs-lookup"><span data-stu-id="18d18-145">Has standard page sizes.</span></span> <span data-ttu-id="18d18-146">美國和加拿大地區的標準是 8.5 "x11" 紙;其他地方的標準是 A4 紙張。</span><span class="sxs-lookup"><span data-stu-id="18d18-146">The standard in the United States and Canada is 8.5"x11" paper; the standard everywhere else is A4 paper.</span></span>
    -   <span data-ttu-id="18d18-147">有分頁符號。</span><span class="sxs-lookup"><span data-stu-id="18d18-147">Has page breaks.</span></span>
    -   <span data-ttu-id="18d18-148">具有頁面邊界。</span><span class="sxs-lookup"><span data-stu-id="18d18-148">Has page margins.</span></span>
    -   <span data-ttu-id="18d18-149">具有頁首和頁尾。</span><span class="sxs-lookup"><span data-stu-id="18d18-149">Has headers and footers.</span></span>
    -   <span data-ttu-id="18d18-150">具有單一或雙面輸出。</span><span class="sxs-lookup"><span data-stu-id="18d18-150">Has single- or double-sided output.</span></span>
    -   <span data-ttu-id="18d18-151">可能有多個複本。</span><span class="sxs-lookup"><span data-stu-id="18d18-151">May have multiple copies.</span></span>
    -   <span data-ttu-id="18d18-152">可能依順序或選擇性地列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-152">May be printed out of order or selectively.</span></span>
-   <span data-ttu-id="18d18-153">**有許多選項。**</span><span class="sxs-lookup"><span data-stu-id="18d18-153">**Has many options.**</span></span> <span data-ttu-id="18d18-154">使用者可能會想要選擇印表機和紙張大小、印表機選項 (例如列印品質、雙面列印，以及裝訂) 、份數、頁面範圍、定序和列印格式。</span><span class="sxs-lookup"><span data-stu-id="18d18-154">Users may want to choose a printer and paper size, printer options (such as print quality, double-sided printing, and stapling), number of copies, page ranges, collation, and print format.</span></span>
-   <span data-ttu-id="18d18-155">**花費時間和金錢。**</span><span class="sxs-lookup"><span data-stu-id="18d18-155">**Takes time and money.**</span></span> <span data-ttu-id="18d18-156">列印大型檔或高品質的相片可能需要相當長的時間，而紙張和筆墨的成本會隨時間增加。</span><span class="sxs-lookup"><span data-stu-id="18d18-156">It can take a significant amount of time to print a large document or a high-quality photo, and the cost of the paper and ink adds up over time.</span></span> <span data-ttu-id="18d18-157">相反地，顯示輸出是瞬間的，基本上是免費的。</span><span class="sxs-lookup"><span data-stu-id="18d18-157">By contrast, display output is instantaneous and essentially free.</span></span>
-   <span data-ttu-id="18d18-158">**可能是黑色和白色。**</span><span class="sxs-lookup"><span data-stu-id="18d18-158">**May be black and white.**</span></span> <span data-ttu-id="18d18-159">現今許多印表機都是黑色和白色，但很少會顯示單色。</span><span class="sxs-lookup"><span data-stu-id="18d18-159">Many printers today are black and white, whereas few displays are monochrome.</span></span>
-   <span data-ttu-id="18d18-160">**不是互動式的。**</span><span class="sxs-lookup"><span data-stu-id="18d18-160">**Is not interactive.**</span></span> <span data-ttu-id="18d18-161">使用者無法滾動頁面或控制項來查看更多內容。</span><span class="sxs-lookup"><span data-stu-id="18d18-161">Users can't scroll pages or controls to see more content.</span></span> <span data-ttu-id="18d18-162">他們無法按一下連結或按鈕，或將滑鼠停留在控制項上。</span><span class="sxs-lookup"><span data-stu-id="18d18-162">They can't click links or buttons, or hover over controls.</span></span> <span data-ttu-id="18d18-163">互動式內容列印時沒有任何值。</span><span class="sxs-lookup"><span data-stu-id="18d18-163">Interactive content has no value when printed.</span></span>
-   <span data-ttu-id="18d18-164">**可能會用完紙張、筆墨或碳粉，或離線。**</span><span class="sxs-lookup"><span data-stu-id="18d18-164">**Can run out of paper, ink, or toner, or be offline.**</span></span> <span data-ttu-id="18d18-165">因此，紙張輸出需要更多錯誤處理和疑難排解。</span><span class="sxs-lookup"><span data-stu-id="18d18-165">Consequently, paper output needs more error handling and troubleshooting.</span></span>

<span data-ttu-id="18d18-166">這些差異可能會影響您的列印設計。</span><span class="sxs-lookup"><span data-stu-id="18d18-166">These differences may affect your printing design.</span></span> <span data-ttu-id="18d18-167">建立良好的列印體驗所需的並不只是將程式的輸出導向印表機。</span><span class="sxs-lookup"><span data-stu-id="18d18-167">Creating a good print experience requires more than just directing your program's output to the printer.</span></span>

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a><span data-ttu-id="18d18-168">WYSIWYG 和不斷演進的螢幕顯示需求</span><span class="sxs-lookup"><span data-stu-id="18d18-168">WYSIWYG and the evolving requirements of screen display</span></span>

<span data-ttu-id="18d18-169">在過去，列印使用者體驗的最基本原則就是所謂的 WYSIWYG ( 「您看到的內容是什麼」 ) 。</span><span class="sxs-lookup"><span data-stu-id="18d18-169">Historically, the most fundamental principle for the printing user experience is known as WYSIWYG ("what you see is what you get").</span></span> <span data-ttu-id="18d18-170">此準則表示在顯示的內容和列印的內容之間應該有強式關聯性。</span><span class="sxs-lookup"><span data-stu-id="18d18-170">This principle suggests that there should be a strong relationship between what is seen on the display and what is printed.</span></span> <span data-ttu-id="18d18-171">在 WYSIWYG 成為標準實務之前，檔的顯示和列印版本之間通常沒有關聯性。</span><span class="sxs-lookup"><span data-stu-id="18d18-171">Before WYSIWYG became a standard practice, there was often no relationship between the display and print versions of a document.</span></span> <span data-ttu-id="18d18-172">使用者必須列印才能查看檔在紙張上的實際外觀。</span><span class="sxs-lookup"><span data-stu-id="18d18-172">Users had to print in order to see what the document really looked like on paper.</span></span> <span data-ttu-id="18d18-173">使用 WYSIWYG 是生產力的絕佳改進，因為大部分的程式主要是設計來建立和列印檔案。</span><span class="sxs-lookup"><span data-stu-id="18d18-173">Using WYSIWYG was a great improvement in productivity because most programs at the time were primarily designed for document creation and printing.</span></span>

<span data-ttu-id="18d18-174">現今，網站通常會針對顯示進行優化，而且其印表機易記的格式可能會有很大的不同。</span><span class="sxs-lookup"><span data-stu-id="18d18-174">Today, it is common for Web sites to optimize for the display, and their printer-friendly format may appear much different.</span></span> <span data-ttu-id="18d18-175">此外，我們有各式各樣的運算裝置 (例如智慧型手機和個人數位助理) ，通常需要針對小型顯示器優化的輸出。</span><span class="sxs-lookup"><span data-stu-id="18d18-175">Furthermore, we have diverse computing devices (for example, smart phones and personal digital assistants) that often need output optimized for small displays.</span></span> <span data-ttu-id="18d18-176">雖然 WYSIWYG 仍是檔建立程式的最佳方法，但是對於其他程式來說，針對各種目標裝置進行優化通常更合理。</span><span class="sxs-lookup"><span data-stu-id="18d18-176">While WYSIWYG is still the best approach for document creation programs, for other programs it often makes more sense to optimize for a variety of target devices.</span></span> <span data-ttu-id="18d18-177">針對這類程式，您在電腦顯示器上看到的內容可能與您在其他裝置顯示器上看到的不同，這可能與您在列印頁面上看到的不同。</span><span class="sxs-lookup"><span data-stu-id="18d18-177">For such programs, what you see on a PC display may be different from what you see on other device displays, which may be different from what you get on the printed page.</span></span>

### <a name="optimize-for-printing"></a><span data-ttu-id="18d18-178">針對列印優化</span><span class="sxs-lookup"><span data-stu-id="18d18-178">Optimize for printing</span></span>

<span data-ttu-id="18d18-179">未採用嚴格 WYSIWYG 列印體驗的程式仍可透過下列方式優化列印：</span><span class="sxs-lookup"><span data-stu-id="18d18-179">Programs that don't employ a strict WYSIWYG print experience can still optimize for printing in the following ways:</span></span>

-   <span data-ttu-id="18d18-180">重新格式化目標頁面大小的版面配置。</span><span class="sxs-lookup"><span data-stu-id="18d18-180">Reformat the layout for the target page size.</span></span>
-   <span data-ttu-id="18d18-181">提供預覽列印，最好是使用簡單的自訂選項，讓使用者可以直接在 [列印] 對話方塊中進行實驗 (例如，將邊界拖曳) 。</span><span class="sxs-lookup"><span data-stu-id="18d18-181">Provide print preview, preferably with easy customization options allowing users to experiment directly in the print dialog (for example, dragging margins).</span></span>
-   <span data-ttu-id="18d18-182">如果適用的話，請提供印表機易記的格式選項。</span><span class="sxs-lookup"><span data-stu-id="18d18-182">If appropriate, provide a printer-friendly format option.</span></span>
    -   <span data-ttu-id="18d18-183">將個別的部分檔合併成單一檔。</span><span class="sxs-lookup"><span data-stu-id="18d18-183">Consolidate separate partial documents into a single document.</span></span>
    -   <span data-ttu-id="18d18-184">移除背景和其他設計項目（例如 ads），特別是當它們不適合黑色和白色印表機時。</span><span class="sxs-lookup"><span data-stu-id="18d18-184">Remove backgrounds and other design elements such as ads, especially if they are unsuitable for a black and white printer.</span></span>
    -   <span data-ttu-id="18d18-185">移除互動式元素，例如導覽控制項和命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="18d18-185">Remove interactive elements, such as navigation controls and command buttons.</span></span>
    -   <span data-ttu-id="18d18-186">確定所有資料都是可見的，但不顯示捲軸或暫留。</span><span class="sxs-lookup"><span data-stu-id="18d18-186">Make sure that all data is visible without scrollbars or hovering.</span></span>

        <span data-ttu-id="18d18-187">**顯示版本：**</span><span class="sxs-lookup"><span data-stu-id="18d18-187">**Display version:**</span></span>

        ![<span data-ttu-id="18d18-188">針對螢幕優化之報表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-188">screen shot of report optimized for screen</span></span> ](images/exper-printing-image1.png)

        <span data-ttu-id="18d18-189">**印表機易記版本：**</span><span class="sxs-lookup"><span data-stu-id="18d18-189">**Printer-friendly version:**</span></span>

        ![<span data-ttu-id="18d18-190">針對列印優化的相同報表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-190">screen shot of same report optimized for print</span></span> ](images/exper-printing-image2.png)

        <span data-ttu-id="18d18-191">在適合印表機的版本中，所有資料都會顯示在列印的頁面上，並移除互動式元素。</span><span class="sxs-lookup"><span data-stu-id="18d18-191">In the printer-friendly version, all the data is visible on the printed page, and the interactive elements are removed.</span></span>

    -   <span data-ttu-id="18d18-192">以對應的文字取代連結。</span><span class="sxs-lookup"><span data-stu-id="18d18-192">Replace links with their text equivalent.</span></span>

        <span data-ttu-id="18d18-193">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="18d18-193">**Acceptable:**</span></span>

        <span data-ttu-id="18d18-194">如需詳細資訊，請參閱 UX 指南。</span><span class="sxs-lookup"><span data-stu-id="18d18-194">For more information, see UX Guide.</span></span>

        <span data-ttu-id="18d18-195">**已針對列印優化：**</span><span class="sxs-lookup"><span data-stu-id="18d18-195">**Optimized for printing:**</span></span>

        <span data-ttu-id="18d18-196">如需詳細資訊，請參閱 UX 指南 (https://msdn.microsoft.com/windowsvista/uxguide) 。</span><span class="sxs-lookup"><span data-stu-id="18d18-196">For more information, see UX Guide (https://msdn.microsoft.com/windowsvista/uxguide).</span></span>

-   <span data-ttu-id="18d18-197">將深色背景的燈光文字轉換成白色背景上的深色文字。</span><span class="sxs-lookup"><span data-stu-id="18d18-197">Convert light text on a dark background to dark text on a white background.</span></span>

### <a name="include-the-right-print-options"></a><span data-ttu-id="18d18-198">包含正確的列印選項</span><span class="sxs-lookup"><span data-stu-id="18d18-198">Include the right print options</span></span>

<span data-ttu-id="18d18-199">[列印選項] 通用對話方塊提供下列選項：</span><span class="sxs-lookup"><span data-stu-id="18d18-199">The Print options common dialog provides options to:</span></span>

-   <span data-ttu-id="18d18-200">選取印表機和紙張大小。</span><span class="sxs-lookup"><span data-stu-id="18d18-200">Select the printer and paper size.</span></span>
-   <span data-ttu-id="18d18-201">設定印表機屬性。</span><span class="sxs-lookup"><span data-stu-id="18d18-201">Set printer properties.</span></span>
-   <span data-ttu-id="18d18-202">選取頁面範圍、份數和定序。</span><span class="sxs-lookup"><span data-stu-id="18d18-202">Select the page range, number of copies, and collation.</span></span>
-   <span data-ttu-id="18d18-203">使用紙張的兩側。</span><span class="sxs-lookup"><span data-stu-id="18d18-203">Use both sides of the paper.</span></span>

<span data-ttu-id="18d18-204">您的程式可能需要其他選項（例如檔內容選項） (要列印) 的內容、格式選項 (如何列印，包括列印品質、圖片大小、調整至框架) 和色彩選項。</span><span class="sxs-lookup"><span data-stu-id="18d18-204">Your program may require additional options, such as document content options (which content to print), format options (how to print, including print quality, picture sizes, fitting to frame), and color options.</span></span> <span data-ttu-id="18d18-205">如果您需要提供其他選項，請展開 [列印選項] 通用對話方塊來進行。</span><span class="sxs-lookup"><span data-stu-id="18d18-205">If you need to provide additional options, do so by extending the Print options common dialog.</span></span> <span data-ttu-id="18d18-206">不要建立自訂的 [列印] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-206">Don't create a custom Print dialog box.</span></span>

<span data-ttu-id="18d18-207">在設計列印選項時，請考慮列印多份檔時的體驗。</span><span class="sxs-lookup"><span data-stu-id="18d18-207">When designing the Print options, consider the experience when printing multiple documents.</span></span> <span data-ttu-id="18d18-208">下一次的列印工作可能會非常類似于上次的列印工作。</span><span class="sxs-lookup"><span data-stu-id="18d18-208">Chances are the next print job will be very similar to the last print job.</span></span> <span data-ttu-id="18d18-209">優化 reprints 的預設設定和類似的列印工作，並不會讓使用者每次都能完全啟動。</span><span class="sxs-lookup"><span data-stu-id="18d18-209">Optimize the default settings for reprints and similar print jobs don't make users start over completely each time.</span></span>

### <a name="design-print-preview-for-performance-and-usability"></a><span data-ttu-id="18d18-210">設計適用于效能和可用性的預覽列印</span><span class="sxs-lookup"><span data-stu-id="18d18-210">Design print preview for performance and usability</span></span>

<span data-ttu-id="18d18-211">**不正確的列印工作會浪費時間和金錢。針對檔建立程式，使用者應該能夠在進行實際列印之前，先評估結果。**</span><span class="sxs-lookup"><span data-stu-id="18d18-211">**An incorrect print job wastes time and money. For document creation programs, users should be able to evaluate the results before doing the actual printing.**</span></span> <span data-ttu-id="18d18-212">預覽列印應可讓使用者：</span><span class="sxs-lookup"><span data-stu-id="18d18-212">A print preview should allow users to:</span></span>

-   <span data-ttu-id="18d18-213">評估邊界、分頁符號、頁面方向、標題和頁尾。</span><span class="sxs-lookup"><span data-stu-id="18d18-213">Evaluate margins, page breaks, page orientation, headers, and footers.</span></span>
-   <span data-ttu-id="18d18-214">流覽所有頁面。</span><span class="sxs-lookup"><span data-stu-id="18d18-214">Browse through all the pages.</span></span>
-   <span data-ttu-id="18d18-215">直接從預覽列印列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-215">Print directly from the print preview.</span></span>

<span data-ttu-id="18d18-216">某些複雜的檔 (例如電腦輔助設計 \[ CAD \] 繪圖) 可能需要很長的時間才能呈現。</span><span class="sxs-lookup"><span data-stu-id="18d18-216">Some complex documents (such as computer-aided design \[CAD\] drawings) can take a long time to render.</span></span> <span data-ttu-id="18d18-217">預覽的效能很重要，因為預覽列印需要一段時間才會轉譯每個頁面。</span><span class="sxs-lookup"><span data-stu-id="18d18-217">The performance of the preview is important a print preview can become quite tedious if it takes awhile to render each page.</span></span> <span data-ttu-id="18d18-218">**因此，最好是讓預覽列印快速呈現，且精確度足以讓使用者評估列印結果，而不是讓呈現速度變得很慢的完全精確預覽。**</span><span class="sxs-lookup"><span data-stu-id="18d18-218">**Consequently, it's better to have a print preview that renders quickly and is accurate enough to allow users to evaluate the print results than to have a completely accurate preview that renders slowly.**</span></span>

<span data-ttu-id="18d18-219">設計預覽列印時，請考慮準備列印的整個工作。</span><span class="sxs-lookup"><span data-stu-id="18d18-219">When designing the print preview, consider the whole task of preparing to print.</span></span> <span data-ttu-id="18d18-220">使用者要尋找哪些專案？</span><span class="sxs-lookup"><span data-stu-id="18d18-220">What are users going to be looking for?</span></span> <span data-ttu-id="18d18-221">他們會變更哪些專案？</span><span class="sxs-lookup"><span data-stu-id="18d18-221">What are they going to change?</span></span> <span data-ttu-id="18d18-222">檔建立程式應提供互動式預覽列印，讓使用者可以調整預覽中經常變更的設定，例如邊界和換行。</span><span class="sxs-lookup"><span data-stu-id="18d18-222">Document creation programs should provide an interactive print preview so that users can adjust frequently changed settings like margins and line breaks within the preview.</span></span>

<span data-ttu-id="18d18-223">不過，若要達到最佳的範圍，您的程式預設應該會有正確的專案。</span><span class="sxs-lookup"><span data-stu-id="18d18-223">However, to the best extent possible, your program should do the right thing by default.</span></span> <span data-ttu-id="18d18-224">如有必要，請在不太可能是使用者所需的列印情況時發出警告。</span><span class="sxs-lookup"><span data-stu-id="18d18-224">When necessary, warn about printing situations that are unlikely to be what the user intended.</span></span> <span data-ttu-id="18d18-225">請勿依賴使用者使用預覽列印找出問題。</span><span class="sxs-lookup"><span data-stu-id="18d18-225">Don't rely on users finding problems using the print preview.</span></span> <span data-ttu-id="18d18-226">例如，假設試算表的資料行太多，無法在直向模式的單一頁面上列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-226">For example, suppose a spreadsheet has too many columns to print on a single page in portrait mode.</span></span> <span data-ttu-id="18d18-227">雖然程式可能出現確認對話方塊，但更好的解決方案是以橫向模式自動列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-227">While the program could present a confirmation dialog box, a better solution is to print in landscape mode automatically.</span></span>

<span data-ttu-id="18d18-228">**如果您只進行五件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="18d18-228">**If you do only five things...**</span></span>

1.  <span data-ttu-id="18d18-229">為您的程式類型設計適合的列印體驗。</span><span class="sxs-lookup"><span data-stu-id="18d18-229">Design a printing experience appropriate for your program type.</span></span>
2.  <span data-ttu-id="18d18-230">請參閱您的程式案例，其中包含列印和最佳範圍，因此需要列印選用專案。</span><span class="sxs-lookup"><span data-stu-id="18d18-230">Review your program's scenarios that involve printing and to the best extent possible, make the need to print optional.</span></span>
3.  <span data-ttu-id="18d18-231">自訂列印通用對話方塊來提供有用的列印延伸模組。</span><span class="sxs-lookup"><span data-stu-id="18d18-231">Provide useful printing extensions by customizing the Print common dialog.</span></span> <span data-ttu-id="18d18-232">請勿建立此用途的自訂列印對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-232">Don't create a custom Print dialog box for this purpose.</span></span>
4.  <span data-ttu-id="18d18-233">優化 reprints 和類似列印工作的列印選項。</span><span class="sxs-lookup"><span data-stu-id="18d18-233">Optimize the Print options for reprints and similar print jobs.</span></span>
5.  <span data-ttu-id="18d18-234">請在適當時提供預覽功能。</span><span class="sxs-lookup"><span data-stu-id="18d18-234">Provide a preview feature whenever appropriate.</span></span>

## <a name="printing-patterns"></a><span data-ttu-id="18d18-235">列印模式</span><span class="sxs-lookup"><span data-stu-id="18d18-235">Printing patterns</span></span>

<span data-ttu-id="18d18-236">程式類型是適當列印體驗的主要指示器：</span><span class="sxs-lookup"><span data-stu-id="18d18-236">The type of program is the primary indicator of the appropriate printing experience:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18d18-237"><strong>建立 Advanced document</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-237"><strong>Advanced document creation</strong></span></span><br/> <span data-ttu-id="18d18-238">用來建立、查看和列印高階檔。</span><span class="sxs-lookup"><span data-stu-id="18d18-238">Used to create, view, and print high-end documents.</span></span> <span data-ttu-id="18d18-239">建立高品質輸出的能力，是程式存在的主要原因之一。</span><span class="sxs-lookup"><span data-stu-id="18d18-239">The ability to create high-quality printouts is one of the main reasons why the program exists.</span></span> <span data-ttu-id="18d18-240">以專業使用者為目標。</span><span class="sxs-lookup"><span data-stu-id="18d18-240">Targeted at expert users.</span></span> <br/></td>
<td><span data-ttu-id="18d18-241"><strong>使用者目標：</strong> 完美的結果會詳細控制列印輸出。</span><span class="sxs-lookup"><span data-stu-id="18d18-241"><strong>User goals:</strong> Perfect results detailed control over the print output.</span></span><br/> <span data-ttu-id="18d18-242"><strong>範例：</strong> Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="18d18-242"><strong>Example:</strong> Microsoft Word</span></span><br/> <span data-ttu-id="18d18-243"><strong>建議的列印體驗：</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-243"><strong>Recommended printing experience:</strong></span></span><br/>
<ul>
<li><span data-ttu-id="18d18-244">針對 print (WYSIWYG) 進行的輸出優化。</span><span class="sxs-lookup"><span data-stu-id="18d18-244">Output optimized for print (WYSIWYG).</span></span></li>
<li><span data-ttu-id="18d18-245">先進的檔案格式設定功能，以及列印大型物件的選項。</span><span class="sxs-lookup"><span data-stu-id="18d18-245">Advanced document formatting features, with options to print large objects.</span></span></li>
<li><span data-ttu-id="18d18-246">先進的列印選項，包括頁首和頁尾。</span><span class="sxs-lookup"><span data-stu-id="18d18-246">Advanced print options, including headers and footers.</span></span> <span data-ttu-id="18d18-247">檔相關的列印選項會儲存在檔本身內。</span><span class="sxs-lookup"><span data-stu-id="18d18-247">Document-related print options are saved within the document itself.</span></span></li>
<li><span data-ttu-id="18d18-248">快速、準確、功能強大的預覽列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-248">Fast, accurate, powerful print previews.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18d18-249"><strong>建立中繼檔</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-249"><strong>Intermediate document creation</strong></span></span><br/> <span data-ttu-id="18d18-250">用來建立和查看更複雜的檔。</span><span class="sxs-lookup"><span data-stu-id="18d18-250">Used to create and view more complex documents.</span></span> <span data-ttu-id="18d18-251">建立優質列印的能力很重要，但不一定是程式存在的主要原因之一。</span><span class="sxs-lookup"><span data-stu-id="18d18-251">The ability to create good-quality printouts is important, but not necessarily one of the main reasons why the program exists.</span></span> <span data-ttu-id="18d18-252">以中繼使用者為目標。</span><span class="sxs-lookup"><span data-stu-id="18d18-252">Targeted at intermediate users.</span></span> <br/></td>
<td><span data-ttu-id="18d18-253"><strong>使用者目標：</strong> 以極短的努力提供良好的結果。</span><span class="sxs-lookup"><span data-stu-id="18d18-253"><strong>User goals:</strong> Good results with minimal effort.</span></span> <span data-ttu-id="18d18-254">對列印輸出有一些控制權。</span><span class="sxs-lookup"><span data-stu-id="18d18-254">Some control over the print output.</span></span><br/> <span data-ttu-id="18d18-255"><strong>範例：</strong> 大部分 Microsoft Office 程式，例如 Outlook 和 Excel。</span><span class="sxs-lookup"><span data-stu-id="18d18-255"><strong>Examples:</strong> Most Microsoft Office programs, such as Outlook and Excel.</span></span><br/> <span data-ttu-id="18d18-256"><strong>建議的列印體驗：</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-256"><strong>Recommended printing experience:</strong></span></span><br/>
<ul>
<li><span data-ttu-id="18d18-257">針對 print (WYSIWYG) 進行的輸出優化。</span><span class="sxs-lookup"><span data-stu-id="18d18-257">Output optimized for print (WYSIWYG).</span></span></li>
<li><span data-ttu-id="18d18-258">某些檔案格式功能，能夠在不截斷的情況下列印大型物件。</span><span class="sxs-lookup"><span data-stu-id="18d18-258">Some document formatting features, with ability to print large objects without truncation.</span></span></li>
<li><span data-ttu-id="18d18-259">某些自訂列印選項，包括頁首和頁尾。</span><span class="sxs-lookup"><span data-stu-id="18d18-259">Some custom print options, including headers and footers.</span></span></li>
<li><span data-ttu-id="18d18-260">精確、容易使用的預覽列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-260">Accurate, easy to use print previews.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18d18-261"><strong>建立簡單的檔</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-261"><strong>Simple document creation</strong></span></span><br/> <span data-ttu-id="18d18-262">用來建立和查看簡單的檔。</span><span class="sxs-lookup"><span data-stu-id="18d18-262">Used to create and view simple documents.</span></span> <span data-ttu-id="18d18-263">以所有使用者為目標。</span><span class="sxs-lookup"><span data-stu-id="18d18-263">Targeted at all users.</span></span> <br/></td>
<td><span data-ttu-id="18d18-264"><strong>使用者目標：</strong> 使用標準列印選項的基本列印支援。</span><span class="sxs-lookup"><span data-stu-id="18d18-264"><strong>User goals:</strong> Basic printing support with standard printing options.</span></span> <span data-ttu-id="18d18-265">使用者預期會有良好的結果，而不需要進行任何調整。</span><span class="sxs-lookup"><span data-stu-id="18d18-265">Users expect good results without any tweaking.</span></span><br/> <span data-ttu-id="18d18-266"><strong>範例：</strong> WordPad、油漆。</span><span class="sxs-lookup"><span data-stu-id="18d18-266"><strong>Examples:</strong> WordPad, Paint.</span></span><br/> <span data-ttu-id="18d18-267"><strong>建議的列印體驗：</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-267"><strong>Recommended printing experience:</strong></span></span><br/>
<ul>
<li><span data-ttu-id="18d18-268">輸出可針對 print (WYSIWYG) 進行優化，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="18d18-268">Output may be optimized for print (WYSIWYG), but this is not required.</span></span></li>
<li><span data-ttu-id="18d18-269">某些檔案格式功能，能夠在不截斷的情況下列印大型物件。</span><span class="sxs-lookup"><span data-stu-id="18d18-269">Some document formatting features, with ability to print large objects without truncation.</span></span></li>
<li><span data-ttu-id="18d18-270">標準列印選項;自訂列印選項是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="18d18-270">Standard print options; custom print options are optional.</span></span></li>
<li><span data-ttu-id="18d18-271">簡單或沒有預覽列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-271">Simple or no print previews.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18d18-272"><strong>檔檢視器</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-272"><strong>Document viewers</strong></span></span><br/> <span data-ttu-id="18d18-273">用來查看檔。</span><span class="sxs-lookup"><span data-stu-id="18d18-273">Used to view documents.</span></span> <span data-ttu-id="18d18-274">使用者無法變更檔內容或格式。</span><span class="sxs-lookup"><span data-stu-id="18d18-274">Users can't change the document content or format.</span></span> <br/></td>
<td><span data-ttu-id="18d18-275"><strong>使用者目標：</strong> 使用標準列印選項的基本列印支援。</span><span class="sxs-lookup"><span data-stu-id="18d18-275"><strong>User goals:</strong> Basic printing support with standard printing options.</span></span> <span data-ttu-id="18d18-276">使用者預期會有良好的結果，而不需要進行任何調整。</span><span class="sxs-lookup"><span data-stu-id="18d18-276">Users expect good results without any tweaking.</span></span> <span data-ttu-id="18d18-277">系統會自動處理列印問題，因為使用者無法修改檔。</span><span class="sxs-lookup"><span data-stu-id="18d18-277">Printing problems are handled automatically because users can't modify the document.</span></span><br/> <span data-ttu-id="18d18-278"><strong>範例：</strong> Windows Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="18d18-278"><strong>Example:</strong> Windows Internet Explorer</span></span><br/> <span data-ttu-id="18d18-279"><strong>建議的列印體驗：</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-279"><strong>Recommended printing experience:</strong></span></span><br/>
<ul>
<li><span data-ttu-id="18d18-280">輸出可針對 print (WYSIWYG) 進行優化，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="18d18-280">Output may be optimized for print (WYSIWYG), but this is not required.</span></span></li>
<li><span data-ttu-id="18d18-281">程式會自動處理分頁符號、消除空白頁面、處理大型物件，以及移除背景和其他設計項目。</span><span class="sxs-lookup"><span data-stu-id="18d18-281">Program automatically handles page breaks, eliminates blank pages, handles large objects, and removes backgrounds and other design elements.</span></span></li>
<li><span data-ttu-id="18d18-282">標準列印選項;自訂列印選項是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="18d18-282">Standard print options; custom print options are optional.</span></span></li>
<li><span data-ttu-id="18d18-283">簡單或沒有預覽列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-283">Simple or no print previews.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18d18-284"><strong>公用程式或企業營運應用程式</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-284"><strong>Utilities or line-of-business applications</strong></span></span><br/> <span data-ttu-id="18d18-285">用來執行簡單的特定工作。</span><span class="sxs-lookup"><span data-stu-id="18d18-285">Used to perform simple, specific tasks.</span></span> <span data-ttu-id="18d18-286">以所有使用者為目標。</span><span class="sxs-lookup"><span data-stu-id="18d18-286">Targeted at all users.</span></span> <br/></td>
<td><span data-ttu-id="18d18-287"><strong>使用者目標：</strong> 能夠有效率地匯出選取的資料。</span><span class="sxs-lookup"><span data-stu-id="18d18-287"><strong>User goals:</strong> Ability to export selected data efficiently.</span></span> <span data-ttu-id="18d18-288">使用者預期會有良好的結果，而不需要進行任何調整。</span><span class="sxs-lookup"><span data-stu-id="18d18-288">Users expect good results without any tweaking.</span></span> <span data-ttu-id="18d18-289">通常對於這類程式而言，使用者會驚喜驚訝地尋找任何列印支援。</span><span class="sxs-lookup"><span data-stu-id="18d18-289">Often for such programs, users are pleasantly surprised to find any printing support at all.</span></span><br/> <span data-ttu-id="18d18-290"><strong>建議的列印體驗：</strong></span><span class="sxs-lookup"><span data-stu-id="18d18-290"><strong>Recommended printing experience:</strong></span></span><br/>
<ul>
<li><span data-ttu-id="18d18-291">根據支援的案例，列印支援是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="18d18-291">Printing support is optional depending upon supported scenarios.</span></span></li>
<li><span data-ttu-id="18d18-292">輸出可針對 print (WYSIWYG) 進行優化，但這並非必要。</span><span class="sxs-lookup"><span data-stu-id="18d18-292">Output may be optimized for print (WYSIWYG), but this is not required.</span></span></li>
<li><span data-ttu-id="18d18-293">某些檔案格式功能。</span><span class="sxs-lookup"><span data-stu-id="18d18-293">Some document formatting features.</span></span> <span data-ttu-id="18d18-294">如果已截斷大型物件，則可能是可接受的。</span><span class="sxs-lookup"><span data-stu-id="18d18-294">Might be acceptable if large objects are truncated.</span></span></li>
<li><span data-ttu-id="18d18-295">標準列印選項。</span><span class="sxs-lookup"><span data-stu-id="18d18-295">Standard print options.</span></span></li>
<li><span data-ttu-id="18d18-296">預覽列印：選擇性。</span><span class="sxs-lookup"><span data-stu-id="18d18-296">Print previews optional.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="18d18-297">指導方針</span><span class="sxs-lookup"><span data-stu-id="18d18-297">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="18d18-298">一般</span><span class="sxs-lookup"><span data-stu-id="18d18-298">General</span></span>

-   <span data-ttu-id="18d18-299">**請勿列印只有頁首和頁尾的空白頁面或頁面。**</span><span class="sxs-lookup"><span data-stu-id="18d18-299">**Don't print blank pages or pages with just headers and footers.**</span></span> <span data-ttu-id="18d18-300">但是，如果頁首或頁尾包含頁碼，而且可能會在其他位置參考這些頁碼，則列印空白頁面。</span><span class="sxs-lookup"><span data-stu-id="18d18-300">However, print blank pages if the headers or footers contain page numbers and those page numbers might referenced elsewhere.</span></span>
-   <span data-ttu-id="18d18-301">**在關閉程式之前，請完全將任何暫止的列印工作完全停用。**</span><span class="sxs-lookup"><span data-stu-id="18d18-301">**Completely spool out any pending print jobs before shutting down a program.**</span></span>

### <a name="formatting-pages"></a><span data-ttu-id="18d18-302">格式化頁面</span><span class="sxs-lookup"><span data-stu-id="18d18-302">Formatting pages</span></span>

-   <span data-ttu-id="18d18-303">**重新格式化文字版面配置以符合目標頁面大小。**</span><span class="sxs-lookup"><span data-stu-id="18d18-303">**Reformat text layout to fit within the target page size.**</span></span> <span data-ttu-id="18d18-304">絕不截斷文字。</span><span class="sxs-lookup"><span data-stu-id="18d18-304">Never truncate text.</span></span>
-   <span data-ttu-id="18d18-305">如果使用者不控制檔的格式：</span><span class="sxs-lookup"><span data-stu-id="18d18-305">If users don't control the format of the document:</span></span>
    -   <span data-ttu-id="18d18-306">**藉由在頁面之間調整、旋轉或分割，自動處理大型物件。**</span><span class="sxs-lookup"><span data-stu-id="18d18-306">**Automatically handle large objects by scaling, rotating, or splitting across pages.**</span></span> <span data-ttu-id="18d18-307">如需有關列印大型物件的詳細指導方針，請參閱 [超大物件](#oversized-objects)。</span><span class="sxs-lookup"><span data-stu-id="18d18-307">For more guidelines about printing large objects, see [Oversized objects](#oversized-objects).</span></span>
    -   <span data-ttu-id="18d18-308">**將分頁符號優化，以消除空白和近空白的頁面。**</span><span class="sxs-lookup"><span data-stu-id="18d18-308">**Optimize the page breaks to eliminate blank and nearly blank pages.**</span></span>
    -   <span data-ttu-id="18d18-309">**將深色背景的燈光文字轉換成白色背景上的深色文字。**</span><span class="sxs-lookup"><span data-stu-id="18d18-309">**Convert light text on a dark background to dark text on a white background.**</span></span>
    -   <span data-ttu-id="18d18-310">**移除背景和其他設計項目，** 特別是在不適合黑色和白色印表機的情況下。</span><span class="sxs-lookup"><span data-stu-id="18d18-310">**Remove backgrounds and other design elements,** especially if they are unsuitable for a black and white printer.</span></span>
-   <span data-ttu-id="18d18-311">**如果您的程式提供個別的部分檔，請提供印表機易記的格式選項，將它們合併成單一檔以進行列印。**</span><span class="sxs-lookup"><span data-stu-id="18d18-311">**If your program presents separate partial documents, provide a printer-friendly format option to consolidate them into a single document for printing.**</span></span>
-   <span data-ttu-id="18d18-312">**移除互動式元素：**</span><span class="sxs-lookup"><span data-stu-id="18d18-312">**Remove interactive elements:**</span></span>
    -   <span data-ttu-id="18d18-313">移除導覽控制項和命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="18d18-313">Remove navigation controls and command buttons.</span></span>
    -   <span data-ttu-id="18d18-314">確定所有資料在沒有捲軸的情況下都是可見的。</span><span class="sxs-lookup"><span data-stu-id="18d18-314">Make sure that all data is visible without scrollbars.</span></span>
    -   <span data-ttu-id="18d18-315">以對應的文字取代連結。</span><span class="sxs-lookup"><span data-stu-id="18d18-315">Replace links with their text equivalent.</span></span>

        <span data-ttu-id="18d18-316">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="18d18-316">**Acceptable:**</span></span>

        <span data-ttu-id="18d18-317">如需詳細資訊，請參閱 UX 指南。</span><span class="sxs-lookup"><span data-stu-id="18d18-317">For more information, see UX Guide.</span></span>

        <span data-ttu-id="18d18-318">**已針對列印優化：**</span><span class="sxs-lookup"><span data-stu-id="18d18-318">**Optimized for printing:**</span></span>

        <span data-ttu-id="18d18-319">如需詳細資訊，請參閱 UX 指南 (https://msdn.microsoft.com/windowsvista/uxguide) 。</span><span class="sxs-lookup"><span data-stu-id="18d18-319">For more information, see UX Guide (https://msdn.microsoft.com/windowsvista/uxguide).</span></span>

        <span data-ttu-id="18d18-320">在此範例中，連結會取代為其在括弧中的文字對等專案。</span><span class="sxs-lookup"><span data-stu-id="18d18-320">In this example, the link is replaced with its text equivalent in parentheses.</span></span>

    -   <span data-ttu-id="18d18-321">將滑鼠停留時顯示的有用資訊移動至內嵌。</span><span class="sxs-lookup"><span data-stu-id="18d18-321">Move useful information displayed on hover to inline.</span></span>

### <a name="oversized-objects"></a><span data-ttu-id="18d18-322">超大物件</span><span class="sxs-lookup"><span data-stu-id="18d18-322">Oversized objects</span></span>

<span data-ttu-id="18d18-323">處理大型物件（例如試算表、圖形和相片）是列印的獨特問題。</span><span class="sxs-lookup"><span data-stu-id="18d18-323">Handling large objects, such as spreadsheets, graphics, and photos, is a problem unique to printing.</span></span> <span data-ttu-id="18d18-324">選擇下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="18d18-324">Choose one of the following approaches:</span></span>

-   <span data-ttu-id="18d18-325">**調整物件大小以容納在頁面上。**</span><span class="sxs-lookup"><span data-stu-id="18d18-325">**Scale the object to fit on the page.**</span></span> <span data-ttu-id="18d18-326">如果物件只稍微太大而無法列印、將物件保持在單一頁面上很重要，且物件在相應減少時仍可供使用，這種方法就很有用。</span><span class="sxs-lookup"><span data-stu-id="18d18-326">This approach works well if the object is only slightly too large to print, keeping the object on a single page is important, and the object is still legible when scaled down.</span></span>

    ![<span data-ttu-id="18d18-327">調整為頁面一半的相片螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-327">screen shot of photo scaled to half of a page</span></span> ](images/exper-printing-image3.png)

    <span data-ttu-id="18d18-328">在此範例中，會縮放大型影像以容納在頁面上。</span><span class="sxs-lookup"><span data-stu-id="18d18-328">In this example, the large image is scaled to fit on the page.</span></span>

-   <span data-ttu-id="18d18-329">**旋轉頁面。**</span><span class="sxs-lookup"><span data-stu-id="18d18-329">**Rotate the page.**</span></span> <span data-ttu-id="18d18-330">當在直向模式中以橫向模式列印較佳的頁面時，此方法的效果很好， (，反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="18d18-330">This approach works well when a few pages print better in landscape mode when in portrait mode (and vice versa).</span></span>

    ![<span data-ttu-id="18d18-331">旋轉為直向縱向的橫向相片螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-331">screen shot of landscape photo rotated to portrait</span></span> ](images/exper-printing-image4.png)

    <span data-ttu-id="18d18-332">在此範例中，會旋轉大型影像，使其在頁面上變得更好。</span><span class="sxs-lookup"><span data-stu-id="18d18-332">In this example, the large image is rotated to fit better on the page.</span></span>

-   <span data-ttu-id="18d18-333">**將物件列印在數個頁面上。**</span><span class="sxs-lookup"><span data-stu-id="18d18-333">**Print the object on several pages.**</span></span> <span data-ttu-id="18d18-334">當物件無法調整或不應調整，而且旋轉頁面不會有説明或不想要時，此方法的效果很好。</span><span class="sxs-lookup"><span data-stu-id="18d18-334">The approach works well when the object can't be scaled, or shouldn't be scaled, and rotating the page doesn't help or isn't wanted.</span></span> <span data-ttu-id="18d18-335">如果物件具有內部界限 (例如試算表中的資料行和資料列分隔) ，請將這些界限的頁面（而不是在內容中）中斷。</span><span class="sxs-lookup"><span data-stu-id="18d18-335">If the object has internal boundaries (such as the column and row dividers in a spreadsheet), break the pages on these boundaries instead of within the content.</span></span> <span data-ttu-id="18d18-336">此外，請重複瞭解頁面所需的任何元素，例如圖例或資料行標頭。</span><span class="sxs-lookup"><span data-stu-id="18d18-336">Also, repeat any elements required to understand the page, such as legends or column headers.</span></span> <span data-ttu-id="18d18-337">在數個頁面上分割物件時，請以 [讀取順序] (由左至右、從上到下) 來指派頁碼。</span><span class="sxs-lookup"><span data-stu-id="18d18-337">When splitting an object on several pages, assign the page numbers in reading order (left to right, top to bottom).</span></span>

    ![<span data-ttu-id="18d18-338">下一頁上重複的資料行標題螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-338">screen shot of column heads repeated on next page</span></span> ](images/exper-printing-image5.png)

    <span data-ttu-id="18d18-339">在此範例中，大型資料表會列印在兩個頁面上。</span><span class="sxs-lookup"><span data-stu-id="18d18-339">In this example, the large table is printed on two pages.</span></span> <span data-ttu-id="18d18-340">資料行標頭會從頁面保存到頁面，方便您快速理解。</span><span class="sxs-lookup"><span data-stu-id="18d18-340">Column headers persist from page to page to facilitate quick comprehension.</span></span>

-   <span data-ttu-id="18d18-341">**截斷物件** (只列印截斷) 之後仍可見的物件部分。</span><span class="sxs-lookup"><span data-stu-id="18d18-341">**Truncate the object** (printing only the part of the object still visible after truncation).</span></span> <span data-ttu-id="18d18-342">這種方法是最簡單的解決方案，但可能是最不接受的。</span><span class="sxs-lookup"><span data-stu-id="18d18-342">This approach is the simplest solution to implement, but likely to be the least acceptable.</span></span> <span data-ttu-id="18d18-343">另請注意，文字永遠無法接受截斷。</span><span class="sxs-lookup"><span data-stu-id="18d18-343">Also note that truncating is never acceptable for text.</span></span>

    ![<span data-ttu-id="18d18-344">直向頁面上全半相片的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-344">screen shot of half of wide photo on portrait page</span></span> ](images/exper-printing-image6.png)

    <span data-ttu-id="18d18-345">在此範例中，會截斷大型影像。</span><span class="sxs-lookup"><span data-stu-id="18d18-345">In this example, the large image is truncated.</span></span>

### <a name="headers-and-footers"></a><span data-ttu-id="18d18-346">頁首和頁尾</span><span class="sxs-lookup"><span data-stu-id="18d18-346">Headers and footers</span></span>

-   <span data-ttu-id="18d18-347">**提供 advanced 和中級檔建立程式的標頭和頁尾。**</span><span class="sxs-lookup"><span data-stu-id="18d18-347">**Provide headers and footers for advanced and intermediate document creation programs.**</span></span> <span data-ttu-id="18d18-348">如果用於多頁檔，請考慮為其他類型的程式提供標頭和頁尾。</span><span class="sxs-lookup"><span data-stu-id="18d18-348">Consider providing headers and footers for other types of programs if they are used for multipage documents.</span></span>
-   <span data-ttu-id="18d18-349">**讓標題和頁尾可自訂。**</span><span class="sxs-lookup"><span data-stu-id="18d18-349">**Make headers and footers customizable.**</span></span> <span data-ttu-id="18d18-350">允許使用者定義左邊、中間和右邊的部分。</span><span class="sxs-lookup"><span data-stu-id="18d18-350">Allow users to define the left, center, and right portions.</span></span>
    -   <span data-ttu-id="18d18-351">如果是標頭，請在預設的左邊放置檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="18d18-351">For headers, put the document name on the left side by default.</span></span>
    -   <span data-ttu-id="18d18-352">針對頁尾，將檔的著作權或來源放在左側，並依預設將頁碼放在右邊。</span><span class="sxs-lookup"><span data-stu-id="18d18-352">For footers, put the document copyright or source on the left side, and the page number on the right side, by default.</span></span>
-   <span data-ttu-id="18d18-353">**使用易記的檔案路徑和 Url。**</span><span class="sxs-lookup"><span data-stu-id="18d18-353">**Use friendly file path and URLs.**</span></span> <span data-ttu-id="18d18-354">將空格顯示為空格，而不是 "%20"。</span><span class="sxs-lookup"><span data-stu-id="18d18-354">Display spaces as spaces, not "%20."</span></span>

### <a name="print-commands"></a><span data-ttu-id="18d18-355">列印命令</span><span class="sxs-lookup"><span data-stu-id="18d18-355">Print commands</span></span>

-   <span data-ttu-id="18d18-356">**若為功能表列和快捷方式功能表，請使用顯示 [列印選項] 一般對話方塊的 [列印] 命令。**</span><span class="sxs-lookup"><span data-stu-id="18d18-356">**For menu bars and shortcut menus, use the Print command that displays the Print options common dialog.**</span></span> <span data-ttu-id="18d18-357">使用省略號表示需要額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="18d18-357">Use an ellipsis to indicate that additional information is required.</span></span>

    ![<span data-ttu-id="18d18-358">[檔案] 功能表的螢幕擷取畫面，已選取 [列印命令]</span><span class="sxs-lookup"><span data-stu-id="18d18-358">screen shot of file menu, print command selected</span></span> ](images/exper-printing-image7.png)

    <span data-ttu-id="18d18-359">在此範例中，Print 命令的省略號表示它將會顯示 [列印選項] 通用對話方塊，以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="18d18-359">In this example, the Print command has an ellipsis to indicate that it will display the Print options common dialog to get more information.</span></span>

-   <span data-ttu-id="18d18-360">**針對搭配功能表列使用的工具列，請使用立即列印命令。**</span><span class="sxs-lookup"><span data-stu-id="18d18-360">**For toolbars used with a menu bar, use an immediate Print command.**</span></span> <span data-ttu-id="18d18-361">按一下按鈕會將檔的單一複本列印到預設印表機。</span><span class="sxs-lookup"><span data-stu-id="18d18-361">Clicking the button prints a single copy of the document to the default printer.</span></span> <span data-ttu-id="18d18-362">這類工具列命令應該是立即的。</span><span class="sxs-lookup"><span data-stu-id="18d18-362">Such toolbar commands should be immediate.</span></span> <span data-ttu-id="18d18-363">若要指出命令是 immediate，請將預設印表機放在工具提示中。</span><span class="sxs-lookup"><span data-stu-id="18d18-363">To indicate that the command is immediate, put the default printer in the tooltip.</span></span> <span data-ttu-id="18d18-364">使用者可以從功能表列存取完整的列印命令。</span><span class="sxs-lookup"><span data-stu-id="18d18-364">Users can access the full Print command from the menu bar.</span></span>

    ![<span data-ttu-id="18d18-365">印表機圖示及其工具提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-365">screen shot of printer icon and its tooltip</span></span> ](images/exper-printing-image8.png)

    <span data-ttu-id="18d18-366">在此範例中，會立即列印工具列中的列印命令，而不是顯示 [列印選項] 一般對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-366">In this example, the Print command in a toolbar prints immediately instead of displaying the Print options common dialog.</span></span> <span data-ttu-id="18d18-367">將預設印表機放在工具提示中，可提供使用者略過對話方塊的文字增強式。</span><span class="sxs-lookup"><span data-stu-id="18d18-367">Putting the default printer in the tooltip provides textual reinforcement that the user is bypassing the dialog.</span></span>

-   <span data-ttu-id="18d18-368">**如果沒有功能表列使用的工具列，請使用 [列印分割] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="18d18-368">**For toolbars used without a menu bar, use a Print split button.**</span></span> <span data-ttu-id="18d18-369">按一下按鈕會將檔的單一複本列印到預設印表機。</span><span class="sxs-lookup"><span data-stu-id="18d18-369">Clicking the button prints a single copy of the document to the default printer.</span></span> <span data-ttu-id="18d18-370">按一下按鈕的箭號部分，就會以完整的列印、預覽列印和頁面設定命令來下移功能表。</span><span class="sxs-lookup"><span data-stu-id="18d18-370">Clicking the arrow portion of the button drops down a menu with full Print, Print preview, and Page setup commands.</span></span>

    ![<span data-ttu-id="18d18-371">[分割] 按鈕上的印表機圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-371">screen shot of printer icon on split button</span></span> ](images/exper-printing-image9.png)

    <span data-ttu-id="18d18-372">在此範例中，Windows Internet Explorer 工具列會使用分割按鈕控制項來提供所有列印命令。</span><span class="sxs-lookup"><span data-stu-id="18d18-372">In this example, the Windows Internet Explorer toolbar uses a split button control to provide all the print commands.</span></span>

-   <span data-ttu-id="18d18-373">**在 [功能區命令] 使用者介面中，將 [列印] 命令放在 [應用程式] 功能表中。**</span><span class="sxs-lookup"><span data-stu-id="18d18-373">**For the ribbon command user interface, put the Print command in the application menu.**</span></span>

    ![<span data-ttu-id="18d18-374">垂直放在左側的命令螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-374">screen shot of commands placed vertically on left</span></span> ](images/exper-printing-image10.png)

    <span data-ttu-id="18d18-375">針對功能區，可以使用 [應用程式] 功能表來存取列印命令。</span><span class="sxs-lookup"><span data-stu-id="18d18-375">For ribbons, the Print command is accessed using the application menu.</span></span>

### <a name="print-options"></a><span data-ttu-id="18d18-376">列印選項</span><span class="sxs-lookup"><span data-stu-id="18d18-376">Print options</span></span>

-   <span data-ttu-id="18d18-377">**不要建立自訂的 [列印選項] 對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="18d18-377">**Don't create a custom Print options dialog box.**</span></span> <span data-ttu-id="18d18-378">如果您必須提供其他選項，請展開 [列印選項一般] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-378">If you must provide additional options, extend the Print options common dialog.</span></span> <span data-ttu-id="18d18-379">請勿使用個別的對話方塊來進行其他列印選項。</span><span class="sxs-lookup"><span data-stu-id="18d18-379">Don't use a separate dialog for additional print options.</span></span>

<span data-ttu-id="18d18-380">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="18d18-380">**Incorrect:**</span></span>

![<span data-ttu-id="18d18-381">[自訂列印選項] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-381">screen shot of custom print options dialog box</span></span> ](images/exper-printing-image11.png)

<span data-ttu-id="18d18-382">在此範例中，Fabrikam 錯誤地針對其他列印選項使用個別的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-382">In this example, Fabrikam incorrectly uses a separate dialog for additional print options.</span></span>

<span data-ttu-id="18d18-383">**開發人員：** 如需如何擴充列印通用對話方塊的詳細資訊，請參閱 [PRINTDLGEX 結構](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)。</span><span class="sxs-lookup"><span data-stu-id="18d18-383">**Developers:** For information about how to extend the Print common dialog, see [PRINTDLGEX Structure](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).</span></span>

-   <span data-ttu-id="18d18-384">**擴充 [列印選項] 通用對話方塊時，請勿複製任何已提供的功能。**</span><span class="sxs-lookup"><span data-stu-id="18d18-384">**When extending the Print options common dialog, don't duplicate any features already provided.**</span></span>
-   <span data-ttu-id="18d18-385">**如果使用者可能會維護來自某個列印工作的設定，請將這些設定設為預設值。**</span><span class="sxs-lookup"><span data-stu-id="18d18-385">**If users are likely to maintain settings from one print job to the next, make those settings the defaults.**</span></span> <span data-ttu-id="18d18-386">若為程式啟動後的第一次列印工作，請使用標準預設值，包括預設印表機。</span><span class="sxs-lookup"><span data-stu-id="18d18-386">For the first print job after program launch, use the standard default values, including the default printer.</span></span> <span data-ttu-id="18d18-387">針對程式 [實例](glossary.md)中的後續列印工作，保留最後選取的印表機和紙張大小。</span><span class="sxs-lookup"><span data-stu-id="18d18-387">For subsequent print jobs in the program [instance](glossary.md), preserve the last selected printer and paper size.</span></span> <span data-ttu-id="18d18-388">請勿保留複本或頁面範圍的數目，因為它們在稍後可能較不問題。</span><span class="sxs-lookup"><span data-stu-id="18d18-388">Don't preserve the number of copies or page ranges, because these are far less likely to be reselected later.</span></span>
-   <span data-ttu-id="18d18-389">**移除目前未套用的選項，以將設定優化。**</span><span class="sxs-lookup"><span data-stu-id="18d18-389">**Optimize the settings by removing options that currently don't apply.**</span></span> <span data-ttu-id="18d18-390">移除與所選印表機的功能不一致的選項，或目前檔的特性。</span><span class="sxs-lookup"><span data-stu-id="18d18-390">Remove options that are inconsistent with the capabilities of the selected printer or characteristics of the current document.</span></span> <span data-ttu-id="18d18-391">例如，相片列印應用程式可能會限制提供最佳結果的紙張大小、紙張類型和列印品質的組合，因此選擇光澤紙選項可能會從紙張格式移除信封。</span><span class="sxs-lookup"><span data-stu-id="18d18-391">For example, a photo printing application could limit the combinations of paper size, paper type, and print quality that give the best results, so choosing a glossy paper option might remove envelopes from the paper formats.</span></span> <span data-ttu-id="18d18-392">如果使用者想要查看所有的選項，您可以透過控制項（例如核取方塊）提供這種功能。</span><span class="sxs-lookup"><span data-stu-id="18d18-392">If for any reason users want to see all the options, you can provide this ability through a control such as a check box.</span></span>

<span data-ttu-id="18d18-393">**開發人員：** 若要瞭解如何判斷所選印表機的功能，請參閱 [Print Schema](../printdocs/print-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="18d18-393">**Developers:** To learn how to determine the capabilities of the selected printer, see [Print Schema](../printdocs/print-schema.md).</span></span>

-   <span data-ttu-id="18d18-394">**若為 advanced document 建立程式，請在檔本身內儲存檔相關的列印選項。**</span><span class="sxs-lookup"><span data-stu-id="18d18-394">**For advanced document creation programs, save the document-related print options within the document itself.**</span></span> <span data-ttu-id="18d18-395">在這些程式中，列印選項是檔不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="18d18-395">For these programs, the print options are an integral part of the document.</span></span>
-   <span data-ttu-id="18d18-396">**針對其他類型的程式，請以每個使用者為基礎來儲存設定。**</span><span class="sxs-lookup"><span data-stu-id="18d18-396">**For other types of programs, save settings on a per-user basis.**</span></span>
-   <span data-ttu-id="18d18-397">**請考慮選取非預設印表機以進行特製化列印。**</span><span class="sxs-lookup"><span data-stu-id="18d18-397">**Consider selecting a non-default printer for specialized printing.**</span></span> <span data-ttu-id="18d18-398">例如，不論系統預設印表機為何，相片列印應用程式一律會選取程式最後使用的印表機。</span><span class="sxs-lookup"><span data-stu-id="18d18-398">For example, a photo printing application could always select the printer last used by the program, regardless of the system default printer.</span></span> <span data-ttu-id="18d18-399">這麼做會假設系統預設印表機不太可能是相片印表機。</span><span class="sxs-lookup"><span data-stu-id="18d18-399">Doing so assumes that the system default printer isn't likely to be a photo printer.</span></span> <span data-ttu-id="18d18-400">這類程式應儲存最後選取之印表機的設定。</span><span class="sxs-lookup"><span data-stu-id="18d18-400">Such programs should save the setting for the last selected printer.</span></span>
-   <span data-ttu-id="18d18-401">**偵測印表機功能時，請勿鎖定您的程式。**</span><span class="sxs-lookup"><span data-stu-id="18d18-401">**Don't lock up your program while detecting printer capabilities.**</span></span> <span data-ttu-id="18d18-402">這樣做會提供不佳的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="18d18-402">Doing so presents a poor user experience.</span></span> <span data-ttu-id="18d18-403">請改為：</span><span class="sxs-lookup"><span data-stu-id="18d18-403">Instead, either:</span></span>
    -   <span data-ttu-id="18d18-404">在不同的執行緒中執行印表機功能偵測。</span><span class="sxs-lookup"><span data-stu-id="18d18-404">Perform the printer capability detection in a separate thread.</span></span>
    -   <span data-ttu-id="18d18-405">10秒後的超時時間。</span><span class="sxs-lookup"><span data-stu-id="18d18-405">Time out after 10 seconds.</span></span>
    -   <span data-ttu-id="18d18-406">提供可讓使用者取消的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-406">Provide a dialog box to allow users to cancel.</span></span>

![<span data-ttu-id="18d18-407">[連接到] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-407">screen shot of 'connecting to' dialog box</span></span> ](images/exper-printing-image12.png)

<span data-ttu-id="18d18-408">在此範例中，如果使用者判斷工作所花的時間太長，對話方塊可讓您輕鬆地取消印表機功能偵測。</span><span class="sxs-lookup"><span data-stu-id="18d18-408">In this example, the dialog box makes it easy to cancel the printer capability detection if the user decides the task is taking too long.</span></span>

### <a name="print-previews"></a><span data-ttu-id="18d18-409">預覽列印</span><span class="sxs-lookup"><span data-stu-id="18d18-409">Print previews</span></span>

-   <span data-ttu-id="18d18-410">**在適當時提供預覽列印功能。**</span><span class="sxs-lookup"><span data-stu-id="18d18-410">**Provide a print preview feature whenever appropriate.**</span></span> <span data-ttu-id="18d18-411">所有檔建立程式都受益于預覽列印，但使用者不會在簡單的檔建立程式中預期這些程式。</span><span class="sxs-lookup"><span data-stu-id="18d18-411">All document creation programs benefit from print previews, but users don't expect them in simple document creation programs.</span></span> <span data-ttu-id="18d18-412">針對先進的檔建立程式，請考慮直接在主要程式視窗內提供預覽列印支援。</span><span class="sxs-lookup"><span data-stu-id="18d18-412">For advanced document creation programs, consider having print preview support directly within the main program window.</span></span>

![<span data-ttu-id="18d18-413">顯示于預覽列印中頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-413">screen shot of page displayed in print preview</span></span> ](images/exper-printing-image13.png)

<span data-ttu-id="18d18-414">在此範例中，Word 在主要程式視窗內有預覽列印支援。</span><span class="sxs-lookup"><span data-stu-id="18d18-414">In this example, Word has print preview support within the main program window.</span></span>

-   <span data-ttu-id="18d18-415">提供預覽列印功能，讓使用者能夠：</span><span class="sxs-lookup"><span data-stu-id="18d18-415">Provide print preview features that allow users to:</span></span>
    -   <span data-ttu-id="18d18-416">評估邊界、分頁符號、頁面方向、標題和頁尾。</span><span class="sxs-lookup"><span data-stu-id="18d18-416">Evaluate margins, page breaks, page orientation, headers, and footers.</span></span>
    -   <span data-ttu-id="18d18-417">流覽所有頁面。</span><span class="sxs-lookup"><span data-stu-id="18d18-417">Browse through all the pages.</span></span>
    -   <span data-ttu-id="18d18-418">直接從預覽列印列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-418">Print directly from the print preview.</span></span>

<span data-ttu-id="18d18-419">請考慮提供互動式預覽列印，讓使用者可以直接在預覽中調整經常變更的設定，例如邊界和分行符號。</span><span class="sxs-lookup"><span data-stu-id="18d18-419">Consider providing an interactive print preview so that users can adjust frequently changed settings like margins and line breaks directly within the preview.</span></span>

-   <span data-ttu-id="18d18-420">**讓預覽列印頁面在一秒內轉譯。**</span><span class="sxs-lookup"><span data-stu-id="18d18-420">**Have print preview pages render within one second.**</span></span> <span data-ttu-id="18d18-421">最好是讓預覽列印快速呈現，且精確度足以讓使用者評估列印結果，而不是完全精確的預覽以產生緩慢的呈現。</span><span class="sxs-lookup"><span data-stu-id="18d18-421">It's better to have a print preview that renders quickly and is accurate enough to allow users to evaluate the print results than to have a completely accurate preview that renders slowly.</span></span>
-   <span data-ttu-id="18d18-422">**針對先進的檔建立程式，請考慮直接在其中併入預覽功能，** 而不是為它建立個別的對話方塊，以擴充標準的 [列印] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="18d18-422">**For advanced document creation programs, consider extending the standard Print dialog box by incorporating preview functionality directly within it,** rather than creating a separate dialog for it.</span></span>
-   <span data-ttu-id="18d18-423">**提供明顯的按鈕來關閉預覽模式。**</span><span class="sxs-lookup"><span data-stu-id="18d18-423">**Provide an obvious button for closing preview mode.**</span></span>

![<span data-ttu-id="18d18-424">關閉預覽列印圖示和標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="18d18-424">screen shot of close print preview icon and label</span></span> ](images/exper-printing-image14.png)

<span data-ttu-id="18d18-425">Word 中的預覽列印模式有明顯的關閉預覽命令。</span><span class="sxs-lookup"><span data-stu-id="18d18-425">The Print Preview mode in Word has an obvious close preview command.</span></span>

### <a name="printing-errors"></a><span data-ttu-id="18d18-426">列印錯誤</span><span class="sxs-lookup"><span data-stu-id="18d18-426">Printing errors</span></span>

<span data-ttu-id="18d18-427">**注意：** 將列印工作送入印表機之後，Windows 就會負責任何後續的錯誤。</span><span class="sxs-lookup"><span data-stu-id="18d18-427">**Note:** Once the print job has been spooled to the printer, Windows is responsible for any subsequent errors.</span></span> <span data-ttu-id="18d18-428">您的程式只需要處理列印工作在幕後處理之前發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="18d18-428">Your program only has to handle errors that happen before the print job is spooled.</span></span>

-   <span data-ttu-id="18d18-429">**在將列印工作緩衝處理之前，請檢查使用者是否可以修正任何可能的列印問題。**</span><span class="sxs-lookup"><span data-stu-id="18d18-429">**Before spooling a print job, check for any potential printing problems the user can fix.**</span></span> <span data-ttu-id="18d18-430">請先提出清楚、精確的確認，再繼續進行列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-430">Present a clear, concise confirmation before continuing to print.</span></span> <span data-ttu-id="18d18-431">可能的話，請提供，以自動修正問題。</span><span class="sxs-lookup"><span data-stu-id="18d18-431">Whenever possible, offer to fix the problem automatically.</span></span> <span data-ttu-id="18d18-432">這樣做可能會導致浪費時間和金錢。</span><span class="sxs-lookup"><span data-stu-id="18d18-432">Doing so can prevent a waste of time and money.</span></span>

## <a name="text"></a><span data-ttu-id="18d18-433">Text</span><span class="sxs-lookup"><span data-stu-id="18d18-433">Text</span></span>

-   <span data-ttu-id="18d18-434">若要在紙張兩側列印的選項，請將選項標記為雙面列印。</span><span class="sxs-lookup"><span data-stu-id="18d18-434">For the option to print on both sides of the paper, label the option Print double-sided.</span></span> <span data-ttu-id="18d18-435">請勿使用片語手動雙工。</span><span class="sxs-lookup"><span data-stu-id="18d18-435">Don't use the phrase Manual Duplex.</span></span>

## <a name="documentation"></a><span data-ttu-id="18d18-436">文件</span><span class="sxs-lookup"><span data-stu-id="18d18-436">Documentation</span></span>

-   <span data-ttu-id="18d18-437">使用 print （非 print out）作為動詞。</span><span class="sxs-lookup"><span data-stu-id="18d18-437">Use print, not print out, as a verb.</span></span>
-   <span data-ttu-id="18d18-438">您可以使用列印輸出來參考列印工作的結果。</span><span class="sxs-lookup"><span data-stu-id="18d18-438">It's acceptable to use printout to refer to the result of a print job.</span></span>
-   <span data-ttu-id="18d18-439">使用列印佇列，而非印表機佇列。</span><span class="sxs-lookup"><span data-stu-id="18d18-439">Use print queue, not printer queue.</span></span>

