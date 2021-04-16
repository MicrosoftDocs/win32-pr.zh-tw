---
title: 協力廠商輸入法編輯器
description: 協力廠商輸入法編輯器
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca9768de96b9dcdeac7f4b0da210f7aa788801b
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104562795"
---
# <a name="third-party-input-method-editors"></a><span data-ttu-id="a2ae7-103">協力廠商輸入法編輯器</span><span class="sxs-lookup"><span data-stu-id="a2ae7-103">Third-party input method editors</span></span>

## <a name="platforms"></a><span data-ttu-id="a2ae7-104">平台</span><span class="sxs-lookup"><span data-stu-id="a2ae7-104">Platforms</span></span>

<span data-ttu-id="a2ae7-105">**客戶** 端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2ae7-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="a2ae7-106">**伺服器** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2ae7-106">**Servers** - Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="a2ae7-107">Description</span><span class="sxs-lookup"><span data-stu-id="a2ae7-107">Description</span></span>

<span data-ttu-id="a2ae7-108">輸入法編輯器 (Ime) 是軟體元件，可讓使用者輸入比在鍵盤上可以表示更多字元的語言文字。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-108">Input method editors (IMEs) are software components that allow a user to type text in a language that has more characters than can be represented on a keyboard.</span></span> <span data-ttu-id="a2ae7-109"> (這種情況很常見，但不限於東亞語言。 ) ，而不是每個出現在單一按鍵上的單一字元，使用者可以輸入輸入法所轉譯的按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-109">(This is common, but not limited to, East Asian languages.) Instead of each single character appearing on a single key, users type combinations of keys that are then interpreted by the IME.</span></span> <span data-ttu-id="a2ae7-110">IME 會產生符合一組按鍵筆劃的字元，有時會向使用者呈現可從中挑選的可能字元清單，然後將該字元插入使用者應用程式的 [編輯] 控制項視窗中。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-110">The IME generates the character that matches the set of key strokes, sometimes presenting the user with a list of possible characters to pick from, and then inserts the character into the edit control window of the user’s app.</span></span>

<span data-ttu-id="a2ae7-111">在過去，Windows 已允許協力廠商的 Ime 在 Windows 系統中執行，而這項功能會繼續進行 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-111">In the past, Windows has allowed third-party IMEs to run in the Windows system, and this capability continues for Windows 8.</span></span> <span data-ttu-id="a2ae7-112">使用者可以安裝協力廠商的輸入法，並加以使用。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-112">Users can install a third-party IME and use it.</span></span> <span data-ttu-id="a2ae7-113">此外，我們也強化了系統和程式，以防止惡意的 Ime、提升安全性，以及強化使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-113">In addition, we are hardening the system and processes to prevent malicious IMEs, improve security, and enhance the user experience.</span></span>

<span data-ttu-id="a2ae7-114">在 Windows 8 中，您將會發現：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-114">In Windows 8, you will find:</span></span>

-   <span data-ttu-id="a2ae7-115">硬體鍵盤和觸控鍵盤的協力廠商 IME 支援</span><span class="sxs-lookup"><span data-stu-id="a2ae7-115">Third-party IME support for both hardware keyboards and touch keyboards</span></span>
-   <span data-ttu-id="a2ae7-116">協力廠商 IME 廠商必須遵循 Microsoft 指導方針來開發其 Ime 以進行 Windows 8</span><span class="sxs-lookup"><span data-stu-id="a2ae7-116">Third-party IME vendors must follow Microsoft guidelines to develop their IMEs for Windows 8</span></span>
-   <span data-ttu-id="a2ae7-117">協力廠商 Ime 必須經過數位簽署</span><span class="sxs-lookup"><span data-stu-id="a2ae7-117">Third-party IMEs must be digitally signed</span></span>
-   <span data-ttu-id="a2ae7-118">協力廠商 Ime 必須是文字服務架構 (TSF) 感知，而且必須將適當的 IME 旗標設定為在 Windows 8 中正確執行。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-118">Third-party IMEs must be Text Services Framework (TSF) aware, and proper IME flags must be set to run correctly in Windows 8</span></span>
-   <span data-ttu-id="a2ae7-119">舊版的協力廠商 Ime 將能夠在桌面應用程式中執行，但在 Windows Store 應用程式中會遭到封鎖</span><span class="sxs-lookup"><span data-stu-id="a2ae7-119">Legacy third-party IMEs will be able to run in desktop apps, but will be blocked in Windows Store apps</span></span>
-   <span data-ttu-id="a2ae7-120">協力廠商 Ime 可以使用 Windows 所提供的觸控鍵盤配置來連結其 IME，讓使用者可以使用其 IME 搭配觸控鍵盤。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-120">Third-party IMEs can use the touch keyboard layout provided by Windows to link their IME, so that users can use their IME with touch keyboards.</span></span> <span data-ttu-id="a2ae7-121">不過，協力廠商 Ime 將無法使用適用于觸控鍵盤的內建 Ime 功能</span><span class="sxs-lookup"><span data-stu-id="a2ae7-121">However, certain functions of in-box IMEs for touch keyboards will not be available to third-party IMEs</span></span>
-   <span data-ttu-id="a2ae7-122">Windows Defender 會從 Windows 系統移除惡意的 Ime</span><span class="sxs-lookup"><span data-stu-id="a2ae7-122">Windows Defender will remove malicious IMEs from the Windows system</span></span>

