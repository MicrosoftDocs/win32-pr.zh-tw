---
title: 消費者介面文字
description: 使用者介面文字會出現在 UI 表面上。
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1c1a60ba0bfef33dcf1e72c5ba19b11c4a5f38a2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104561952"
---
# <a name="user-interface-text"></a><span data-ttu-id="fb065-103">消費者介面文字</span><span class="sxs-lookup"><span data-stu-id="fb065-103">User Interface Text</span></span>

> [!NOTE]
> <span data-ttu-id="fb065-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="fb065-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="fb065-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="fb065-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="fb065-106">使用者介面文字會出現在 UI 表面上。</span><span class="sxs-lookup"><span data-stu-id="fb065-106">User interface text appears on UI surfaces.</span></span> <span data-ttu-id="fb065-107">此文字包含控制項標籤和靜態文字：</span><span class="sxs-lookup"><span data-stu-id="fb065-107">This text includes control labels and static text:</span></span>

-   <span data-ttu-id="fb065-108">控制項標籤可識別控制項，並且直接放在控制項的旁邊或旁邊。</span><span class="sxs-lookup"><span data-stu-id="fb065-108">Control labels identify controls and are placed directly on or next to the controls.</span></span>
-   <span data-ttu-id="fb065-109">靜態文字（因為它不是互動式控制項的一部分）會為使用者提供詳細的指示或說明，讓他們能夠做出明智的決策。</span><span class="sxs-lookup"><span data-stu-id="fb065-109">Static text, which is so called because it is not part of an interactive control, provides users with detailed instructions or explanations so they can make informed decisions.</span></span>

<span data-ttu-id="fb065-110">**注意：**[樣式和語氣、字型](text-style-tone.md)[和](vis-fonts.md)[通用控制項](controls.md)標籤的相關指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="fb065-110">**Note:** Guidelines related to [style and tone](text-style-tone.md), [fonts](vis-fonts.md), and [comon control](controls.md) labels are presented in separate articles.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="fb065-111">使用模式</span><span class="sxs-lookup"><span data-stu-id="fb065-111">Usage patterns</span></span>

<span data-ttu-id="fb065-112">UI 文字有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="fb065-112">UI text has several usage patterns:</span></span>



