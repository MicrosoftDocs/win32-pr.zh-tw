---
title: 標準圖示
description: 標準圖示是 Windows 中的錯誤、警告、資訊和問號圖示。
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 69085f4c527db8431b5e33f0dba4668d43d1c669
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321399"
---
# <a name="standard-icons"></a><span data-ttu-id="4c6a9-103">標準圖示</span><span class="sxs-lookup"><span data-stu-id="4c6a9-103">Standard Icons</span></span>

> [!NOTE]
> <span data-ttu-id="4c6a9-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="4c6a9-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="4c6a9-106">標準圖示是 Windows 中的錯誤、警告、資訊和問號圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-106">Standard icons are the error, warning, information, and question mark icons that are part of Windows.</span></span>

![<span data-ttu-id="4c6a9-107">四個標準圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-107">screen shot of four standard icons</span></span> ](images/vis-std-icons-image1.png)

<span data-ttu-id="4c6a9-108">標準錯誤、警告、資訊和問號圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-108">The standard error, warning, information, and question mark icons.</span></span>

<span data-ttu-id="4c6a9-109">標準圖示具有下列意義：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-109">The standard icons have these meanings:</span></span>

-   <span data-ttu-id="4c6a9-110">**錯誤圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-110">**Error icon.**</span></span> <span data-ttu-id="4c6a9-111">使用者介面 (UI) 正在呈現發生的錯誤或問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-111">The user interface (UI) is presenting an error or problem that has occurred.</span></span>
-   <span data-ttu-id="4c6a9-112">**警告圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-112">**Warning icon.**</span></span> <span data-ttu-id="4c6a9-113">UI 正在呈現可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-113">The UI is presenting a condition that might cause a problem in the future.</span></span>
-   <span data-ttu-id="4c6a9-114">**資訊圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-114">**Information icon.**</span></span> <span data-ttu-id="4c6a9-115">UI 會呈現有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-115">The UI is presenting useful information.</span></span>
-   <span data-ttu-id="4c6a9-116">**問號圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-116">**Question mark icon.**</span></span> <span data-ttu-id="4c6a9-117">UI 表示說明進入點。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-117">The UI indicates a Help entry point.</span></span>

<span data-ttu-id="4c6a9-118">標準圖示很值得注意，因為它們內建在許多 Windows 應用程式開發介面中， (Api) ，例如工作 [對話方塊](win-dialog-box.md)、 [訊息方塊](glossary.md)、 [氣球](ctrl-balloons.md)和 [通知](mess-notif.md)。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-118">The standard icons are notable because they are built into many Windows application programming interfaces (APIs), such as [task dialogs](win-dialog-box.md), [message boxes](glossary.md), [balloons](ctrl-balloons.md), and [notifications](mess-notif.md).</span></span> <span data-ttu-id="4c6a9-119">它們也經常用於就地 [訊息](glossary.md) 和 [狀態列](ctrl-status-bars.md)。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-119">They are also commonly used on [in-place messages](glossary.md) and [status bars](ctrl-status-bars.md).</span></span>

<span data-ttu-id="4c6a9-120">**注意：** 與 [圖示](vis-icons.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-120">**Note:** Guidelines related to [icons](vis-icons.md) are presented in a separate article.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="4c6a9-121">設計概念</span><span class="sxs-lookup"><span data-stu-id="4c6a9-121">Design concepts</span></span>

<span data-ttu-id="4c6a9-122">選擇適當的標準圖示時，有幾個因素，其中部分說明為何通常會不正確地使用它們。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-122">There are several factors in choosing the appropriate standard icon which in part explains why they are so often used incorrectly.</span></span> <span data-ttu-id="4c6a9-123">最常見的錯誤是：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-123">The most common mistakes are:</span></span>

-   <span data-ttu-id="4c6a9-124">針對次要錯誤使用警告圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-124">Using a warning icon for minor errors.</span></span> <span data-ttu-id="4c6a9-125">警告不是「晚年」錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-125">Warnings are not "softened" errors.</span></span>
-   <span data-ttu-id="4c6a9-126">使用標準圖示時，最好不要使用任何圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-126">Using a standard icon when it is better to use no icon at all.</span></span> <span data-ttu-id="4c6a9-127">並非每個訊息都需要圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-127">Not every message needs an icon.</span></span>
-   <span data-ttu-id="4c6a9-128">藉由提供小問題的警告，或以警告的形式呈現常式問題，來為使用者發出警示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-128">Alarming users by giving warnings for minor issues or presenting routine questions as warnings.</span></span> <span data-ttu-id="4c6a9-129">這樣做會讓程式變得更容易遭受風險，並且從真正的重大問題會使。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-129">Doing so makes programs appear prone to hazard, and detracts from truly significant issues.</span></span>

<span data-ttu-id="4c6a9-130">本節的其餘部分將說明如何考慮標準圖示，以避免這些常見的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-130">The remainder of this section explains how to think about standard icons in order to avoid these common mistakes.</span></span>

### <a name="message-type-vs-severity"></a><span data-ttu-id="4c6a9-131">訊息類型與嚴重性</span><span class="sxs-lookup"><span data-stu-id="4c6a9-131">Message type vs. severity</span></span>

<span data-ttu-id="4c6a9-132">選擇以訊息類型為基礎的標準圖示，而不是基礎問題的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-132">Choose standard icons based the message type, not the severity of the underlying issue.</span></span> <span data-ttu-id="4c6a9-133">訊息類型為：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-133">The message types are:</span></span>

-   <span data-ttu-id="4c6a9-134">**錯誤。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-134">**Error.**</span></span> <span data-ttu-id="4c6a9-135">發生的錯誤或問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-135">An error or problem that has occurred.</span></span>
-   <span data-ttu-id="4c6a9-136">**警告。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-136">**Warning.**</span></span> <span data-ttu-id="4c6a9-137">可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-137">A condition that might cause a problem in the future.</span></span>
-   <span data-ttu-id="4c6a9-138">**資訊。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-138">**Information.**</span></span> <span data-ttu-id="4c6a9-139">有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-139">Useful information.</span></span>

<span data-ttu-id="4c6a9-140">因此，錯誤訊息可能會出現錯誤圖示，但永遠不會出現警告圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-140">Consequently, an error message might take an error icon but never a warning icon.</span></span> <span data-ttu-id="4c6a9-141">請勿使用警告圖示作為「柔化」次要錯誤的一種方式。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-141">Don't use warning icons as a way to "soften" minor errors.</span></span> <span data-ttu-id="4c6a9-142">儘管如此，雖然它們的嚴重性有所差異，但是「不正確的字型大小」是一項錯誤，而「繼續進行這項作業將會設定您的房屋」是一項警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-142">So despite their difference in severity, "Incorrect font size" is an error, whereas "Continuing with this operation will set your house on fire" is a warning.</span></span>

### <a name="determining-the-appropriate-message-type"></a><span data-ttu-id="4c6a9-143">判斷適當的訊息類型</span><span class="sxs-lookup"><span data-stu-id="4c6a9-143">Determining the appropriate message type</span></span>

<span data-ttu-id="4c6a9-144">根據強調和措辭，某些問題可能會顯示為錯誤、警告或資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-144">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="4c6a9-145">例如，假設網頁無法根據目前的 Windows Internet Explorer 設定載入未簽署的 ActiveX 控制項：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-145">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="4c6a9-146">**錯誤。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-146">**Error.**</span></span> <span data-ttu-id="4c6a9-147">「此頁面無法載入未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="4c6a9-147">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="4c6a9-148"> (片語做為現有的問題。 ) </span><span class="sxs-lookup"><span data-stu-id="4c6a9-148">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="4c6a9-149">**警告。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-149">**Warning.**</span></span> <span data-ttu-id="4c6a9-150">「此頁面可能無法如預期般運作，因為 Windows Internet Explorer 未設定為載入未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="4c6a9-150">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="4c6a9-151">或「允許此頁面安裝未簽署的 ActiveX 控制項？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-151">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="4c6a9-152">從不受信任的來源執行此動作可能會危害您的電腦。」</span><span class="sxs-lookup"><span data-stu-id="4c6a9-152">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="4c6a9-153"> (這兩個片語為可能會導致未來問題的狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="4c6a9-153">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="4c6a9-154">**資訊。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-154">**Information.**</span></span> <span data-ttu-id="4c6a9-155">「您已設定 Windows Internet Explorer 封鎖未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="4c6a9-155">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="4c6a9-156"> (片語作為事實的陳述。 ) </span><span class="sxs-lookup"><span data-stu-id="4c6a9-156">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="4c6a9-157">**若要判斷適當的訊息類型，請將焦點放在使用者需要知道或採取行動之問題的最重要層面。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-157">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="4c6a9-158">一般來說，如果問題封鎖使用者繼續進行，則會顯示為錯誤。如果使用者可以繼續，則會出現警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-158">Typically, if an issue blocks the user from proceeding, it is presented as an error; if the user can proceed, it's a warning.</span></span> <span data-ttu-id="4c6a9-159">根據焦點製作 [主要指示](text-ui.md) 或其他對應的文字，然後選擇符合文字的圖示 (標準或) 。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-159">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, and then choose an icon (standard or otherwise) that matches the text.</span></span> <span data-ttu-id="4c6a9-160">主要的指令文字和圖示應該一律相符。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-160">The main instruction text and icons should always match.</span></span>

### <a name="severity"></a><span data-ttu-id="4c6a9-161">嚴重性</span><span class="sxs-lookup"><span data-stu-id="4c6a9-161">Severity</span></span>

<span data-ttu-id="4c6a9-162">雖然在錯誤、警告和資訊圖示之間選擇時，嚴重性並不是考慮的，但 **嚴重性是決定是否應該使用標準圖示的一項因素。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-162">While severity isn't a consideration when choosing among the error, warning, and information icons, **severity is a factor in determining if a standard icon should be used at all.**</span></span>

<span data-ttu-id="4c6a9-163">圖示最適合用來以視覺化方式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-163">Icons work best when used to communicate visually.</span></span> <span data-ttu-id="4c6a9-164"> (請注意，基於協助工具的考慮，此視覺效果的通訊必須永遠與另一個表單（例如文字或音效）重複。 ) 使用者應該能夠一目了然資訊的本質及其回應的結果，因此我們必須區分重大錯誤和警告與其一般的對應專案。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-164">(Note that for accessibility reasons, this visual communication must always be redundant with another form, such as text or sound.) Users should be able to tell at a glance the nature of the information and the consequences of their response, so we must differentiate critical errors and warnings from their ordinary counterparts.</span></span> <span data-ttu-id="4c6a9-165">重大錯誤和警告有下列特性：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-165">Critical errors and warnings have these characteristics:</span></span>

-   <span data-ttu-id="4c6a9-166">它們牽涉到可能遺失下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-166">They involve potential loss of one or more of the following:</span></span>
    -   <span data-ttu-id="4c6a9-167">有價值的資產，例如資料遺失或財務損失。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-167">A valuable asset, such as data loss or financial loss.</span></span>
    -   <span data-ttu-id="4c6a9-168">系統存取或完整性。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-168">System access or integrity.</span></span>
    -   <span data-ttu-id="4c6a9-169">隱私權或對機密資訊的控制。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-169">Privacy or control over confidential information.</span></span>
    -   <span data-ttu-id="4c6a9-170">使用者的時間 (大量的時間，例如30秒或更多的) 。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-170">User's time (a significant amount, such as 30 seconds or more).</span></span>
-   <span data-ttu-id="4c6a9-171">它們有非預期或非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-171">They have unexpected or unintended consequences.</span></span>
-   <span data-ttu-id="4c6a9-172">它們現在需要正確的處理，因為錯誤無法輕易地修正，甚至可能無法復原。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-172">They require correct handling now, because mistakes can't be easily fixed and may even be irreversible.</span></span>

<span data-ttu-id="4c6a9-173">若要區分非重大錯誤和警告和嚴重錯誤，通常會顯示非關鍵性的訊息，而不會有圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-173">To distinguish non-critical errors and warnings from critical ones, non-critical messages are usually displayed without an icon.</span></span> <span data-ttu-id="4c6a9-174">這麼做會將重點放在重要的訊息，讓重要和非關鍵性的訊息以視覺化方式區分，並且與 [Windows 語氣](text-style-tone.md)一致。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-174">Doing so draws attention to critical messages, makes critical and non-critical messages visually distinct, and is consistent with the [Windows tone](text-style-tone.md).</span></span>

<span data-ttu-id="4c6a9-175">並非每個訊息都需要圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-175">Not every message needs an icon.</span></span> <span data-ttu-id="4c6a9-176">圖示不是裝飾訊息的方法。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-176">Icons are not a way to decorate messages.</span></span>

<span data-ttu-id="4c6a9-177">以下是重大警告的良好範例，因為它符合先前定義的特性。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-177">The following is a good example of a critical warning because it meets the previously defined characteristics.</span></span>

![<span data-ttu-id="4c6a9-178">用來備份資料的警告螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-178">screen shot of a warning to back up data</span></span> ](images/vis-std-icons-image2.png)

<span data-ttu-id="4c6a9-179">在此範例中，重大警告會警示使用者可能無法復原的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-179">In this example, a critical warning alerts users of potential irreversible data loss.</span></span>

<span data-ttu-id="4c6a9-180">不過，下一個範例並不重要，因為它可能是刻意的，且其結果很容易復原。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-180">However, the next example isn't critical because it is likely to be intentional and its results are easily undone.</span></span>

<span data-ttu-id="4c6a9-181">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-181">**Incorrect:**</span></span>

![<span data-ttu-id="4c6a9-182">有誤導的警告圖示使用的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-182">screen shot of a misleading use of a warning icon</span></span> ](images/vis-std-icons-image3.png)

<span data-ttu-id="4c6a9-183">在此範例中，這項 [確認](mess-confirm.md) 並不重要，因為它可能是刻意且很容易復原。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-183">In this example, this [confirmation](mess-confirm.md) isn't critical because it's likely to be intentional and easily undone.</span></span>

<span data-ttu-id="4c6a9-184">在一般的 UI 中，大部分的錯誤都與使用者輸入錯誤有關。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-184">In a typical UI, most errors relate to user input errors.</span></span> <span data-ttu-id="4c6a9-185">大部分的使用者輸入錯誤都不重要，因為它們很容易更正，而使用者必須更正這些錯誤才能繼續。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-185">Most user input errors aren't critical because they are easily corrected, and users must correct them before continuing.</span></span> <span data-ttu-id="4c6a9-186">此外，繪製太多錯誤的使用者錯誤，與 Windows 的語氣相反。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-186">Also, drawing too much attention to minor user mistakes is contrary to the Windows tone.</span></span> <span data-ttu-id="4c6a9-187">因此，通常會顯示次要使用者輸入錯誤，而不會出現錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-187">Consequently, minor user input errors are usually displayed without an error icon.</span></span> <span data-ttu-id="4c6a9-188">為了強化其非關鍵本質，我們將這些視為使用者輸入問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-188">To reinforce their non-critical nature, we refer to these as user input problems.</span></span>

![<span data-ttu-id="4c6a9-189">螢幕擷取畫面會通知使用者正確的輸入</span><span class="sxs-lookup"><span data-stu-id="4c6a9-189">screen shot informing users of correct input</span></span> ](images/vis-std-icons-image4.png)

<span data-ttu-id="4c6a9-190">在此範例中，這個次要的使用者輸入問題並不重要，因此在對話方塊中顯示時不需要圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-190">In this example, this minor user input problem isn't critical, so it doesn't need an icon when presented in a dialog box.</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="4c6a9-191">避免 overwarning</span><span class="sxs-lookup"><span data-stu-id="4c6a9-191">Avoid overwarning</span></span>

<span data-ttu-id="4c6a9-192">我們在 Windows 程式中 overwarn。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-192">We overwarn in Windows programs.</span></span> <span data-ttu-id="4c6a9-193">一般的 Windows 程式具有看似在所有位置的警告圖示，這是關於有意義的事物的警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-193">The typical Windows program has warning icons seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="4c6a9-194">在某些程式中，幾乎每個問題都會顯示為警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-194">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="4c6a9-195">Overwarning 讓程式感覺像是有害的活動，而且會使真正的重大問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-195">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="4c6a9-196">單獨可能遺失資料的可能性不足以呼叫警告圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-196">The mere potential for data loss alone is insufficient to call for a warning icon.</span></span> <span data-ttu-id="4c6a9-197">此外，任何非預期的結果都應該是非預期的或非預期的結果，而且不容易更正。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-197">Additionally, any undesirable results should be unexpected or unintended and not easily corrected.</span></span> <span data-ttu-id="4c6a9-198">否則，您可以將任何不正確回答的問題解釋為會導致某種資料遺失，並提出警告圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-198">Otherwise, just about any incorrectly answered question could be construed to result in data loss of some kind and merit a warning icon.</span></span>

<span data-ttu-id="4c6a9-199">若要將警告圖示聚焦在真正的重大問題上：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-199">To focus warning icons on truly critical issues:</span></span>

-   <span data-ttu-id="4c6a9-200">請確定問題有提高的使用者注意。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-200">Make sure that the issue warrants heightened user attention.</span></span> <span data-ttu-id="4c6a9-201">[例行確認](mess-confirm.md) 與問題不應出現警告圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-201">[Routine confirmations](mess-confirm.md) and questions shouldn't have warning icons.</span></span>
-   <span data-ttu-id="4c6a9-202">使用者是否有可能以不同的方式運作，因為出現警告圖示的結果？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-202">Are users likely to behave differently as a result of the warning icon?</span></span> <span data-ttu-id="4c6a9-203">使用者是否可能更仔細考慮決策？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-203">Are users likely to consider the decision more carefully?</span></span>

<span data-ttu-id="4c6a9-204">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-204">**Incorrect:**</span></span>

![<span data-ttu-id="4c6a9-205">使用非必要的警告圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-205">screen shot of warning icon used unnecessarily</span></span> ](images/vis-std-icons-image5.png)

<span data-ttu-id="4c6a9-206">在此範例中，使用者是否有可能因警告圖示而以不同的方式回答這個問題？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-206">In this example, are users likely to answer this question differently because of the warning icon?</span></span>

-   <span data-ttu-id="4c6a9-207">是否有一些重要的動作需要進行或決定？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-207">Is there some significant action to do or decision to make?</span></span> <span data-ttu-id="4c6a9-208">沒有動作的警告只會讓使用者感覺擇善固執。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-208">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="4c6a9-209">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-209">**Incorrect:**</span></span>

![<span data-ttu-id="4c6a9-210">用於提醒的警告圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-210">screen shot of warning icon used with reminder</span></span> ](images/vis-std-icons-image6.png)

<span data-ttu-id="4c6a9-211">為什麼此通知會出現警告？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-211">Why is this notification a warning?</span></span> <span data-ttu-id="4c6a9-212">使用者應該怎麼做 (在擔心) ？</span><span class="sxs-lookup"><span data-stu-id="4c6a9-212">What are users supposed to do (beside worry)?</span></span>

### <a name="context"></a><span data-ttu-id="4c6a9-213">Context</span><span class="sxs-lookup"><span data-stu-id="4c6a9-213">Context</span></span>

<span data-ttu-id="4c6a9-214">內容也是使用標準圖示的考慮，因為內容本身會傳達資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-214">Context is also a consideration in using standard icons because the context itself communicates information.</span></span> <span data-ttu-id="4c6a9-215">具體來說：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-215">Specifically:</span></span>

-   <span data-ttu-id="4c6a9-216">雖然對話方塊 (包括工作對話方塊和訊息方塊) 和通知不需要非嚴重錯誤的圖示，但就地錯誤一律需要錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-216">While dialog boxes (including task dialogs and message boxes) and notifications don't need icons for non-critical errors, in-place errors always need error icons.</span></span> <span data-ttu-id="4c6a9-217">否則，這類非強制回應的意見反應可能太容易忽略。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-217">Otherwise, such non-modal feedback would be too easy to overlook.</span></span>
-   <span data-ttu-id="4c6a9-218">就地警告一律需要警告圖示，以區別它們與一般文字。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-218">In-place warnings always need warning icons to distinguish them from regular text.</span></span>
-   <span data-ttu-id="4c6a9-219">對話方塊、通知和氣球不需要資訊圖示，因為它們清楚呈現資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-219">Dialog boxes, notifications, and balloons don't need information icons because they are clearly presenting information.</span></span> <span data-ttu-id="4c6a9-220">相反地，橫幅需要16x16 圖元資訊或其他圖示，因為這類非強制回應的意見反應可能太容易忽略。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-220">By contrast, banners need 16x16 pixel information or other icons because such non-modal feedback would be too easy to overlook.</span></span>

<span data-ttu-id="4c6a9-221">由於內容是圖示使用方式的重要因素，因此本文中的標準圖示指導方針會以其內容為依據。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-221">Because context is a significant factor in icon usage, the standard icon guidelines in this article are given in terms of their context.</span></span>

### <a name="evaluating-standard-icon-appropriateness"></a><span data-ttu-id="4c6a9-222">評估標準圖示」適當性</span><span class="sxs-lookup"><span data-stu-id="4c6a9-222">Evaluating standard icon appropriateness</span></span>

<span data-ttu-id="4c6a9-223">評估您的 UI 文字時，請一併閱讀任何標準圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-223">When evaluating your UI text, read any standard icons as well.</span></span> <span data-ttu-id="4c6a9-224">將錯誤圖示讀取為「錯誤！」、警告圖示為「警告，請務必小心！」，並將資訊圖示視為「注意！」。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-224">Read error icons as "error!", warning icons as "warning, be very careful here!", and information icons as "attention!".</span></span> <span data-ttu-id="4c6a9-225">然後繼續讀取剩餘的內容，例如主要指示、內容區域和認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-225">Then continue to read the remaining context, such as the main instruction, content area, and commit buttons.</span></span> <span data-ttu-id="4c6a9-226">請確定每個標準圖示的意義和語氣符合其內容的意義和語氣。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-226">Make sure the meaning and the tone of each standard icon matches the meaning and the tone of its context.</span></span> <span data-ttu-id="4c6a9-227">如果沒有，您發現問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-227">If they don't, you've found a problem.</span></span>

<span data-ttu-id="4c6a9-228">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-228">**If you do only one thing...**</span></span>

<span data-ttu-id="4c6a9-229">請確定每個標準圖示的意義和語氣符合其內容的意義和語氣。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-229">Make sure the meaning and the tone of each standard icon matches the meaning and the tone of its context.</span></span> <span data-ttu-id="4c6a9-230">如果不相符，請變更或移除圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-230">If they don't match, change or remove the icon.</span></span>

## <a name="guidelines"></a><span data-ttu-id="4c6a9-231">指導方針</span><span class="sxs-lookup"><span data-stu-id="4c6a9-231">Guidelines</span></span>

<span data-ttu-id="4c6a9-232">**注意：** 針對下列指導方針，「就地」表示在任何一般視窗介面上，例如在 [wizard]、[屬性工作表] 或 [控制台專案] 頁面的內容區域內。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-232">**Note:** For the following guidelines, "in-place" means on any normal window surface, such as within the content area of a wizard, property sheet, or control panel item page.</span></span>

### <a name="general"></a><span data-ttu-id="4c6a9-233">一般</span><span class="sxs-lookup"><span data-stu-id="4c6a9-233">General</span></span>

-   <span data-ttu-id="4c6a9-234">根據其訊息類型選擇標準圖示，而不是基礎問題的嚴重性：</span><span class="sxs-lookup"><span data-stu-id="4c6a9-234">Choose standard icons based their message type, not the severity of the underlying issue:</span></span>
    -   <span data-ttu-id="4c6a9-235">**錯誤。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-235">**Error.**</span></span> <span data-ttu-id="4c6a9-236">發生的錯誤或問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-236">An error or problem that has occurred.</span></span>
    -   <span data-ttu-id="4c6a9-237">**警告。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-237">**Warning.**</span></span> <span data-ttu-id="4c6a9-238">可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-238">A condition that might cause a problem in the future.</span></span>
    -   <span data-ttu-id="4c6a9-239">**資訊。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-239">**Information.**</span></span> <span data-ttu-id="4c6a9-240">有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-240">Useful information.</span></span>
-   <span data-ttu-id="4c6a9-241">如果問題跨越不同的訊息類型，請將焦點放在使用者需要採取行動的最重要層面。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-241">If an issue straddles different message types, focus on the most important aspect that users need to act on.</span></span>
-   <span data-ttu-id="4c6a9-242">圖示必須一律符合主要指示或其他對應的文字。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-242">Icons must always match the main instruction or other corresponding text.</span></span>

<span data-ttu-id="4c6a9-243">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-243">**Correct:**</span></span>

![<span data-ttu-id="4c6a9-244">錯誤文字所使用之錯誤圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-244">screen shot of error icon used with error text</span></span> ](images/vis-std-icons-image7.png)

<span data-ttu-id="4c6a9-245">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-245">**Incorrect:**</span></span>

![<span data-ttu-id="4c6a9-246">與錯誤文字一起使用的警告圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-246">screen shot of warning icon used with error text</span></span> ](images/vis-std-icons-image8.png)

<span data-ttu-id="4c6a9-247">在不正確的範例中，標準警告圖示與主要指令 (不相符，這會導致錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-247">In the incorrect example, the standard warning icon doesn't match the main instruction (which gives an error).</span></span>

### <a name="icon-size"></a><span data-ttu-id="4c6a9-248">圖示大小</span><span class="sxs-lookup"><span data-stu-id="4c6a9-248">Icon size</span></span>

-   <span data-ttu-id="4c6a9-249">**根據內容選擇標準圖示大小：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-249">**Choose the standard icon size based on the context:**</span></span>
  



    | <span data-ttu-id="4c6a9-250">Context</span><span class="sxs-lookup"><span data-stu-id="4c6a9-250">Context</span></span>                         | <span data-ttu-id="4c6a9-251">使用時機</span><span class="sxs-lookup"><span data-stu-id="4c6a9-251">When to use</span></span>                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | <span data-ttu-id="4c6a9-252">對話方塊</span><span class="sxs-lookup"><span data-stu-id="4c6a9-252">Dialog boxes</span></span><br/>  | <span data-ttu-id="4c6a9-253">將32x32 圖元用於內容區域圖示;適用于註腳區圖示的16x16 圖元。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-253">Use 32x32 pixel for content area icons; 16x16 pixel for footnote area icons.</span></span><br/> |
    | <span data-ttu-id="4c6a9-254">就地</span><span class="sxs-lookup"><span data-stu-id="4c6a9-254">In-place</span></span><br/>      | <span data-ttu-id="4c6a9-255">將32x32 圖元用於錯誤頁面;所有其他專案的16x16 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-255">Use 32x32 pixel for error pages; 16x16 pixel icons for all others.</span></span><br/>           |
    | <span data-ttu-id="4c6a9-256">通知</span><span class="sxs-lookup"><span data-stu-id="4c6a9-256">Notifications</span></span><br/> | <span data-ttu-id="4c6a9-257">使用16x16 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-257">Use 16x16 pixel icons.</span></span><br/>                                                       |
    | <span data-ttu-id="4c6a9-258">汽球</span><span class="sxs-lookup"><span data-stu-id="4c6a9-258">Balloons</span></span><br/>      | <span data-ttu-id="4c6a9-259">使用16x16 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-259">Use 16x16 pixel icons.</span></span><br/>                                                       |
    | <span data-ttu-id="4c6a9-260">橫幅</span><span class="sxs-lookup"><span data-stu-id="4c6a9-260">Banners</span></span><br/>       | <span data-ttu-id="4c6a9-261">使用16x16 圖元圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-261">Use 16x16 pixel icons.</span></span><br/>                                                       |



 

### <a name="error-icons"></a><span data-ttu-id="4c6a9-262">錯誤圖示</span><span class="sxs-lookup"><span data-stu-id="4c6a9-262">Error icons</span></span>

-   <span data-ttu-id="4c6a9-263">**只有在發生錯誤或問題時，才使用錯誤圖示：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-263">**Use error icons only when an error or a problem has occurred:**</span></span>



    | <span data-ttu-id="4c6a9-264">Context</span><span class="sxs-lookup"><span data-stu-id="4c6a9-264">Context</span></span>                           | <span data-ttu-id="4c6a9-265">使用時機</span><span class="sxs-lookup"><span data-stu-id="4c6a9-265">When to use</span></span>                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4c6a9-266">對話方塊</span><span class="sxs-lookup"><span data-stu-id="4c6a9-266">Dialog boxes</span></span><br/>    | <span data-ttu-id="4c6a9-267">僅用於重大錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-267">Use for critical errors only.</span></span> <span data-ttu-id="4c6a9-268"> (不會將標準圖示用於非嚴重錯誤。 ) </span><span class="sxs-lookup"><span data-stu-id="4c6a9-268">(don't use standard icons for non-critical errors.)</span></span> <br/> ![<span data-ttu-id="4c6a9-269">顯示錯誤圖示搭配錯誤訊息使用的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-269">Screenshot that shows the error icon used with error message</span></span> ](images/vis-std-icons-image9.png)<br/>                                              |
    | <span data-ttu-id="4c6a9-270">就地錯誤</span><span class="sxs-lookup"><span data-stu-id="4c6a9-270">In-place errors</span></span><br/> | <span data-ttu-id="4c6a9-271">用於所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-271">Use for all errors.</span></span> <br/> ![錯誤圖示的螢幕擷取畫面，與錯誤訊息一起使用。](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | <span data-ttu-id="4c6a9-273">通知</span><span class="sxs-lookup"><span data-stu-id="4c6a9-273">Notifications</span></span><br/>   | <span data-ttu-id="4c6a9-274">僅用於重大錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-274">Use for critical errors only.</span></span> <span data-ttu-id="4c6a9-275">[動作失敗](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx)的 (。 ) </span><span class="sxs-lookup"><span data-stu-id="4c6a9-275">(for [action failures](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx).)</span></span> <br/> <span data-ttu-id="4c6a9-276">![顯示與通知錯誤訊息一起使用之錯誤圖示的螢幕擷取畫面。](images/vis-std-icons-image11.png)</span><span class="sxs-lookup"><span data-stu-id="4c6a9-276">![Screenshot that shows an error icon used with a notification error message.](images/vis-std-icons-image11.png)</span></span><br/> |
    | <span data-ttu-id="4c6a9-277">汽球</span><span class="sxs-lookup"><span data-stu-id="4c6a9-277">Balloons</span></span><br/>        | <span data-ttu-id="4c6a9-278">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-278">Don't use.</span></span> <span data-ttu-id="4c6a9-279">不應針對嚴重錯誤使用氣球，也不需要針對非嚴重錯誤的錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-279">Balloons shouldn't be used for critical errors, and they don't need error icons for non-critical errors.</span></span><br/>                                                                                                               |
    | <span data-ttu-id="4c6a9-280">橫幅</span><span class="sxs-lookup"><span data-stu-id="4c6a9-280">Banners</span></span><br/>         | <span data-ttu-id="4c6a9-281">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-281">Don't use.</span></span> <span data-ttu-id="4c6a9-282">橫幅不應用於錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-282">Banners shouldn't be used for errors.</span></span><br/>                                                                                                                                                                                  |



 

-   <span data-ttu-id="4c6a9-283">一般而言，非關鍵性使用者輸入問題不需要錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-283">Generally, error icons aren't needed for non-critical user input problems.</span></span> <span data-ttu-id="4c6a9-284">不過，就地錯誤需要圖示，因為這類內容相關的意見反應可能太容易忽略。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-284">However, icons are needed for in-place errors, because otherwise such contextual feedback would be too easy to overlook.</span></span>
-   <span data-ttu-id="4c6a9-285">**針對工作對話方塊，請不要使用錯誤註腳圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-285">**For task dialogs, don't use error footnote icons.**</span></span> <span data-ttu-id="4c6a9-286">錯誤圖示必須只顯示在內容區域中。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-286">Error icons must be presented in the content area only.</span></span>

### <a name="warning-icons"></a><span data-ttu-id="4c6a9-287">警告圖示</span><span class="sxs-lookup"><span data-stu-id="4c6a9-287">Warning icons</span></span>

-   <span data-ttu-id="4c6a9-288">**只有在條件可能會在未來發生問題時，才使用警告圖示：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-288">**Use warning icons only when a condition might cause a problem in the future:**</span></span>



    | <span data-ttu-id="4c6a9-289">Context</span><span class="sxs-lookup"><span data-stu-id="4c6a9-289">Context</span></span>                             |  <span data-ttu-id="4c6a9-290">使用時機</span><span class="sxs-lookup"><span data-stu-id="4c6a9-290">When to use</span></span>                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4c6a9-291">對話方塊</span><span class="sxs-lookup"><span data-stu-id="4c6a9-291">Dialog boxes</span></span><br/>      | <span data-ttu-id="4c6a9-292">用於所有警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-292">Use for all warnings.</span></span> <br/> ![<span data-ttu-id="4c6a9-293">檔案名稱延伸模組變更的螢幕擷取畫面警告</span><span class="sxs-lookup"><span data-stu-id="4c6a9-293">screen shot warning of file-name extension change</span></span> ](images/vis-std-icons-image12.png)<br/>                                                   |
    | <span data-ttu-id="4c6a9-294">就地警告</span><span class="sxs-lookup"><span data-stu-id="4c6a9-294">In-place warnings</span></span><br/> | <span data-ttu-id="4c6a9-295">用來將文字識別為警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-295">Use to identify the text as a warning.</span></span> <br/> ![<span data-ttu-id="4c6a9-296">沒有足夠的可用空間之警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-296">screen shot of warning of not enough free space</span></span> ](images/vis-std-icons-image13.png)<br/>                                    |
    | <span data-ttu-id="4c6a9-297">通知</span><span class="sxs-lookup"><span data-stu-id="4c6a9-297">Notifications</span></span><br/>     | <span data-ttu-id="4c6a9-298">用於所有警告。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-298">Use for all warnings.</span></span> <span data-ttu-id="4c6a9-299">[非關鍵系統事件](glossary.md)的 (。 ) </span><span class="sxs-lookup"><span data-stu-id="4c6a9-299">(for [non-critical system events](glossary.md).)</span></span> <br/> <span data-ttu-id="4c6a9-300">![電力偏低警告通知的螢幕擷取畫面 ](images/vis-std-icons-image14.png)</span><span class="sxs-lookup"><span data-stu-id="4c6a9-300">![screen shot of low-battery warning notification ](images/vis-std-icons-image14.png)</span></span><br/> |
    | <span data-ttu-id="4c6a9-301">汽球</span><span class="sxs-lookup"><span data-stu-id="4c6a9-301">Balloons</span></span><br/>          | <span data-ttu-id="4c6a9-302">用於 [特殊條件](ctrl-balloons.md)。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-302">Use for [special conditions](ctrl-balloons.md).</span></span> <br/> <span data-ttu-id="4c6a9-303">![caps lock on 的氣球警告螢幕擷取畫面 ](images/vis-std-icons-image15.png)</span><span class="sxs-lookup"><span data-stu-id="4c6a9-303">![screen shot of balloon warning of caps lock on ](images/vis-std-icons-image15.png)</span></span><br/>                           |
    | <span data-ttu-id="4c6a9-304">橫幅</span><span class="sxs-lookup"><span data-stu-id="4c6a9-304">Banners</span></span><br/>           | <span data-ttu-id="4c6a9-305">用來吸引橫幅。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-305">Use to draw attention to the banner.</span></span> <br/> ![<span data-ttu-id="4c6a9-306">橫幅的螢幕擷取畫面，其中包含缺少 tpm 的警告</span><span class="sxs-lookup"><span data-stu-id="4c6a9-306">screen shot of banner with warning of missing tpm</span></span> ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   <span data-ttu-id="4c6a9-307">**請勿使用警告圖示來「柔化」非重大錯誤。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-307">**Don't use warning icons to "soften" non-critical errors.**</span></span> <span data-ttu-id="4c6a9-308">錯誤不是警告會改為套用錯誤圖示指導方針。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-308">Errors aren't warnings apply the error icon guidelines instead.</span></span>
-   <span data-ttu-id="4c6a9-309">**針對問題對話方塊，請只針對具有顯著後果的問題使用警告圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-309">**For question dialogs, use warning icons only for questions with significant consequences.**</span></span> <span data-ttu-id="4c6a9-310">請勿使用警告圖示進行例行問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-310">Don't use warning icons for routine questions.</span></span>

<span data-ttu-id="4c6a9-311">**正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-311">**Correct:**</span></span>

![<span data-ttu-id="4c6a9-312">螢幕擷取畫面警告不停止系統還原</span><span class="sxs-lookup"><span data-stu-id="4c6a9-312">screen shot warning not to stop system restore</span></span> ](images/vis-std-icons-image17.png)

<span data-ttu-id="4c6a9-313">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-313">**Incorrect:**</span></span>

![<span data-ttu-id="4c6a9-314">有關關閉提醒的警告螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-314">screen shot of warning about dismissing reminders</span></span> ](images/vis-std-icons-image18.png)

<span data-ttu-id="4c6a9-315">在不正確的範例中，不正確地將警告圖示用於常式問題。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-315">In the incorrect example, a warning icon is incorrectly used for a routine question.</span></span>

-   <span data-ttu-id="4c6a9-316">**針對 [工作] 對話方塊，您可以使用警告註腳圖示來警示使用者有風險的後果。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-316">**For task dialogs, you can use a warning footnote icon to alert users of risky consequences.**</span></span> <span data-ttu-id="4c6a9-317">不過，您可以在內容區域或註腳區域中使用警告圖示，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-317">However, use a warning icon either in the content area or the footnote area, but not both.</span></span>

![<span data-ttu-id="4c6a9-318">可能不安全檔案的螢幕擷取畫面警告</span><span class="sxs-lookup"><span data-stu-id="4c6a9-318">screen shot warning of a potentially unsafe file</span></span> ](images/vis-std-icons-image19.png)

<span data-ttu-id="4c6a9-319">在此範例中，會在註腳中使用黃色的安全盾。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-319">In this example, a yellow security shield is used in a footnote.</span></span>

### <a name="information-icons"></a><span data-ttu-id="4c6a9-320">資訊圖示</span><span class="sxs-lookup"><span data-stu-id="4c6a9-320">Information icons</span></span>

-   <span data-ttu-id="4c6a9-321">**只有在內容不會明顯呈現資訊時，才使用資訊圖示：**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-321">**Use information icons only when the context isn't obviously presenting information:**</span></span>



    | <span data-ttu-id="4c6a9-322">Context</span><span class="sxs-lookup"><span data-stu-id="4c6a9-322">Context</span></span>                         | <span data-ttu-id="4c6a9-323">使用時機</span><span class="sxs-lookup"><span data-stu-id="4c6a9-323">When to use</span></span>                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="4c6a9-324">對話方塊</span><span class="sxs-lookup"><span data-stu-id="4c6a9-324">Dialog boxes</span></span><br/>  | <span data-ttu-id="4c6a9-325">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-325">Don't use.</span></span><br/>                                                                                                                             |
    | <span data-ttu-id="4c6a9-326">就地</span><span class="sxs-lookup"><span data-stu-id="4c6a9-326">In-place</span></span><br/>      | <span data-ttu-id="4c6a9-327">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-327">Don't use.</span></span> <span data-ttu-id="4c6a9-328">請改用純靜態文字或橫幅。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-328">Use either plain static text or a banner instead.</span></span><br/>                                                                           |
    | <span data-ttu-id="4c6a9-329">通知</span><span class="sxs-lookup"><span data-stu-id="4c6a9-329">Notifications</span></span><br/> | <span data-ttu-id="4c6a9-330">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-330">Don't use.</span></span><br/>                                                                                                                             |
    | <span data-ttu-id="4c6a9-331">汽球</span><span class="sxs-lookup"><span data-stu-id="4c6a9-331">Balloons</span></span><br/>      | <span data-ttu-id="4c6a9-332">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-332">Don't use.</span></span><br/>                                                                                                                             |
    | <span data-ttu-id="4c6a9-333">橫幅</span><span class="sxs-lookup"><span data-stu-id="4c6a9-333">Banners</span></span><br/>       | <span data-ttu-id="4c6a9-334">用來吸引橫幅。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-334">use to draw attention to the banner.</span></span> <br/> ![<span data-ttu-id="4c6a9-335">具有設定資訊的橫幅螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4c6a9-335">screen shot of banner with settings information</span></span> ](images/vis-std-icons-image20.png)<br/> |



 

-   <span data-ttu-id="4c6a9-336">對話方塊、通知和氣球中不需要資訊圖示，因為它們的內容可充分地傳達給使用者提供資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-336">Information icons aren't needed in dialog boxes, notifications, and balloons because their context sufficiently communicates that they are providing users with information.</span></span>
-   <span data-ttu-id="4c6a9-337">**針對工作對話方塊，請不要使用資訊註腳圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-337">**For task dialogs, don't use information footnote icons.**</span></span> <span data-ttu-id="4c6a9-338">註腳看起來夠清楚，不會說它們是資訊。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-338">Footnotes are sufficiently visible and it goes without saying that they are information.</span></span>

### <a name="question-mark-icons"></a><span data-ttu-id="4c6a9-339">問號圖示</span><span class="sxs-lookup"><span data-stu-id="4c6a9-339">Question mark icons</span></span>

-   <span data-ttu-id="4c6a9-340">**請僅針對說明進入點使用問號圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-340">**Use the question mark icon only for Help entry points.**</span></span> <span data-ttu-id="4c6a9-341">如需詳細資訊，請參閱說明 [進入點](winenv-help.md) 的指導方針。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-341">For more information, see the [Help entry point](winenv-help.md) guidelines.</span></span>
-   <span data-ttu-id="4c6a9-342">**請勿使用問號圖示提出問題。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-342">**Don't use the question mark icon to ask questions.**</span></span> <span data-ttu-id="4c6a9-343">同樣地，請只針對說明進入點使用問號圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-343">Again, use the question mark icon only for Help entry points.</span></span> <span data-ttu-id="4c6a9-344">您也不需要使用問號圖示來詢問問題，也就足以以問題的形式呈現主要的指示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-344">There is no need to ask questions using the question mark icon anyway it's sufficient to present a main instruction as a question.</span></span>
-   <span data-ttu-id="4c6a9-345">**請勿定期以警告圖示取代問號圖示。**</span><span class="sxs-lookup"><span data-stu-id="4c6a9-345">**Don't routinely replace question mark icons with warning icons.**</span></span> <span data-ttu-id="4c6a9-346">只有在問題有重大影響時，才以警告圖示取代問號圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-346">Replace a question mark icon with a warning icon only if the question has significant consequences.</span></span> <span data-ttu-id="4c6a9-347">否則，請不要使用圖示。</span><span class="sxs-lookup"><span data-stu-id="4c6a9-347">Otherwise, use no icon.</span></span>

 