## <a name="manifestation"></a><span data-ttu-id="a2ae7-123">表現</span><span class="sxs-lookup"><span data-stu-id="a2ae7-123">Manifestation</span></span>

<span data-ttu-id="a2ae7-124">**輸入語言和輸入方法切換變更**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-124">**Input language and input method switch changes**</span></span>

<span data-ttu-id="a2ae7-125">並不會顯示所有 IME 模式圖示，以及輸入法商標圖示，只會顯示一個 IME 模式圖示以及輸入法商標圖示。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-125">Instead of showing all the IME mode icons along with the IME branding icon, only one IME mode icon along with the IME branding icon is shown.</span></span> <span data-ttu-id="a2ae7-126">下列兩個圖形顯示 Windows 8 輸入飛出視窗和輸入法飛出視窗，以日文 IME 作為目前的輸入方法。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-126">The two figures below show the Windows 8 input flyout and the IME flyout, with Japanese IME as the current input method.</span></span> <span data-ttu-id="a2ae7-127">如果您按一下 [IME 商標] 圖示，就可以切換輸入方法。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-127">If you click the IME branding icon, you can switch input methods.</span></span>

![切換輸入方法](images/inputindicator2.png)

<span data-ttu-id="a2ae7-129">如果您按一下輸入法模式圖示，就可以切換到不同的 IME 模式。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-129">If you click the IME mode icon, you can switch to a different IME mode.</span></span>

![切換輸入法模式](images/inputindicator1.png)

<span data-ttu-id="a2ae7-131">如果 IME 依賴語言列在 Windows 7 中顯示其模式圖示，則必須變更 IME，才能在 Windows 8 的輸入指標中顯示其商標圖示和模式圖示。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-131">If an IME relies on the language bar to show its mode icons in Windows 7, the IME must be changed in order to show its branding icon and mode icon in the input indicator in Windows 8.</span></span>

> [!Note]  
> <span data-ttu-id="a2ae7-132">注意：在桌面工作列上的工作列中，IME 如何顯示商標圖示和模式圖示的詳細資料，將會以 Windows 8 IME 指導方針的方式記載並公佈。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-132">Note: The details about how an IME can show its branding icon and mode icon in the SysTray on the desktop Taskbar will be documented and posted publicly in the Windows 8 IME Guidelines.</span></span>

 

<span data-ttu-id="a2ae7-133">**新的 Windows 環境**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-133">**New Windows environment**</span></span>

<span data-ttu-id="a2ae7-134">Windows 8 中的環境會變更 Ime 的橫向。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-134">The environment in Windows 8 changes the landscape for IMEs.</span></span> <span data-ttu-id="a2ae7-135">Windows 7 不提供 Windows Store 應用程式的概念、本機內容應用程式容器，以及對 Ime 的 API 限制。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-135">The concepts of Windows Store apps, local context app containers, and API restrictions on IMEs were not present in Windows 7.</span></span> <span data-ttu-id="a2ae7-136">某些現有的 Windows 7 Ime 在 Windows Store 應用程式內執行時停止回應，因此不允許在 Windows Store 應用程式內執行舊版 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-136">Some existing Windows 7 IMEs stop responding when run inside a Windows Store app and therefore don’t allow legacy IMEs to run inside Windows Store apps.</span></span> <span data-ttu-id="a2ae7-137">此外，請確定已驗證新版本的 Ime，以確保它們在 Windows Store 應用程式內執行之前，都能與新的 UI 環境相容。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-137">Additionally, make sure that new versions of IMEs are validated to ensure that they are compatible with the new UI environment before they are run inside Windows Store apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a2ae7-138">降低</span><span class="sxs-lookup"><span data-stu-id="a2ae7-138">Mitigation</span></span>

<span data-ttu-id="a2ae7-139">您可以在系統上使用桌面相容的 IME。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-139">You can use a desktop-compatible IME on the system.</span></span> <span data-ttu-id="a2ae7-140">如果您主要是使用桌面應用程式，而您想要繼續使用慣用的舊版 IME 進行輸入，這可能是您的最佳選擇。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-140">This might be your best option if you mainly use desktop apps, and you want to continue to use a preferred legacy IME for input.</span></span> <span data-ttu-id="a2ae7-141">建議您使用 Windows 8 IME，並停止使用舊版/非認證的 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-141">We recommend that you use a Windows 8 IME, and stop using legacy/non-certified IMEs.</span></span> <span data-ttu-id="a2ae7-142">通知是由語言 CPL 和輸入參數提供，以警告您使用桌面相容 IME 的效果。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-142">Notifications are provided by both the Language CPL and the Input Switch to warn you of the effects of using a desktop-compatible IME.</span></span>

<span data-ttu-id="a2ae7-143">如果電腦相容的 IME 無法在您的系統上運作，您將會看到下列其中一種行為：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-143">You will see either of the below behaviors if a desktop-compatible IME doesn’t work across your system:</span></span>

