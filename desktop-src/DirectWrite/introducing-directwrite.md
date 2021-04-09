---
title: DirectWrite 簡介
description: 人們會在每日生活中隨時與文字進行通訊。
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite，關於
- DirectWrite，印刷樣式功能
- 印刷樣式
- DirectWrite，國際文字
- DirectWrite，OpenType 字型
- OpenType 字型
- DirectWrite，ClearType
- ClearType
- DirectWrite，API 總覽
- DirectWrite、IDWriteFontFace
- IDWriteFontFace
- DirectWrite，文字轉譯
- DirectWrite，轉譯模式
- DirectWrite，GDI 交互操作
- DirectWrite，互通性
- 互通性，DirectWrite
- '互通性、圖形裝置介面 (GDI) '
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842679"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="ed2ba-122">DirectWrite 簡介</span><span class="sxs-lookup"><span data-stu-id="ed2ba-122">Introducing DirectWrite</span></span>

<span data-ttu-id="ed2ba-123">人們會在每日生活中隨時與文字進行通訊。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="ed2ba-124">這是人們取用增加資訊量的主要方式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="ed2ba-125">過去，它是用來透過印刷的內容，主要是檔、報紙、書籍等等。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="ed2ba-126">越來越多，它是 Windows 電腦上的線上內容。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="ed2ba-127">一般的 Windows 使用者從電腦螢幕上花了很多時間來進行讀取。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="ed2ba-128">他們可能會在網路上衝浪、掃描電子郵件、撰寫報表、填寫試算表或撰寫軟體，但他們其實正在閱讀。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="ed2ba-129">雖然文字和字型幾乎穿透 Windows 中使用者體驗的每個部分，但對大部分的使用者而言，在螢幕上閱讀並不如閱讀列印輸出一樣愉快。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="ed2ba-130">針對 Windows 應用程式開發人員，撰寫文字處理程式碼是一項挑戰，因為提高可讀性、精密的格式和版面配置控制項，以及支援應用程式必須顯示的多種語言都有更高的需求。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="ed2ba-131">即使是最基本的文字處理系統，也必須允許文字輸入、版面配置、顯示、編輯和複製和貼上。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="ed2ba-132">Windows 使用者通常會預期更多的基本功能，甚至需要簡單的編輯器來支援多種字型、各種段落樣式、內嵌影像、拼寫檢查，以及其他功能。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="ed2ba-133">新式 UI 設計也不再局限于單一格式（純文字），但需要以豐富的字型和文字版面配置提供更好的體驗。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="ed2ba-134">這是 [DirectWrite](direct-write-portal.md) 如何讓 Windows 應用程式增強 UI 和檔文字體驗的簡介。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="ed2ba-135">改善文字體驗</span><span class="sxs-lookup"><span data-stu-id="ed2ba-135">Improving the Text Experience</span></span>

<span data-ttu-id="ed2ba-136">新式 Windows 應用程式對於其 UI 和檔中的文字有精密的需求。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="ed2ba-137">這些包括更好的可讀性、支援多種語言和腳本，以及出色的轉譯效能。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="ed2ba-138">此外，大部分現有的應用程式都需要一種方法，在 WindowsWin32 程式碼基底中履行現有的投資。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="ed2ba-139">[DirectWrite](direct-write-portal.md) 提供下列三項功能，可讓 Windows 應用程式開發人員改善其應用程式內的文字體驗：與轉譯系統的獨立性、高品質的印刷樣式，以及多層的功能。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="ed2ba-140">Rendering-System 獨立性</span><span class="sxs-lookup"><span data-stu-id="ed2ba-140">Rendering-System Independence</span></span>

<span data-ttu-id="ed2ba-141">[DirectWrite](direct-write-portal.md) 與任何特定圖形技術無關。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="ed2ba-142">應用程式可自由使用最適合其需求的轉譯技術。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="ed2ba-143">如此一來，應用程式就可以透過 Direct3D 或 [Direct2D](../direct2d/direct2d-portal.md)，彈性地繼續透過 GDI 和其他部分來呈現應用程式的某些部分。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="ed2ba-144">事實上，應用程式可以選擇透過專屬的轉譯堆疊來呈現 DirectWrite。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="ed2ba-145">High-Quality 印刷樣式</span><span class="sxs-lookup"><span data-stu-id="ed2ba-145">High-Quality Typography</span></span>

