---
title: AMSI 如何協助您抵禦惡意軟體
description: 作為應用程式開發人員，您可以主動參與惡意程式碼防護。 具體來說，您可以協助保護您的客戶免于動態的腳本式惡意程式碼，以及從網路攻擊的非傳統途徑。
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671632"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a><span data-ttu-id="242fa-104">反惡意程式碼掃描介面 (AMSI) 如何協助您抵禦惡意程式碼</span><span class="sxs-lookup"><span data-stu-id="242fa-104">How the Antimalware Scan Interface (AMSI) helps you defend against malware</span></span>

<span data-ttu-id="242fa-105">如需 Windows 反惡意程式碼掃描介面 (AMSI) 的簡介，請參閱 [反惡意程式碼掃描介面 (AMSI) ](antimalware-scan-interface-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="242fa-105">For an introduction to the Windows Antimalware Scan Interface (AMSI), see [Antimalware Scan Interface (AMSI)](antimalware-scan-interface-portal.md).</span></span>

<span data-ttu-id="242fa-106">作為應用程式開發人員，您可以主動參與惡意程式碼防護。</span><span class="sxs-lookup"><span data-stu-id="242fa-106">As an application developer, you can actively participate in malware defense.</span></span> <span data-ttu-id="242fa-107">具體來說，您可以協助保護您的客戶免于動態的腳本式惡意程式碼，以及從網路攻擊的非傳統途徑。</span><span class="sxs-lookup"><span data-stu-id="242fa-107">Specifically, you can help protect your customers from dynamic script-based malware, and from non-traditional avenues of cyberattack.</span></span>

<span data-ttu-id="242fa-108">以範例為例，假設您的應用程式可編寫腳本：它接受任意的腳本，並透過腳本引擎執行。</span><span class="sxs-lookup"><span data-stu-id="242fa-108">By way of an example, let's say that your application is scriptable: it accepts arbitrary script, and executes it via a scripting engine.</span></span> <span data-ttu-id="242fa-109">在腳本準備好提供給腳本引擎的時候，您的應用程式可以呼叫 Windows AMSI Api 來要求掃描內容。</span><span class="sxs-lookup"><span data-stu-id="242fa-109">At the point when a script is ready to be supplied to the scripting engine, your application can call the Windows AMSI APIs to request a scan of the content.</span></span> <span data-ttu-id="242fa-110">如此一來，您就可以安全地判斷腳本是否為惡意，然後再決定是否要繼續執行。</span><span class="sxs-lookup"><span data-stu-id="242fa-110">That way, you can safely determine whether or not the script is malicious before you decide to go ahead and execute it.</span></span>

<span data-ttu-id="242fa-111">即使腳本是在執行時間產生的也是如此。</span><span class="sxs-lookup"><span data-stu-id="242fa-111">This is true even if the script was generated at runtime.</span></span> <span data-ttu-id="242fa-112">腳本 (惡意或) ，可能會經歷數次的消除混淆。</span><span class="sxs-lookup"><span data-stu-id="242fa-112">Script (malicious or otherwise), might go through several passes of de-obfuscation.</span></span> <span data-ttu-id="242fa-113">但是您最終必須以簡單、未混淆的程式碼提供腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="242fa-113">But you ultimately need to supply the scripting engine with plain, un-obfuscated code.</span></span> <span data-ttu-id="242fa-114">這就是您叫用 AMSI Api 的那個點。</span><span class="sxs-lookup"><span data-stu-id="242fa-114">And that's the point at which you invoke the AMSI APIs.</span></span>

<span data-ttu-id="242fa-115">以下是 AMSI 架構的圖例，其中您的應用程式是由其中一個 [其他應用程式] 方塊表示。</span><span class="sxs-lookup"><span data-stu-id="242fa-115">Here's an illustration of the AMSI architecture, where your own application is represented by one of the "Other Application" boxes.</span></span>

![AMSI 架構](images/AMSI7Archi.jpg)

<span data-ttu-id="242fa-117">Windows AMSI 介面已開啟。</span><span class="sxs-lookup"><span data-stu-id="242fa-117">The Windows AMSI interface is open.</span></span> <span data-ttu-id="242fa-118">這表示任何應用程式都可以呼叫它;而且任何已註冊的反惡意程式碼引擎都可以處理提交給它的內容。</span><span class="sxs-lookup"><span data-stu-id="242fa-118">Which means that any application can call it; and any registered Antimalware engine can process the content submitted to it.</span></span>

<span data-ttu-id="242fa-119">我們不想要將討論限制在腳本引擎的討論範圍。</span><span class="sxs-lookup"><span data-stu-id="242fa-119">We needn't limit the discussion to scripting engines, either.</span></span> <span data-ttu-id="242fa-120">您的應用程式可能是通訊應用程式，它會在向您的客戶顯示時，先掃描立即病毒的訊息。</span><span class="sxs-lookup"><span data-stu-id="242fa-120">Perhaps your application is a communication app, and it scans instant messages for viruses before it shows them to your customers.</span></span> <span data-ttu-id="242fa-121">或者，您的軟體可能是在安裝外掛程式之前驗證外掛程式的遊戲。</span><span class="sxs-lookup"><span data-stu-id="242fa-121">Or maybe your software is a game that validates plugins before installing them.</span></span> <span data-ttu-id="242fa-122">使用 AMSI 有許多機會和案例。</span><span class="sxs-lookup"><span data-stu-id="242fa-122">There are plenty of opportunities and scenarios for using AMSI.</span></span>

## <a name="amsi-in-action"></a><span data-ttu-id="242fa-123">AMSI 實際操作</span><span class="sxs-lookup"><span data-stu-id="242fa-123">AMSI in action</span></span>

<span data-ttu-id="242fa-124">讓我們來看看 AMSI 的實際運作方式。</span><span class="sxs-lookup"><span data-stu-id="242fa-124">Let's take a look at AMSI in action.</span></span> <span data-ttu-id="242fa-125">在此範例中，Windows Defender 是呼叫 AMSI Api 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="242fa-125">In this example, Windows Defender is the application that's calling AMSI APIs.</span></span> <span data-ttu-id="242fa-126">但是，您可以從自己的應用程式中呼叫相同的 Api。</span><span class="sxs-lookup"><span data-stu-id="242fa-126">But you can call the same APIs from within your own application.</span></span>

<span data-ttu-id="242fa-127">以下是使用 XOR 編碼技術來隱藏意圖的腳本範例 (該意圖是否為良性或不) 。</span><span class="sxs-lookup"><span data-stu-id="242fa-127">Here's a sample of a script that uses the XOR-encoding technique to hide its intent (whether that intent is benign or not).</span></span> <span data-ttu-id="242fa-128">在此圖中，我們可以想像此腳本是從網際網路下載。</span><span class="sxs-lookup"><span data-stu-id="242fa-128">For this illustration, we can imagine that this script was downloaded from the Internet.</span></span>

![以 Base64 編碼的範例腳本](images/AMSI8.png)

<span data-ttu-id="242fa-130">為了讓事情更有趣，我們可以在命令列手動輸入此腳本，如此就不會有實際的檔案可供監視。</span><span class="sxs-lookup"><span data-stu-id="242fa-130">To make things more interesting, we can enter this script manually at the command line so that there is no actual file to monitor.</span></span> <span data-ttu-id="242fa-131">這會鏡像所謂的「無檔案威脅」。</span><span class="sxs-lookup"><span data-stu-id="242fa-131">This mirrors what's known as a "fileless threat".</span></span> <span data-ttu-id="242fa-132">這並不像是在磁片上掃描檔案一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="242fa-132">It's not as simple as scanning files on disk.</span></span> <span data-ttu-id="242fa-133">威脅可能是只有在電腦記憶體中的後門。</span><span class="sxs-lookup"><span data-stu-id="242fa-133">The threat might be a backdoor that lives only in the memory of a machine.</span></span>

<span data-ttu-id="242fa-134">接下來，我們會看到在 Windows PowerShell 中執行腳本的結果。</span><span class="sxs-lookup"><span data-stu-id="242fa-134">Below, we see the result of running the script in Windows PowerShell.</span></span> <span data-ttu-id="242fa-135">您會看到 Windows Defender 能夠在這個複雜的案例中偵測 AMSI 測試範例，只是使用標準 AMSI 測試範例簽章。</span><span class="sxs-lookup"><span data-stu-id="242fa-135">You'll see that Windows Defender is able to detect the AMSI test sample in this complicated scenario, merely by using the standard AMSI test sample signature.</span></span>

![Windows Defender 偵測 AMSI 測試範例](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a><span data-ttu-id="242fa-137">AMSI 與 JavaScript/VBA 整合</span><span class="sxs-lookup"><span data-stu-id="242fa-137">AMSI integration with JavaScript/VBA</span></span>

<span data-ttu-id="242fa-138">以下所述的工作流程說明另一個範例的端對端流程，我們會在其中示範 AMSI 與 Microsoft Office 內的宏執行整合。</span><span class="sxs-lookup"><span data-stu-id="242fa-138">The illustrated workflow below describes the end-to-end flow of another example, in which we demonstrate AMSI's integration with macro execution within Microsoft Office.</span></span>

![AMSI 與 JavaScript/VBA 整合](images/integ-js-vba.png)

- <span data-ttu-id="242fa-140">使用者會收到包含 (惡意) 宏的檔，evades 靜態防毒軟體掃描，方法是採用像是模糊化、受密碼保護的檔案等技術。</span><span class="sxs-lookup"><span data-stu-id="242fa-140">The user receives a document containing a (malicious) macro, which evades static antivirus software scans by employing techniques such as obfuscation, password-protected files, or other.</span></span>
- <span data-ttu-id="242fa-141">然後，使用者會開啟包含 (惡意) 宏的檔。</span><span class="sxs-lookup"><span data-stu-id="242fa-141">The user then opens the document containing the (malicious) macro.</span></span> <span data-ttu-id="242fa-142">如果檔在 [受保護的檢視] 中開啟，則使用者按一下 [ **啟用編輯** ] 以結束受保護的檢視。</span><span class="sxs-lookup"><span data-stu-id="242fa-142">If the document opens in Protected View, then the user clicks **Enable Editing** to exit Protected View.</span></span>
- <span data-ttu-id="242fa-143">使用者按一下 [ **啟用宏** ] 以允許執行宏。</span><span class="sxs-lookup"><span data-stu-id="242fa-143">The user clicks **Enable Macros** to allow macros to run.</span></span>
- <span data-ttu-id="242fa-144">當宏執行時，VBA 執行時間會使用迴圈緩衝區來記錄 \[ 與 \] WIN32、COM 和 VBA api 呼叫相關的1資料和參數。</span><span class="sxs-lookup"><span data-stu-id="242fa-144">As the macro runs, the VBA runtime uses a circular buffer to log \[1\] data and parameters related to calls to Win32, COM, and VBA APIs.</span></span>
- <span data-ttu-id="242fa-145">當被視為高風險的特定 Win32 或 COM Api (也稱為 *觸發* 程式) \[ 2 時 \] ，會停止執行宏，而迴圈緩衝區的內容會傳遞至 AMSI。</span><span class="sxs-lookup"><span data-stu-id="242fa-145">When specific Win32 or COM APIs that are considered high risk (also known as *triggers*) \[2\] are observed, macro execution is halted, and the contents of the circular buffer are passed to AMSI.</span></span>
- <span data-ttu-id="242fa-146">註冊的 AMSI 反惡意程式碼服務提供者會以判斷提示回應，指出宏行為是否為惡意。</span><span class="sxs-lookup"><span data-stu-id="242fa-146">The registered AMSI anti-malware service provider responds with a verdict to indicate whether or not the macro behavior is malicious.</span></span>
- <span data-ttu-id="242fa-147">如果行為不是惡意的，則會繼續執行宏。</span><span class="sxs-lookup"><span data-stu-id="242fa-147">If the behavior is non-malicious, then macro execution proceeds.</span></span>
- <span data-ttu-id="242fa-148">否則，如果行為是惡意的，則 Microsoft Office 會關閉會話以回應警示 \[ 3 \] ，而 AV 可隔離檔案。</span><span class="sxs-lookup"><span data-stu-id="242fa-148">Otherwise, if the behavior is malicious, then Microsoft Office closes the session in response to the alert \[3\], and the AV can quarantine the file.</span></span>

## <a name="what-does-this-mean-for-you"></a><span data-ttu-id="242fa-149">這對您的意義為何？</span><span class="sxs-lookup"><span data-stu-id="242fa-149">What does this mean for you?</span></span>

<span data-ttu-id="242fa-150">針對 Windows 使用者，任何在 Windows 10 內建腳本主機上使用模糊化和規避技術的惡意軟體，都會自動以比以往更深層的方式進行檢查，以提供額外的保護層級。</span><span class="sxs-lookup"><span data-stu-id="242fa-150">For Windows users, any malicious software that uses obfuscation and evasion techniques on Windows 10's built-in scripting hosts is automatically inspected at a much deeper level than ever before, providing additional levels of protection.</span></span>

<span data-ttu-id="242fa-151">如果您是應用程式開發人員，請考慮讓您的應用程式呼叫 Windows AMSI 介面，如果您想要從 (獲益，並使用) 額外的潛在惡意內容掃描和分析來保護您的客戶。</span><span class="sxs-lookup"><span data-stu-id="242fa-151">For you as an application developer, consider having your application call the Windows AMSI interface if you want to benefit from (and protect your customers with) extra scanning and analysis of potentially malicious content.</span></span>

<span data-ttu-id="242fa-152">作為防毒軟體廠商，您可以考慮針對 AMSI 介面執行支援。</span><span class="sxs-lookup"><span data-stu-id="242fa-152">As an antivirus software vendor, you can consider implementing support for the AMSI interface.</span></span> <span data-ttu-id="242fa-153">當您這樣做時，您的引擎將可深入瞭解應用程式 (包含 Windows 10 內建腳本主機的資料，) 考慮可能是惡意的。</span><span class="sxs-lookup"><span data-stu-id="242fa-153">When you do, your engine will have much deeper insight into the data that applications (including Windows 10's built-in scripting hosts) consider to be potentially malicious.</span></span>

## <a name="more-background-info-about-fileless-threats"></a><span data-ttu-id="242fa-154">更多有關無檔案威脅的背景資訊</span><span class="sxs-lookup"><span data-stu-id="242fa-154">More background info about fileless threats</span></span>

<span data-ttu-id="242fa-155">您可能想要取得有關 Windows AMSI 設計來協助您防禦的無檔案威脅種類的詳細背景資訊。</span><span class="sxs-lookup"><span data-stu-id="242fa-155">You may be curious for more background info about the kinds of fileless threats that Windows AMSI is designed to help you defend against.</span></span> <span data-ttu-id="242fa-156">在本節中，我們將探討惡意程式碼生態系統中的傳統貓和滑鼠遊戲。</span><span class="sxs-lookup"><span data-stu-id="242fa-156">In this section, we'll take a look at the traditional cat-and-mouse game that plays out in the malware ecosystem.</span></span>

<span data-ttu-id="242fa-157">我們會使用 PowerShell 作為範例。</span><span class="sxs-lookup"><span data-stu-id="242fa-157">We'll use PowerShell as an example.</span></span> <span data-ttu-id="242fa-158">但是，您可以利用與任何動態語言（ &mdash; VBScript、Perl、Python、Ruby 等）所示範的相同技巧和流程。</span><span class="sxs-lookup"><span data-stu-id="242fa-158">But you can leverage the same techniques and processes we'll demonstrate with any dynamic language&mdash;VBScript, Perl, Python, Ruby, and more.</span></span>

<span data-ttu-id="242fa-159">以下是惡意 PowerShell 腳本的範例。</span><span class="sxs-lookup"><span data-stu-id="242fa-159">Here's an example of a malicious PowerShell script.</span></span>

![惡意 PowerShell 腳本範例](images/AMSI1.png)

<span data-ttu-id="242fa-161">雖然此腳本只會將訊息寫入畫面，但惡意程式碼通常更是惡意的。</span><span class="sxs-lookup"><span data-stu-id="242fa-161">While this script simply writes a message to the screen, malware is typically more nefarious.</span></span> <span data-ttu-id="242fa-162">但是，您可以輕鬆地撰寫簽章來偵測這種簽章。</span><span class="sxs-lookup"><span data-stu-id="242fa-162">But you could easily write a signature to detect this one.</span></span> <span data-ttu-id="242fa-163">例如，簽章可以搜尋「寫入主機 ' pwnd！ '」字串</span><span class="sxs-lookup"><span data-stu-id="242fa-163">For example, the signature could search for the string "Write-Host 'pwnd!'"</span></span> <span data-ttu-id="242fa-164">在使用者開啟的任何檔案中。</span><span class="sxs-lookup"><span data-stu-id="242fa-164">in any file that the user opens.</span></span> <span data-ttu-id="242fa-165">好：我們偵測到我們的第一種惡意程式碼！</span><span class="sxs-lookup"><span data-stu-id="242fa-165">Great: we've detected our first malware!</span></span>

<span data-ttu-id="242fa-166">不過，在我們的第一個簽章偵測到之後，惡意程式碼作者會回應。</span><span class="sxs-lookup"><span data-stu-id="242fa-166">After being detected by our first signature, though, malware authors will respond.</span></span> <span data-ttu-id="242fa-167">它們會藉由建立動態腳本來回應，例如此範例。</span><span class="sxs-lookup"><span data-stu-id="242fa-167">They respond by creating dynamic scripts such as this example.</span></span>

![動態腳本的範例](images/AMSI2.png)

<span data-ttu-id="242fa-169">在該案例中，惡意程式碼作者會建立字串，代表要執行的 PowerShell 腳本。</span><span class="sxs-lookup"><span data-stu-id="242fa-169">In that scenario, malware authors create a string representing the PowerShell script to run.</span></span> <span data-ttu-id="242fa-170">但它們會使用簡單的字串串連技術來中斷先前的簽章。</span><span class="sxs-lookup"><span data-stu-id="242fa-170">But they use a simple string concatenation technique to break our earlier signature.</span></span> <span data-ttu-id="242fa-171">如果您曾看到載入網頁的來源，您將會看到此技術的許多實例用來避免廣告封鎖軟體。</span><span class="sxs-lookup"><span data-stu-id="242fa-171">If you ever view the source of an ad-laden web page, you'll see many instances of this technique being used to avoid ad-blocking software.</span></span>

<span data-ttu-id="242fa-172">最後，惡意程式碼作者會將這個串連的字串傳遞給 `Invoke-Expression` Cmdlet &mdash; PowerShell 的機制，以評估在執行時間撰寫或建立的腳本。</span><span class="sxs-lookup"><span data-stu-id="242fa-172">Finally, the malware author passes this concatenated string to the `Invoke-Expression` cmdlet&mdash;PowerShell's mechanism to evaluate scripts that are composed or created at runtime.</span></span>

<span data-ttu-id="242fa-173">在回應中，反惡意程式碼軟體會開始進行基礎語言模擬。</span><span class="sxs-lookup"><span data-stu-id="242fa-173">In response, antimalware software starts to do basic language emulation.</span></span> <span data-ttu-id="242fa-174">例如，如果我們看到兩個串連的字串，則我們會模擬這兩個字串的串連，然後在結果上執行簽章。</span><span class="sxs-lookup"><span data-stu-id="242fa-174">For example, if we see two strings being concatenated, then we emulate the concatenation of those two strings, and then run our signatures on the result.</span></span> <span data-ttu-id="242fa-175">可惜的是，這是一種相當脆弱的方法，因為語言通常會有許多方式來表示和串連字號串。</span><span class="sxs-lookup"><span data-stu-id="242fa-175">Unfortunately, this is a fairly fragile approach, because languages tend to have a lot of ways to represent and concatenate strings.</span></span>

<span data-ttu-id="242fa-176">因此，在此簽章攔截之後，惡意程式碼作者會移至更複雜 &mdash; 的內容，例如，以 Base64 編碼腳本內容，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="242fa-176">So, after being caught by this signature, malware authors will move to something more complicated&mdash;for example, encoding script content in Base64, as in this next example.</span></span>

![Base64 的腳本內容範例](images/AMSI3.png)

<span data-ttu-id="242fa-178">資源，大部分的反惡意程式碼引擎也都採用 Base64 解碼模擬。</span><span class="sxs-lookup"><span data-stu-id="242fa-178">Being resourceful, most antimalware engines implement Base64 decoding emulation, as well.</span></span> <span data-ttu-id="242fa-179">因此，由於我們也會執行 Base64 解碼模擬，因此我們將會提前一段時間。</span><span class="sxs-lookup"><span data-stu-id="242fa-179">So, since we also implement Base64 decoding emulation, we're ahead for a time.</span></span>

<span data-ttu-id="242fa-180">在回應中，惡意程式碼作者會移至演算法模糊化， &mdash; 例如它們執行的腳本中的簡單 XOR 編碼機制。</span><span class="sxs-lookup"><span data-stu-id="242fa-180">In response, malware authors move to algorithmic obfuscation&mdash;such as a simple XOR-encoding mechanism in the scripts they run.</span></span>

![演算法模糊化腳本的範例](images/AMSI4.png)

<span data-ttu-id="242fa-182">到目前為止，我們已經超過防毒程式會模擬或偵測到的內容，因此我們不一定會偵測到此腳本的作用。</span><span class="sxs-lookup"><span data-stu-id="242fa-182">At this point, we're generally past what antivirus engines will emulate or detect, so we won't necessarily detect what this script is doing.</span></span> <span data-ttu-id="242fa-183">不過，我們可以開始根據模糊化和編碼技巧來撰寫簽章。</span><span class="sxs-lookup"><span data-stu-id="242fa-183">However, we can start to write signatures against the obfuscation and encoding techniques.</span></span> <span data-ttu-id="242fa-184">事實上，這就是針對以腳本為基礎之惡意程式碼的大部分簽章的帳戶。</span><span class="sxs-lookup"><span data-stu-id="242fa-184">In fact, that's what accounts for the vast majority of signatures for script-based malware.</span></span>

<span data-ttu-id="242fa-185">但是如果混淆器很簡單，那麼它看起來就像是很重要的腳本呢？</span><span class="sxs-lookup"><span data-stu-id="242fa-185">But what if the obfuscator is so trivial that it looks like many well-behaved scripts?</span></span> <span data-ttu-id="242fa-186">它的簽章會產生無法接受的誤報數目。</span><span class="sxs-lookup"><span data-stu-id="242fa-186">A signature for it would generate an unacceptable number of false positives.</span></span> <span data-ttu-id="242fa-187">以下是範例 *stager* 腳本，它本身無法偵測到太良性。</span><span class="sxs-lookup"><span data-stu-id="242fa-187">Here's a sample *stager* script that's too benign to detect on its own.</span></span>

![範例 stager 腳本，太無害，無法自行偵測](images/AMSI5.png)

<span data-ttu-id="242fa-189">在該範例中，我們會下載網頁，並叫用其中的一些內容。</span><span class="sxs-lookup"><span data-stu-id="242fa-189">In that example, we're downloading a web page, and invoking some content from it.</span></span> <span data-ttu-id="242fa-190">以下是 Visual Basic 腳本中的對等專案。</span><span class="sxs-lookup"><span data-stu-id="242fa-190">Here's the equivalent in Visual Basic script.</span></span>

![Visual Basic 腳本中的對等專案](images/AMSI6.png)

<span data-ttu-id="242fa-192">這兩個範例中的專案越糟，防毒軟體引擎會檢查使用者開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="242fa-192">What makes things worse in both of these examples is that the antivirus engine inspects files being opened by the user.</span></span> <span data-ttu-id="242fa-193">如果惡意內容只存在於記憶體中，則可能會偵測到攻擊。</span><span class="sxs-lookup"><span data-stu-id="242fa-193">If the malicious content lives only in memory, then the attack can potentially go undetected.</span></span>

<span data-ttu-id="242fa-194">本節說明使用傳統簽章偵測的限制。</span><span class="sxs-lookup"><span data-stu-id="242fa-194">This section showed the limitations of detection using traditional signatures.</span></span> <span data-ttu-id="242fa-195">但是，雖然惡意腳本可能會經歷數個消除混淆的行程，但最終需要以純 unobfuscated 程式碼提供腳本引擎。</span><span class="sxs-lookup"><span data-stu-id="242fa-195">But, while a malicious script might go through several passes of de-obfuscation, it ultimately needs to supply the scripting engine with plain, unobfuscated code.</span></span> <span data-ttu-id="242fa-196">然後，在 &mdash; 上述第一節中所述， &mdash; Windows 10 的內建腳本主機呼叫 AMSI api 來要求掃描這個未受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="242fa-196">And at that point&mdash;as we described in the first section above&mdash;Windows 10's built-in scripting hosts call the AMSI APIs to request a scan of this unprotected content.</span></span> <span data-ttu-id="242fa-197">而您的應用程式也可以達成相同的目的。</span><span class="sxs-lookup"><span data-stu-id="242fa-197">And your application can do the same thing.</span></span>

## <a name="related-resources"></a><span data-ttu-id="242fa-198">相關資源</span><span class="sxs-lookup"><span data-stu-id="242fa-198">Related resources</span></span>

* [<span data-ttu-id="242fa-199">無檔案型態威脅</span><span class="sxs-lookup"><span data-stu-id="242fa-199">Fileless threats</span></span>](/windows/security/threat-protection/intelligence/fileless-threats)
* [<span data-ttu-id="242fa-200">Office VBA + AMSI：新娘惡意宏的</span><span class="sxs-lookup"><span data-stu-id="242fa-200">Office VBA + AMSI: Parting the veil on malicious macros</span></span>](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [<span data-ttu-id="242fa-201">看不見但不可見：失去無檔案惡意程式碼與行為監視、AMSI 和下一代 AV</span><span class="sxs-lookup"><span data-stu-id="242fa-201">Out of sight but not invisible: Defeating fileless malware with behavior monitoring, AMSI, and next-gen AV</span></span>](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