-   <span data-ttu-id="a2ae7-144">語言 CPL UI 會將桌面相容的 Ime 標記為標籤，並顯示一則訊息，指出不相容的 Ime 只能在桌面應用程式中運作。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-144">The language CPL UI labels desktop-compatible IMEs, and displays a message that non-compatible IMEs work only in desktop apps.</span></span>
-   <span data-ttu-id="a2ae7-145">當使用者在 Windows Store 應用程式中時，輸入飛出視窗會 greys 桌面相容的 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-145">The input flyout greys out desktop-compatible IMEs when the user is inside Windows Store apps.</span></span> <span data-ttu-id="a2ae7-146">這表示輸入法無法在此應用程式中運作。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-146">This indicates that the IME does not work in this app.</span></span> <span data-ttu-id="a2ae7-147">桌上型電腦相容的 Ime 在桌面上 (不會呈現灰色) 。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-147">(In the desktop, desktop-compatible IMEs are not greyed out).</span></span> <span data-ttu-id="a2ae7-148">如果您使用不相容的輸入法切換至 Windows Store 應用程式，併發現輸入法是 off，請使用輸入指標來變更為與 Windows Store 應用程式相容的 IME。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-148">If you switch to Windows Store apps with a non-compatible IME and realize the IME is off, use the input indicator to change to an IME that is compatible with Windows Store apps.</span></span>

<span data-ttu-id="a2ae7-149">舊版或桌面相容的 Ime 僅限於下列條件：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-149">Legacy or desktop-compatible IMEs are limited to these conditions:</span></span>

-   <span data-ttu-id="a2ae7-150">從 Windows 7 升級至 Windows 8，並在系統上使用協力廠商的 Ime</span><span class="sxs-lookup"><span data-stu-id="a2ae7-150">Upgrading from Windows 7 to Windows 8, with third-party IMEs on the system</span></span>
-   <span data-ttu-id="a2ae7-151">廠商尚未發行與 Windows 8 相容的版本，使用者同時嘗試使用現有的 Windows 7 版本</span><span class="sxs-lookup"><span data-stu-id="a2ae7-151">The vendor has not released a version compatible with Windows 8, and the user tries to use an existing Windows 7 version in the meantime</span></span>

## <a name="solution"></a><span data-ttu-id="a2ae7-152">解決方法</span><span class="sxs-lookup"><span data-stu-id="a2ae7-152">Solution</span></span>

<span data-ttu-id="a2ae7-153">**一般**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-153">**General**</span></span>

<span data-ttu-id="a2ae7-154">使用現有的文字服務架構 (TSF) 基礎結構，為您的 Ui 執行您的 IME 邏輯和 Windows Store 應用程式通用控制項。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-154">Use the existing text services framework (TSF) infrastructure to implement your IME logic and the Windows Store app common controls for your UIs.</span></span> <span data-ttu-id="a2ae7-155">建立擁有的 windows 來裝載您的 UI。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-155">Create owned windows to host your UI.</span></span>

<span data-ttu-id="a2ae7-156">新增搜尋 Api 是為了改善搜尋預測，並在 UI 中提供簡潔的搜尋體驗。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-156">New search APIs are being added to improve search prediction and provide a cleaner search experience in the UI.</span></span>

<span data-ttu-id="a2ae7-157">此外，也會新增 Api，以在叫用觸控鍵盤時通知協力廠商 Ime，以防止觸摸鍵盤涵蓋 UI。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-157">APIs are also being added to notify third-party IMEs when a touch keyboard is invoked to protect the UI from being covered by the touch keyboard.</span></span> <span data-ttu-id="a2ae7-158">協力廠商 Ime 會自動載入預設的傳統觸控鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-158">A default classic touch keyboard layout is automatically loaded for third-party IMEs.</span></span> <span data-ttu-id="a2ae7-159">不需要額外的工作就能與此傳統觸控鍵盤配置整合。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-159">No additional work is needed to integrate with this classic touch keyboard layout.</span></span> <span data-ttu-id="a2ae7-160">但是，協力廠商的 Ime 將能夠要求替代的觸控版面配置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-160">However, third-party IMEs will be able to request an alternate touch layout.</span></span>

<span data-ttu-id="a2ae7-161">熟悉 Windows 8 IME 指導方針，讓您可以在您的 IME 中升級重要的 Windows Store 應用程式使用者經驗準則。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-161">Become familiar with the Windows 8 IME guidelines so that you can promote key Windows Store app user experience principles in your IME.</span></span> <span data-ttu-id="a2ae7-162">遵循指導方針的 Ime 必須設定旗標，以指出 IME 與 Microsoft 設計相容。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-162">IMEs that adhere to the guidelines must set a flag to indicate that the IME is compatible with the Microsoft design.</span></span> <span data-ttu-id="a2ae7-163">Windows 8 封鎖所有與桌面相容的 Ime 在 Windows Store 應用程式中執行。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-163">Windows 8 blocks all desktop-compatible IMEs from running in Windows Store apps.</span></span>