<span data-ttu-id="ed2ba-146">[DirectWrite](direct-write-portal.md) 利用 [OpenType](../intl/opentype-font-format.md) 字型技術的進展，在 Windows 應用程式中啟用高品質的印刷功能。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="ed2ba-147">DirectWrite 字型系統提供的服務可處理字型列舉、字型回復和字型快取，這些都是應用程式用來處理字型的必要項。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="ed2ba-148">[DirectWrite](direct-write-portal.md)所提供的[OpenType](../intl/opentype-font-format.md)支援可讓開發人員加入其應用程式的先進印刷樣式功能和國際文字支援。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="ed2ba-149">支援先進的印刷樣式功能</span><span class="sxs-lookup"><span data-stu-id="ed2ba-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="ed2ba-150">[DirectWrite](direct-write-portal.md) 可讓應用程式開發人員將無法在 WINFORMS 或 GDI 中使用的 OpenType 字型功能解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="ed2ba-151">DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) 物件會公開許多 OpenType 字型的 advanced 功能，例如樣式的替換和花飾。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="ed2ba-152">Microsoft Windows 軟體開發套件 (SDK) 提供一組以豐富功能（例如 Pericles 和 Pescadero 字型）設計的範例 [OpenType](../intl/opentype-font-format.md) 字型。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="ed2ba-153">如需 OpenType 功能的詳細資訊，請參閱 [Opentype 字型功能](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="ed2ba-154">支援國際文字</span><span class="sxs-lookup"><span data-stu-id="ed2ba-154">Support for International Text</span></span>

<span data-ttu-id="ed2ba-155">[DirectWrite](direct-write-portal.md) 使用 [OpenType](../intl/opentype-font-format.md) 字型來啟用廣泛的國際文字支援。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="ed2ba-156">支援 Unicode 功能，例如代理程式、雙向、換行和 UVS。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="ed2ba-157">語言導向的腳本明細、數位替換和圖像成形，可確保任何腳本中的文字都具有正確的版面配置和轉譯。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="ed2ba-158">目前支援下列指令碼︰</span><span class="sxs-lookup"><span data-stu-id="ed2ba-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="ed2ba-159">針對以標記的腳本 \* ，沒有預設系統字型。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="ed2ba-160">應用程式必須安裝支援這些腳本的字型。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="ed2ba-161">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-161">Arabic</span></span>
-   <span data-ttu-id="ed2ba-162">亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-162">Armenian</span></span>
-   <span data-ttu-id="ed2ba-163">Bengala</span><span class="sxs-lookup"><span data-stu-id="ed2ba-163">Bengala</span></span>
-   <span data-ttu-id="ed2ba-164">符號</span><span class="sxs-lookup"><span data-stu-id="ed2ba-164">Bopomofo</span></span>
-   <span data-ttu-id="ed2ba-165">盲文\*</span><span class="sxs-lookup"><span data-stu-id="ed2ba-165">Braille\*</span></span>
-   <span data-ttu-id="ed2ba-166">加拿大土著音節</span><span class="sxs-lookup"><span data-stu-id="ed2ba-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="ed2ba-167">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-167">Cherokee</span></span>
-   <span data-ttu-id="ed2ba-168">中文 (簡化 & 傳統) </span><span class="sxs-lookup"><span data-stu-id="ed2ba-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="ed2ba-169">古斯拉夫文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-169">Cyrillic</span></span>
-   <span data-ttu-id="ed2ba-170">科普特文\*</span><span class="sxs-lookup"><span data-stu-id="ed2ba-170">Coptic\*</span></span>
-   <span data-ttu-id="ed2ba-171">梵文字母</span><span class="sxs-lookup"><span data-stu-id="ed2ba-171">Devanagari</span></span>
-   <span data-ttu-id="ed2ba-172">文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-172">Ethiopic</span></span>
-   <span data-ttu-id="ed2ba-173">喬治亞文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-173">Georgian</span></span>
-   <span data-ttu-id="ed2ba-174">文\*</span><span class="sxs-lookup"><span data-stu-id="ed2ba-174">Glagolitic\*</span></span>
-   <span data-ttu-id="ed2ba-175">希臘文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-175">Greek</span></span>
-   <span data-ttu-id="ed2ba-176">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-176">Gujarati</span></span>
-   <span data-ttu-id="ed2ba-177">古木基文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-177">Gurmukhi</span></span>
-   <span data-ttu-id="ed2ba-178">Hebrew</span><span class="sxs-lookup"><span data-stu-id="ed2ba-178">Hebrew</span></span>
-   <span data-ttu-id="ed2ba-179">日文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-179">Japanese</span></span>
-   <span data-ttu-id="ed2ba-180">坎那達文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-180">Kannada</span></span>
-   <span data-ttu-id="ed2ba-181">高棉文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-181">Khmer</span></span>
-   <span data-ttu-id="ed2ba-182">韓文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-182">Korean</span></span>
-   <span data-ttu-id="ed2ba-183">寮文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-183">Lao</span></span>
-   <span data-ttu-id="ed2ba-184">拉丁文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-184">Latin</span></span>
-   <span data-ttu-id="ed2ba-185">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-185">Malayalam</span></span>
-   <span data-ttu-id="ed2ba-186">蒙古文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-186">Mongolian</span></span>
-   <span data-ttu-id="ed2ba-187">緬甸</span><span class="sxs-lookup"><span data-stu-id="ed2ba-187">Myanmar</span></span>
-   <span data-ttu-id="ed2ba-188">新傣文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-188">New Tai Lue</span></span>
-   <span data-ttu-id="ed2ba-189">豎\*</span><span class="sxs-lookup"><span data-stu-id="ed2ba-189">Ogham\*</span></span>
-   <span data-ttu-id="ed2ba-190">歐迪亞文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-190">Odia</span></span>
-   <span data-ttu-id="ed2ba-191">' 八位 pa</span><span class="sxs-lookup"><span data-stu-id="ed2ba-191">'Phags-pa</span></span>
-   <span data-ttu-id="ed2ba-192">符文\*</span><span class="sxs-lookup"><span data-stu-id="ed2ba-192">Runic\*</span></span>
-   <span data-ttu-id="ed2ba-193">僧伽羅文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-193">Sinhala</span></span>
-   <span data-ttu-id="ed2ba-194">敘利亞文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-194">Syriac</span></span>
-   <span data-ttu-id="ed2ba-195">泰 Le</span><span class="sxs-lookup"><span data-stu-id="ed2ba-195">Tai Le</span></span>
-   <span data-ttu-id="ed2ba-196">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-196">Tamil</span></span>
-   <span data-ttu-id="ed2ba-197">泰盧固文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-197">Telugu</span></span>
-   <span data-ttu-id="ed2ba-198">塔安那文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-198">Thaana</span></span>
-   <span data-ttu-id="ed2ba-199">泰文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-199">Thai</span></span>
-   <span data-ttu-id="ed2ba-200">西藏文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-200">Tibetan</span></span>
-   <span data-ttu-id="ed2ba-201">爨文</span><span class="sxs-lookup"><span data-stu-id="ed2ba-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="ed2ba-202">多層功能</span><span class="sxs-lookup"><span data-stu-id="ed2ba-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="ed2ba-203">[DirectWrite](direct-write-portal.md) 提供一些要素的功能，每一層都能與下一層緊密互動。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="ed2ba-204">API 設計可讓應用程式開發人員根據其需求和排程，自由且彈性地採用個別層。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="ed2ba-205">下圖顯示這些圖層之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-205">The following diagram shows the relationship between these layers.</span></span>