|                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb065-113">**標題列文字**</span><span class="sxs-lookup"><span data-stu-id="fb065-113">**Title bar text**</span></span><br/> <span data-ttu-id="fb065-114">使用標題列文字來識別視窗或對話方塊的來源。</span><span class="sxs-lookup"><span data-stu-id="fb065-114">use title bar text to identify a window or the source of a dialog box.</span></span> <br/>                                                                            | ![資料夾選項標題列的螢幕擷取畫面](images/text-ui-image1.png)<br/> <span data-ttu-id="fb065-116">在此範例中，標題列文字會識別視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-116">In this example, the title bar text identifies a window.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fb065-117">**主要指示**</span><span class="sxs-lookup"><span data-stu-id="fb065-117">**Main instructions**</span></span><br/> <span data-ttu-id="fb065-118">您可以使用重要的主要指示，清楚地說明在視窗或頁面中要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="fb065-118">use the prominent main instruction to explain concisely what to do in the window or page.</span></span> <br/>                                                      | <span data-ttu-id="fb065-119">指令應該是特定的語句、命令式方向或問題。</span><span class="sxs-lookup"><span data-stu-id="fb065-119">The instruction should be a specific statement, imperative direction, or question.</span></span> <span data-ttu-id="fb065-120">良好的主要指示傳達使用者的目標，而不是只著重在操作 ui。</span><span class="sxs-lookup"><span data-stu-id="fb065-120">good main instructions communicate the user's objective rather than focusing just on manipulating the ui.</span></span> <br/> ![<span data-ttu-id="fb065-121">問題的螢幕擷取畫面：您是否想要最新的協助？</span><span class="sxs-lookup"><span data-stu-id="fb065-121">screen shot of question: do you want latest help?</span></span> ](images/text-ui-image2.png)<br/> <span data-ttu-id="fb065-122">在此範例中，主要的指令文字會以使用者自己的權益或興趣，直接對使用者提出問題。</span><span class="sxs-lookup"><span data-stu-id="fb065-122">In this example, the main instruction text directly engages the user with a question in terms of the user's own benefit or interest.</span></span><br/>             |
| <span data-ttu-id="fb065-123">**補充指示**</span><span class="sxs-lookup"><span data-stu-id="fb065-123">**Supplemental instructions**</span></span><br/> <span data-ttu-id="fb065-124">必要時，請使用補充指示來呈現有助於瞭解或使用視窗或頁面的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-124">when necessary, use a supplemental instruction to present additional information helpful to understanding or using the window or page.</span></span> <br/> | <span data-ttu-id="fb065-125">您可以提供更詳細的資訊、提供內容，以及定義術語。</span><span class="sxs-lookup"><span data-stu-id="fb065-125">You can provide more detailed information, provide context, and define terminology.</span></span> <span data-ttu-id="fb065-126">在主要指令上詳細說明的補充指示，而不只是重新用語。</span><span class="sxs-lookup"><span data-stu-id="fb065-126">supplemental instructions elaborate on the main instruction without simply re-wording it.</span></span> <br/> ![<span data-ttu-id="fb065-127">切換至系統管理員帳戶的文字螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-127">screen shot of text on switching to admin account</span></span> ](images/text-ui-image3.png)<br/> <span data-ttu-id="fb065-128">在此範例中，補充指示會提供兩個可能的動作課程，以回應主要指示中所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-128">In this example, the supplemental instructions provide two possible courses of action to take in response to the information presented in the main instruction.</span></span><br/> |
| <span data-ttu-id="fb065-129">**控制項標籤**</span><span class="sxs-lookup"><span data-stu-id="fb065-129">**Control labels**</span></span><br/> <span data-ttu-id="fb065-130">直接在控制項上或旁邊的標籤。</span><span class="sxs-lookup"><span data-stu-id="fb065-130">labels directly on or next to controls.</span></span> <br/>                                                                                                           | ![<span data-ttu-id="fb065-131">桌面時鐘選項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-131">screen shot of desktop clock options</span></span> ](images/text-ui-image4.png)<br/> <span data-ttu-id="fb065-132">在此範例中，控制項標籤會識別使用者可以選取或修改的桌面時鐘設定。</span><span class="sxs-lookup"><span data-stu-id="fb065-132">In this example, control labels identify desktop clock settings that users can select or modify.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fb065-133">**補充說明**</span><span class="sxs-lookup"><span data-stu-id="fb065-133">**Supplemental explanations**</span></span><br/> <span data-ttu-id="fb065-134">控制項標籤的詳述通常 (命令連結、選項按鈕和核取方塊) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-134">an elaboration of the control labels (typically for command links, radio buttons, and check boxes).</span></span> <br/>                                    | ![顯示 [安全性設定] 對話方塊的螢幕擷取畫面。](images/text-ui-image5.png)<br/> <span data-ttu-id="fb065-136">在此範例中，補充說明說明這些選項。</span><span class="sxs-lookup"><span data-stu-id="fb065-136">In this example, the supplemental explanations clarify the choices.</span></span><br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a><span data-ttu-id="fb065-137">設計概念</span><span class="sxs-lookup"><span data-stu-id="fb065-137">Design concepts</span></span>

<span data-ttu-id="fb065-138">軟體發展人員通常會將文字視為產品檔和技術支援。</span><span class="sxs-lookup"><span data-stu-id="fb065-138">Software developers often think of text as relegated to product documentation and technical support.</span></span> <span data-ttu-id="fb065-139">「首先我們要撰寫程式碼，然後雇用某人協助我們解釋我們所開發的內容。」</span><span class="sxs-lookup"><span data-stu-id="fb065-139">"First we'll write the code, and then we'll hire someone to help us explain what we have developed."</span></span> <span data-ttu-id="fb065-140">但事實上，在程式中，我們會在程式中稍早撰寫重要的文字，因為 UI 是在設計和撰寫程式碼時。</span><span class="sxs-lookup"><span data-stu-id="fb065-140">Yet in reality, important text is written earlier in the process, as the UI is conceived and coded.</span></span> <span data-ttu-id="fb065-141">在所有的情況下，這種文字會比其他類型的技術撰寫更頻繁、更多人看到。</span><span class="sxs-lookup"><span data-stu-id="fb065-141">This text is, after all, seen more frequently and by more people than perhaps any other type of technical writing.</span></span>

<span data-ttu-id="fb065-142">**理解文字對有效的 UI 而言很重要。**</span><span class="sxs-lookup"><span data-stu-id="fb065-142">**Comprehensible text is crucial to effective UI.**</span></span> <span data-ttu-id="fb065-143">專業作者和編輯者應該與軟體發展人員一起使用 UI 文字，做為設計流程不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb065-143">Professional writers and editors should work with software developers on UI text as an integral part of the design process.</span></span> <span data-ttu-id="fb065-144">讓它們提早處理文字，因為文字問題通常會顯示設計問題。</span><span class="sxs-lookup"><span data-stu-id="fb065-144">Have them work on text early because text problems often reveal design problems.</span></span> <span data-ttu-id="fb065-145">如果您的小組在說明設計方面遇到問題，通常這是設計，而不是說明，需要改善。</span><span class="sxs-lookup"><span data-stu-id="fb065-145">If your team has trouble explaining a design, quite often it is the design, not the explanation, that needs improving.</span></span>

### <a name="a-design-model-for-ui-text"></a><span data-ttu-id="fb065-146">UI 文字的設計模型</span><span class="sxs-lookup"><span data-stu-id="fb065-146">A design model for UI text</span></span>

<span data-ttu-id="fb065-147">當您考慮 UI 文字及其在 UI 表面上的位置時，請考慮下列事實：</span><span class="sxs-lookup"><span data-stu-id="fb065-147">As you think about UI text and its placement on your UI surfaces, consider these facts:</span></span>

-   <span data-ttu-id="fb065-148">在焦點的情況下，大聲閱讀的讀者會以左至右、由上到下的順序， (西方文化特性) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-148">During focused, immersive reading, people read in a left-to-right, top-to-bottom order (in Western cultures).</span></span>
-   <span data-ttu-id="fb065-149">使用軟體時，使用者不會在 UI 本身的工作中可以沉浸。</span><span class="sxs-lookup"><span data-stu-id="fb065-149">When using software, users aren't immersed in the UI itself but in their work.</span></span> <span data-ttu-id="fb065-150">因此，使用者不會讀取其掃描的 UI 文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-150">Consequently, users don't read UI text they scan it.</span></span>
-   <span data-ttu-id="fb065-151">當您掃描視窗時，使用者可能會看到文字正在進行篩選，而實際上是正在進行篩選。</span><span class="sxs-lookup"><span data-stu-id="fb065-151">When scanning a window, users may appear to be reading text when in reality they are filtering it.</span></span> <span data-ttu-id="fb065-152">除非他們觀察到的需求，否則通常不會真正理解 UI 文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-152">They often don't truly comprehend the UI text unless they perceive the need to.</span></span>
-   <span data-ttu-id="fb065-153">在視窗中，不同的 UI 元素會收到不同的注意層級。</span><span class="sxs-lookup"><span data-stu-id="fb065-153">Within a window, different UI elements receive different levels of attention.</span></span> <span data-ttu-id="fb065-154">使用者通常會先讀取控制項標籤，特別是與完成工作相關的程式。</span><span class="sxs-lookup"><span data-stu-id="fb065-154">Users tend to read control labels first, especially those that appear relevant to completing the task at hand.</span></span> <span data-ttu-id="fb065-155">相較之下，使用者通常會在他們認為需要時才讀取靜態文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-155">By contrast, users tend to read static text only when they think they need to.</span></span>

<span data-ttu-id="fb065-156">若為一般設計模型，請不要假設使用者謹慎地以左至右、由上到下的順序讀取文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-156">For a general design model, don't assume that users carefully read the text in a left-to-right, top-to-bottom order.</span></span> <span data-ttu-id="fb065-157">相反地，假設使用者從快速掃描整個視窗開始，然後以大約下列順序讀取 UI 文字：</span><span class="sxs-lookup"><span data-stu-id="fb065-157">Rather, assume that users start by quickly scanning the whole window, then read UI text in roughly the following order:</span></span>

-   <span data-ttu-id="fb065-158">中心內的互動式控制項</span><span class="sxs-lookup"><span data-stu-id="fb065-158">Interactive controls in the center</span></span>
-   <span data-ttu-id="fb065-159">[認可按鈕](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="fb065-159">The [commit buttons](glossary.md)</span></span>
-   <span data-ttu-id="fb065-160">在其他地方找到互動式控制項</span><span class="sxs-lookup"><span data-stu-id="fb065-160">Interactive controls found elsewhere</span></span>
-   <span data-ttu-id="fb065-161">主要指示</span><span class="sxs-lookup"><span data-stu-id="fb065-161">Main instruction</span></span>
-   <span data-ttu-id="fb065-162">補充說明</span><span class="sxs-lookup"><span data-stu-id="fb065-162">Supplemental explanations</span></span>
-   <span data-ttu-id="fb065-163">視窗標題</span><span class="sxs-lookup"><span data-stu-id="fb065-163">Window title</span></span>
-   <span data-ttu-id="fb065-164">主要主體中的其他靜態文字</span><span class="sxs-lookup"><span data-stu-id="fb065-164">Other static text in main body</span></span>
-   <span data-ttu-id="fb065-165">註腳</span><span class="sxs-lookup"><span data-stu-id="fb065-165">Footnotes</span></span>

<span data-ttu-id="fb065-166">您也應該假設一旦使用者決定要做什麼之後，他們就會立即停止讀取並進行。</span><span class="sxs-lookup"><span data-stu-id="fb065-166">You should also assume that once users have decided what to do, they will immediately stop reading and do it.</span></span>

### <a name="eliminate-redundancy"></a><span data-ttu-id="fb065-167">消除冗余</span><span class="sxs-lookup"><span data-stu-id="fb065-167">Eliminate redundancy</span></span>

<span data-ttu-id="fb065-168">多餘的文字不僅需要寶貴的螢幕空間，還可削弱您嘗試傳達的重要想法或動作的有效性。</span><span class="sxs-lookup"><span data-stu-id="fb065-168">Redundant text not only takes valuable screen space, but weakens the effectiveness of the important ideas or actions that you are trying to convey.</span></span> <span data-ttu-id="fb065-169">它也會浪費讀者的時間，而在掃描的情況下則會有更多的內容。</span><span class="sxs-lookup"><span data-stu-id="fb065-169">It is also a waste of the reader's time, and all the more so in a context where scanning is the norm.</span></span> <span data-ttu-id="fb065-170">**Windows 致力於說明使用者需要做什麼才能順利完成。**</span><span class="sxs-lookup"><span data-stu-id="fb065-170">**Windows strives to explain what users need to do once well and concisely.**</span></span>

<span data-ttu-id="fb065-171">請檢查每個視窗，並消除重複的單字和語句（不論是在控制項內或跨控制項）。</span><span class="sxs-lookup"><span data-stu-id="fb065-171">Review each window and eliminate duplicate words and statements, both within and across controls.</span></span> <span data-ttu-id="fb065-172">請勿在必要的地方明確地明確地顯示文字，但不是多餘的，也不會說明明顯的。</span><span class="sxs-lookup"><span data-stu-id="fb065-172">Don't avoid important text be explicit wherever necessary but don't be redundant and don't explain the obvious.</span></span>

### <a name="avoid-over-communication"></a><span data-ttu-id="fb065-173">避免過度通訊</span><span class="sxs-lookup"><span data-stu-id="fb065-173">Avoid over-communication</span></span>

<span data-ttu-id="fb065-174">即使文字不是多餘的，也可能太冗長，以說明每個詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb065-174">Even if text isn't redundant, it can simply be too wordy in an effort to explain every detail.</span></span> <span data-ttu-id="fb065-175">**太多文字不太方便閱讀，很可能會略過它諷刺是，而不是比其他更少的通訊。**</span><span class="sxs-lookup"><span data-stu-id="fb065-175">**Too much text discourages reading the eye tends to skip right over it ironically resulting in less communication rather than more.**</span></span> <span data-ttu-id="fb065-176">在 UI 文字中，明確地傳達基本資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-176">In UI text, concisely communicate the essential information.</span></span> <span data-ttu-id="fb065-177">如果某些使用者或某些案例需要詳細資訊，請提供更詳細說明 [內容](winenv-help.md)的連結，或可能的詞彙專案以進行詞彙的澄清。</span><span class="sxs-lookup"><span data-stu-id="fb065-177">If more information is necessary for some users or some scenarios, provide a link to more detailed [Help content](winenv-help.md), or perhaps to a glossary entry for clarification of a term.</span></span>

<span data-ttu-id="fb065-178">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-178">**Incorrect:**</span></span>

![具有6個段落之對話方塊的螢幕擷取畫面](images/text-ui-image6.png)

<span data-ttu-id="fb065-180">在此範例中，有太多文字可以輕易地進行掃描。</span><span class="sxs-lookup"><span data-stu-id="fb065-180">In this example, there is too much text to scan easily.</span></span> <span data-ttu-id="fb065-181">雖然設計工具並不會用到，但使用者很可能會按 [下一步]，而不需要讀取任何文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-181">Although not intended by the designer, there is so much text that users will most likely click Next without reading anything.</span></span>

<span data-ttu-id="fb065-182">若要避免不鼓勵閱讀的文字，請製作您的文字來建立每個字數的字數。</span><span class="sxs-lookup"><span data-stu-id="fb065-182">To avoid text that discourages reading, craft your text to make every word count.</span></span> <span data-ttu-id="fb065-183">未加入減法，所以請使用簡單簡潔的文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-183">What doesn't add subtracts, so use simple, concise text.</span></span>

### <a name="use-the-inverted-pyramid"></a><span data-ttu-id="fb065-184">使用反向金字塔</span><span class="sxs-lookup"><span data-stu-id="fb065-184">Use the inverted pyramid</span></span>

<span data-ttu-id="fb065-185">學術撰寫通常是使用「金字塔」結構樣式來奠定事實的基礎、使用這些事實，然後建立結論形成類似金字塔的結構。</span><span class="sxs-lookup"><span data-stu-id="fb065-185">Academic writing typically uses a "pyramid" structural style that lays down a foundation of facts, works with those facts, and builds up to a conclusion forming a pyramid-like structure.</span></span> <span data-ttu-id="fb065-186">相較之下，新聞工作者會使用「反向金字塔」樣式，開頭為「重點」的基本概念，讀者必須要有這些結果。</span><span class="sxs-lookup"><span data-stu-id="fb065-186">By contrast, journalists use an "inverted pyramid" style that starts with the conclusion the fundamental "takeaway" that readers must have.</span></span> <span data-ttu-id="fb065-187">然後，它會更詳細地填滿讀者可能會想要掃描的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb065-187">It then fills in progressively more detail that readers may be interested in perhaps just to scan.</span></span> <span data-ttu-id="fb065-188">這種樣式的優點是它是直接的，並且可讓讀者在選擇的任何時間點停止讀取，並且仍瞭解重要資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-188">The advantage of this style is that it gets right to the point, and allows readers to stop reading at any point they choose and still understand the essential information.</span></span>

<span data-ttu-id="fb065-189">您應該將反向金字塔結構套用至 UI 文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-189">You should apply the inverted pyramid structure to UI text.</span></span> <span data-ttu-id="fb065-190">取得重要資訊的重點，讓使用者隨時都能隨時停止閱讀，並使用說明連結來呈現金字塔的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="fb065-190">Get right to the point with the essential information, let users stop reading at any time they choose, and use a Help link to present the remainder of the pyramid.</span></span>

![<span data-ttu-id="fb065-191">加入 windows 程式之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-191">screen shot of message on joining windows program</span></span> ](images/text-ui-image7.png)

<span data-ttu-id="fb065-192">在此範例中，基本資訊是在查詢主要指示文字時，其他有用的資訊則是在補充指示中，而您可以按一下 [說明] 連結來取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb065-192">In this example, the essential information is in the query of the main instruction text, additional helpful information is in the supplemental instructions, and details are available by clicking a Help link.</span></span>

<span data-ttu-id="fb065-193">**如果您只進行五件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="fb065-193">**If you do only five things...**</span></span>

1.  <span data-ttu-id="fb065-194">及早處理文字，因為文字問題通常會顯示設計問題。</span><span class="sxs-lookup"><span data-stu-id="fb065-194">Work on text early because text problems often reveal design problems.</span></span>
2.  <span data-ttu-id="fb065-195">設計要掃描的文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-195">Design your text for scanning.</span></span>
3.  <span data-ttu-id="fb065-196">消除重複的文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-196">Eliminate redundant text.</span></span>
4.  <span data-ttu-id="fb065-197">使用簡單易懂的文字;不要進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-197">Use easy-to-understand text; don't over-communicate.</span></span>
5.  <span data-ttu-id="fb065-198">如有必要，請提供說明內容的連結，以取得更詳細的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-198">When necessary, provide links to Help content for more detailed information.</span></span>

## <a name="guidelines"></a><span data-ttu-id="fb065-199">指導方針</span><span class="sxs-lookup"><span data-stu-id="fb065-199">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="fb065-200">一般</span><span class="sxs-lookup"><span data-stu-id="fb065-200">General</span></span>

-   <span data-ttu-id="fb065-201">**移除多餘的文字。**</span><span class="sxs-lookup"><span data-stu-id="fb065-201">**Remove redundant text.**</span></span> <span data-ttu-id="fb065-202">在視窗標題、主要指示、補充指示、內容區域、命令連結和認可按鈕中尋找重複的文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-202">Look for redundant text in window titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="fb065-203">一般而言，請將全文檢索保留在主要指示和互動式控制項中，並從其他地方移除任何多餘的內容。</span><span class="sxs-lookup"><span data-stu-id="fb065-203">Generally, leave full text in main instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="fb065-204">**避免 UI 文字的大型區塊。**</span><span class="sxs-lookup"><span data-stu-id="fb065-204">**Avoid large blocks of UI text.**</span></span> <span data-ttu-id="fb065-205">執行這項操作的方法包括：</span><span class="sxs-lookup"><span data-stu-id="fb065-205">Ways of doing this include:</span></span>
    -   <span data-ttu-id="fb065-206">將文字區塊化成較短的句子和段落。</span><span class="sxs-lookup"><span data-stu-id="fb065-206">Chunking text into shorter sentences and paragraphs.</span></span>
    -   <span data-ttu-id="fb065-207">必要時，提供實用但不重要的資訊說明 [連結](winenv-help.md) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-207">When necessary, providing [Help links](winenv-help.md) to useful, but not essential, information.</span></span>
-   <span data-ttu-id="fb065-208">**選擇明確通訊的物件名稱和標籤，並區分物件的用途。**</span><span class="sxs-lookup"><span data-stu-id="fb065-208">**Choose object names and labels that clearly communicate and differentiate what the object does.**</span></span> <span data-ttu-id="fb065-209">使用者不應該需要找出物件真正的意義，或與其他物件有何不同。</span><span class="sxs-lookup"><span data-stu-id="fb065-209">Users shouldn't have to figure out what the object really means or how it differs from other objects.</span></span>

    <span data-ttu-id="fb065-210">不正確：</span><span class="sxs-lookup"><span data-stu-id="fb065-210">Incorrect:</span></span>

    ![未命名的監視器清單螢幕擷取畫面](images/text-ui-image8.png)

    <span data-ttu-id="fb065-212">較佳：</span><span class="sxs-lookup"><span data-stu-id="fb065-212">Better:</span></span>

    ![特定網路介面卡清單的螢幕擷取畫面](images/text-ui-image9.png)

    <span data-ttu-id="fb065-214">在不正確的範例中，物件名稱完全沒有差異;更好的範例會依產品名稱顯示強式差異。</span><span class="sxs-lookup"><span data-stu-id="fb065-214">In the incorrect example, the object names are not differentiated at all; the better example shows strong differentiation by product name.</span></span>

-   <span data-ttu-id="fb065-215">**如果您想要確保使用者讀取與某個動作相關的特定文字，請將它放在互動式控制項上。**</span><span class="sxs-lookup"><span data-stu-id="fb065-215">**If you want to make sure that users read specific text related to an action, place it on an interactive control.**</span></span>
    -   <span data-ttu-id="fb065-216">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="fb065-216">**Acceptable:**</span></span>
    -   ![<span data-ttu-id="fb065-217">使用 [確定] 按鈕格式化警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-217">screen shot of formatting warning using ok button</span></span> ](images/text-ui-image10.png)
    -   <span data-ttu-id="fb065-218">在此範例中，使用者有可能無法讀取說明他們正在確認內容的文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-218">In this example, there's a chance that users won't read the text that explains what they're confirming.</span></span>
    -   <span data-ttu-id="fb065-219">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="fb065-219">**Better:**</span></span>
    -   ![<span data-ttu-id="fb065-220">格式化警告和格式按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-220">screen shot of formatting warning and format button</span></span> ](images/text-ui-image11.png)
    -   <span data-ttu-id="fb065-221">在此範例中，您可以確定至少使用者瞭解它們即將格式化磁片。</span><span class="sxs-lookup"><span data-stu-id="fb065-221">In this example, you can be sure that at least users understand that they are about to format a disk.</span></span>
-   <span data-ttu-id="fb065-222">**在句子之間使用一個空格。**</span><span class="sxs-lookup"><span data-stu-id="fb065-222">**Use one space between sentences.**</span></span> <span data-ttu-id="fb065-223">不是二。</span><span class="sxs-lookup"><span data-stu-id="fb065-223">Not two.</span></span>

### <a name="text-fonts-sizes-and-colors"></a><span data-ttu-id="fb065-224">文字字型、大小和色彩</span><span class="sxs-lookup"><span data-stu-id="fb065-224">Text fonts, sizes, and colors</span></span>

-   <span data-ttu-id="fb065-225">**只針對連結和主要指示使用藍色文字。**</span><span class="sxs-lookup"><span data-stu-id="fb065-225">**Use blue text only for links and main instructions.**</span></span>
-   <span data-ttu-id="fb065-226">**針對搜尋結果中的 Url 使用綠色文字。**</span><span class="sxs-lookup"><span data-stu-id="fb065-226">**Use green text only for URLs in search results.**</span></span>

<span data-ttu-id="fb065-227">下列字型和色彩是 Windows 的預設值。</span><span class="sxs-lookup"><span data-stu-id="fb065-227">The following fonts and colors are defaults for Windows.</span></span>



| <span data-ttu-id="fb065-228">模式</span><span class="sxs-lookup"><span data-stu-id="fb065-228">Pattern</span></span>                                                                                     | <span data-ttu-id="fb065-229">主題符號</span><span class="sxs-lookup"><span data-stu-id="fb065-229">Theme symbol</span></span>                            | <span data-ttu-id="fb065-230">字型、色彩</span><span class="sxs-lookup"><span data-stu-id="fb065-230">Font, Color</span></span>                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![<span data-ttu-id="fb065-231">第一個資料行：標題列文字</span><span class="sxs-lookup"><span data-stu-id="fb065-231">first column: title bar text</span></span> ](images/text-ui-image12.png)<br/>              | <span data-ttu-id="fb065-232">CaptionFont</span><span class="sxs-lookup"><span data-stu-id="fb065-232">CaptionFont</span></span><br/>      | <span data-ttu-id="fb065-233">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-233">9 pt.</span></span> <span data-ttu-id="fb065-234">黑色 (\# 000000) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-234">black (\#000000) Segoe UI</span></span><br/>                 |
| ![<span data-ttu-id="fb065-235">第一個資料行：主要指示</span><span class="sxs-lookup"><span data-stu-id="fb065-235">first column: main instructions</span></span> ](images/text-ui-image13.png)<br/>           | <span data-ttu-id="fb065-236">MainInstruction</span><span class="sxs-lookup"><span data-stu-id="fb065-236">MainInstruction</span></span><br/>  | <span data-ttu-id="fb065-237">12 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-237">12 pt.</span></span> <span data-ttu-id="fb065-238">藍色 (\# 003399) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-238">blue (\#003399) Segoe UI</span></span><br/>                 |
| ![<span data-ttu-id="fb065-239">第一個資料行：次要指示</span><span class="sxs-lookup"><span data-stu-id="fb065-239">first column: secondary instructions</span></span> ](images/text-ui-image14.png)<br/>      | <span data-ttu-id="fb065-240">指令</span><span class="sxs-lookup"><span data-stu-id="fb065-240">Instruction</span></span><br/>      | <span data-ttu-id="fb065-241">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-241">9 pt.</span></span> <span data-ttu-id="fb065-242">黑色 (\# 000000) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-242">black (\#000000) Segoe UI</span></span><br/>                 |
| ![<span data-ttu-id="fb065-243">第一個資料行：一般文字</span><span class="sxs-lookup"><span data-stu-id="fb065-243">first column: normal text</span></span> ](images/text-ui-image15.png)<br/>                 | <span data-ttu-id="fb065-244">BodyText</span><span class="sxs-lookup"><span data-stu-id="fb065-244">BodyText</span></span><br/>         | <span data-ttu-id="fb065-245">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-245">9 pt.</span></span> <span data-ttu-id="fb065-246">黑色 (\# 000000) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-246">black (\#000000) Segoe UI</span></span><br/>                 |
| ![<span data-ttu-id="fb065-247">第一個資料行：強調文字</span><span class="sxs-lookup"><span data-stu-id="fb065-247">first column: emphasized text</span></span> ](images/text-ui-image16.png)<br/>             | <span data-ttu-id="fb065-248">BodyText</span><span class="sxs-lookup"><span data-stu-id="fb065-248">BodyText</span></span><br/>         | <span data-ttu-id="fb065-249">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-249">9 pt.</span></span> <span data-ttu-id="fb065-250">黑色 (\# 000000) Segoe UI、粗體或斜體</span><span class="sxs-lookup"><span data-stu-id="fb065-250">black (\#000000) Segoe UI, bold or italic</span></span><br/> |
| ![<span data-ttu-id="fb065-251">第一個資料行：可編輯的文字</span><span class="sxs-lookup"><span data-stu-id="fb065-251">first column: editable text</span></span> ](images/text-ui-image17.png)<br/>               | <span data-ttu-id="fb065-252">BodyText</span><span class="sxs-lookup"><span data-stu-id="fb065-252">BodyText</span></span><br/>         | <span data-ttu-id="fb065-253">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-253">9 pt.</span></span> <span data-ttu-id="fb065-254">\#box 中的黑色 (000000) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-254">black (\#000000) Segoe UI, in a box</span></span><br/>       |
| ![<span data-ttu-id="fb065-255">第一個資料行：停用的文字</span><span class="sxs-lookup"><span data-stu-id="fb065-255">first column: disabled text</span></span> ](images/text-ui-image18.png)<br/>               | <span data-ttu-id="fb065-256">Disabled</span><span class="sxs-lookup"><span data-stu-id="fb065-256">Disabled</span></span><br/>         | <span data-ttu-id="fb065-257">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-257">9 pt.</span></span> <span data-ttu-id="fb065-258">暗灰色 (\# 323232) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-258">dark gray (\#323232) Segoe UI</span></span><br/>             |
| ![<span data-ttu-id="fb065-259">第一個資料行：連結</span><span class="sxs-lookup"><span data-stu-id="fb065-259">first column: link</span></span> ](images/text-ui-image19.png)<br/>                        | <span data-ttu-id="fb065-260">HyperLinkText</span><span class="sxs-lookup"><span data-stu-id="fb065-260">HyperLinkText</span></span><br/>    | <span data-ttu-id="fb065-261">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-261">9 pt.</span></span> <span data-ttu-id="fb065-262">blue (\# 0066CC) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-262">blue (\#0066CC) Segoe UI</span></span><br/>                  |
| ![<span data-ttu-id="fb065-263">第一個資料行：連結 (停留) </span><span class="sxs-lookup"><span data-stu-id="fb065-263">first column: links (hover)</span></span> ](images/text-ui-image20.png)<br/>               | <span data-ttu-id="fb065-264">經常性存取層</span><span class="sxs-lookup"><span data-stu-id="fb065-264">Hot</span></span><br/>              | <span data-ttu-id="fb065-265">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-265">9 pt.</span></span> <span data-ttu-id="fb065-266">淺藍色 (\# 3399FF) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-266">light blue (\#3399FF) Segoe UI</span></span><br/>            |
| ![<span data-ttu-id="fb065-267">第一個資料行：群組標頭</span><span class="sxs-lookup"><span data-stu-id="fb065-267">first column: group header</span></span> ](images/text-ui-image21.png)<br/>                |  <br/>                | <span data-ttu-id="fb065-268">11 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-268">11 pt.</span></span> <span data-ttu-id="fb065-269">藍色 (\# 003399) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-269">blue (\#003399) Segoe UI</span></span><br/>                 |
| ![<span data-ttu-id="fb065-270">第一個資料行：內容視圖中的檔案名 () </span><span class="sxs-lookup"><span data-stu-id="fb065-270">first column: file name (in content view)</span></span> ](images/text-ui-image22.png)<br/> |  <br/>                | <span data-ttu-id="fb065-271">11 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-271">11 pt.</span></span> <span data-ttu-id="fb065-272">黑色 (\# 000000) Segoe UI</span><span class="sxs-lookup"><span data-stu-id="fb065-272">black (\#000000) Segoe UI</span></span><br/>                |
| ![<span data-ttu-id="fb065-273">第一個資料行：檔文字</span><span class="sxs-lookup"><span data-stu-id="fb065-273">first column: document text</span></span> ](images/text-ui-image23.png)<br/>               | <span data-ttu-id="fb065-274">(無)</span><span class="sxs-lookup"><span data-stu-id="fb065-274">(none)</span></span><br/>           | <span data-ttu-id="fb065-275">9 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-275">9 pt.</span></span> <span data-ttu-id="fb065-276">黑色 (\# 000000) Calibri</span><span class="sxs-lookup"><span data-stu-id="fb065-276">black (\#000000) Calibri</span></span><br/>                  |
| ![<span data-ttu-id="fb065-277">第一個資料行：檔標題</span><span class="sxs-lookup"><span data-stu-id="fb065-277">first column: document headings</span></span> ](images/text-ui-image24.png)<br/>           | <span data-ttu-id="fb065-278">(無)</span><span class="sxs-lookup"><span data-stu-id="fb065-278">(none)</span></span><br/>           | <span data-ttu-id="fb065-279">17 pt。</span><span class="sxs-lookup"><span data-stu-id="fb065-279">17 pt.</span></span> <span data-ttu-id="fb065-280">黑色 (\# 000000) Calibri</span><span class="sxs-lookup"><span data-stu-id="fb065-280">black (\#000000) Calibri</span></span><br/>                 |



 

<span data-ttu-id="fb065-281">如需詳細資訊和範例， [請參閱字型](vis-fonts.md) 和 [色彩](vis-color.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-281">For more information and examples, see [Fonts](vis-fonts.md) and [Color](vis-color.md).</span></span>

### <a name="other-text-characteristics"></a><span data-ttu-id="fb065-282">其他文字特性</span><span class="sxs-lookup"><span data-stu-id="fb065-282">Other text characteristics</span></span>

<span data-ttu-id="fb065-283">**粗體字**</span><span class="sxs-lookup"><span data-stu-id="fb065-283">**Bold**</span></span>

-   <span data-ttu-id="fb065-284">**請謹慎使用粗體，以吸引使用者必須閱讀的文字。**</span><span class="sxs-lookup"><span data-stu-id="fb065-284">**Use bold sparingly to draw attention to text users must read.**</span></span> <span data-ttu-id="fb065-285">例如，當使用者掃描選項按鈕選項清單時，可能會很樂意看到以粗體顯示的標籤，而是從新增每個選項相關補充資訊的文字中取出。</span><span class="sxs-lookup"><span data-stu-id="fb065-285">For example, users scanning down a list of radio button options may appreciate seeing the labels in bold, to stand out from text that adds supplemental information about each option.</span></span> <span data-ttu-id="fb065-286">請注意，使用太多粗體會減少其影響。</span><span class="sxs-lookup"><span data-stu-id="fb065-286">Be aware that using too much bold lessens its impact.</span></span>
-   <span data-ttu-id="fb065-287">**使用加上標籤的資料時，請使用粗體來強調對資料整體來說較重要的資料。**</span><span class="sxs-lookup"><span data-stu-id="fb065-287">**With labeled data, use bold to emphasize whichever is more important for the data as a whole.**</span></span>
    -   <span data-ttu-id="fb065-288">大部分的一般資料 (，其中的資料在沒有標籤的情況下沒有任何意義，如同數位或日期) 一樣，請使用粗體標籤和一般資料，讓使用者可以更輕鬆地掃描及瞭解資料類型。</span><span class="sxs-lookup"><span data-stu-id="fb065-288">For mostly generic data (where the data has little meaning without its labels, as with numerals or dates), use bold labels and plain data so that users can more easily scan and understand the types of data.</span></span>
    -   <span data-ttu-id="fb065-289">大部分的自我理解資料都是使用純文字標籤和粗體資料，讓使用者可以專注于資料本身。</span><span class="sxs-lookup"><span data-stu-id="fb065-289">For mostly self-explanatory data, use plain labels and bold data so that users can focus on the data itself.</span></span>
    -   <span data-ttu-id="fb065-290">或者，您可以使用暗灰色文字來消除不重要的資訊，而不是使用粗體來強調更重要的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-290">Alternatively, you can use dark gray text to de-emphasize less important information instead of using bold to emphasize the more important information.</span></span>

        ![<span data-ttu-id="fb065-291">windows explorer 縮圖視圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-291">screen shot of windows explorer thumbnail view</span></span> ](images/text-ui-image25.png)

        <span data-ttu-id="fb065-292">在此範例中，您不會使用粗體強調資料，而是使用深灰色來反白顯示標籤。</span><span class="sxs-lookup"><span data-stu-id="fb065-292">In this example, instead of emphasizing the data using bold, the labels are de-emphasized by using dark gray.</span></span>

-   <span data-ttu-id="fb065-293">**並非所有字型都支援粗體，因此在瞭解文字時絕對不重要。**</span><span class="sxs-lookup"><span data-stu-id="fb065-293">**Not all fonts support bold, so it should never be crucial to understanding the text.**</span></span>

<span data-ttu-id="fb065-294">**斜體**</span><span class="sxs-lookup"><span data-stu-id="fb065-294">**Italic**</span></span>

-   <span data-ttu-id="fb065-295">用來真正參考文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-295">Use to refer to text literally.</span></span> <span data-ttu-id="fb065-296">請勿將引號用於此用途。</span><span class="sxs-lookup"><span data-stu-id="fb065-296">Don't use quotation marks for this purpose.</span></span>

    <span data-ttu-id="fb065-297">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-297">**Correct:**</span></span>

    <span data-ttu-id="fb065-298">檔和檔案等詞彙通常會交替使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-298">The terms document and file are often used interchangeably.</span></span>

-   <span data-ttu-id="fb065-299">用於[文字方塊](ctrl-text-boxes.md)中的[提示](glossary.md)和[可編輯的下拉式清單](/windows/desktop/uxguide/ctrl-drop)。</span><span class="sxs-lookup"><span data-stu-id="fb065-299">Use for [prompts](glossary.md) in [text boxes](ctrl-text-boxes.md) and [editable drop-down lists](/windows/desktop/uxguide/ctrl-drop).</span></span>

    ![<span data-ttu-id="fb065-300">[搜尋] 文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-300">screen shot of search text box</span></span> ](images/text-ui-image26.png)

    <span data-ttu-id="fb065-301">在此範例中，[搜尋] 方塊中的提示會格式化為斜體文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-301">In this example, the prompt in the Search box is formatted as italic text.</span></span>

-   <span data-ttu-id="fb065-302">請謹慎使用以強調特定文字，以協助理解。</span><span class="sxs-lookup"><span data-stu-id="fb065-302">Use sparingly to emphasize specific words to aid in comprehension.</span></span>
-   <span data-ttu-id="fb065-303">**並非所有字型都支援斜體，因此在瞭解文字時絕對不重要。**</span><span class="sxs-lookup"><span data-stu-id="fb065-303">**Not all fonts support italic, so it should never be crucial to understanding the text.**</span></span>

<span data-ttu-id="fb065-304">**粗體斜體**</span><span class="sxs-lookup"><span data-stu-id="fb065-304">**Bold italic**</span></span>

-   <span data-ttu-id="fb065-305">請勿在 UI 文字中使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-305">Don't use in UI text.</span></span>

<span data-ttu-id="fb065-306">**Underline**</span><span class="sxs-lookup"><span data-stu-id="fb065-306">**Underline**</span></span>

-   <span data-ttu-id="fb065-307">請勿使用，但連結除外。</span><span class="sxs-lookup"><span data-stu-id="fb065-307">Don't use, except for links.</span></span>
-   <span data-ttu-id="fb065-308">請勿使用強調。</span><span class="sxs-lookup"><span data-stu-id="fb065-308">Don't use for emphasis.</span></span> <span data-ttu-id="fb065-309">改用斜體。</span><span class="sxs-lookup"><span data-stu-id="fb065-309">Use italic instead.</span></span>

### <a name="punctuation"></a><span data-ttu-id="fb065-310">標點符號</span><span class="sxs-lookup"><span data-stu-id="fb065-310">Punctuation</span></span>

<span data-ttu-id="fb065-311">**時期**</span><span class="sxs-lookup"><span data-stu-id="fb065-311">**Periods**</span></span>

-   <span data-ttu-id="fb065-312">**請勿放置於控制項標籤、主要指示或說明連結的結尾。**</span><span class="sxs-lookup"><span data-stu-id="fb065-312">**Don't place at the end of control labels, main instructions, or Help links.**</span></span>
-   <span data-ttu-id="fb065-313">放在補充指示的結尾、補充說明，或形成完整句子的任何其他靜態文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-313">Place at the end of supplemental instructions, supplemental explanations, or any other static text that forms a complete sentence.</span></span>

<span data-ttu-id="fb065-314">**問號**</span><span class="sxs-lookup"><span data-stu-id="fb065-314">**Question marks**</span></span>

-   <span data-ttu-id="fb065-315">**放在所有問題的結尾。**</span><span class="sxs-lookup"><span data-stu-id="fb065-315">**Place at the end of all questions.**</span></span> <span data-ttu-id="fb065-316">與句號不同的是，所有類型的文字都會使用問號。</span><span class="sxs-lookup"><span data-stu-id="fb065-316">Unlike periods, question marks are used for all types of text.</span></span>

<span data-ttu-id="fb065-317">**驚嘆號**</span><span class="sxs-lookup"><span data-stu-id="fb065-317">**Exclamation points**</span></span>

-   <span data-ttu-id="fb065-318">在商務應用程式中，請避免。</span><span class="sxs-lookup"><span data-stu-id="fb065-318">In business applications, avoid.</span></span>
    -   <span data-ttu-id="fb065-319">**例外狀況：** 在下載完成的內容中，有時會使用驚嘆號 ( 「完成！」) ，並 ( 「新的！」中呼叫 Web 內容) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-319">**Exceptions:** Exclamation points are sometimes used in the context of download completion ("Done!") and to call attention to Web content ("New!").</span></span>

<span data-ttu-id="fb065-320">**逗號**</span><span class="sxs-lookup"><span data-stu-id="fb065-320">**Commas**</span></span>

-   <span data-ttu-id="fb065-321">在三個或多個專案的清單中，一律在清單中的下一個到最後一個專案後面加上逗號。</span><span class="sxs-lookup"><span data-stu-id="fb065-321">In a list of three or more items, always put a comma after the next-to-last item in the list.</span></span>

<span data-ttu-id="fb065-322">**冒號**</span><span class="sxs-lookup"><span data-stu-id="fb065-322">**Colons**</span></span>

-   <span data-ttu-id="fb065-323">**在外部控制標籤的結尾使用冒號。**</span><span class="sxs-lookup"><span data-stu-id="fb065-323">**Use colons at the end of external control labels.**</span></span> <span data-ttu-id="fb065-324">這對存取範圍特別重要，因為有些輔助技術會尋找用來識別控制項標籤的冒號。</span><span class="sxs-lookup"><span data-stu-id="fb065-324">This is particularly important for accessibility because some assistive technologies look for colons to identify control labels.</span></span>
-   <span data-ttu-id="fb065-325">使用冒號來引進專案清單。</span><span class="sxs-lookup"><span data-stu-id="fb065-325">Use a colon to introduce a list of items.</span></span>

<span data-ttu-id="fb065-326">**橢圓**</span><span class="sxs-lookup"><span data-stu-id="fb065-326">**Ellipses**</span></span>

-   <span data-ttu-id="fb065-327">**省略號表示不完整性。**</span><span class="sxs-lookup"><span data-stu-id="fb065-327">**Ellipses mean incompleteness.**</span></span> <span data-ttu-id="fb065-328">使用 UI 文字中的省略號，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fb065-328">Use ellipses in UI text as follows:</span></span>
    -   <span data-ttu-id="fb065-329">**命令：** 指出命令需要額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-329">**Commands:** Indicate that a command needs additional information.</span></span> <span data-ttu-id="fb065-330">當動作只在需要額外的資訊時顯示另一個視窗時，請勿使用省略號。</span><span class="sxs-lookup"><span data-stu-id="fb065-330">Don't use an ellipsis whenever an action displays another window only when additional information is required.</span></span> <span data-ttu-id="fb065-331">如需詳細資訊，請參閱 [命令按鈕](ctrl-command-buttons.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-331">For more information, see [Command Buttons](ctrl-command-buttons.md).</span></span>
    -   <span data-ttu-id="fb065-332">**資料：** 指出文字已被截斷。</span><span class="sxs-lookup"><span data-stu-id="fb065-332">**Data:** Indicate that text is truncated.</span></span>
    -   <span data-ttu-id="fb065-333">**標籤：** 指出工作正在進行中 (例如「正在搜尋 ...」 ) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-333">**Labels:** Indicate that a task is in progress (for example, "Searching...").</span></span>

        <span data-ttu-id="fb065-334">**秘訣：** 在具有未使用空間的視窗或頁面中截斷文字表示版面配置不良，或預設視窗大小太小。</span><span class="sxs-lookup"><span data-stu-id="fb065-334">**Tip:** Truncated text in a window or page with unused space indicates poor layout or a default window size that is too small.</span></span> <span data-ttu-id="fb065-335">致力於消除或減少截斷文字數量的版面配置和預設視窗大小。</span><span class="sxs-lookup"><span data-stu-id="fb065-335">Strive for layouts and default window sizes that eliminate or reduce the amount of truncated text.</span></span> <span data-ttu-id="fb065-336">如需詳細資訊，請參閱[配置](vis-layout.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-336">For more information, see [Layout](vis-layout.md).</span></span>

-   <span data-ttu-id="fb065-337">**不要讓橢圓形成為互動。**</span><span class="sxs-lookup"><span data-stu-id="fb065-337">**Don't make ellipses interactive.**</span></span> <span data-ttu-id="fb065-338">若要顯示截斷的文字，請讓使用者調整控制項大小以查看更多文字，或改用 [漸進式洩漏控制項](ctrl-progressive-disclosure-controls.md) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-338">To show truncated text, let users resize the control to see more text or use a [progressive disclosure control](ctrl-progressive-disclosure-controls.md) instead.</span></span>

<span data-ttu-id="fb065-339">**引號和單引號**</span><span class="sxs-lookup"><span data-stu-id="fb065-339">**Quotation marks and apostrophes**</span></span>

-   <span data-ttu-id="fb065-340">若要逐字參考文字，請使用斜體格式，而非引號。</span><span class="sxs-lookup"><span data-stu-id="fb065-340">To refer to text literally, use italic formatting rather than quotation marks.</span></span>
-   <span data-ttu-id="fb065-341">只有在需要時才將視窗標題和控制項標籤放在引號中，以避免混淆，您也無法改為使用粗體來格式化。</span><span class="sxs-lookup"><span data-stu-id="fb065-341">Put window titles and control labels in quotation marks only if required to prevent confusion and you can't format using bold instead.</span></span>
-   <span data-ttu-id="fb065-342">如果是引號，則偏好使用雙引號 ( "" ) ;請避免用單引號括住。</span><span class="sxs-lookup"><span data-stu-id="fb065-342">For quotation marks, prefer double-quotation marks (" "); avoid single-quotation marks.</span></span>

    <span data-ttu-id="fb065-343">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-343">**Correct:**</span></span>

    <span data-ttu-id="fb065-344">確定要刪除「Sparky 的貓資料夾」嗎？</span><span class="sxs-lookup"><span data-stu-id="fb065-344">Are you sure you want to delete "Sparky's cat folder"?</span></span>

    <span data-ttu-id="fb065-345">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-345">**Incorrect:**</span></span>

    <span data-ttu-id="fb065-346">確定要刪除 ' Sparky ' 的貓資料夾 ' 嗎？</span><span class="sxs-lookup"><span data-stu-id="fb065-346">Are you sure you want to delete 'Sparky's cat folder'?</span></span>

### <a name="capitalization"></a><span data-ttu-id="fb065-347">大寫</span><span class="sxs-lookup"><span data-stu-id="fb065-347">Capitalization</span></span>

-   <span data-ttu-id="fb065-348">**針對標題使用標題樣式的大小寫，針對所有其他 UI 元素使用句子樣式的大小寫。**</span><span class="sxs-lookup"><span data-stu-id="fb065-348">**Use title-style capitalization for titles, sentence-style capitalization for all other UI elements.**</span></span> <span data-ttu-id="fb065-349">這麼做會更適合 Windows 的 [聲音](text-style-tone.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-349">Doing so is more appropriate for the [Windows tone](text-style-tone.md).</span></span>

    -   <span data-ttu-id="fb065-350">**例外狀況：** 針對繼承應用程式，如果有必要，您可以針對命令按鈕、功能表和資料行標題使用標題樣式的大小寫，以避免混用大小寫樣式。</span><span class="sxs-lookup"><span data-stu-id="fb065-350">**Exception:** For legacy applications, you may use title-style capitalization for command buttons, menus, and column headings if necessary to avoid mixing capitalization styles.</span></span>

        ![<span data-ttu-id="fb065-351">一般屬性工作表的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-351">screen shot of generic property sheet</span></span> ](images/text-ui-image27.png)

    <span data-ttu-id="fb065-352">此一般範例會針對屬性工作表顯示正確的大小寫和標點符號。</span><span class="sxs-lookup"><span data-stu-id="fb065-352">This generic example shows correct capitalization and punctuation for property sheets.</span></span>

    ![<span data-ttu-id="fb065-353">[一般] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-353">screen shot of generic dialog box</span></span> ](images/text-ui-image28.png)

    <span data-ttu-id="fb065-354">此一般範例會針對對話方塊顯示正確的大小寫和標點符號。</span><span class="sxs-lookup"><span data-stu-id="fb065-354">This generic example shows correct capitalization and punctuation for dialogs.</span></span>

-   <span data-ttu-id="fb065-355">**對於功能和技術名稱而言，請務必保守。**</span><span class="sxs-lookup"><span data-stu-id="fb065-355">**For feature and technology names, be conservative in capitalizing.**</span></span> <span data-ttu-id="fb065-356">一般來說， (使用標題樣式的大小寫) ，則只能使用大寫的主要元件。</span><span class="sxs-lookup"><span data-stu-id="fb065-356">Typically, only major components should be capitalized (using title-style capitalization).</span></span>

    <span data-ttu-id="fb065-357">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-357">**Correct:**</span></span>

    <span data-ttu-id="fb065-358">Analysis Services、cube、維度</span><span class="sxs-lookup"><span data-stu-id="fb065-358">Analysis Services, cubes, dimensions</span></span>

    <span data-ttu-id="fb065-359">Analysis Services 是 SQL Server 的主要元件，所以符合標題樣式的大小寫;cube 和維度是資料庫分析軟體的通用元素，因此不需要將其設為大寫。</span><span class="sxs-lookup"><span data-stu-id="fb065-359">Analysis Services is a major component of SQL Server, so title-style capitalization is appropriate; cubes and dimensions are common elements of database analysis software, so it is unnecessary to capitalize them.</span></span>

-   <span data-ttu-id="fb065-360">**若為功能和技術名稱，請在大寫中保持一致。**</span><span class="sxs-lookup"><span data-stu-id="fb065-360">**For feature and technology names, be consistent in capitalizing.**</span></span> <span data-ttu-id="fb065-361">如果名稱在 UI 畫面上出現一次以上，則應該一律以相同的方式來顯示。</span><span class="sxs-lookup"><span data-stu-id="fb065-361">If the name appears more than once on a UI screen, it should always appear the same way.</span></span> <span data-ttu-id="fb065-362">同樣地，在程式的所有 UI 畫面中，名稱應該一致地呈現。</span><span class="sxs-lookup"><span data-stu-id="fb065-362">Likewise, across all UI screens in the program, the name should be consistently presented.</span></span>
-   <span data-ttu-id="fb065-363">不要將一般使用者介面專案的名稱大寫，例如工具列、功能表、捲軸、按鈕和圖示。</span><span class="sxs-lookup"><span data-stu-id="fb065-363">Don't capitalize the names of generic user interface elements, such as toolbar, menu, scroll bar, button, and icon.</span></span>
    -   <span data-ttu-id="fb065-364">**例外狀況：** 網址列、連結列。</span><span class="sxs-lookup"><span data-stu-id="fb065-364">**Exceptions:** Address bar, Links bar.</span></span>
-   <span data-ttu-id="fb065-365">所有大寫字母都不要使用鍵盤按鍵。</span><span class="sxs-lookup"><span data-stu-id="fb065-365">Don't use all capital letters for keyboard keys.</span></span> <span data-ttu-id="fb065-366">相反地，請遵循標準鍵盤所使用的大小寫，或者，如果鍵盤上未標示按鍵，則為小寫。</span><span class="sxs-lookup"><span data-stu-id="fb065-366">Instead, follow the capitalization used by standard keyboards, or lowercase if the key is not labeled on the keyboard.</span></span>

    <span data-ttu-id="fb065-367">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-367">**Correct:**</span></span>

    <span data-ttu-id="fb065-368">空格鍵、Tab、Enter、Page Up、Ctrl + Alt + Del</span><span class="sxs-lookup"><span data-stu-id="fb065-368">spacebar, Tab, Enter, Page Up, Ctrl+Alt+Del</span></span>

    <span data-ttu-id="fb065-369">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-369">**Incorrect:**</span></span>

    <span data-ttu-id="fb065-370">空格鍵、TAB、ENTER、PG、CTRL + ALT + DEL</span><span class="sxs-lookup"><span data-stu-id="fb065-370">SPACEBAR, TAB, ENTER, PG UP, CTRL+ALT+DEL</span></span>

-   <span data-ttu-id="fb065-371">**請勿使用所有大寫字母來強調。**</span><span class="sxs-lookup"><span data-stu-id="fb065-371">**Don't use all capital letters for emphasis.**</span></span> <span data-ttu-id="fb065-372">研究顯示這很難閱讀，使用者傾向于將它視為「尖叫」。</span><span class="sxs-lookup"><span data-stu-id="fb065-372">Studies have shown that this is hard to read, and users tend to regard it as "screaming."</span></span> <span data-ttu-id="fb065-373">若為警告，請使用警告圖示及清楚的措辭說明這種情況。</span><span class="sxs-lookup"><span data-stu-id="fb065-373">For warnings, use a warning icon and a clearly-worded explanation of the situation.</span></span> <span data-ttu-id="fb065-374">例如，不需要新增所有大寫字母的字詞警告。</span><span class="sxs-lookup"><span data-stu-id="fb065-374">There is no need to add, for example, the term WARNING in all capital letters.</span></span>

<span data-ttu-id="fb065-375">如需詳細資訊，請參閱特定 UI 元件指導方針中的「文字」或「標籤」一節。</span><span class="sxs-lookup"><span data-stu-id="fb065-375">For more information, see the "Text" or "Labels" section in the specific UI component guidelines.</span></span>

### <a name="dates-and-times"></a><span data-ttu-id="fb065-376">日期和時間</span><span class="sxs-lookup"><span data-stu-id="fb065-376">Dates and times</span></span>

-   <span data-ttu-id="fb065-377">**不要以硬式編碼的格式來格式化日期和時間。**</span><span class="sxs-lookup"><span data-stu-id="fb065-377">**Don't hard-code the format of dates and times.**</span></span> <span data-ttu-id="fb065-378">遵循使用者對日期和時間格式的地區設定和自訂選項的選擇。</span><span class="sxs-lookup"><span data-stu-id="fb065-378">Respect the user's choice of locale and customization options for the date and time formats.</span></span> <span data-ttu-id="fb065-379">使用者會在 [地區和語言] 控制台專案中選取這些專案。</span><span class="sxs-lookup"><span data-stu-id="fb065-379">The user selects these in the Region and Language control panel item.</span></span>

    ![日期格式的螢幕擷取畫面：2009年7月6日星期一](images/text-ui-image29.png)![日期格式的螢幕擷取畫面：2009年7月6日](images/text-ui-image30.png)

    <span data-ttu-id="fb065-382">在這些來自 Microsoft Outlook 的範例中，完整格式的兩種格式都是正確的。</span><span class="sxs-lookup"><span data-stu-id="fb065-382">In these examples from Microsoft Outlook, both formats for the long date are correct.</span></span> <span data-ttu-id="fb065-383">它們會反映使用者在 [地區和語言] 控制台專案中所做的不同選擇。</span><span class="sxs-lookup"><span data-stu-id="fb065-383">They reflect different choices users have made in the Region and Language control panel item.</span></span>

-   <span data-ttu-id="fb065-384">**針對可獲得額外資訊的案例，請使用完整的日期格式。**</span><span class="sxs-lookup"><span data-stu-id="fb065-384">**Use the long date format for scenarios that benefit from having additional information.**</span></span> <span data-ttu-id="fb065-385">針對沒有足夠空間可供完整格式的內容使用簡短日期格式。</span><span class="sxs-lookup"><span data-stu-id="fb065-385">Use the short date format for contexts that don't have sufficient space for the long format.</span></span> <span data-ttu-id="fb065-386">當使用者選擇要包含在完整和簡短格式的資訊時，設計工具會根據案例和內容，選擇要在程式中顯示的格式。</span><span class="sxs-lookup"><span data-stu-id="fb065-386">While users choose what information they would like to include in the long and short formats, designers choose which format to display in their programs based on the scenario and the context.</span></span>

    ![具有開始和到期日期之格式的螢幕擷取畫面](images/text-ui-image31.png)

    <span data-ttu-id="fb065-388">在此範例中，完整日期格式可協助使用者組織工作和期限。</span><span class="sxs-lookup"><span data-stu-id="fb065-388">In this example, the long date format helps users organize tasks and deadlines.</span></span>

### <a name="globalization-and-localization"></a><span data-ttu-id="fb065-389">全球化和當地語系化</span><span class="sxs-lookup"><span data-stu-id="fb065-389">Globalization and localization</span></span>

<span data-ttu-id="fb065-390">全球化表示建立可在任何國家、地區或文化特性中使用的檔或產品。</span><span class="sxs-lookup"><span data-stu-id="fb065-390">Globalization means to create documents or products that are usable in any country, region, or culture.</span></span> <span data-ttu-id="fb065-391">當地語系化指的是調整檔或產品，以用於非來源國家/地區以外的地區設定。</span><span class="sxs-lookup"><span data-stu-id="fb065-391">Localization means to adapt documents or products for use in a locale other than the country/region of origin.</span></span> <span data-ttu-id="fb065-392">撰寫 UI 文字時，請考慮全球化和當地語系化。</span><span class="sxs-lookup"><span data-stu-id="fb065-392">Consider globalization and localization when writing UI text.</span></span> <span data-ttu-id="fb065-393">您的程式可能會轉譯成其他語言，而且與您自己的文化特性不同。</span><span class="sxs-lookup"><span data-stu-id="fb065-393">Your program may be translated into other languages and used in cultures very different from your own.</span></span>

-   <span data-ttu-id="fb065-394">針對具有變數內容 (例如清單查看和樹狀檢視) 的控制項，請 **選擇適用于最長有效資料的寬度。**</span><span class="sxs-lookup"><span data-stu-id="fb065-394">For controls with variable contents (such as list views and tree views), **choose a width appropriate for the longest valid data.**</span></span>
-   <span data-ttu-id="fb065-395">**在 UI 介面中包含足夠的空間來提供額外的 30%** (高達200% 的文字，以縮短文字 (的文字) ，而非將當地語系化的數位) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-395">**Include space enough in the UI surface for an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span> <span data-ttu-id="fb065-396">從一種語言翻譯成另一種語言，通常會變更文字的行長度。</span><span class="sxs-lookup"><span data-stu-id="fb065-396">Translation from one language to another often changes line length of text.</span></span>
-   <span data-ttu-id="fb065-397">請勿在執行時間從子字串撰寫字串。</span><span class="sxs-lookup"><span data-stu-id="fb065-397">Don't compose strings from substrings at run time.</span></span> <span data-ttu-id="fb065-398">相反地，請使用完整的句子，讓翻譯工具不會有任何混淆。</span><span class="sxs-lookup"><span data-stu-id="fb065-398">Instead, use complete sentences so that there is no ambiguity for the translator.</span></span>
-   <span data-ttu-id="fb065-399">**請勿使用從屬控制項、它所包含的值，或其單位標籤來建立句子或片語。**</span><span class="sxs-lookup"><span data-stu-id="fb065-399">**Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.**</span></span> <span data-ttu-id="fb065-400">這種設計不可當地語系化，因為句子結構會隨著語言而有所不同。</span><span class="sxs-lookup"><span data-stu-id="fb065-400">Such a design is not localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="fb065-401">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-401">**Incorrect:**</span></span>

    ![<span data-ttu-id="fb065-402">核取方塊標籤內文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-402">screen shot of text box within a check box label</span></span> ](images/text-ui-image32.png)

    <span data-ttu-id="fb065-403">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-403">**Correct:**</span></span>

    ![<span data-ttu-id="fb065-404">核取方塊標籤之後文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-404">screen shot of text box after a check box label</span></span> ](images/text-ui-image33.png)

    <span data-ttu-id="fb065-405">在不正確的範例中，文字方塊放在核取方塊標籤內。</span><span class="sxs-lookup"><span data-stu-id="fb065-405">In the incorrect example, the text box is placed inside the check box label.</span></span>

-   <span data-ttu-id="fb065-406">請勿讓句子的一部分成為連結，因為翻譯時，該文字可能不會保持在一起。</span><span class="sxs-lookup"><span data-stu-id="fb065-406">Don't make only part of a sentence a link, because when translated, that text might not remain together.</span></span> <span data-ttu-id="fb065-407">因此，連結文字應自行形成完整的句子。</span><span class="sxs-lookup"><span data-stu-id="fb065-407">Link text should therefore form a complete sentence by itself.</span></span>
    -   <span data-ttu-id="fb065-408">**例外狀況：** 詞彙連結可以內嵌方式插入，作為句子的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb065-408">**Exception:** Glossary links can be inserted inline, as part of a sentence.</span></span>

<span data-ttu-id="fb065-409">如需詳細資訊，請參閱「 [移至全球開發人員中心](https://msdn.microsoft.com/goglobal/)」。</span><span class="sxs-lookup"><span data-stu-id="fb065-409">For more information, see the [Go Global Developer Center](https://msdn.microsoft.com/goglobal/).</span></span>

### <a name="title-bar-text"></a><span data-ttu-id="fb065-410">標題列文字</span><span class="sxs-lookup"><span data-stu-id="fb065-410">Title bar text</span></span>

-   <span data-ttu-id="fb065-411">根據視窗的類型選擇標題列文字：</span><span class="sxs-lookup"><span data-stu-id="fb065-411">Choose the title bar text based on the type of window:</span></span>
    -   <span data-ttu-id="fb065-412">以 **檔為主的最上層程式視窗：** 使用「檔案名稱程式名稱」格式。</span><span class="sxs-lookup"><span data-stu-id="fb065-412">**Top-level, document-centric program windows:** Use a "document name   program name" format.</span></span> <span data-ttu-id="fb065-413">首先會顯示檔案名稱，以提供以檔為中心的風格。</span><span class="sxs-lookup"><span data-stu-id="fb065-413">Document names are displayed first to give a document-centric feel.</span></span>
    -   <span data-ttu-id="fb065-414">**不是以檔為主的最上層程式視窗：** 只顯示程式名稱。</span><span class="sxs-lookup"><span data-stu-id="fb065-414">**Top-level program windows that are not document-centric:** Display the program name only.</span></span>
    -   <span data-ttu-id="fb065-415">**對話方塊：** 顯示對話方塊的命令、功能或程式。</span><span class="sxs-lookup"><span data-stu-id="fb065-415">**Dialog boxes:** Display the command, feature, or program from which the dialog box came.</span></span> <span data-ttu-id="fb065-416">請勿使用標題來說明此對話方塊的目的，也就是主要指示的用途。</span><span class="sxs-lookup"><span data-stu-id="fb065-416">Don't use the title to explain the dialog box's purpose that's the purpose of the main instructions.</span></span> <span data-ttu-id="fb065-417">如需詳細指導方針，請參閱 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-417">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>
    -   <span data-ttu-id="fb065-418">**嚮導：** 顯示嚮導名稱。</span><span class="sxs-lookup"><span data-stu-id="fb065-418">**Wizards:** Display the wizard name.</span></span> <span data-ttu-id="fb065-419">請注意，「wizard」這個字不應該包含在嚮導名稱中。</span><span class="sxs-lookup"><span data-stu-id="fb065-419">Note that the word "wizard" should not be included in wizard names.</span></span> <span data-ttu-id="fb065-420">如需詳細的指導方針，請參閱 [嚮導](win-wizards.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-420">For more guidelines, see [Wizards](win-wizards.md).</span></span>
-   <span data-ttu-id="fb065-421">**針對最上層的程式視窗，如果標題列標題和圖示在視窗頂端附近顯示，您可以隱藏標題列標題和圖示來避免重複。**</span><span class="sxs-lookup"><span data-stu-id="fb065-421">**For top-level program windows, if the title bar caption and icon are displayed prominently near the top of the window, you can hide the title bar caption and icon to avoid redundancy.**</span></span> <span data-ttu-id="fb065-422">不過，您仍然必須在內部設定適合用於 Windows 的標題。</span><span class="sxs-lookup"><span data-stu-id="fb065-422">However, you still have to set a suitable title internally for use by Windows.</span></span>
-   <span data-ttu-id="fb065-423">**在對話方塊中，請勿在標題中包含 "dialog" 或 "進度" 單字。**</span><span class="sxs-lookup"><span data-stu-id="fb065-423">**For dialog boxes, don't include the words "dialog" or "progress" in the titles.**</span></span> <span data-ttu-id="fb065-424">這些概念是隱含的，而將這些字組保持不變，可讓使用者更容易掃描標題。</span><span class="sxs-lookup"><span data-stu-id="fb065-424">These concepts are implied and leaving these words off makes the titles easier for users to scan.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="fb065-425">主要指示</span><span class="sxs-lookup"><span data-stu-id="fb065-425">Main instructions</span></span>

-   <span data-ttu-id="fb065-426">**您可以使用主要指示，精確地說明使用者在指定視窗或頁面中應執行的動作。**</span><span class="sxs-lookup"><span data-stu-id="fb065-426">**Use the main instruction to explain concisely what users should do in a given window or page.**</span></span> <span data-ttu-id="fb065-427">良好的主要指示傳達使用者的目標，而不是只著重在操作 UI。</span><span class="sxs-lookup"><span data-stu-id="fb065-427">Good main instructions communicate the user's objective rather than focusing just on manipulating the UI.</span></span>
-   <span data-ttu-id="fb065-428">**以命令式方向或特定問題的形式表達主要指令。**</span><span class="sxs-lookup"><span data-stu-id="fb065-428">**Express the main instruction in the form of an imperative direction or specific question.**</span></span>

    <span data-ttu-id="fb065-429">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-429">**Incorrect:**</span></span>

    ![<span data-ttu-id="fb065-430">程式名稱的螢幕擷取畫面，作為主要指示</span><span class="sxs-lookup"><span data-stu-id="fb065-430">screen shot of program name as main instruction</span></span> ](images/text-ui-image34.png)

    <span data-ttu-id="fb065-431">在此範例中，main 指令只會指出程式的名稱;它不會明確邀請使用者採取動作。</span><span class="sxs-lookup"><span data-stu-id="fb065-431">In this example, the main instruction simply states the name of the program; it doesn't explicitly invite a course of action for the user to take.</span></span>

    <span data-ttu-id="fb065-432">**例外狀況：** 錯誤訊息、警告訊息和確認可能會在其主要指示中使用不同的句子結構。</span><span class="sxs-lookup"><span data-stu-id="fb065-432">**Exceptions:** Error messages, warning messages, and confirmations may use different sentence structures in their main instructions.</span></span>

-   <span data-ttu-id="fb065-433">**盡可能使用特定動詞。**</span><span class="sxs-lookup"><span data-stu-id="fb065-433">**Use specific verbs whenever possible.**</span></span> <span data-ttu-id="fb065-434">特定動詞 (範例： [連接]、[儲存]、[安裝) 比一般使用者更有意義， (範例：設定、管理、設定) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-434">Specific verbs (examples: connect, save, install) are more meaningful to users than generic ones (examples: configure, manage, set).</span></span>
    -   <span data-ttu-id="fb065-435">針對 [控制台] 頁面和 [wizard] 頁面，如果您無法使用特定的動詞，您可能會想要完全省略動詞。</span><span class="sxs-lookup"><span data-stu-id="fb065-435">For control panel pages and wizard pages, if you can't use a specific verb, you may prefer to omit the verb completely.</span></span>

        <span data-ttu-id="fb065-436">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="fb065-436">**Acceptable:**</span></span>

        <span data-ttu-id="fb065-437">輸入您的地區設定、地區和語言</span><span class="sxs-lookup"><span data-stu-id="fb065-437">Enter your locale, region, and language</span></span>

        <span data-ttu-id="fb065-438">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="fb065-438">**Better:**</span></span>

        <span data-ttu-id="fb065-439">地區設定、地區和語言</span><span class="sxs-lookup"><span data-stu-id="fb065-439">Locale, region, and language</span></span>

    -   <span data-ttu-id="fb065-440">針對對話方塊（例如錯誤訊息和警告），請勿省略動詞。</span><span class="sxs-lookup"><span data-stu-id="fb065-440">For dialogs, such as error messages and warnings, don't omit the verb.</span></span>

-   <span data-ttu-id="fb065-441">如果新增它只會在 UI 的內容中重複或明顯，請不要覺得不必使用主要的指令文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-441">Don't feel obliged to use main instruction text if adding it would only be redundant or obvious from the context of the UI.</span></span>

    ![<span data-ttu-id="fb065-442">[另存新檔] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-442">screen shot of save as dialog box</span></span> ](images/text-ui-image35.png)

    <span data-ttu-id="fb065-443">在此範例中，UI 的內容已經非常清楚;不需要加入主要的指令文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-443">In this example, the context of the UI is already very clear; there is no need to add main instruction text.</span></span>

-   <span data-ttu-id="fb065-444">**請務必只使用單一的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="fb065-444">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="fb065-445">削減主要指示以瞭解基本資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-445">Pare the main instruction down to the essential information.</span></span> <span data-ttu-id="fb065-446">如果您必須進一步說明，請考慮使用補充指令。</span><span class="sxs-lookup"><span data-stu-id="fb065-446">If you must explain anything more, consider using a supplemental instruction.</span></span>
-   <span data-ttu-id="fb065-447">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="fb065-447">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="fb065-448">**如果指令是語句，則不包含最後句號。**</span><span class="sxs-lookup"><span data-stu-id="fb065-448">**Don't include final periods if the instruction is a statement.**</span></span> <span data-ttu-id="fb065-449">如果指令是問題，請包含最後一個問號。</span><span class="sxs-lookup"><span data-stu-id="fb065-449">If the instruction is a question, include a final question mark.</span></span>
-   <span data-ttu-id="fb065-450">在 **[進度] 對話方塊中，使用現在片語來簡短說明進行中的作業，** 並以省略號結尾。</span><span class="sxs-lookup"><span data-stu-id="fb065-450">**For progress dialogs, use a gerund phrase briefly explaining the operation in progress,** ending with an ellipsis.</span></span> <span data-ttu-id="fb065-451">範例：「列印您的圖片 ...」</span><span class="sxs-lookup"><span data-stu-id="fb065-451">Example: "Printing your pictures..."</span></span>
-   <span data-ttu-id="fb065-452">**秘訣：** 您可以在說明要如何使用視窗或頁面時，藉由想像您對朋友的看法來評估主要指示。</span><span class="sxs-lookup"><span data-stu-id="fb065-452">**Tip:** You can evaluate a main instruction by imagining what you would say to a friend when explaining what to do with the window or page.</span></span> <span data-ttu-id="fb065-453">如果回應主要指示的非自然、無用或麻煩，請重新修改指令。</span><span class="sxs-lookup"><span data-stu-id="fb065-453">If responding with the main instruction would be unnatural, unhelpful, or awkward, rework the instruction.</span></span>

<span data-ttu-id="fb065-454">如需詳細資訊，請參閱特定 UI 元件指導方針中的「主要指令」一節。</span><span class="sxs-lookup"><span data-stu-id="fb065-454">For more information, see the "Main instruction" section in the specific UI component guidelines.</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="fb065-455">補充指示</span><span class="sxs-lookup"><span data-stu-id="fb065-455">Supplemental instructions</span></span>

-   <span data-ttu-id="fb065-456">必要時，請 **使用補充指示來呈現有助於瞭解或使用視窗或頁面的其他資訊，** 例如：</span><span class="sxs-lookup"><span data-stu-id="fb065-456">When necessary, **use a supplemental instruction to present additional information helpful to understanding or using the window or page,** such as:</span></span>
    -   <span data-ttu-id="fb065-457">提供內容來說明視窗在程式或系統起始時，顯示的原因。</span><span class="sxs-lookup"><span data-stu-id="fb065-457">Providing context to explain why the window is being displayed if it is program or system initiated.</span></span>
    -   <span data-ttu-id="fb065-458">協助使用者決定如何處理主要指示的合格資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-458">Qualifying information that helps users decide how to act on the main instruction.</span></span>
    -   <span data-ttu-id="fb065-459">定義重要術語。</span><span class="sxs-lookup"><span data-stu-id="fb065-459">Defining important terminology.</span></span>
-   <span data-ttu-id="fb065-460">**如果不需要，請不要使用補充指令。**</span><span class="sxs-lookup"><span data-stu-id="fb065-460">**Don't use a supplemental instruction if one isn't necessary.**</span></span> <span data-ttu-id="fb065-461">如果您可以簡潔地進行，則偏好使用主要指示傳達所有專案。</span><span class="sxs-lookup"><span data-stu-id="fb065-461">Prefer to communicate everything with the main instruction if you can do so concisely.</span></span>
-   <span data-ttu-id="fb065-462">**請勿以稍微不同的用語重複主要指令。**</span><span class="sxs-lookup"><span data-stu-id="fb065-462">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="fb065-463">相反地，如果沒有其他專案要加入，請省略補充指令。</span><span class="sxs-lookup"><span data-stu-id="fb065-463">Instead, omit the supplemental instruction if there is nothing more to add.</span></span>
-   <span data-ttu-id="fb065-464">使用完整句子和句子樣式的大小寫。</span><span class="sxs-lookup"><span data-stu-id="fb065-464">Use complete sentences and sentence-style capitalization.</span></span>

### <a name="control-labels"></a><span data-ttu-id="fb065-465">控制項標籤</span><span class="sxs-lookup"><span data-stu-id="fb065-465">Control labels</span></span>

-   <span data-ttu-id="fb065-466">**為每個控制項或一組控制項加上標籤。異常：**</span><span class="sxs-lookup"><span data-stu-id="fb065-466">**Label every control or group of controls. Exceptions:**</span></span>
    -   <span data-ttu-id="fb065-467">您可以使用提示來標記文字方塊和下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="fb065-467">Text boxes and drop-down lists can be labeled using prompts.</span></span>
    -   <span data-ttu-id="fb065-468">漸進式洩漏控制項通常是未標記的。</span><span class="sxs-lookup"><span data-stu-id="fb065-468">Progressive disclosure controls are generally unlabeled.</span></span>
    -   <span data-ttu-id="fb065-469">**次級控制項使用其相關聯控制項的標籤。**</span><span class="sxs-lookup"><span data-stu-id="fb065-469">**Subordinate controls use the label of their associated control.**</span></span> <span data-ttu-id="fb065-470">微調控制項一律為從屬控制項。</span><span class="sxs-lookup"><span data-stu-id="fb065-470">Spin controls are always subordinate controls.</span></span>
    -   <span data-ttu-id="fb065-471">**省略重新聲明主要指令的控制項標籤。**</span><span class="sxs-lookup"><span data-stu-id="fb065-471">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="fb065-472">在此情況下，主要指令會採用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb065-472">In this case, the main instruction takes the access key.</span></span>

        <span data-ttu-id="fb065-473">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="fb065-473">**Acceptable:**</span></span>

        ![<span data-ttu-id="fb065-474">具有指令和標籤的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-474">screen shot of text box with instruction and label</span></span> ](images/text-ui-image36.png)

        <span data-ttu-id="fb065-475">在此範例中，文字方塊標籤只是主要指令的重述。</span><span class="sxs-lookup"><span data-stu-id="fb065-475">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="fb065-476">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="fb065-476">**Better:**</span></span>

        ![<span data-ttu-id="fb065-477">只有指示的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-477">screen shot of text box with instruction only</span></span> ](images/text-ui-image37.png)

        <span data-ttu-id="fb065-478">在此範例中，會移除多餘的標籤，所以主要指令會取得存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb065-478">In this example, the redundant label is removed, so the main instruction takes the access key.</span></span>

-   <span data-ttu-id="fb065-479">標籤位置：</span><span class="sxs-lookup"><span data-stu-id="fb065-479">Label placement:</span></span>
    -   <span data-ttu-id="fb065-480">文字提示、核取方塊、命令按鈕、群組方塊、連結、索引標籤和提示都會直接由控制項本身標記。</span><span class="sxs-lookup"><span data-stu-id="fb065-480">Balloons, check boxes, command buttons, group boxes, links, tabs, and tips are labeled directly by the control itself.</span></span>
    -   <span data-ttu-id="fb065-481">下拉式清單、清單方塊、清單視圖、進度列、滑杆、文字方塊和樹狀檢視會標記在上方、靠左或靠左對齊。</span><span class="sxs-lookup"><span data-stu-id="fb065-481">Drop-down lists, list boxes, list views, progress bars, sliders, text boxes, and tree views are labeled above, flush left, or to the left.</span></span>
    -   <span data-ttu-id="fb065-482">漸進式洩漏控制項通常是未標記的。</span><span class="sxs-lookup"><span data-stu-id="fb065-482">Progressive disclosure controls are usually unlabeled.</span></span> <span data-ttu-id="fb065-483">箭號按鈕會標示在右邊。</span><span class="sxs-lookup"><span data-stu-id="fb065-483">Chevron buttons are labeled to the right.</span></span>
-   <span data-ttu-id="fb065-484">為 **每個互動式控制項指派唯一的存取金鑰**，但連結除外。</span><span class="sxs-lookup"><span data-stu-id="fb065-484">**Assign a unique access key for each interactive control** except for links.</span></span> <span data-ttu-id="fb065-485">如需詳細資訊，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="fb065-485">For more information, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="fb065-486">**將標籤保持簡短。**</span><span class="sxs-lookup"><span data-stu-id="fb065-486">**Keep labels brief.**</span></span> <span data-ttu-id="fb065-487">不過，請注意，將一個或兩個字組新增至標籤有助於清楚起見，有時也不需要補充說明。</span><span class="sxs-lookup"><span data-stu-id="fb065-487">Note, however, that adding a word or two to a label can help clarity, and sometimes eliminates the need for supplemental explanations.</span></span>
-   <span data-ttu-id="fb065-488">**偏好泛型標籤上的特定標籤。**</span><span class="sxs-lookup"><span data-stu-id="fb065-488">**Prefer specific labels over generic ones.**</span></span> <span data-ttu-id="fb065-489">在理想的情況下，使用者不需要讀取任何其他人來瞭解標籤。</span><span class="sxs-lookup"><span data-stu-id="fb065-489">Ideally users shouldn't have to read anything else to understand the label.</span></span>

    <span data-ttu-id="fb065-490">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-490">**Incorrect:**</span></span>

    ![<span data-ttu-id="fb065-491">[確定] 命令按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-491">screen shot of ok command button</span></span> ](images/text-ui-image38.png)

    <span data-ttu-id="fb065-492">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-492">**Correct:**</span></span>

    ![<span data-ttu-id="fb065-493">[發行] 命令按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-493">screen shot of publish command button</span></span> ](images/text-ui-image39.png)

    <span data-ttu-id="fb065-494">在正確的範例中，會使用 [認可] 按鈕的特定標籤。</span><span class="sxs-lookup"><span data-stu-id="fb065-494">In the correct example, a specific label is used for the commit button.</span></span>

-   <span data-ttu-id="fb065-495">如需 **標籤清單（例如選項按鈕），請使用平行片語，** 並嘗試保留所有標籤的相同長度。</span><span class="sxs-lookup"><span data-stu-id="fb065-495">**For lists of labels, such as radio buttons, use parallel phrasing,** and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="fb065-496">**如需標籤的清單，請將標籤文字焦點放在選項之間的差異。**</span><span class="sxs-lookup"><span data-stu-id="fb065-496">**For lists of labels, focus the label text on the differences among the options.**</span></span> <span data-ttu-id="fb065-497">如果所有選項都有相同的簡介文字，請將該文字移至群組標籤。</span><span class="sxs-lookup"><span data-stu-id="fb065-497">If all the options have the same introductory text, move that text to the group label.</span></span>

    <span data-ttu-id="fb065-498">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-498">**Incorrect:**</span></span>

    ![具有重複的第一個片語之標籤的螢幕擷取畫面](images/text-ui-image40.png)

    <span data-ttu-id="fb065-500">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-500">**Correct:**</span></span>

    ![第一個片語移至群組標籤的螢幕擷取畫面](images/text-ui-image41.png)

    <span data-ttu-id="fb065-502">正確的範例會將相同的簡介片語移至標籤，因此這兩個選項的差異更明確。</span><span class="sxs-lookup"><span data-stu-id="fb065-502">The correct example moves the identical introductory phrasing to the label, so the two options are more cleanly differentiated.</span></span>

-   <span data-ttu-id="fb065-503">**一般情況下，建議使用正片語。**</span><span class="sxs-lookup"><span data-stu-id="fb065-503">**In general, prefer positive phrasing.**</span></span> <span data-ttu-id="fb065-504">例如，使用 do 而不是 [否]，而不會通知，而不是 [沒有通知]。</span><span class="sxs-lookup"><span data-stu-id="fb065-504">For example, use do instead of do not, and notify instead of do not notify.</span></span>
    -   <span data-ttu-id="fb065-505">**例外狀況：** 已廣泛使用 [不要再顯示此訊息] 核取方塊標籤。</span><span class="sxs-lookup"><span data-stu-id="fb065-505">**Exception:** The check box label, "Don't show this message again," is widely used.</span></span>
-   <span data-ttu-id="fb065-506">**省略套用至指定類型之所有控制項的指令動詞。**</span><span class="sxs-lookup"><span data-stu-id="fb065-506">**Omit instructional verbs that apply to all controls of the given type.**</span></span> <span data-ttu-id="fb065-507">相反地，會將焦點放在控制項的唯一相關標籤上。</span><span class="sxs-lookup"><span data-stu-id="fb065-507">Rather, focus labels on what is unique about the controls.</span></span> <span data-ttu-id="fb065-508">例如，它不會告訴使用者需要輸入文字方塊控制項，或是使用者必須按一下連結。</span><span class="sxs-lookup"><span data-stu-id="fb065-508">For example, it goes without saying that users need to type into a text box control or that users need to click a link.</span></span>

    <span data-ttu-id="fb065-509">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-509">**Incorrect:**</span></span>

    ![<span data-ttu-id="fb065-510">標籤的螢幕擷取畫面： [輸入您的名稱]</span><span class="sxs-lookup"><span data-stu-id="fb065-510">screen shot of label: 'type your name'</span></span> ](images/text-ui-image42.png)

    <span data-ttu-id="fb065-511">**正確：**</span><span class="sxs-lookup"><span data-stu-id="fb065-511">**Correct:**</span></span>

    ![<span data-ttu-id="fb065-512">標籤的螢幕擷取畫面： ' 您的名稱 '</span><span class="sxs-lookup"><span data-stu-id="fb065-512">screen shot of label: 'your name'</span></span> ](images/text-ui-image43.png)

    <span data-ttu-id="fb065-513">在不正確的範例中，控制項標籤具有適用于其型別之所有控制項的說明動詞。</span><span class="sxs-lookup"><span data-stu-id="fb065-513">In the incorrect examples, the control labels have instructional verbs that apply to all controls of their type.</span></span>

-   <span data-ttu-id="fb065-514">在某些情況下，控制標籤的下列括弧批註可能很有説明：</span><span class="sxs-lookup"><span data-stu-id="fb065-514">In some cases, the following parenthetical annotations to control labels may be helpful:</span></span>
    -   <span data-ttu-id="fb065-515">**如果選項是選擇性的，請考慮將「 (選擇性) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="fb065-515">**If an option is optional, consider adding "(optional)" to the label.**</span></span>
    -   <span data-ttu-id="fb065-516">**如果強烈建議選項，請將「 (建議的) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="fb065-516">**If an option is strongly recommended, add "(recommended)" to the label.**</span></span> <span data-ttu-id="fb065-517">這麼做表示設定是選擇性的，但仍應設定。</span><span class="sxs-lookup"><span data-stu-id="fb065-517">Doing so means the setting is optional, but should be set anyway.</span></span>
    -   <span data-ttu-id="fb065-518">**如果選項僅供 advanced 使用者使用，請考慮將「 (advanced) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="fb065-518">**If an option is intended only for advanced users, consider adding "(advanced)" to the label.**</span></span>
-   <span data-ttu-id="fb065-519">您可以在標籤後面的括弧中，指定單位 (秒、連接等) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-519">You may specify units (seconds, connections, and so on) in parenthesis after the label.</span></span>

    ![<span data-ttu-id="fb065-520">標籤的螢幕擷取畫面：初始大小 (mb) </span><span class="sxs-lookup"><span data-stu-id="fb065-520">screen shot of label: initial size (mb)</span></span> ](images/text-ui-image44.png)

    <span data-ttu-id="fb065-521">此範例顯示度量單位為 mb (MB) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-521">This example shows that the unit of measurement is megabytes (MB).</span></span>

<span data-ttu-id="fb065-522">如需詳細資訊，請參閱特定 UI 元件指導方針中的「文字」或「標籤」一節。</span><span class="sxs-lookup"><span data-stu-id="fb065-522">For more information, see the "Text" or "Labels" section in the specific UI component guidelines.</span></span>

### <a name="supplemental-explanations"></a><span data-ttu-id="fb065-523">補充說明</span><span class="sxs-lookup"><span data-stu-id="fb065-523">Supplemental explanations</span></span>

-   <span data-ttu-id="fb065-524">**當控制項所需的資訊超過其標籤可傳達的資訊時，請使用補充說明。**</span><span class="sxs-lookup"><span data-stu-id="fb065-524">**Use supplemental explanations when controls require more information than can be conveyed by their label.**</span></span> <span data-ttu-id="fb065-525">但是，如果您可以很簡潔地進行，請不要使用補充說明，如果您不想要將所有專案與控制項標籤進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-525">But don't use a supplemental explanation if one isn't necessary prefer to communicate everything with the control label if you can do so concisely.</span></span> <span data-ttu-id="fb065-526">通常，補充說明會搭配命令連結、選項按鈕和核取方塊使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-526">Typically, supplemental explanations are used with command links, radio buttons, and check boxes.</span></span>
-   <span data-ttu-id="fb065-527">必要時，請 **在控制項標籤中使用粗體，讓文字** 在有補充說明時更容易掃描。</span><span class="sxs-lookup"><span data-stu-id="fb065-527">When necessary, **use bold in the control labels to make the text easier to scan** when there are supplemental explanations.</span></span>

    ![<span data-ttu-id="fb065-528">[安全性-設定] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-528">screen shot of security-settings dialog box</span></span> ](images/text-ui-image45.png)

    <span data-ttu-id="fb065-529">在此範例中，選項按鈕標籤為粗體，可讓您更輕鬆地進行掃描。</span><span class="sxs-lookup"><span data-stu-id="fb065-529">In this example, the radio button labels are bold to make them easier to scan.</span></span>

-   <span data-ttu-id="fb065-530">**將補充說明新增至群組中的一個控制項，並不表示您必須為群組中的所有其他控制項提供說明。**</span><span class="sxs-lookup"><span data-stu-id="fb065-530">**Adding a supplemental explanation to one control in a group doesn't mean that you have to provide explanations for all the other controls in the group.**</span></span> <span data-ttu-id="fb065-531">如果您只有在必要時才可以和使用說明，請在標籤中提供相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fb065-531">Provide the relevant information in the label if you can and use explanations only when necessary.</span></span> <span data-ttu-id="fb065-532">沒有只重新聲明一致性標籤的補充說明。</span><span class="sxs-lookup"><span data-stu-id="fb065-532">Don't have supplemental explanations that merely restate the label for consistency.</span></span>

    ![<span data-ttu-id="fb065-533">三個選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="fb065-533">screen shot of three radio buttons</span></span> ](images/text-ui-image46.png)

    <span data-ttu-id="fb065-534">在此範例中，群組中的兩個控制項包含補充說明，但第三個則否。</span><span class="sxs-lookup"><span data-stu-id="fb065-534">In this example, two controls in the group include supplemental explanations, but the third does not.</span></span>

-   <span data-ttu-id="fb065-535">如果有補充說明，請在命令連結之後，以第二個人撰寫補充文字。</span><span class="sxs-lookup"><span data-stu-id="fb065-535">If a supplemental explanation follows a command link, write the supplemental text in second person.</span></span>

    <span data-ttu-id="fb065-536">**範例：** 命令連結：建立無線網路設定並儲存至 USB 快閃磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="fb065-536">**Example:** Command link: Create wireless network settings and save to USB flash drive</span></span>

    <span data-ttu-id="fb065-537">補充說明：這會建立您可以使用 USB 快閃磁片磁碟機傳送至路由器的設定。</span><span class="sxs-lookup"><span data-stu-id="fb065-537">Supplemental explanation: This will create settings that you can transfer to the router with a USB flash drive.</span></span> <span data-ttu-id="fb065-538">只有當您有支援 USB 快閃磁片磁碟機設定的無線路由器時，才需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="fb065-538">Do this only if you have a wireless router that supports USB flash drive configuration.</span></span>

-   <span data-ttu-id="fb065-539">使用完整的句子和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="fb065-539">Use complete sentences and ending punctuation.</span></span>

### <a name="commit-button-labels"></a><span data-ttu-id="fb065-540">認可按鈕標籤</span><span class="sxs-lookup"><span data-stu-id="fb065-540">Commit button labels</span></span>

<span data-ttu-id="fb065-541">下表顯示最常見的認可按鈕標籤和其使用方式。</span><span class="sxs-lookup"><span data-stu-id="fb065-541">The following table shows the most common commit button labels and their usage.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb065-542"><strong>按鈕標籤</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-542"><strong>Button label</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-543"><strong>意義</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-543"><strong>Meaning</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-544"><strong>使用時機</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-544"><strong>When to use</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-545"><strong>存取金鑰</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-545"><strong>Access key</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb065-546"><strong>確定</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-546"><strong>OK</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-547">在對話方塊中：將變更或認可套用至工作，然後關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-547">In dialog boxes: apply the changes or commit to the task and close the window.</span></span></li>
<li><span data-ttu-id="fb065-548">在 [擁有者] 屬性視窗中：套用自視窗開啟後 (所做的暫止變更，或上次套用) 並關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-548">In owner property windows: apply the pending changes (made since the window was opened or the last Apply) and close the window.</span></span></li>
<li><span data-ttu-id="fb065-549">在 [擁有的屬性] 視窗中：保留變更、關閉視窗，並在套用主控視窗的變更時套用變更。</span><span class="sxs-lookup"><span data-stu-id="fb065-549">In owned property windows: keep the changes, close the window, and apply the changes when the owner window's changes are applied.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fb065-550">使用不是特定工作的 windows，例如屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="fb065-550">Use with windows that aren't task specific, such as property sheets.</span></span></li>
<li><span data-ttu-id="fb065-551">針對用來執行一項特定工作的 windows，請使用特定標籤，而不是以動詞 (範例： Print) 。</span><span class="sxs-lookup"><span data-stu-id="fb065-551">For windows used to perform one specific task, use a specific label instead that starts with a verb (example: Print).</span></span></li>
<li><span data-ttu-id="fb065-552">對於使用者無法進行變更的 windows，請使用 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="fb065-552">For windows in which users can't make changes, use Close.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-553">Enter</span><span class="sxs-lookup"><span data-stu-id="fb065-553">Enter</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb065-554"><strong>是/否</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-554"><strong>Yes/No</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-555">[是] 是 [是] 或 [否] 問題的肯定回應，而不是負回應。</span><span class="sxs-lookup"><span data-stu-id="fb065-555">Yes is the affirmative response to a yes or no question, whereas No is the negative response.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-556">請使用 [是] 和 [無] 按鈕來回應是或沒有任何問題。</span><span class="sxs-lookup"><span data-stu-id="fb065-556">Use Yes and No buttons only to respond to yes or no questions.</span></span> <span data-ttu-id="fb065-557">請勿使用 [確定] 並取消 [是] 或 [否]。</span><span class="sxs-lookup"><span data-stu-id="fb065-557">Never use OK and Cancel for yes or no questions.</span></span></li>
<li><span data-ttu-id="fb065-558">偏好具有 [是] 和 [否] 按鈕的特定回應。</span><span class="sxs-lookup"><span data-stu-id="fb065-558">Prefer specific responses over Yes and No buttons.</span></span> <span data-ttu-id="fb065-559">雖然使用 [是] 和 [否] 並沒有任何問題，但可以更快速地瞭解特定的回應，進而做出有效率的決策。</span><span class="sxs-lookup"><span data-stu-id="fb065-559">While there's nothing wrong with using Yes and No, specific responses can be understood more quickly, resulting in efficient decision making.</span></span></li>
<li><span data-ttu-id="fb065-560">但是，如果特定回應的措辭很長或更難使用，請考慮使用 Yes 和 No 回應。</span><span class="sxs-lookup"><span data-stu-id="fb065-560">However, consider using Yes and No responses if the phrasing of specific responses turns out to be long or awkward.</span></span></li>
<li><span data-ttu-id="fb065-561">如果沒有回應的意義不清楚，請不要使用 [是] 和 [否] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fb065-561">Don't use Yes and No buttons if the meaning of the No response is unclear.</span></span> <span data-ttu-id="fb065-562">若是如此，請改用特定回應。</span><span class="sxs-lookup"><span data-stu-id="fb065-562">If so, use specific responses instead.</span></span></li>
<li><span data-ttu-id="fb065-563">是，而不一定要用成對的。</span><span class="sxs-lookup"><span data-stu-id="fb065-563">Yes and No must always be used as a pair.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-564">Y 和 N</span><span class="sxs-lookup"><span data-stu-id="fb065-564">Y and N</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb065-565"><strong>取消</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-565"><strong>Cancel</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-566">在對話方塊中：捨棄所有變更或進行中的工作、還原為先前的狀態 (不會有明顯的副作用) ，然後關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-566">In dialog boxes: discard all changes or work in progress, revert to the previous state (leaving no noticeable side effect), and close the window.</span></span></li>
<li><span data-ttu-id="fb065-567">在 [屬性工作表：] 中，捨棄開啟視窗之後 (所做的所有暫止變更，或上次套用) 並關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-567">In property sheets: discard all pending changes (made since the window was opened or the last Apply) and close the window.</span></span></li>
<li><span data-ttu-id="fb065-568">在 [控制台專案] 中：捨棄所有變更或進行中的工作、還原為先前的狀態，然後返回啟動工作的中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="fb065-568">In control panel items: discard all changes or work in progress, revert to the previous state, and return to the hub page from which the task was launched.</span></span> <span data-ttu-id="fb065-569">如果沒有這類中樞頁面，請改為關閉 [控制台專案] 視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-569">If there is no such hub page, close the control panel item window instead.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fb065-570">當所有暫止的變更或動作都可以捨棄，且任何副作用都可以復原時使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-570">Use when all pending changes or actions can be discarded and any side effects can be undone.</span></span></li>
<li><span data-ttu-id="fb065-571">針對無法捨棄的變更，請使用 Close。</span><span class="sxs-lookup"><span data-stu-id="fb065-571">For changes that can't be discarded, use Close.</span></span> <span data-ttu-id="fb065-572">若為可停止的動作，請使用 [停止]。</span><span class="sxs-lookup"><span data-stu-id="fb065-572">For actions in progress that can be stopped, use Stop.</span></span> <span data-ttu-id="fb065-573">如果一開始可以捨棄變更或動作，您可以先使用 [取消]，然後在無法復原之後變更為關閉或停止。</span><span class="sxs-lookup"><span data-stu-id="fb065-573">If initially changes or actions can be discarded, you can use Cancel initially then change to Close or Stop once it can't be undone.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-574">Esc</span><span class="sxs-lookup"><span data-stu-id="fb065-574">Esc</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb065-575"><strong>關閉</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-575"><strong>Close</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-576">關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-576">Close the window.</span></span> <span data-ttu-id="fb065-577">不會捨棄任何變更或副作用。</span><span class="sxs-lookup"><span data-stu-id="fb065-577">Any changes or side effects are not discarded.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-578">當無法捨棄變更或副作用時使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-578">Use when changes or side effects can't be discarded.</span></span> <span data-ttu-id="fb065-579">針對主要視窗使用 [關閉] 而非 [取消]。</span><span class="sxs-lookup"><span data-stu-id="fb065-579">Use Close instead of Cancel for primary windows.</span></span></li>
<li><span data-ttu-id="fb065-580">用於使用者無法進行變更的 windows。</span><span class="sxs-lookup"><span data-stu-id="fb065-580">Use for windows in which users can't make changes.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-581">Alt + F4、Ctrl + F4</span><span class="sxs-lookup"><span data-stu-id="fb065-581">Alt+F4, Ctrl+F4</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb065-582"><strong>停止</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-582"><strong>Stop</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-583">停止目前正在執行的工作並關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-583">Stop a currently running task and close the window.</span></span> <span data-ttu-id="fb065-584">任何正在進行或副作用的工作都不會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="fb065-584">Any work in progress or side effects are not discarded.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-585">當進行中的工作和任何副作用都不會被捨棄（通常是使用進度列或動畫）時，請使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-585">Use when work in progress and any side effects can't or won't be discarded, typically with progress bars or animations.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-586">Esc</span><span class="sxs-lookup"><span data-stu-id="fb065-586">Esc</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb065-587"><strong>套用</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-587"><strong>Apply</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-588">在 [擁有者] 屬性工作表中：套用自視窗開啟後 (所做的暫止變更，或上次套用) ，但讓視窗保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="fb065-588">In owner property sheets: apply the pending changes (made since the window was opened or the last Apply), but leave the window open.</span></span> <span data-ttu-id="fb065-589">這麼做可讓使用者在關閉屬性工作表之前評估變更。</span><span class="sxs-lookup"><span data-stu-id="fb065-589">Doing so allows users to evaluate the changes before closing the property sheet.</span></span> <span data-ttu-id="fb065-590">在擁有的屬性工作表中：不使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-590">In owned property sheets: don't use.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-591">只在屬性工作表中使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-591">Use only in property sheets.</span></span></li>
<li><span data-ttu-id="fb065-592">只有當屬性工作表的設定 (至少一個) 具有使用者可透過有意義的方式評估的效果時，才提供 [套用] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fb065-592">Provide an Apply button only if the property sheet has settings (at least one) with effects that users can evaluate in a meaningful way.</span></span> <span data-ttu-id="fb065-593">一般情況下，[套用] 按鈕會在設定進行可見變更時使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-593">Typically, Apply buttons are used when settings make visible changes.</span></span> <span data-ttu-id="fb065-594">使用者應該能夠套用變更、評估變更，然後根據該評估進行進一步的變更。</span><span class="sxs-lookup"><span data-stu-id="fb065-594">Users should be able to apply a change, evaluate the change, and make further changes based on that evaluation.</span></span> <span data-ttu-id="fb065-595">如果沒有，請移除 [套用] 按鈕，而不要停用它。</span><span class="sxs-lookup"><span data-stu-id="fb065-595">If not, remove the Apply button instead of disabling it.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-596">A</span><span class="sxs-lookup"><span data-stu-id="fb065-596">A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb065-597"><strong>下一步</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-597"><strong>Next</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-598">在 [嚮導] 和 [多步驟工作] 中：前進至下一個步驟，而不需要認可工作。</span><span class="sxs-lookup"><span data-stu-id="fb065-598">In wizards and multi-step tasks: advance to the next step without committing to the task.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-599">只有在嚮導和多步驟工作中使用，才能前進到下一個步驟而不做任何承諾。</span><span class="sxs-lookup"><span data-stu-id="fb065-599">Use only in wizards and multi-step tasks to advance to the next step without commitment.</span></span></li>
<li><span data-ttu-id="fb065-600">您可以按一下 [上一步]，隨時復原 [下一步] 按鈕的效果。</span><span class="sxs-lookup"><span data-stu-id="fb065-600">The effect of a Next button can always be undone by clicking Back.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-601">N</span><span class="sxs-lookup"><span data-stu-id="fb065-601">N</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb065-602"><strong>[完成]</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-602"><strong>Finish</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-603">在 [嚮導] 和 [多步驟工作] 中：關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="fb065-603">In wizards and multi-step tasks: close the window.</span></span> <span data-ttu-id="fb065-604">如果尚未執行此工作，請執行此工作。</span><span class="sxs-lookup"><span data-stu-id="fb065-604">If the task hasn't been performed yet, perform the task.</span></span> <span data-ttu-id="fb065-605">如果已執行該工作，則不會捨棄任何變更或副作用。</span><span class="sxs-lookup"><span data-stu-id="fb065-605">If that task has already been performed, any changes or side effects are not discarded.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-606">只使用於嚮導和多步驟工作。</span><span class="sxs-lookup"><span data-stu-id="fb065-606">Use only in wizards and multi-step tasks.</span></span> <span data-ttu-id="fb065-607">但是，不建議使用 [完成]，因為通常會有更明確、更明確的 [認可] 按鈕：</span><span class="sxs-lookup"><span data-stu-id="fb065-607">However, the use of Finish is discouraged because there is usually a better, more specific commit button:</span></span>
<ul>
<li><span data-ttu-id="fb065-608">如果按一下 [對工作的認可] 按鈕 (所以尚未執行此工作) ，請使用以動詞開頭的特定標籤 (範例： [列印]、[連接]、[開始) ] 作為主要指示的回應。</span><span class="sxs-lookup"><span data-stu-id="fb065-608">If clicking the button commits to the task (so the task hasn't already been performed), use a specific label that starts with a verb (examples: Print, Connect, Start) that is a response to the main instruction.</span></span></li>
<li><span data-ttu-id="fb065-609">如果已在嚮導內執行此工作，請改用 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="fb065-609">If the task has already been performed within the wizard, use Close instead.</span></span></li>
</ul></li>
<li><span data-ttu-id="fb065-610">不過，您可以在下列情況下使用 Finish：</span><span class="sxs-lookup"><span data-stu-id="fb065-610">However, you can use Finish when:</span></span>
<ul>
<li><span data-ttu-id="fb065-611">特定標籤仍然是泛型，例如 Save、Select、Choose 或 Get。</span><span class="sxs-lookup"><span data-stu-id="fb065-611">The specific label is still generic, such as Save, Select, Choose, or Get.</span></span></li>
<li><span data-ttu-id="fb065-612">工作牽涉到變更設定或設定集合。</span><span class="sxs-lookup"><span data-stu-id="fb065-612">The task involves changing a setting or collection of settings.</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="fb065-613">Enter</span><span class="sxs-lookup"><span data-stu-id="fb065-613">Enter</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb065-614"><strong>完成</strong></span><span class="sxs-lookup"><span data-stu-id="fb065-614"><strong>Done</strong></span></span><br/></td>
<td><span data-ttu-id="fb065-615">不適用。</span><span class="sxs-lookup"><span data-stu-id="fb065-615">Not applicable.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="fb065-616">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="fb065-616">Don't use.</span></span> <span data-ttu-id="fb065-617">以命令語法不正確的方式完成。</span><span class="sxs-lookup"><span data-stu-id="fb065-617">Done as a command is grammatically incorrect.</span></span></li>
</ul></td>
<td><span data-ttu-id="fb065-618">不適用。</span><span class="sxs-lookup"><span data-stu-id="fb065-618">Not applicable.</span></span><br/></td>
</tr>
</tbody>
</table>



 