<span data-ttu-id="a2ae7-164">數位簽章除了 Windows Defender 撤銷之外，還能防止將惡意的 Ime 安裝到 Windows 8 系統上。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-164">Digital signing, in addition to revocation by Windows Defender, prevents malicious IMEs from being installed onto the Windows 8 system.</span></span> <span data-ttu-id="a2ae7-165">身分識別驗證之後，會以數位方式簽署協力廠商輸入的 .dll。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-165">Upon identity verification, a third-party IME’s .dll is digitally signed.</span></span> <span data-ttu-id="a2ae7-166">只有具有這個數位簽章的 Ime 可以安裝到系統上，而不會對使用者顯示重大警告訊息。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-166">Only IMEs that have this digital signature can be installed onto the system without having a critical warning message appear to the user.</span></span> <span data-ttu-id="a2ae7-167">使用者可以報告惡意的 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-167">Users can report malicious IMEs.</span></span> <span data-ttu-id="a2ae7-168">當 IME 判斷為惡意之後，Windows Defender 會將它從 Windows 系統中移除。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-168">After an IME has been determined to be malicious, Windows Defender removes it from the Windows system.</span></span>

<span data-ttu-id="a2ae7-169">**Text Services Framework (TSF)**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-169">**Text Services Framework**</span></span>

<span data-ttu-id="a2ae7-170">IME 必須是 TSF 感知，才能在 Windows 8 中執行。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-170">The IME must be TSF-aware in order to be able to run in Windows 8.</span></span> <span data-ttu-id="a2ae7-171">Windows 8 封鎖在 Windows Store 應用程式中執行的非 TSF 感知 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-171">Windows 8 blocks non-TSF-aware IMEs from running in Windows Store apps.</span></span> <span data-ttu-id="a2ae7-172">當應用程式啟動時，TSF 會針對使用者已選取到應用程式進程中的 IME 載入輸入輸入。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-172">When an app is started, TSF loads the IME .dll for the IME that the user has selected into the app process.</span></span>

> [!Note]  
> <span data-ttu-id="a2ae7-173">為了在 Windows Store 應用程式與桌面應用程式之間提供個別的功能或 Ui，TSF 所載入的 .dll 可以檢查載入的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-173">To provide separate functionality or UIs between Windows Store apps and desktop apps, the .dll loaded by TSF can check which type of app it is being loaded into.</span></span> <span data-ttu-id="a2ae7-174">IME 會呼叫 [ITfThreadMgrEx：： GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) 方法，並檢查 TF \_ TMF \_ IMMERSIVEMODE 旗標，並根據結果觸發不同的應用程式邏輯。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-174">The IME calls the [ITfThreadMgrEx::GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) method and checks the TF\_TMF\_IMMERSIVEMODE flag, and can trigger different app logic depending on the result.</span></span>

 

<span data-ttu-id="a2ae7-175">當 IME 載入至 Windows Store 應用程式時，它會受限於與應用程式本身相同的應用程式容器限制。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-175">When an IME is loaded into a Windows Store app, it is subject to the same app container restrictions as the app itself.</span></span> <span data-ttu-id="a2ae7-176">這種行為可確保 Ime 無法違反 Windows Store 應用程式安全性合約，儘管可以存取桌面 SDK (，因為它們不是由 Windows Store) 發佈或認證。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-176">This behavior ensures that IMEs are not able to violate Windows Store app security contracts, despite having access to the desktop SDK (because they are not distributed or certified by the Windows Store).</span></span> <span data-ttu-id="a2ae7-177">某些 Ime 目前執行的函式會在應用程式容器內受到影響。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-177">Some functions that IMEs currently perform are affected inside an app container.</span></span> <span data-ttu-id="a2ae7-178">這些函數包括：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-178">Those functions include:</span></span>

-   <span data-ttu-id="a2ae7-179">字典檔</span><span class="sxs-lookup"><span data-stu-id="a2ae7-179">Dictionary files</span></span>
-   <span data-ttu-id="a2ae7-180">網際網路更新</span><span class="sxs-lookup"><span data-stu-id="a2ae7-180">Internet updating</span></span>
-   <span data-ttu-id="a2ae7-181">即時學習</span><span class="sxs-lookup"><span data-stu-id="a2ae7-181">On-the-fly learning</span></span>
-   <span data-ttu-id="a2ae7-182">在進程之間共用資訊</span><span class="sxs-lookup"><span data-stu-id="a2ae7-182">Sharing info between processes</span></span>

<span data-ttu-id="a2ae7-183">如需詳細資訊，請參閱 Windows 8 IME 指導方針。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-183">See the Windows 8 IME Guidelines for more info.</span></span>