![directwrite 圖層的圖表，以及它們如何與應用程式或 ui 架構和圖形 api 通訊](images/intro-01.png)

<span data-ttu-id="ed2ba-207">文字版面配置 API 提供可從 [DirectWrite](direct-write-portal.md)取得的最高層級功能。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="ed2ba-208">它提供應用程式用來測量、顯示及與豐富格式化文字字串互動的服務。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="ed2ba-209">此文字 API 可用於目前使用 Win32 DrawText 的應用程式，以豐富的格式化文字建立新式 UI。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="ed2ba-210">需要大量文字的應用程式，這些應用程式會執行自己的版面配置引擎，可以使用下一個圖層：腳本處理器。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="ed2ba-211">腳本處理器會將文字區塊細分為腳本區塊，並處理 Unicode 標記法與字型中適當圖像標記法之間的對應，讓腳本的文字可以正確地以正確的語言顯示。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="ed2ba-212">文字版面配置 API 層所使用的版面配置系統是以字型和腳本處理系統為基礎。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="ed2ba-213">圖像呈現圖層是最小的功能層，可為執行自己的文字配置引擎的應用程式提供圖像轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="ed2ba-214">圖像轉譯層也適用于實作為自訂轉譯器的應用程式，透過 [DirectWrite](direct-write-portal.md) 文字格式 API 中的回呼函式修改圖像繪圖行為。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="ed2ba-215">[DirectWrite](direct-write-portal.md)字型系統適用于所有 DirectWrite 功能層，並可讓應用程式存取字型和圖像資訊。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="ed2ba-216">它是設計來處理常見的字型技術和資料格式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="ed2ba-217">DirectWrite 字型模型遵循在相同字型家族中支援任意數量的加權、樣式和伸展的一般印刷方式作法。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="ed2ba-218">這個模型（也就是 WPF 和 CSS 的相同模型）會指定只有權數 (粗體、淺色等字型，以及) 、樣式 (垂直、斜體或傾斜) 或延展 (窄、緊縮、寬等等) 視為單一字型家族的成員。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="ed2ba-219">使用 ClearType 改進文字轉譯</span><span class="sxs-lookup"><span data-stu-id="ed2ba-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="ed2ba-220">在螢幕上提高可讀性是所有 Windows 應用程式的重要需求。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="ed2ba-221">認知心理學研究中的辨識項表示我們必須能夠準確地辨識每個字母，而字母之間的間距甚至是快速處理的關鍵。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="ed2ba-222">未對稱的字母和單字會被視為不美觀，而且會降低閱讀體驗。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="ed2ba-223">Larson，Microsoft Advanced 閱讀技術群組，在以 IEEE 為範圍發行的主體上撰寫了一篇文章。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="ed2ba-224">本文稱為「文字技術」 (https://www.spectrum.ieee.org/print/5049) 。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="ed2ba-225">[DirectWrite](direct-write-portal.md)中的文字是使用 Microsoft ClearType 轉譯的，可增強文字的清晰和可讀性。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="ed2ba-226">ClearType 利用新式 LCD 顯示器對每個可個別控制的圖元具有 RGB 條紋。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="ed2ba-227">DirectWrite 使用最新的 ClearType 增強功能，第一次隨附于包含 Windows Presentation Foundation 的 Windows Vista，可讓它不只評估個別的字母，也可以評估字母之間的間距。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="ed2ba-228">在這些 ClearType 增強功能之前，「讀取」大小為10或12點的文字難以顯示：我們可以在字母之間放置1圖元，這通常太小，或2個圖元，這通常太過多。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="ed2ba-229">使用 subpixels 中的額外解析度可提供我們小數間距，以改善整個頁面的平均和對稱性。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="ed2ba-230">下列兩個圖顯示使用子圖元定位時，如何在任何子圖元界限上開始使用符號。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="ed2ba-231">下圖是使用「ClearType」版本的「ClearType 轉譯器」（不採用子圖元定位）來呈現。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![在不含子圖元定位的情況下呈現的「技術」圖例](images/intro-03.png)

