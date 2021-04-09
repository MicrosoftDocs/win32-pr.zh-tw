---
title: HTML 剪貼簿格式
description: 本節討論 HTML 剪貼簿格式。
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows 消費者介面，剪貼簿
- 剪貼簿，資料剪下
- 剪貼簿，複製資料
- 剪貼簿，貼上資料
- 剪貼簿，格式
- 剪貼簿、HTML 格式
- 剪貼簿、剪切的 HTML 文字
- 剪貼簿，貼上 HTML 文字
- CF_HTML 剪貼簿格式
- 剪貼簿，CF_HTML 格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021621"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="400b7-113">HTML 剪貼簿格式</span><span class="sxs-lookup"><span data-stu-id="400b7-113">HTML Clipboard Format</span></span>

<span data-ttu-id="400b7-114">根據案例，透過剪貼簿傳輸 HTML 文字的需求會有所不同。</span><span class="sxs-lookup"><span data-stu-id="400b7-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="400b7-115">本文將說明如何剪下和貼上 HTML 檔案的片段。</span><span class="sxs-lookup"><span data-stu-id="400b7-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="400b7-116">可能需要透過剪貼簿傳送整個 HTML 檔案;不過，這篇文章是由傳送所選 HTML 文字片段的需求所驅動。</span><span class="sxs-lookup"><span data-stu-id="400b7-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="400b7-117">因此，需要將整個 HTML 檔案複製到剪貼簿的方法會被視為過於重量級。</span><span class="sxs-lookup"><span data-stu-id="400b7-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="400b7-118">CF \_ html 剪貼簿格式允許原始 HTML 文字和其內容的片段以 ASCII 的形式儲存在剪貼簿上。</span><span class="sxs-lookup"><span data-stu-id="400b7-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="400b7-119">這可讓應用程式檢查 HTML 片段的內容（由所有前面加上標籤組成），讓 HTML 片段的周圍標記可以用其屬性來注明。</span><span class="sxs-lookup"><span data-stu-id="400b7-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="400b7-120">雖然應用程式是由決定如何解讀這類片段的應用程式所決定，但根據 IE4/MSHTML 的執行，這裡有一些基本的指導方針。</span><span class="sxs-lookup"><span data-stu-id="400b7-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="400b7-121">剪貼簿的官方名稱 (RegisterClipboardFormat) 使用的字串是 HTML 格式。</span><span class="sxs-lookup"><span data-stu-id="400b7-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="400b7-122">說明</span><span class="sxs-lookup"><span data-stu-id="400b7-122">Description</span></span>](#description)
-   [<span data-ttu-id="400b7-123">案例</span><span class="sxs-lookup"><span data-stu-id="400b7-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="400b7-124">Description</span><span class="sxs-lookup"><span data-stu-id="400b7-124">Description</span></span>

<span data-ttu-id="400b7-125">CF \_ html 完全是文字格式 (是在 HTML 精神中的其他專案，而且會使用 utf-8) 並在內容中包含 `description` 、選擇性和 `context` `fragment` 。</span><span class="sxs-lookup"><span data-stu-id="400b7-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="400b7-126">以下是剪貼簿的範例：</span><span class="sxs-lookup"><span data-stu-id="400b7-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="400b7-127">描述包括剪貼簿版本號碼和位移，指出內容和片段的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="400b7-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="400b7-128">描述是 ASCII 文字關鍵字的清單， (min/maj 沒有意義) 後面接著字串，並以冒號 (： ) 分隔。</span><span class="sxs-lookup"><span data-stu-id="400b7-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="400b7-129">**版本**：剪貼簿的 >-vv 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="400b7-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="400b7-130">起始版本為0.9。</span><span class="sxs-lookup"><span data-stu-id="400b7-130">Starting version is 0.9.</span></span>

<span data-ttu-id="400b7-131">**StartHTML**：從剪貼簿的開頭 bytecount 至內容的開頭; 如果沒有內容，則為-1。</span><span class="sxs-lookup"><span data-stu-id="400b7-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="400b7-132">**EndHTML**：從剪貼簿的開頭 bytecount 至內容的結尾，如果沒有內容，則為-1。</span><span class="sxs-lookup"><span data-stu-id="400b7-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="400b7-133">**StartFragment**：從剪貼簿開頭到片段開頭的 bytecount。</span><span class="sxs-lookup"><span data-stu-id="400b7-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="400b7-134">**EndFragment**：從剪貼簿開頭到片段結尾的 bytecount。</span><span class="sxs-lookup"><span data-stu-id="400b7-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="400b7-135">**StartSelection**：從剪貼簿的開頭 bytecount 至選取範圍的開頭。</span><span class="sxs-lookup"><span data-stu-id="400b7-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="400b7-136">**EndSelection**：從剪貼簿的開頭 bytecount 至選取範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="400b7-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="400b7-137">StartSelection 和 EndSelection 關鍵字是選擇性的，如果您不想讓應用程式產生這項資訊，則必須省略這兩者。</span><span class="sxs-lookup"><span data-stu-id="400b7-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="400b7-138">此類型的其他資訊可以在稍後加入，因為 HTML 是從 StartHTMLoffset 開始。</span><span class="sxs-lookup"><span data-stu-id="400b7-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="400b7-139">例如，您可以稍後新增多組 StartFragment/EndFragment，以支援連續選取的片段。</span><span class="sxs-lookup"><span data-stu-id="400b7-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="400b7-140">為了方便產生 bytecounts 的程式，bytecounts 可能會以零填補。</span><span class="sxs-lookup"><span data-stu-id="400b7-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="400b7-141">例如，產生 bytecounts 的程式可能會對每個關鍵字 (StartHTML： 0000000000)  (10 個) 零產生任意影響，然後，如果已知的 StartHTML bytecount 是已知的 bytecount （ (假設為 71) ），則程式可以將 StartHTML (： 0000000071) 取代為適當的零數目。</span><span class="sxs-lookup"><span data-stu-id="400b7-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="400b7-142">剪貼簿唯一支援的字元集是其 UTF-8 編碼中的 Unicode。</span><span class="sxs-lookup"><span data-stu-id="400b7-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="400b7-143">由於 UTF-8 和 ASCII 的第一個字元相符，因此描述一律為 ASCII，但是內容 (的位元組在 StartHTML) 可能會使用以 UTF-8 編碼的其他任何字元。</span><span class="sxs-lookup"><span data-stu-id="400b7-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="400b7-144">剪貼簿格式標頭中的行尾可以是 CR 或 CR/LF 或 LF。</span><span class="sxs-lookup"><span data-stu-id="400b7-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="400b7-145">片段包含純有效的 HTML，代表使用者選取 (複製的區域，例如) 。</span><span class="sxs-lookup"><span data-stu-id="400b7-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="400b7-146">這包含選取的文字加上在選取的文字中具有結束標記之任何專案的開頭標記和屬性，以及包含任何開始標記之片段結尾的結束記號。</span><span class="sxs-lookup"><span data-stu-id="400b7-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="400b7-147">這是基本貼上 HTML 片段所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="400b7-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="400b7-148">片段前後都必須加上 HTML 批註</span><span class="sxs-lookup"><span data-stu-id="400b7-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="400b7-149">及</span><span class="sxs-lookup"><span data-stu-id="400b7-149">and</span></span> <!--EndFragment--> <span data-ttu-id="400b7-150"> (!--和文字) 之間不允許空格，方便地指出片段的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="400b7-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="400b7-151">因此，片段的開頭和結尾會以這些批註的存在，以及描述中的 StartFragment 和 EndFragment 位元組計數來表示。</span><span class="sxs-lookup"><span data-stu-id="400b7-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="400b7-152">預期工具會產生此資訊。</span><span class="sxs-lookup"><span data-stu-id="400b7-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="400b7-153">導入此冗余是為了能夠快速地從 [位元組計數]) 中找出片段 (的起點，並將片段的位置直接標示在 HTML 樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="400b7-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="400b7-154">選取範圍會在片段中指出使用者已選取 (複製的確切 HTML 區域，例如) 。</span><span class="sxs-lookup"><span data-stu-id="400b7-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="400b7-155">這會藉由指出確切選取的文字，而不使用已新增的開頭標記和結束標記，將更多資訊新增至片段，以確保片段是格式正確的 HTML。</span><span class="sxs-lookup"><span data-stu-id="400b7-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="400b7-156">選取範圍是選擇性的，因為包含在基本貼上的片段中包含足夠的資訊。</span><span class="sxs-lookup"><span data-stu-id="400b7-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="400b7-157">如果未儲存選取專案，StartSelection 和 EndSelection 都不會儲存在標頭中。</span><span class="sxs-lookup"><span data-stu-id="400b7-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="400b7-158">內容是有效、完整的 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="400b7-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="400b7-159">本文包含片段和所有前面的標記 (開始和結束標記;這些先前周圍的標記代表片段的所有父節點，直到 HTML 節點) 為止。</span><span class="sxs-lookup"><span data-stu-id="400b7-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="400b7-160">本文也包含完整的標頭，並允許包含 BASE 和 TITLE 元素，因此可以取得此額外資訊。</span><span class="sxs-lookup"><span data-stu-id="400b7-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="400b7-161">將 HTML 片段複製到剪貼簿的應用程式可以選擇建立要包含在內容中的基底專案，如果這類元素不存在，就可以解析片段中的部分 Url。</span><span class="sxs-lookup"><span data-stu-id="400b7-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="400b7-162">內容是選擇性的，因為片段中包含足夠的資訊，可讓您進行基本的 HTML 片段貼上。</span><span class="sxs-lookup"><span data-stu-id="400b7-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="400b7-163">如果未儲存內容，則只會儲存片段，且 StartHTML = EndHTML =-1。</span><span class="sxs-lookup"><span data-stu-id="400b7-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="400b7-164">案例</span><span class="sxs-lookup"><span data-stu-id="400b7-164">Scenarios</span></span>

<span data-ttu-id="400b7-165">下列案例描述 IE4/MSHTML HTML 編輯器如何處理 HTML 剪下和貼上;其他應用程式不一定會遵循這些案例。</span><span class="sxs-lookup"><span data-stu-id="400b7-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="400b7-166">此處所述的剪貼簿格式，目的是要讓應用程式選擇運作的彈性更加靈活。</span><span class="sxs-lookup"><span data-stu-id="400b7-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="400b7-167"> (這些案例只會顯示良好的 HTML，也就是沒有重迭的標記。 ) </span><span class="sxs-lookup"><span data-stu-id="400b7-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="400b7-168">HTML 的簡單片段。</span><span class="sxs-lookup"><span data-stu-id="400b7-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="400b7-169">HTML 文字：</span><span class="sxs-lookup"><span data-stu-id="400b7-169">HTML text:</span></span>

            <span data-ttu-id="400b7-170"><BODY>這是正常的，這是<B>粗體</B> <I><B>斜體</B>，這是斜體</I></BODY></span><span class="sxs-lookup"><span data-stu-id="400b7-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="400b7-171">顯示為：</span><span class="sxs-lookup"><span data-stu-id="400b7-171">Appears as:</span></span>

            <span data-ttu-id="400b7-172">這是正常的，這是 **粗體**，此為    \*    斜體 \*</span><span class="sxs-lookup"><span data-stu-id="400b7-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="400b7-173">選取的文字 \* \* 並複製到剪貼簿：</span><span class="sxs-lookup"><span data-stu-id="400b7-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="400b7-174">這 **是正常的，這** 是粗體，這是 \* \*     \* **粗體**   的 \* \* \* *是斜體*</span><span class="sxs-lookup"><span data-stu-id="400b7-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="400b7-175">這是剪貼簿 (注意這是 IE4/MSHTML 的解讀) ：</span><span class="sxs-lookup"><span data-stu-id="400b7-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="400b7-176">版本：0。9</span><span class="sxs-lookup"><span data-stu-id="400b7-176">Version:0.9</span></span>

            <span data-ttu-id="400b7-177">StartHTML：71</span><span class="sxs-lookup"><span data-stu-id="400b7-177">StartHTML:71</span></span>

            <span data-ttu-id="400b7-178">EndHTML：160</span><span class="sxs-lookup"><span data-stu-id="400b7-178">EndHTML:160</span></span>

            <span data-ttu-id="400b7-179">StartFragment：130</span><span class="sxs-lookup"><span data-stu-id="400b7-179">StartFragment:130</span></span>

            <span data-ttu-id="400b7-180">EndFragment：150</span><span class="sxs-lookup"><span data-stu-id="400b7-180">EndFragment:150</span></span>

            <span data-ttu-id="400b7-181">**StartSelection：130**</span><span class="sxs-lookup"><span data-stu-id="400b7-181">**StartSelection:130**</span></span>

            <span data-ttu-id="400b7-182">**EndSelection：150**</span><span class="sxs-lookup"><span data-stu-id="400b7-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="400b7-183">**<B>粗體</B><I><B>，這是以粗體顯示</B></I>**</span><span class="sxs-lookup"><span data-stu-id="400b7-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="400b7-184">在此案例中，只有內文標記和 HTML 標籤會出現在內容中，如同選取的片段之前。</span><span class="sxs-lookup"><span data-stu-id="400b7-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="400b7-185">請注意，開始標記和結束標記會包含在內容中。</span><span class="sxs-lookup"><span data-stu-id="400b7-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="400b7-186">選取範圍（以 StartSelection 和 EndSelection 分隔）會以粗體顯示。</span><span class="sxs-lookup"><span data-stu-id="400b7-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="400b7-187">HTML 中資料表的片段。</span><span class="sxs-lookup"><span data-stu-id="400b7-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="400b7-188">HTML 文字：</span><span class="sxs-lookup"><span data-stu-id="400b7-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="400b7-189">Head1</span><span class="sxs-lookup"><span data-stu-id="400b7-189">Head1</span></span></TH><TD><span data-ttu-id="400b7-190">項目 1</span><span class="sxs-lookup"><span data-stu-id="400b7-190">Item 1</span></span></TD><TD><span data-ttu-id="400b7-191">項目 2</span><span class="sxs-lookup"><span data-stu-id="400b7-191">Item 2</span></span></TD><TD><span data-ttu-id="400b7-192">項目 3</span><span class="sxs-lookup"><span data-stu-id="400b7-192">Item 3</span></span></TD><TD><span data-ttu-id="400b7-193">專案4</span><span class="sxs-lookup"><span data-stu-id="400b7-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="400b7-194">專案5</span><span class="sxs-lookup"><span data-stu-id="400b7-194">Item 5</span></span></TD><TD><span data-ttu-id="400b7-195">專案6</span><span class="sxs-lookup"><span data-stu-id="400b7-195">Item 6</span></span></TD><TD><span data-ttu-id="400b7-196">專案7</span><span class="sxs-lookup"><span data-stu-id="400b7-196">Item 7</span></span></TD><TD><span data-ttu-id="400b7-197">專案8</span><span class="sxs-lookup"><span data-stu-id="400b7-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="400b7-198">Head2</span><span class="sxs-lookup"><span data-stu-id="400b7-198">Head2</span></span></TH><TD><span data-ttu-id="400b7-199">專案9</span><span class="sxs-lookup"><span data-stu-id="400b7-199">Item 9</span></span></TD><TD><span data-ttu-id="400b7-200">項目 10</span><span class="sxs-lookup"><span data-stu-id="400b7-200">Item 10</span></span></TD><TD><span data-ttu-id="400b7-201">專案11</span><span class="sxs-lookup"><span data-stu-id="400b7-201">Item 11</span></span></TD><TD><span data-ttu-id="400b7-202">專案12</span><span class="sxs-lookup"><span data-stu-id="400b7-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="400b7-203">顯示為： ></span><span class="sxs-lookup"><span data-stu-id="400b7-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="400b7-204">Head1</span><span class="sxs-lookup"><span data-stu-id="400b7-204">Head1</span></span></TH><TD><span data-ttu-id="400b7-205">項目 1</span><span class="sxs-lookup"><span data-stu-id="400b7-205">Item 1</span></span></TD><TD><span data-ttu-id="400b7-206">項目 2</span><span class="sxs-lookup"><span data-stu-id="400b7-206">Item 2</span></span></TD><TD><span data-ttu-id="400b7-207">項目 3</span><span class="sxs-lookup"><span data-stu-id="400b7-207">Item 3</span></span></TD><TD><span data-ttu-id="400b7-208">專案4</span><span class="sxs-lookup"><span data-stu-id="400b7-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="400b7-209">專案5</span><span class="sxs-lookup"><span data-stu-id="400b7-209">Item 5</span></span></TD><TD><span data-ttu-id="400b7-210">專案6</span><span class="sxs-lookup"><span data-stu-id="400b7-210">Item 6</span></span></TD><TD><span data-ttu-id="400b7-211">專案7</span><span class="sxs-lookup"><span data-stu-id="400b7-211">Item 7</span></span></TD><TD><span data-ttu-id="400b7-212">專案8</span><span class="sxs-lookup"><span data-stu-id="400b7-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="400b7-213">Head2</span><span class="sxs-lookup"><span data-stu-id="400b7-213">Head2</span></span></TH><TD><span data-ttu-id="400b7-214">專案9</span><span class="sxs-lookup"><span data-stu-id="400b7-214">Item 9</span></span></TD><TD><span data-ttu-id="400b7-215">項目 10</span><span class="sxs-lookup"><span data-stu-id="400b7-215">Item 10</span></span></TD><TD><span data-ttu-id="400b7-216">專案11</span><span class="sxs-lookup"><span data-stu-id="400b7-216">Item 11</span></span></TD><TD><span data-ttu-id="400b7-217">專案12</span><span class="sxs-lookup"><span data-stu-id="400b7-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="400b7-218"><！ \[Cdata\[\]\]></span><span class="sxs-lookup"><span data-stu-id="400b7-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="400b7-219">系統會選取資料表的專案6、Tuple.item7、專案10和專案11元素做為區塊，然後複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="400b7-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="400b7-220">這是剪貼簿 (注意這是 IE4/MSHTML 的解讀) ：</span><span class="sxs-lookup"><span data-stu-id="400b7-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="400b7-221">**<TR><TD>專案 6 </TD> <TD> 專案 7 </TD> </TR> <TR> <TD> 專案 10 </TD> <TD> 專案11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="400b7-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="400b7-222">將已排序清單的片段貼入純文字中。</span><span class="sxs-lookup"><span data-stu-id="400b7-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="400b7-223">HTML 文字：</span><span class="sxs-lookup"><span data-stu-id="400b7-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="400b7-224">項目 1</span><span class="sxs-lookup"><span data-stu-id="400b7-224">Item 1</span></span><LI><span data-ttu-id="400b7-225">項目 2</span><span class="sxs-lookup"><span data-stu-id="400b7-225">Item 2</span></span><LI><span data-ttu-id="400b7-226">項目 3</span><span class="sxs-lookup"><span data-stu-id="400b7-226">Item 3</span></span><LI><span data-ttu-id="400b7-227">專案4</span><span class="sxs-lookup"><span data-stu-id="400b7-227">Item 4</span></span><LI><span data-ttu-id="400b7-228">專案5</span><span class="sxs-lookup"><span data-stu-id="400b7-228">Item 5</span></span><LI><span data-ttu-id="400b7-229">專案6</span><span class="sxs-lookup"><span data-stu-id="400b7-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="400b7-230">顯示為：</span><span class="sxs-lookup"><span data-stu-id="400b7-230">Appears as:</span></span>
            1.  <span data-ttu-id="400b7-231">項目 1</span><span class="sxs-lookup"><span data-stu-id="400b7-231">Item 1</span></span>
            2.  <span data-ttu-id="400b7-232">項目 2</span><span class="sxs-lookup"><span data-stu-id="400b7-232">Item 2</span></span>
            3.  <span data-ttu-id="400b7-233">項目 3</span><span class="sxs-lookup"><span data-stu-id="400b7-233">Item 3</span></span>
            4.  <span data-ttu-id="400b7-234">專案4</span><span class="sxs-lookup"><span data-stu-id="400b7-234">Item 4</span></span>
            5.  <span data-ttu-id="400b7-235">專案5</span><span class="sxs-lookup"><span data-stu-id="400b7-235">Item 5</span></span>
            6.  <span data-ttu-id="400b7-236">專案6</span><span class="sxs-lookup"><span data-stu-id="400b7-236">Item 6</span></span>
        -   <span data-ttu-id="400b7-237">使用者選取並將專案3到5複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="400b7-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="400b7-238">下列 HTML 位於剪貼簿中：</span><span class="sxs-lookup"><span data-stu-id="400b7-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="400b7-239"><DOCTYPE ... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="400b7-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="400b7-240">**<LI>專案 3 <LI> 專案 4 <LI> 專案5**</span><span class="sxs-lookup"><span data-stu-id="400b7-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="400b7-241">選取範圍（以 StartSelection 和 EndSelection 分隔）會以粗體顯示。</span><span class="sxs-lookup"><span data-stu-id="400b7-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="400b7-242">如果此片段現在貼入空白檔，將會建立下列 HTML：</span><span class="sxs-lookup"><span data-stu-id="400b7-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="400b7-243">項目 3</span><span class="sxs-lookup"><span data-stu-id="400b7-243">Item 3</span></span><LI><span data-ttu-id="400b7-244">專案4</span><span class="sxs-lookup"><span data-stu-id="400b7-244">Item 4</span></span><LI><span data-ttu-id="400b7-245">專案5</span><span class="sxs-lookup"><span data-stu-id="400b7-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="400b7-246">顯示為：</span><span class="sxs-lookup"><span data-stu-id="400b7-246">Appearing as:</span></span>
            1.  <span data-ttu-id="400b7-247">項目 3</span><span class="sxs-lookup"><span data-stu-id="400b7-247">Item 3</span></span>
            2.  <span data-ttu-id="400b7-248">專案4</span><span class="sxs-lookup"><span data-stu-id="400b7-248">Item 4</span></span>
            3.  <span data-ttu-id="400b7-249">專案5</span><span class="sxs-lookup"><span data-stu-id="400b7-249">Item 5</span></span>

4.  <span data-ttu-id="400b7-250">貼入部分選取的區域。</span><span class="sxs-lookup"><span data-stu-id="400b7-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="400b7-251">HTML 文字：</span><span class="sxs-lookup"><span data-stu-id="400b7-251">HTML text:</span></span>

            <P> <span data-ttu-id="400b7-252">IE4/MSHTML 是 WYSIWYG 編輯器，支援：</span><span class="sxs-lookup"><span data-stu-id="400b7-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="400b7-253">剪下</span><span class="sxs-lookup"><span data-stu-id="400b7-253">Cut</span></span><LI><span data-ttu-id="400b7-254">複製</span><span class="sxs-lookup"><span data-stu-id="400b7-254">Copy</span></span><LI><span data-ttu-id="400b7-255">貼上</span><span class="sxs-lookup"><span data-stu-id="400b7-255">Paste</span></span></UL><P><span data-ttu-id="400b7-256">這是很棒的工具！</span><span class="sxs-lookup"><span data-stu-id="400b7-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="400b7-257">顯示為： IE4/MSHTML 是 WYSIWYG 編輯器，支援：</span><span class="sxs-lookup"><span data-stu-id="400b7-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="400b7-258">剪下</span><span class="sxs-lookup"><span data-stu-id="400b7-258">Cut</span></span>
                -   <span data-ttu-id="400b7-259">複製</span><span class="sxs-lookup"><span data-stu-id="400b7-259">Copy</span></span>
                -   <span data-ttu-id="400b7-260">貼上</span><span class="sxs-lookup"><span data-stu-id="400b7-260">Paste</span></span>

        -   <span data-ttu-id="400b7-261">使用者從 "WYSIWYG" 開始選取，直到 "Cop" 為止。下列 HTML 位於剪貼簿中：</span><span class="sxs-lookup"><span data-stu-id="400b7-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="400b7-262"><DOCTYPE ... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="400b7-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="400b7-263">**WYSIWYG 編輯器，支援**</span><span class="sxs-lookup"><span data-stu-id="400b7-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="400b7-264">**<UL><LI>剪下 <LI> Cop**</span><span class="sxs-lookup"><span data-stu-id="400b7-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="400b7-265">使用者選取 "複製"，直到「絕佳」。</span><span class="sxs-lookup"><span data-stu-id="400b7-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="400b7-266">下列 HTML 位於剪貼簿中：</span><span class="sxs-lookup"><span data-stu-id="400b7-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="400b7-267"><DOCTYPE ... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="400b7-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="400b7-268">**複製 <LI> 貼上很 </UL> <P> 棒**</span><span class="sxs-lookup"><span data-stu-id="400b7-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="400b7-269">選取範圍（以 StartSelection 和 EndSelection 分隔）會以粗體顯示。</span><span class="sxs-lookup"><span data-stu-id="400b7-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