<span data-ttu-id="a2ae7-184">舊版 Ime 無法在 Windows Store 應用程式中運作，以避免可能發生不正確的使用者體驗，包括系統阻礙。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-184">Legacy IMEs do not work in Windows Store apps in order to avoid the potential for bad user experiences including system stoppages.</span></span> <span data-ttu-id="a2ae7-185">與 Windows Store 應用程式相容的 Ime 必須透過設定指出此相容性的旗標來自我宣告。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-185">IMEs that are compatible with the Windows Store apps must self-declare by setting a flag indicating this compatibility.</span></span> <span data-ttu-id="a2ae7-186">此旗標是由 TF INPUTPROCESSORPROFILE 結構中的 TSF 所提供 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-186">This flag is provided by TSF in the TF\_INPUTPROCESSORPROFILE structure.</span></span> <span data-ttu-id="a2ae7-187">有關如何使用此旗標將協力廠商 IME 宣告為 Windows Store 應用程式相容的詳細資料，將會記載並公佈在 Windows 8 IME 指導方針中。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-187">Details regarding how to use this flag to declare a third-party IME as Windows Store app-compatible will be documented and posted publicly in the Windows 8 IME Guidelines.</span></span>

<span data-ttu-id="a2ae7-188">您可以在桌面應用程式或 Windows Store 應用程式中，執行與 Windows Store 應用程式相容的 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-188">IMEs that are compatible with Windows Store apps are allowed to run in either desktop apps or Windows Store apps.</span></span> <span data-ttu-id="a2ae7-189">不相容的 Ime 只能在桌面進程中執行。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-189">IMEs that are not compatible can only run in desktop processes.</span></span>

<span data-ttu-id="a2ae7-190">**User Interface** (使用者介面)</span><span class="sxs-lookup"><span data-stu-id="a2ae7-190">**User interface**</span></span>

<span data-ttu-id="a2ae7-191">雖然協力廠商 Ime 可以存取桌面視窗化 Api，但它們必須遵循與執行應用程式相同的 windows API 限制。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-191">Although third-party IMEs have access to desktop windowing APIs, they must follow the same window API restrictions as the app they are running in.</span></span> <span data-ttu-id="a2ae7-192">例如，在傳統型應用程式中使用中時，IME 無法在 Windows Store 應用程式上繪製。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-192">For example, an IME cannot draw on top of a Windows Store app while active in a desktop app.</span></span> <span data-ttu-id="a2ae7-193">API 限制的目標是要避免這些情況：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-193">API restrictions are targeted to prevent these scenarios:</span></span>

-   <span data-ttu-id="a2ae7-194">從 Windows Store 應用程式取得焦點的桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="a2ae7-194">Desktop apps taking focus from Windows Store apps</span></span>
-   <span data-ttu-id="a2ae7-195">Windows Store 應用程式中的桌面應用程式繪圖</span><span class="sxs-lookup"><span data-stu-id="a2ae7-195">Desktop apps drawing in Windows Store app</span></span>
-   <span data-ttu-id="a2ae7-196">桌面應用程式干擾 Windows Store 應用程式</span><span class="sxs-lookup"><span data-stu-id="a2ae7-196">Desktop apps interfering with Windows Store apps</span></span>

<span data-ttu-id="a2ae7-197">**觸控鍵盤支援**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-197">**Touch keyboard support**</span></span>

<span data-ttu-id="a2ae7-198">雖然觸控鍵盤 (TKB) 支援仍然可供協力廠商的 IME 廠商使用，但 Windows 8 中不提供可完全自訂和整合的觸控鍵盤體驗。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-198">While touch keyboard (TKB) support is still available to third-party IME vendors, a fully customizable and integrated touch keyboard experience is not provided in Windows 8.</span></span> <span data-ttu-id="a2ae7-199">但是，協力廠商 Ime 可以對應其 Ime 與針對觸控優化的鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-199">However, third-party IMEs can map their IMEs with the keyboard layout optimized for touch.</span></span> <span data-ttu-id="a2ae7-200">Windows 軟輸入面板 (SIP) 預設會提供協力廠商 Ime 的傳統鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-200">The Windows Soft Input Panel (SIP) provides a classic keyboard layout by default for third-party IMEs.</span></span> <span data-ttu-id="a2ae7-201">由於傳統鍵盤產生的按鍵事件與硬體鍵盤的運作方式類似，因此協力廠商的 Ime 目前沒有特殊的執行需求可使用觸控鍵盤。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-201">Because the classic keyboard generates key events similar to how a hardware keyboard does, there is currently no special implementation requirement for third-party IMEs to work with a touch keyboard.</span></span> <span data-ttu-id="a2ae7-202">硬體金鑰事件的輸入處理也會處理來自傳統觸控配置的重要事件。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-202">The input handling for hardware key events will also handle key events from classic touch layouts.</span></span>

> [!Note]  
> <span data-ttu-id="a2ae7-203">注意：如果 TKB 支援已擴充為包含優化的鍵盤配置，則 Ime 可能需要開始處理 Unicode 輸入事件。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-203">Note: IMEs might need to begin handling Unicode input events if TKB support is extended to include optimized keyboard layouts as well.</span></span>

 

<span data-ttu-id="a2ae7-204">協力廠商 IME 可以選擇針對其 IME 使用優化的鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-204">A third-party IME can choose to use the optimized keyboard layout for their IME.</span></span> <span data-ttu-id="a2ae7-205">如需詳細資訊，請參閱協力廠商輸入法指導方針。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-205">See the third-party IME Guideline for more info.</span></span>