<span data-ttu-id="ed2ba-233">下圖是使用 [DirectWrite](direct-write-portal.md) 版本的 ClearType 轉譯器轉譯，其使用子圖元定位。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![以子圖元定位呈現的「技術」圖例](images/intro-04.png)

<span data-ttu-id="ed2ba-235">請注意，字母 h 和 n 之間的間距甚至是第二個影像中的間距，而字母 o 會從字母 n 更進一步地分隔，甚至是使用字母 l。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="ed2ba-236">另請注意，字母 l 的詞幹在自然的尋找方式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="ed2ba-237">子圖元 ClearType 定位可在螢幕上提供最精確的字元間距，尤其是子圖元與整個圖元之間的差異表示大量字元寬度的小型大小。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="ed2ba-238">它可讓文字以理想的解析度空間來測量，並以其自然位置呈現于 LCD 色條紋，以及子圖元細微度。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="ed2ba-239">使用這項技術測量和轉譯的文字是依定義、解析度無關，這表示完全相同的文字版面配置可跨各種顯示器解析度來達成。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="ed2ba-240">不同于任何一種 GDI ClearType 轉譯，子圖元 ClearType 提供最精確的字元寬度。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="ed2ba-241">文字字串 API 預設採用子圖元文字轉譯，這表示它會根據目前的顯示解析度來測量文字的理想解析度，並根據真正縮放的圖像前移寬度和定位位移來產生圖像定位結果。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="ed2ba-242">針對大型文字， [DirectWrite](direct-write-portal.md) 也會啟用 y 軸的消除鋸齒，讓邊緣更平滑，並以字型設計工具的形式呈現字母。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="ed2ba-243">下圖顯示 y 方向消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-243">The following illustration shows y-direction anti-aliasing.</span></span>

![使用 y 方向消除鋸齒將 "cleartype" 轉譯為 gdi 文字和 directwrite 文字的圖例](images/intro-05.png)