<span data-ttu-id="a2ae7-206">確定您的候選窗格的 UI (和其他 UI 元素) 不會繪製在觸摸鍵盤之下。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-206">Make sure that your candidate pane’s UI (and other UI elements) are not drawn underneath the touch keyboard.</span></span> <span data-ttu-id="a2ae7-207">在大部分情況下，應用程式應調整其視窗的大小，以考慮觸控鍵盤。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-207">In most cases, the app should resize its window to account for the touch keyboard.</span></span> <span data-ttu-id="a2ae7-208">但是，如果應用程式沒有這麼做，Ime 仍可以使用 InputPaneFramework API 來瞭解觸控鍵盤的位置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-208">However, if an app doesn’t do this, IMEs can still use the InputPaneFramework API to learn the position of the touch keyboard.</span></span> <span data-ttu-id="a2ae7-209">協力廠商 Ime 可以使用此 API 來取得觸控鍵盤在繪製候選 (或其他) Ui 之前所耗用的螢幕空間，以及重新排列其 UI，以避免在觸摸鍵盤下進行繪製。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-209">Third-party IMEs can use this API to get the screen space consumed by the touch keyboard prior to drawing candidate (or other) UIs, and reflow their UI to avoid drawing underneath the touch keyboard.</span></span>

<span data-ttu-id="a2ae7-210">**搜索**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-210">**Searching**</span></span>

<span data-ttu-id="a2ae7-211">在 Windows 8 中，Windows Store 應用程式可以藉由執行 [搜尋合約](/previous-versions/windows/apps/hh464906(v=win.10)) 並與 [搜尋] 窗格整合，輕鬆地為使用者提供搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-211">In Windows 8, Windows Store apps can easily provide their users with search features by implementing the [search contract](/previous-versions/windows/apps/hh464906(v=win.10)) and integrating with the Search pane.</span></span> <span data-ttu-id="a2ae7-212">[搜尋] 窗格是讓使用者在所有應用程式中執行搜尋的中心位置。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-212">The Search pane is a central location for users to perform searches across all their apps.</span></span> <span data-ttu-id="a2ae7-213">Windows 可協助使用 [搜尋] 窗格的應用程式，讓他們的使用者盡可能快速地前往。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-213">Windows helps apps that use the Search pane get their users where they want to go as fast as possible.</span></span> <span data-ttu-id="a2ae7-214">尤其是針對 IME 使用者，它提供了獨特的搜尋體驗，可讓相容的 Ime 與 Windows 8 整合，以提高效率和可用性。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-214">In particular, for IME users, it provides a unique search experience that lets compatible IMEs integrate with the Windows 8 for greater efficiency and usability.</span></span>

<span data-ttu-id="a2ae7-215">如果 IME 符合下列準則，則 IME 與整合式搜尋體驗相容：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-215">An IME is compatible with the integrated search experience if it meets these criteria:</span></span>

-   <span data-ttu-id="a2ae7-216">與 Windows Store 應用程式環境相容</span><span class="sxs-lookup"><span data-stu-id="a2ae7-216">Is compatible with the Windows Store app environment</span></span>
-   <span data-ttu-id="a2ae7-217">實行 TFS UILess 模式 Api</span><span class="sxs-lookup"><span data-stu-id="a2ae7-217">Implements TFS UILess mode APIs</span></span>
-   <span data-ttu-id="a2ae7-218">實行 TFS 搜尋整合 Api：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-218">Implements TFS search integration APIs:</span></span>
-   -   <span data-ttu-id="a2ae7-219">ItfSearchCandidateProvider</span><span class="sxs-lookup"><span data-stu-id="a2ae7-219">ItfSearchCandidateProvider</span></span>
    -   <span data-ttu-id="a2ae7-220">ItfSearchHardwareKeyboardBehaviors</span><span class="sxs-lookup"><span data-stu-id="a2ae7-220">ItfSearchHardwareKeyboardBehaviors</span></span>

<span data-ttu-id="a2ae7-221">在 [搜尋] 窗格中啟用時，相容的 IME 會置於 UILess 模式，而且無法顯示其 UI。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-221">When activated in the Search pane, the compatible IME is placed in UILess mode and cannot show its UI.</span></span> <span data-ttu-id="a2ae7-222">相反地，它會將轉換候選項目傳送給 Windows，然後將其顯示在內嵌候選清單控制項中。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-222">Instead, it sends conversion candidates to Windows, which will then display them in the inline candidate list control.</span></span>

<span data-ttu-id="a2ae7-223">IME 也會傳送應該用來執行目前搜尋的 Windows 候選項目，這些候選項目可以與轉換候選項目相同，或可針對搜尋量身打造。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-223">The IME also sends Windows candidates that should be used to run the current search – these candidates could be the same as the conversion candidates, or could be tailored for search.</span></span> <span data-ttu-id="a2ae7-224">良好的搜尋候選人符合下列準則：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-224">Good search candidates meet these criteria:</span></span>

-   <span data-ttu-id="a2ae7-225">沒有前置詞重迭</span><span class="sxs-lookup"><span data-stu-id="a2ae7-225">No prefix overlap</span></span>
-   <span data-ttu-id="a2ae7-226">沒有僅限完成的預測候選 () </span><span class="sxs-lookup"><span data-stu-id="a2ae7-226">No prediction candidate (only completion)</span></span>

<span data-ttu-id="a2ae7-227">不符合準則且與搜尋不相容的 Ime 會以與其他 Windows Store 應用程式控制的相同方式顯示，而且無法利用 UI 整合和搜尋候選項目。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-227">IMEs that do not meet the criteria and are not compatible with search are shown in the same way as in other Windows Store app controls and are not able to take advantage of UI integration and search candidates.</span></span> <span data-ttu-id="a2ae7-228"> (的應用程式只會在使用者撰寫完成之後才接收查詢。 ) </span><span class="sxs-lookup"><span data-stu-id="a2ae7-228">(Apps receive queries only after the user is done composing.)</span></span>

<span data-ttu-id="a2ae7-229">當支援搜尋合約的應用程式收到查詢時，查詢事件將會包含 "queryTextAlternatives" 陣列，其中包含所有已知的替代方案，並根據最相關的 (可能) 最相關的 (不太可能) 。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-229">When an app that supports the search contract receives a query, the query event will include a “queryTextAlternatives” array containing all known alternatives, ranked from the most relevant (likely) to least relevant (unlikely).</span></span> <span data-ttu-id="a2ae7-230">每當提供替代專案時，應用程式應該將每個替代方案視為查詢，並傳回符合任何替代專案的所有結果 (如同使用者已同時發出多個查詢) ，基本上是對提供結果的服務發出「或」查詢。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-230">Whenever alternatives are provided, the app should treat each alternative as a query, and return all results that match any of the alternatives (as if the user had issued multiple queries at the same time), essentially issuing an “or” query to the service providing the results.</span></span> <span data-ttu-id="a2ae7-231">為了增強效能，應用程式通常會限制比對10個最相關的替代方案。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-231">To enhance performance, apps will often limit matching to the 10 most relevant alternatives.</span></span>

<span data-ttu-id="a2ae7-232">**IME 數位簽章**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-232">**IME digital signature**</span></span>

<span data-ttu-id="a2ae7-233">所有協力廠商的 Ime 都必須經過數位簽署，才能安裝到 Windows 8 系統作為 IME。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-233">All third-party IMEs must be digitally signed in order to be installed onto the Windows 8 system as an IME.</span></span> <span data-ttu-id="a2ae7-234">使用 SmartScreen 時，使用者可以在從 web 下載未簽署的 IME 時看到警告訊息。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-234">Using SmartScreen, users can see a warning message when downloading an unsigned IME from the web.</span></span> <span data-ttu-id="a2ae7-235">取得憑證並簽署檔案：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-235">To obtain a certificate and sign your files:</span></span>

-   <span data-ttu-id="a2ae7-236">**使用 Authenticode 簽章以數位方式簽署程式**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-236">**Use an Authenticode signature to digitally sign programs**</span></span>
    -   <span data-ttu-id="a2ae7-237">從 Windows 支援的許多憑證授權單位單位之一取得有效的 Authenticode 程式碼簽署憑證</span><span class="sxs-lookup"><span data-stu-id="a2ae7-237">Obtain a valid Authenticode code signing certificate from one of the many certificate authorities supported by Windows</span></span>
    -   <span data-ttu-id="a2ae7-238">使用開發工具 (例如 [signtool.exe](../seccrypto/signtool.md)) 來簽署應用程式，再進行散發</span><span class="sxs-lookup"><span data-stu-id="a2ae7-238">Use development tools (such as [signtool.exe](../seccrypto/signtool.md)) to sign the apps prior to distribution</span></span>
    -   <span data-ttu-id="a2ae7-239">如需程式碼簽署程式的詳細資訊和逐步說明，請參閱 [Authenticode 程式碼簽署](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing) blog 專案的須知事項</span><span class="sxs-lookup"><span data-stu-id="a2ae7-239">For more information and a step-by-step description of the code signing process, see the [Everything you need to know about Authenticode code signing](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing) blog entry</span></span>
-   <span data-ttu-id="a2ae7-240">**確定未偵測到下載為惡意程式碼**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-240">**Ensure downloads are not detected as malware**</span></span>
    -   <span data-ttu-id="a2ae7-241">偵測到並確認為惡意程式碼的下載程式，會影響下載的信譽以及用來簽署該檔案的數位憑證信譽</span><span class="sxs-lookup"><span data-stu-id="a2ae7-241">Downloaded programs that are detected and confirmed as malware affect both the download’s reputation and the reputation of the digital certificate used to sign that file</span></span>
-   <span data-ttu-id="a2ae7-242">**適用于 Windows 認證**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-242">**Apply for Windows certification**</span></span>
    -   <span data-ttu-id="a2ae7-243">造訪 MSDN 上的 Windows 應用程式認證頁面</span><span class="sxs-lookup"><span data-stu-id="a2ae7-243">Visit the Windows App Certification page on MSDN</span></span>

<span data-ttu-id="a2ae7-244">如需詳細資訊，請參閱下列有關數位簽章和程式碼簽署的文章：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-244">For more info, see these articles about digital signatures and code signing:</span></span>