<span data-ttu-id="ed2ba-245">雖然 [DirectWrite](direct-write-portal.md) 文字預設是使用子圖元 ClearType 來定位和轉譯，但仍有其他轉譯選項可用。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="ed2ba-246">許多現有的應用程式都使用 GDI 來轉譯大部分的 UI，有些應用程式則使用系統編輯控制項，以繼續使用 GDI 進行文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="ed2ba-247">將 DirectWrite 文字新增至這些應用程式時，可能需要犧牲子圖元 ClearType 提供的讀取體驗改進，讓文字在應用程式中具有一致的外觀。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="ed2ba-248">為了符合這些需求， [DirectWrite](direct-write-portal.md) 也支援下列轉譯選項：</span><span class="sxs-lookup"><span data-stu-id="ed2ba-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="ed2ba-249">子圖元 ClearType (預設) 。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="ed2ba-250">在水準和垂直維度中具有消除鋸齒的子圖元 ClearType。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="ed2ba-251">別名文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-251">Aliased text.</span></span>
-   <span data-ttu-id="ed2ba-252">Microsoft Word 閱讀檢視使用的 GDI 自然寬度 (，例如) 。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="ed2ba-253">GDI 相容寬度 (包含東亞內嵌點陣圖) 。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="ed2ba-254">您可以透過 DirectWrite API 和新的 Windows 7 收件匣 ClearType 調諧器來微調這些轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="ed2ba-255">從 Windows 8 開始，在大部分情況下，您應該使用灰階文字消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="ed2ba-256">如需詳細資訊，請參閱下一節。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="ed2ba-257">支援自然版面配置</span><span class="sxs-lookup"><span data-stu-id="ed2ba-257">Support for Natural Layout</span></span>

<span data-ttu-id="ed2ba-258">自然配置與解析度無關，因此當您放大或縮小時，字元間距不會變更，或視顯示器的 DPI 而定。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="ed2ba-259">第二個優點是，在字型的設計上，間距是 true。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="ed2ba-260">自然配置是由 DirectWrite 對自然轉譯的支援所提供，這表示個別的字元可以定位至圖元的一部分。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="ed2ba-261">雖然自然配置是預設值，但有些應用程式需要轉譯與 GDI 具有相同間距和外觀的文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="ed2ba-262">針對這類應用程式，DirectWrite 提供 GDI 傳統和 GDI 自然測量模式和對應的轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="ed2ba-263">上述任何轉譯模式都可以結合兩種消除鋸齒模式的其中一種： ClearType 或灰階。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="ed2ba-264">ClearType 消除鋸齒會藉由個別操作每個圖元的紅色、綠色和藍色色彩值，模擬較高的解析度。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="ed2ba-265">灰階消除鋸齒只會計算每個圖元的一個涵蓋範圍 (或 Alpha) 值。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="ed2ba-266">ClearType 是預設值，但建議針對 Windows Store 應用程式使用灰階消除鋸齒，因為它比較快且與標準消除鋸齒相容，同時仍具有高度可讀性。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="ed2ba-267">API 概觀</span><span class="sxs-lookup"><span data-stu-id="ed2ba-267">API Overview</span></span>

<span data-ttu-id="ed2ba-268">[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)介面是使用 DirectWrite 功能的起點。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="ed2ba-269">Factory 是根物件，它會建立一組可一起使用的物件。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="ed2ba-270">格式設定和版面配置作業是作業的必要條件，因為文字必須正確格式化並配置給一組指定的條件約束，才能進行繪製或點擊測試。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="ed2ba-271">您可以使用 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 來建立的兩個主要物件為此用途，例如 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="ed2ba-272">**IDWriteTextFormat** 物件代表文欄位落的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="ed2ba-273">[**IDWriteFactory：： CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)函式會採用輸入字串、相關聯的條件約束（例如要填入的空間維度）和 **IDWriteTextFormat** 物件，並將經過完整分析和格式化的結果放入 **IDWriteTextLayout** 中，以用於後續作業。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="ed2ba-274">然後，應用程式可以使用 [Direct2D](../direct2d/direct2d-portal.md)所提供的 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)函式，或執行可使用 GDI、Direct2D 或其他圖形系統轉譯圖像的回呼函式，以轉譯文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="ed2ba-275">針對單一格式文字，Direct2D 上的 [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 函式提供較簡單的方式來繪製文字，而不需要先建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="ed2ba-276">使用 DirectWrite 格式化和繪製 "Hello World"</span><span class="sxs-lookup"><span data-stu-id="ed2ba-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="ed2ba-277">下列程式碼範例會示範應用程式如何使用 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 來格式化單一段落，並使用 [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 函式加以繪製。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="ed2ba-278">存取字型系統</span><span class="sxs-lookup"><span data-stu-id="ed2ba-278">Accessing the Font System</span></span>

<span data-ttu-id="ed2ba-279">除了使用上述範例中的 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面來指定文字字串的字型系列名稱之外， [DirectWrite](direct-write-portal.md) 還可讓應用程式透過字型列舉來更充分掌控字型選取，以及根據內嵌檔字型建立自訂字型集合的能力。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="ed2ba-280">[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)物件是字型系列的集合。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="ed2ba-281">DirectWrite 可讓您透過稱為系統字型集合的特殊字型集合，存取系統上安裝的字型集。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="ed2ba-282">這是藉由呼叫 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)物件的 [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection)方法來取得。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="ed2ba-283">應用程式也可以從應用程式定義的回呼所列舉的一組字型建立自訂字型集合，也就是應用程式所安裝的私用字型，或內嵌在檔中的字型。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="ed2ba-284">然後，應用程式可以呼叫 [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) 來取得集合內的特定 FontFamily 物件，然後呼叫 [**IDWriteFontFamily：： GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) 來取得特定的 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 物件。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="ed2ba-285">**IDWriteFont** 物件代表字型集合中的字型，並公開屬性和一些基本字型度量。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="ed2ba-286">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)是另一個代表字型的物件，會在字型上公開一組完整的度量。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="ed2ba-287">您可以直接從字型名稱建立 **IDWriteFontFace** ;應用程式不需要取得字型集合即可存取它。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="ed2ba-288">它適用于需要查詢特定字型詳細資料的文字版面配置應用程式（例如 Microsoft Word）。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="ed2ba-289">下圖說明這些物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-289">The following diagram illustrates the relationship between these objects.</span></span>