-   <span data-ttu-id="a2ae7-245">[Authenticode 總覽](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-245">[Authenticode Overview](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))</span></span>
-   <span data-ttu-id="a2ae7-246">[確保完整性和真實性](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-246">[Ensuring Integrity and Authenticity](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="a2ae7-247">[程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-247">[Code Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
-   <span data-ttu-id="a2ae7-248">[什麼是數位憑證？](/previous-versions/office/developer/office2000/aa190113(v=office.10))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-248">[What are Digital Certificates?](/previous-versions/office/developer/office2000/aa190113(v=office.10))</span></span>

<span data-ttu-id="a2ae7-249">如果 **未** 簽署 ime，當使用者嘗試下載 ime 時，會收到這個警告訊息：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-249">If an IME **is not** signed, the user receives this warning message when they try to download the IME:</span></span>

![輸入法未簽署警告訊息](images/downloadwarning02-fhu-ivu.png)

<span data-ttu-id="a2ae7-251">如果 IME 經過簽署，使用者會看到下列訊息：</span><span class="sxs-lookup"><span data-stu-id="a2ae7-251">If an IME is signed, users see this message instead:</span></span>

![ime 是已簽署的訊息](images/downloadwarning01-fhu-vcu.png)

<span data-ttu-id="a2ae7-253">根據這些通知，使用者可以選擇是否要刪除檔案，或忽略警告並執行下載的程式。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-253">Based on these notifications, users can choose whether to delete the file or ignore the warning and run the downloaded program.</span></span>

<span data-ttu-id="a2ae7-254">**IME 撤銷**</span><span class="sxs-lookup"><span data-stu-id="a2ae7-254">**IME revocation**</span></span>

<span data-ttu-id="a2ae7-255">您可以使用 Windows Defender，從系統中移除惡意或未遵循 Windows 8 IME 指導方針的 Ime。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-255">IMEs that are malicious or that do not follow the Windows 8 IME Guidelines can be removed from the system by using Windows Defender.</span></span> <span data-ttu-id="a2ae7-256">如需有關惡意 Ime 的詳細資訊，請參閱 [Windows 8 中的協力廠商 ime](/previous-versions/windows/apps/hh967426(v=win.10))的相關文章。</span><span class="sxs-lookup"><span data-stu-id="a2ae7-256">For more info about malicious IMEs, see the article on [Third-party IMEs in Windows 8](/previous-versions/windows/apps/hh967426(v=win.10)).</span></span>

## <a name="resources"></a><span data-ttu-id="a2ae7-257">資源</span><span class="sxs-lookup"><span data-stu-id="a2ae7-257">Resources</span></span>

-   [<span data-ttu-id="a2ae7-258">ITfThreadMgrEx：： Get Active Flags 方法</span><span class="sxs-lookup"><span data-stu-id="a2ae7-258">ITfThreadMgrEx::Get Active Flags method</span></span>](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [<span data-ttu-id="a2ae7-259">SignTool</span><span class="sxs-lookup"><span data-stu-id="a2ae7-259">SignTool</span></span>](../seccrypto/signtool.md)
-   [<span data-ttu-id="a2ae7-260">Authenticode 程式碼簽署的所有須知</span><span class="sxs-lookup"><span data-stu-id="a2ae7-260">Everything you need to know about Authenticode Code Signing</span></span>](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   <span data-ttu-id="a2ae7-261">[Windows 應用程式合約和延伸模組](/previous-versions/windows/apps/hh464906(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-261">[Windows app contracts and extensions](/previous-versions/windows/apps/hh464906(v=win.10))</span></span>
-   [<span data-ttu-id="a2ae7-262">Windows 8 桌面應用程式的認證需求</span><span class="sxs-lookup"><span data-stu-id="a2ae7-262">Certification requirements for Windows 8 desktop apps</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="a2ae7-263">Windows 應用程式的認證需求</span><span class="sxs-lookup"><span data-stu-id="a2ae7-263">Certification requirements for Windows apps</span></span>](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [<span data-ttu-id="a2ae7-264">使用 Windows 應用程式認證套件</span><span class="sxs-lookup"><span data-stu-id="a2ae7-264">Using the Windows App Certification Kit</span></span>](../win_cert/using-the-windows-app-certification-kit.md)
-   <span data-ttu-id="a2ae7-265">[Authenticode 總覽](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-265">[Authenticode Overview](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))</span></span>
-   <span data-ttu-id="a2ae7-266">[確保完整性和真實性](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)</span><span class="sxs-lookup"><span data-stu-id="a2ae7-266">[Ensuring Integrity and Authenticity](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)</span></span>
-   <span data-ttu-id="a2ae7-267">[程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-267">[Code Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
-   <span data-ttu-id="a2ae7-268">[什麼是數位憑證？](/previous-versions/office/developer/office2000/aa190113(v=office.10))</span><span class="sxs-lookup"><span data-stu-id="a2ae7-268">[What are Digital Certificates?](/previous-versions/office/developer/office2000/aa190113(v=office.10))</span></span>

 

 