![字型集合、字型系列與字型字型之間關聯性的圖表](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="ed2ba-291">IDWriteFontFace</span><span class="sxs-lookup"><span data-stu-id="ed2ba-291">IDWriteFontFace</span></span>

<span data-ttu-id="ed2ba-292">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件代表字型，並提供比 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)物件更詳細的字型資訊。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="ed2ba-293">**IDWriteFontFace** 中的字型和字元度量適用于執行文字配置的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="ed2ba-294">大部分的主流應用程式不會直接使用這些 Api，而是會直接使用 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 或指定字型系列名稱。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="ed2ba-295">下表摘要說明這兩個物件的使用案例。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="ed2ba-296">類別</span><span class="sxs-lookup"><span data-stu-id="ed2ba-296">Category</span></span>                                                                                                         | [<span data-ttu-id="ed2ba-297">**IDWriteFont**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="ed2ba-298">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="ed2ba-299">支援使用者互動的 Api，例如字型選擇器使用者介面：描述和其他資訊 Api</span><span class="sxs-lookup"><span data-stu-id="ed2ba-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="ed2ba-300">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-300">Yes</span></span>                                        | <span data-ttu-id="ed2ba-301">否</span><span class="sxs-lookup"><span data-stu-id="ed2ba-301">No</span></span>                                                 |
| <span data-ttu-id="ed2ba-302">支援字型對應的 Api：系列、樣式、粗細、延展、字元涵蓋範圍</span><span class="sxs-lookup"><span data-stu-id="ed2ba-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="ed2ba-303">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-303">Yes</span></span>                                        | <span data-ttu-id="ed2ba-304">否</span><span class="sxs-lookup"><span data-stu-id="ed2ba-304">No</span></span>                                                 |
| <span data-ttu-id="ed2ba-305">DrawText API</span><span class="sxs-lookup"><span data-stu-id="ed2ba-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="ed2ba-306">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-306">Yes</span></span>                                        | <span data-ttu-id="ed2ba-307">否</span><span class="sxs-lookup"><span data-stu-id="ed2ba-307">No</span></span>                                                 |
| <span data-ttu-id="ed2ba-308">用於呈現的 Api</span><span class="sxs-lookup"><span data-stu-id="ed2ba-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="ed2ba-309">否</span><span class="sxs-lookup"><span data-stu-id="ed2ba-309">No</span></span>                                         | <span data-ttu-id="ed2ba-310">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-310">Yes</span></span>                                                |
| <span data-ttu-id="ed2ba-311">用於文字版面配置的 Api：圖像度量等</span><span class="sxs-lookup"><span data-stu-id="ed2ba-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="ed2ba-312">否</span><span class="sxs-lookup"><span data-stu-id="ed2ba-312">No</span></span>                                         | <span data-ttu-id="ed2ba-313">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-313">Yes</span></span>                                                |
| <span data-ttu-id="ed2ba-314">UI 控制項和文字版面配置的 Api：全字型計量</span><span class="sxs-lookup"><span data-stu-id="ed2ba-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="ed2ba-315">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-315">Yes</span></span>                                        | <span data-ttu-id="ed2ba-316">是</span><span class="sxs-lookup"><span data-stu-id="ed2ba-316">Yes</span></span>                                                |



 

<span data-ttu-id="ed2ba-317">下列範例應用程式會列舉系統字型集合中的字型。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="ed2ba-318">文字轉譯</span><span class="sxs-lookup"><span data-stu-id="ed2ba-318">Text rendering</span></span>

<span data-ttu-id="ed2ba-319">文字轉譯 Api 可讓 [DirectWrite](direct-write-portal.md) 字型中的字元轉譯成 [DIRECT2D](../direct2d/direct2d-portal.md) 表面或 GDI 裝置獨立點陣圖，或是轉換成大綱或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="ed2ba-320">相較于 Windows 先前的執行版本，DirectWrite 中的 ClearType 轉譯支援以改良的清晰度和對比來進行子圖元定位。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="ed2ba-321">DirectWrite 也支援將黑白文字加上別名，以支援與內嵌點陣圖相關的東亞字型，或使用者已停用任何類型之字型平滑處理的案例。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="ed2ba-322">所有的選項都可透過 [DirectWrite](direct-write-portal.md) api 存取的所有可用 ClearType 旋鈕進行調整，也可以透過新的 Windows 7 ClearType 調諧器控制台小程式來公開。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="ed2ba-323">有兩個 Api 可用於轉譯圖像，一個可透過 [Direct2D](../direct2d/direct2d-portal.md) 提供硬體加速轉譯，另一個則提供軟體轉譯至 GDI 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="ed2ba-324">使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 和執行 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 回呼的應用程式可以呼叫這些函式，以回應 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 回呼。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="ed2ba-325">此外，執行自己配置或處理圖像層級資料的應用程式可以使用這些 Api。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="ed2ba-326">**ID2DRenderTarget：:D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="ed2ba-327">應用程式可以使用 [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) 來提供硬體加速，以使用 GPU 進行文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="ed2ba-328">硬體加速會影響文字轉譯管線的所有階段，包括將字元合併為圖像執行，以及篩選圖像執行點陣圖，以將 ClearType 混合演算法套用至最終顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="ed2ba-329">這是取得最佳轉譯效能的建議 API。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="ed2ba-330">**IDWriteBitmapRenderTarget：:D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="ed2ba-331">應用程式可以使用 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 方法，執行將字元執行到 32-bpp 點陣圖的軟體呈現。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="ed2ba-332">[**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)物件會封裝可用於呈現圖像的點陣圖和記憶體裝置內容。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="ed2ba-333">如果您想要繼續使用 GDI，這個 API 會很有用，因為您有以 GDI 轉譯的現有程式碼基底。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="ed2ba-334">如果您的應用程式具有使用 GDI 的現有文字版面配置程式碼，而且您想要保留其現有的版面配置程式碼，但只在轉譯圖像的最後一個步驟使用 [DirectWrite](direct-write-portal.md) ， [**IDWriteGdiInterop：： CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) 會在這兩個 api 之間提供橋樑。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="ed2ba-335">在呼叫此函式之前，應用程式會使用 **IDWriteGdiInterop：： CreateFontFaceFromHdc** 函數，從裝置內容取得字型臉部參考。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="ed2ba-336">在大部分的情況下，應用程式可能不需要使用這些圖像呈現 Api。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="ed2ba-337">在應用程式建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件之後，就可以使用 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="ed2ba-338">自訂呈現模式</span><span class="sxs-lookup"><span data-stu-id="ed2ba-338">Custom Rendering Modes</span></span>

<span data-ttu-id="ed2ba-339">許多參數會影響文字轉譯，例如 gamma、ClearType 層級、圖元幾何和增強對比。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="ed2ba-340">轉譯參數是由物件封裝，該物件會實作為公用 [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) 介面。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="ed2ba-341">系統會根據 Windows 7 中的 ClearType 控制台小程式所指定的硬體內容和/或使用者喜好設定，自動初始化轉譯參數物件。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="ed2ba-342">一般而言，如果用戶端使用 [DirectWrite](direct-write-portal.md) 版面配置 API，DirectWrite 將會自動選取對應至指定之測量模式的轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="ed2ba-343">需要更多控制權的應用程式可以使用 [**IDWriteFactory：： CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) 來執行不同的轉譯選項。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="ed2ba-344">這個函數也可以用來設定 gamma、圖元幾何和增強對比。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="ed2ba-345">可用的各種呈現選項如下：</span><span class="sxs-lookup"><span data-stu-id="ed2ba-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="ed2ba-346">子圖元消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="ed2ba-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="ed2ba-347">應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯模式，使 \_ \_ \_ 其只以水準維度中的消除鋸齒來指定轉譯。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="ed2ba-348">水準和垂直維度中的子圖元消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="ed2ba-349">應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯 \_ \_ 模式 \_ 自然 \_ 對稱式，以指定以水準和垂直維度的消除鋸齒呈現。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="ed2ba-350">如此一來，曲線和對角線線看起來會比某些柔和的成本更平滑，而且通常會用在 16 ppem 以上的大小。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="ed2ba-351">別名文字</span><span class="sxs-lookup"><span data-stu-id="ed2ba-351">Aliased Text</span></span>

    <span data-ttu-id="ed2ba-352">應用程式會將 *renderingMode* 參數設定為 DWRITE \_ 呈現 \_ 模式 \_ ，以指定別名文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="ed2ba-353">灰階文字</span><span class="sxs-lookup"><span data-stu-id="ed2ba-353">Grayscale Text</span></span>

    <span data-ttu-id="ed2ba-354">應用程式會將 *pixelGeometry* 參數設定為 \_ 平面 DWRITE 圖元 \_ 幾何 \_ ，以指定灰階文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="ed2ba-355">GDI 相容寬度 (包含東亞內嵌點陣圖) </span><span class="sxs-lookup"><span data-stu-id="ed2ba-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="ed2ba-356">應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯 \_ \_ 模式 \_ GDI \_ 傳統，以指定 gdi 相容寬度的消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="ed2ba-357">GDI 自然寬度</span><span class="sxs-lookup"><span data-stu-id="ed2ba-357">GDI natural-width</span></span>

    <span data-ttu-id="ed2ba-358">應用程式會將 *renderingMode* 參數設定為 DWRITE 轉譯 \_ \_ 模式 \_ GDI \_ 自然，以指定 gdi 自然寬度相容的消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="ed2ba-359">大綱文字</span><span class="sxs-lookup"><span data-stu-id="ed2ba-359">Outline text</span></span>

    <span data-ttu-id="ed2ba-360">若要以大尺寸轉譯，應用程式開發人員可能會想要使用字型外框來轉譯，而不是藉由將它柵格化到點陣圖中。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="ed2ba-361">應用程式會將 *renderingMode* 參數設定為 **DWRITE 轉譯 \_ \_ 模式 \_ 大綱** ，以指定轉譯應略過轉譯器並直接使用大綱。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="ed2ba-362">GDI 互通性</span><span class="sxs-lookup"><span data-stu-id="ed2ba-362">GDI Interoperability</span></span>

<span data-ttu-id="ed2ba-363">[**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop)介面提供與 GDI 的互通性。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="ed2ba-364">這可讓應用程式繼續其在 GDI 程式碼基底中的現有投資，並選擇性地使用 [DirectWrite](direct-write-portal.md) 來呈現或配置。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="ed2ba-365">下列 Api 可讓應用程式在 GDI 字型系統中進行遷移：</span><span class="sxs-lookup"><span data-stu-id="ed2ba-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="ed2ba-366">**CreateFontFromLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="ed2ba-367">建立符合 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構所指定之屬性的 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)物件。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="ed2ba-368">**ConvertFontToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="ed2ba-369">根據指定之 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)的 GDI 相容屬性，初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="ed2ba-370">**ConvertFontFaceToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="ed2ba-371">根據指定之 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)的 GDI 相容屬性，初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="ed2ba-372">**CreateFontFaceFromHdc**</span><span class="sxs-lookup"><span data-stu-id="ed2ba-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="ed2ba-373">建立 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) 物件，該物件會對應至目前選取的 **HFONT**。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="ed2ba-374">結論</span><span class="sxs-lookup"><span data-stu-id="ed2ba-374">Conclusion</span></span>

<span data-ttu-id="ed2ba-375">改善閱讀體驗對於使用者是否在螢幕上或在紙張上很有價值。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="ed2ba-376">[DirectWrite](direct-write-portal.md) 可為應用程式開發人員提供簡單易用和分層式程式設計模型，以改善其 Windows 應用程式的文字體驗。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="ed2ba-377">應用程式可以使用 DirectWrite，以版面配置 API 呈現其 UI 和檔的豐富格式化文字。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="ed2ba-378">在更複雜的案例中，應用程式可以直接使用圖像、存取字型等等，並利用 DirectWrite 的強大功能來提供高品質的印刷樣式。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="ed2ba-379">[DirectWrite](direct-write-portal.md)的互通性功能可讓應用程式開發人員執行其現有的 Win32 程式碼基底，並選擇性地在其應用程式中採用 DirectWrite。</span><span class="sxs-lookup"><span data-stu-id="ed2ba-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 