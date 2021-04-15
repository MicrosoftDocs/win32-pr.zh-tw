---
title: 適用于上線類型2線上商店的驗證測試
description: 本主題說明 Microsoft 將執行以驗證您的 Type 2 線上商店的測試。 Microsoft 要求您必須先執行這些測試，才能提交候選版。 您的線上商店必須成功通過這些測試才能進行發佈。
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player 線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372241"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="71698-106">適用于上線類型2線上商店的驗證測試</span><span class="sxs-lookup"><span data-stu-id="71698-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="71698-107">本主題說明 Microsoft 將執行以驗證您的 Type 2 線上商店的測試。</span><span class="sxs-lookup"><span data-stu-id="71698-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="71698-108">Microsoft 要求您必須先執行這些測試，才能提交候選版。</span><span class="sxs-lookup"><span data-stu-id="71698-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="71698-109">您的線上商店必須成功通過這些測試才能進行發佈。</span><span class="sxs-lookup"><span data-stu-id="71698-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="71698-110">如果您的商店是類型1而不是類型2，您可以使用本主題作為指導方針，以瞭解類型1存放區所涵蓋的憑證測試範圍。</span><span class="sxs-lookup"><span data-stu-id="71698-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="71698-111">針對類型1存放區的一組完整測試，請聯絡 [Microsoft 支援服務](https://support.microsoft.com/ph/7763#tab0)。</span><span class="sxs-lookup"><span data-stu-id="71698-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="71698-112">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="71698-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="71698-113">測試檢查清單</span><span class="sxs-lookup"><span data-stu-id="71698-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="71698-114">測試階段準備</span><span class="sxs-lookup"><span data-stu-id="71698-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="71698-115">測試環境</span><span class="sxs-lookup"><span data-stu-id="71698-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="71698-116">組態和設定</span><span class="sxs-lookup"><span data-stu-id="71698-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="71698-117">設定測試電腦</span><span class="sxs-lookup"><span data-stu-id="71698-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="71698-118">設定存放區</span><span class="sxs-lookup"><span data-stu-id="71698-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="71698-119">建立帳戶</span><span class="sxs-lookup"><span data-stu-id="71698-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="71698-120">設定認證快取</span><span class="sxs-lookup"><span data-stu-id="71698-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="71698-121">取得內容</span><span class="sxs-lookup"><span data-stu-id="71698-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="71698-122">串流內容</span><span class="sxs-lookup"><span data-stu-id="71698-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="71698-123">取得內容</span><span class="sxs-lookup"><span data-stu-id="71698-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="71698-124">燒錄內容</span><span class="sxs-lookup"><span data-stu-id="71698-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="71698-125">傳送內容</span><span class="sxs-lookup"><span data-stu-id="71698-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="71698-126">存放區功能</span><span class="sxs-lookup"><span data-stu-id="71698-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="71698-127">管理帳戶</span><span class="sxs-lookup"><span data-stu-id="71698-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="71698-128">管理資訊中心</span><span class="sxs-lookup"><span data-stu-id="71698-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="71698-129">商店互動</span><span class="sxs-lookup"><span data-stu-id="71698-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="71698-130">對使用中的存放區產生</span><span class="sxs-lookup"><span data-stu-id="71698-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="71698-131">防止經過測試的存放區接管使用中的存放區</span><span class="sxs-lookup"><span data-stu-id="71698-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="71698-132">以 High-Contrast 模式存取存放區</span><span class="sxs-lookup"><span data-stu-id="71698-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="71698-133">保護存放區</span><span class="sxs-lookup"><span data-stu-id="71698-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="71698-134">測試檢查清單</span><span class="sxs-lookup"><span data-stu-id="71698-134">Test Checklist</span></span>

<span data-ttu-id="71698-135">您可以使用下表中的檢查清單來驗證您想要帶到面板上的 [類型 2] 線上商店。</span><span class="sxs-lookup"><span data-stu-id="71698-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="71698-136">測試</span><span class="sxs-lookup"><span data-stu-id="71698-136">Test</span></span>

<span data-ttu-id="71698-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="71698-137">Windows XP</span></span>

<span data-ttu-id="71698-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71698-138">Windows Vista</span></span>

<span data-ttu-id="71698-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71698-139">Windows 7</span></span>

<span data-ttu-id="71698-140">結果 (通過/失敗/不適用) </span><span class="sxs-lookup"><span data-stu-id="71698-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="71698-141">32</span><span class="sxs-lookup"><span data-stu-id="71698-141">32</span></span>

<span data-ttu-id="71698-142">64</span><span class="sxs-lookup"><span data-stu-id="71698-142">64</span></span>

<span data-ttu-id="71698-143">32</span><span class="sxs-lookup"><span data-stu-id="71698-143">32</span></span>

<span data-ttu-id="71698-144">64</span><span class="sxs-lookup"><span data-stu-id="71698-144">64</span></span>

<span data-ttu-id="71698-145">32</span><span class="sxs-lookup"><span data-stu-id="71698-145">32</span></span>

<span data-ttu-id="71698-146">64</span><span class="sxs-lookup"><span data-stu-id="71698-146">64</span></span>

1. <span data-ttu-id="71698-147">確認是否已安裝軟體。</span><span class="sxs-lookup"><span data-stu-id="71698-147">Verify that software installs.</span></span>

2. <span data-ttu-id="71698-148">確認已卸載軟體。</span><span class="sxs-lookup"><span data-stu-id="71698-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="71698-149">確認軟體不會在紙匣中執行。</span><span class="sxs-lookup"><span data-stu-id="71698-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="71698-150">確認 [存放區] 索引標籤可運作。</span><span class="sxs-lookup"><span data-stu-id="71698-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="71698-151">確認存放區有建立新帳戶的選項。</span><span class="sxs-lookup"><span data-stu-id="71698-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="71698-152">確認建立的帳戶可以登入。</span><span class="sxs-lookup"><span data-stu-id="71698-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="71698-153">確認存放區有儲存使用者資訊的選項。</span><span class="sxs-lookup"><span data-stu-id="71698-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="71698-154">確認認證快取存在且正常運作。</span><span class="sxs-lookup"><span data-stu-id="71698-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="71698-155">確認如果使用者未快取認證，系統會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="71698-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="71698-156">確認所有可用的內容資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="71698-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="71698-157">確認內容已在 Microsoft Windows Media Player 中播放。</span><span class="sxs-lookup"><span data-stu-id="71698-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="71698-158">確認計算的價格正確。</span><span class="sxs-lookup"><span data-stu-id="71698-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="71698-159">確認已購買的內容已下載至程式庫。</span><span class="sxs-lookup"><span data-stu-id="71698-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="71698-160">確認已下載中繼資料以供購買。</span><span class="sxs-lookup"><span data-stu-id="71698-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="71698-161">確認媒體許可權是否正確以進行購買。</span><span class="sxs-lookup"><span data-stu-id="71698-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="71698-162">確認購買的內容可以播放。</span><span class="sxs-lookup"><span data-stu-id="71698-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="71698-163">確認按一下 [ **購買** ] 或 [ **購物** ] 按鈕會切換至商店。</span><span class="sxs-lookup"><span data-stu-id="71698-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="71698-164">確認已下載購買的內容。</span><span class="sxs-lookup"><span data-stu-id="71698-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="71698-165">確認已購買的內容可以燒錄。</span><span class="sxs-lookup"><span data-stu-id="71698-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="71698-166">確認已減少燒錄計數。</span><span class="sxs-lookup"><span data-stu-id="71698-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="71698-167">確認內容可以傳輸到另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="71698-168">確認內容已傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="71698-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="71698-169">確認同步處理計數已減少。</span><span class="sxs-lookup"><span data-stu-id="71698-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="71698-170">確認購買歷程記錄會追蹤先前的購買專案。</span><span class="sxs-lookup"><span data-stu-id="71698-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="71698-171">確認先前的購買可以還原。</span><span class="sxs-lookup"><span data-stu-id="71698-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="71698-172">確認存放區的功能，以管理多部電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="71698-173">確認資訊中心預設為關閉。</span><span class="sxs-lookup"><span data-stu-id="71698-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="71698-174">確認資訊中心在立即播放的區域中有媒體資訊。</span><span class="sxs-lookup"><span data-stu-id="71698-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="71698-175">確認連結會流覽至存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="71698-176">確認測試的存放區會產生至使用中的存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="71698-177">確認測試的存放區不會佔用目前的存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="71698-178">確認可在高對比模式下存取存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="71698-179">確認存放區是安全的。</span><span class="sxs-lookup"><span data-stu-id="71698-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="71698-180">測試階段準備</span><span class="sxs-lookup"><span data-stu-id="71698-180">Test Pass Preparation</span></span>

<span data-ttu-id="71698-181">在您執行測試階段之前，您應該確定存放區和測試帳戶已準備好進行測試。</span><span class="sxs-lookup"><span data-stu-id="71698-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="71698-182">在開始之前，您應該先判斷下列資訊。</span><span class="sxs-lookup"><span data-stu-id="71698-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="71698-183">如果您可以在測試行程之前的幾天判斷資訊，將會更有效率地執行傳遞。</span><span class="sxs-lookup"><span data-stu-id="71698-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="71698-184">判斷有關存放區所提供之測試帳戶的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="71698-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="71698-185">帳戶和密碼可讓使用者登入</span><span class="sxs-lookup"><span data-stu-id="71698-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="71698-186">針對商店所提供的每一種商務模式，都能正確且適當地進行帳戶的投資</span><span class="sxs-lookup"><span data-stu-id="71698-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="71698-187">帳戶適用于所有要測試的地區設定，如果帳戶不能跨地區設定，則會有每個地區設定的帳戶</span><span class="sxs-lookup"><span data-stu-id="71698-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="71698-188">判斷要測試的地區設定。</span><span class="sxs-lookup"><span data-stu-id="71698-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="71698-189">判斷要測試的語言。</span><span class="sxs-lookup"><span data-stu-id="71698-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="71698-190">判斷有關測試環境的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="71698-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="71698-191">適用于 Windows XP、Windows Vista 和 Windows 7 的即時商店</span><span class="sxs-lookup"><span data-stu-id="71698-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="71698-192">要測試的非即時存放區</span><span class="sxs-lookup"><span data-stu-id="71698-192">The non-live store to test</span></span>
    -   <span data-ttu-id="71698-193">確認所有版本的作業系統和所有版本的 Windows Media Player 平臺都能看到測試的非即時存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="71698-194">判斷下列要測試之存放區的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="71698-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="71698-195">存放區名稱</span><span class="sxs-lookup"><span data-stu-id="71698-195">Store name</span></span>
    -   <span data-ttu-id="71698-196">預期的商店索引標籤標誌圖形和標籤</span><span class="sxs-lookup"><span data-stu-id="71698-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="71698-197">存放區是否適用于所有作業系統版本？</span><span class="sxs-lookup"><span data-stu-id="71698-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="71698-198">這是待測商店的新版本嗎？</span><span class="sxs-lookup"><span data-stu-id="71698-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="71698-199">測試中的商店是否為類型1或類型2存放區？</span><span class="sxs-lookup"><span data-stu-id="71698-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="71698-200">商店類型是否已變更？</span><span class="sxs-lookup"><span data-stu-id="71698-200">Has the store type changed?</span></span>

-   <span data-ttu-id="71698-201">判斷您打算測試存放區的作業系統版本和平臺。</span><span class="sxs-lookup"><span data-stu-id="71698-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="71698-202">判斷安裝程式和外掛程式是否適用于所有要測試的作業系統版本和平臺。</span><span class="sxs-lookup"><span data-stu-id="71698-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="71698-203">判斷是否需要流覽檔。</span><span class="sxs-lookup"><span data-stu-id="71698-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="71698-204">判斷有關存放區所提供媒體的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="71698-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="71698-205">格式</span><span class="sxs-lookup"><span data-stu-id="71698-205">Formats</span></span>
    -   <span data-ttu-id="71698-206">是否需要任何專屬軟體？</span><span class="sxs-lookup"><span data-stu-id="71698-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="71698-207">您是否必須測試所有媒體類型，或只測試一部分的媒體類型？</span><span class="sxs-lookup"><span data-stu-id="71698-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="71698-208">判斷下列媒體許可權的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="71698-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="71698-209">商店媒體是否有內容保護？</span><span class="sxs-lookup"><span data-stu-id="71698-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="71698-210">若是如此，請判斷媒體具有的內容保護類型。</span><span class="sxs-lookup"><span data-stu-id="71698-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="71698-211">若是如此，請判斷預期的受保護行為。</span><span class="sxs-lookup"><span data-stu-id="71698-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="71698-212">媒體許可權是否包含電腦對電腦共用？</span><span class="sxs-lookup"><span data-stu-id="71698-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="71698-213">同步許可權</span><span class="sxs-lookup"><span data-stu-id="71698-213">The sync rights</span></span>
    -   <span data-ttu-id="71698-214">燒錄許可權</span><span class="sxs-lookup"><span data-stu-id="71698-214">The burn rights</span></span>
    -   <span data-ttu-id="71698-215">播放權利</span><span class="sxs-lookup"><span data-stu-id="71698-215">The play rights</span></span>
    -   <span data-ttu-id="71698-216">到期日期（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="71698-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="71698-217">判斷您是否有足夠的媒體 (夠大的目錄) 來提供有意義的範例。</span><span class="sxs-lookup"><span data-stu-id="71698-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="71698-218">判斷階段通過的內容： RC 0、合規性等等。</span><span class="sxs-lookup"><span data-stu-id="71698-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="71698-219">判斷測試階段是否為特定類型：回歸、冒煙等。</span><span class="sxs-lookup"><span data-stu-id="71698-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="71698-220">測試環境</span><span class="sxs-lookup"><span data-stu-id="71698-220">Test Environment</span></span>

<span data-ttu-id="71698-221">您必須對下列設定進行測試：</span><span class="sxs-lookup"><span data-stu-id="71698-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="71698-222">Windows XP Service Pack 3 (SP3) 32 位和64位作業系統上的 Microsoft Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="71698-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="71698-223">Windows Vista 32 位和64位 (32 位 Windows Media Player) 作業系統上的 Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="71698-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="71698-224">Windows 7 32 位和64位 (32 位 Windows Media Player) 作業系統上的 Microsoft Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="71698-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="71698-225">雖然您必須在所有列出的作業系統版本和平臺上執行測試，但是32位版本的 Windows Vista 和 Windows 7 是目標作業系統版本的優先考慮。</span><span class="sxs-lookup"><span data-stu-id="71698-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="71698-226">您必須在所有平臺上測試任何軟體的安裝。</span><span class="sxs-lookup"><span data-stu-id="71698-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="71698-227">本主題中的螢幕擷取畫面使用虛構的商店 Proseware，來示範使用者介面的使用方式。</span><span class="sxs-lookup"><span data-stu-id="71698-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="71698-228">組態和設定</span><span class="sxs-lookup"><span data-stu-id="71698-228">Configuration and Setup</span></span>

<span data-ttu-id="71698-229">下列各節將說明如何設定和設定「類型2」線上商店的驗證測試。</span><span class="sxs-lookup"><span data-stu-id="71698-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="71698-230">設定測試電腦</span><span class="sxs-lookup"><span data-stu-id="71698-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="71698-231">請執行下列步驟來設定測試電腦：</span><span class="sxs-lookup"><span data-stu-id="71698-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="71698-232">藉由新增存放區專屬的登錄機碼，將測試電腦指向內容測試伺服器。</span><span class="sxs-lookup"><span data-stu-id="71698-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="71698-233">將 [ **地區及語言選項** ] 對話方塊中的值設定為適當的語言和地區設定。</span><span class="sxs-lookup"><span data-stu-id="71698-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="71698-234">若要設定語言，請選取 [ **格式** ] 索引標籤，然後從 [ **目前格式** ] 下拉式方塊中選取語言。</span><span class="sxs-lookup"><span data-stu-id="71698-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="71698-235">若要設定區域，請選取 [ **位置** ] 索引標籤，然後從 [ **目前位置** ] 下拉式方塊中選取區域。</span><span class="sxs-lookup"><span data-stu-id="71698-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="71698-236">此外，對於需要安裝外掛程式或存放區特定自訂軟體的存放區，您可能需要將系統地區設定變更為存放區地區設定的語言，以便進行安裝。</span><span class="sxs-lookup"><span data-stu-id="71698-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="71698-237">軟體安裝程式必須同時支援單位元組和雙位元組字元，而且必須在任何地區設定上執行。</span><span class="sxs-lookup"><span data-stu-id="71698-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="71698-238">您必須以原生地區設定進行測試。</span><span class="sxs-lookup"><span data-stu-id="71698-238">You must test in the native locale.</span></span> <span data-ttu-id="71698-239">若要設定原生地區設定，請開啟 [ **地區和語言** ] 對話方塊，選取 [系統 **管理** ] 索引標籤，然後按一下 [ **變更系統地區** 設定] 按鈕，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="71698-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="71698-240">按一下這個按鈕會顯示 [ **區域和語言設定** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="71698-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="71698-241">該對話方塊中的 [ **目前的系統地區設定** ] 下拉式方塊會變更系統地區設定。</span><span class="sxs-lookup"><span data-stu-id="71698-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="71698-242">下列螢幕擷取畫面顯示可設定區域和語言的索引標籤：</span><span class="sxs-lookup"><span data-stu-id="71698-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![[地區及語言選項] 對話方塊的螢幕擷取畫面](images/reg-lang-opt.png)

    ![顯示如何變更目前系統地區設定的螢幕擷取畫面](images/reg-lang-settings.png)

3.  <span data-ttu-id="71698-245">藉由設定 Windows Media Player 來播放視覺效果，關閉商店資訊中心的觀點。</span><span class="sxs-lookup"><span data-stu-id="71698-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="71698-246">平臺之間的主要差異在於，在 Windows Media Player 11 中，您一開始可以按一下 [ **立即播放**]，而在 Windows Media Player 12 中，則是以滑鼠右鍵按一下主視窗開始。</span><span class="sxs-lookup"><span data-stu-id="71698-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="71698-247">下列螢幕擷取畫面顯示在 Windows Media Player 11 中播放視覺效果的功能表選項順序：</span><span class="sxs-lookup"><span data-stu-id="71698-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![顯示如何在 windows media player 11 中播放視覺效果的螢幕擷取畫面](images/wmp11-visual.png)

    <span data-ttu-id="71698-249">下列螢幕擷取畫面顯示在 Windows Media Player 12 中播放視覺效果的功能表選項順序：</span><span class="sxs-lookup"><span data-stu-id="71698-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![顯示如何在 windows media player 12 中播放視覺效果的螢幕擷取畫面](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="71698-251">設定存放區</span><span class="sxs-lookup"><span data-stu-id="71698-251">Setting Up a Store</span></span>

<span data-ttu-id="71698-252">首先，請執行下列步驟來設定存放區，然後執行遵循初始步驟的步驟來確認存放區設定：</span><span class="sxs-lookup"><span data-stu-id="71698-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="71698-253">啟動 Windows Media Player 並等候數秒，以取得最新的 AllServices.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="71698-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="71698-254">針對 Windows XP 和 Windows Vista，若要選取線上商店，請先按一下 [媒體指南] 和 [線上商店] 視圖之間分割的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="71698-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="71698-255">然後，從功能表中按一下 **[流覽所有線上商店]**，然後按一下商店清單中的圖示來選取商店。</span><span class="sxs-lookup"><span data-stu-id="71698-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="71698-256">若為 Windows 7，請按一下 [媒體櫃] 流覽窗格中的按鈕，該按鈕會在 [ **媒體指南** ] 按鈕和 [ **線上商店** ] 按鈕之間進行分割。</span><span class="sxs-lookup"><span data-stu-id="71698-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="71698-257">然後，從功能表中按一下 **[流覽所有線上商店]**，然後按一下商店清單中的圖示來選取商店。</span><span class="sxs-lookup"><span data-stu-id="71698-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="71698-258">下列螢幕擷取畫面顯示如何選取 Windows Media Player 11 的線上商店：</span><span class="sxs-lookup"><span data-stu-id="71698-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![螢幕擷取畫面，顯示如何選取 windows media player 11 中的線上商店](images/wmp11-set-store.png)

    <span data-ttu-id="71698-260">下列螢幕擷取畫面顯示如何選取 Windows Media Player 12 中的線上商店：</span><span class="sxs-lookup"><span data-stu-id="71698-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![顯示如何在 windows media player 12 中選取線上商店的螢幕擷取畫面](images/wmp12-set-store.png)

3.  <span data-ttu-id="71698-262">遵循存放區中的指示，安裝使用該存放區所需的任何其他軟體。</span><span class="sxs-lookup"><span data-stu-id="71698-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="71698-263">**確認存放區設定**</span><span class="sxs-lookup"><span data-stu-id="71698-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="71698-264">確認軟體是否已安裝。</span><span class="sxs-lookup"><span data-stu-id="71698-264">Verify that the software installs.</span></span>

    <span data-ttu-id="71698-265">確認 OCX 外掛程式或存放區中的任何其他軟體都已下載並安裝，而不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="71698-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="71698-266">確認已卸載軟體。</span><span class="sxs-lookup"><span data-stu-id="71698-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="71698-267">確認在主控台的 [ **程式和功能** ] 專案中，存放區安裝的軟體會出現在 [ **卸載或變更程式** ] 清單中，並確認您可以從這份清單中卸載，而不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="71698-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="71698-268">確認軟體未在系統匣中執行。</span><span class="sxs-lookup"><span data-stu-id="71698-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="71698-269">確認在客戶同意下載商店軟體之前，存放區中的軟體都不會將圖示新增至時鐘左邊的程式通知區域 (中) 。</span><span class="sxs-lookup"><span data-stu-id="71698-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="71698-270">基本商店體驗不應要求安裝額外的軟體。</span><span class="sxs-lookup"><span data-stu-id="71698-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="71698-271">應該可以使用基本的媒體體驗，例如串流媒體。</span><span class="sxs-lookup"><span data-stu-id="71698-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="71698-272">有些存放區會安裝其他軟體，例如適用于頂級媒體體驗的下載管理員;如果圖示代表不同于 Windows Media Player 的應用程式，則這些存放區在系統匣中可以有圖示。</span><span class="sxs-lookup"><span data-stu-id="71698-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="71698-273">確認 [存放區] 索引標籤可運作。</span><span class="sxs-lookup"><span data-stu-id="71698-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="71698-274">確認 [存放區] 索引標籤已變更，以指出選取的存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="71698-275">若為具有 Windows Media Player 11 的 Windows XP 和 Windows Vista，請確認已針對深 Windows Media Player 11 背景顯示商店名稱和圖示。</span><span class="sxs-lookup"><span data-stu-id="71698-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="71698-276">針對 Windows Media Player 12 的 Windows 7，請確認在 [程式庫] 導覽窗格中的 [存放區名稱] 和 [圖示] 會顯示在服務選取器內容功能表中。</span><span class="sxs-lookup"><span data-stu-id="71698-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="71698-277">確認商店列在功能表中商店選取器清單的頂端。</span><span class="sxs-lookup"><span data-stu-id="71698-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="71698-278">如果類型2存放區是區域的精選 (預設) 存放區，將不會有 [ **新增目前的服務] 功能表** 選項。</span><span class="sxs-lookup"><span data-stu-id="71698-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="71698-279">下列螢幕擷取畫面顯示當您在 Windows Media Player 11 的右上角按一下索引標籤時，所顯示的功能表：</span><span class="sxs-lookup"><span data-stu-id="71698-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![顯示 windows media player 11 中 [存放區] 索引標籤的螢幕擷取畫面](images/wmp11-verify-store.png)

    <span data-ttu-id="71698-281">下列螢幕擷取畫面顯示當您在 Windows Media Player 12 的左下角按一下 [分割] 按鈕時，所顯示的功能表：</span><span class="sxs-lookup"><span data-stu-id="71698-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![顯示 windows media player 12 中 [存放區] 索引標籤的螢幕擷取畫面](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="71698-283">建立帳戶</span><span class="sxs-lookup"><span data-stu-id="71698-283">Creating an Account</span></span>

<span data-ttu-id="71698-284">**確認帳戶設定**</span><span class="sxs-lookup"><span data-stu-id="71698-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="71698-285">確認存放區有建立新帳戶的選項，然後依照儲存指示建立新的帳戶。</span><span class="sxs-lookup"><span data-stu-id="71698-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="71698-286">下列螢幕擷取畫面會反白顯示 [ **建立新帳戶** ] 按鈕，如 Windows Media Player 11 所示：</span><span class="sxs-lookup"><span data-stu-id="71698-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![顯示如何驗證 windows media player 11 帳戶設定的螢幕擷取畫面](images/wmp11-verify-account.png)

    <span data-ttu-id="71698-288">下列螢幕擷取畫面會反白顯示 [ **建立新帳戶** ] 按鈕，如 Windows Media Player 12：</span><span class="sxs-lookup"><span data-stu-id="71698-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![顯示如何驗證 windows media player 12 帳戶設定的螢幕擷取畫面](images/wmp12-verify-account.png)

2.  <span data-ttu-id="71698-290">確認您可以登入您所建立的帳戶。</span><span class="sxs-lookup"><span data-stu-id="71698-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="71698-291">設定認證快取</span><span class="sxs-lookup"><span data-stu-id="71698-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="71698-292">首先，請執行下列步驟來設定認證快取，然後執行遵循初始步驟的步驟來驗證認證快取設定：</span><span class="sxs-lookup"><span data-stu-id="71698-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="71698-293">在登入頁面上輸入認證，然後選取儲存使用者資訊的選項。</span><span class="sxs-lookup"><span data-stu-id="71698-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="71698-294">確認登入頁面具有可讓使用者快取認證的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="71698-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="71698-295">選用的認證快取是一個重要的安全點。</span><span class="sxs-lookup"><span data-stu-id="71698-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="71698-296">自動認證快取可以公開登入共用或公用電腦之使用者的個人識別資訊。</span><span class="sxs-lookup"><span data-stu-id="71698-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="71698-297">您應該提供可轉譯快取選項的核取方塊，以保護客戶資訊。</span><span class="sxs-lookup"><span data-stu-id="71698-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="71698-298">**驗證認證快取**</span><span class="sxs-lookup"><span data-stu-id="71698-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="71698-299">確認存放區具有 [ **儲存我的使用者資訊** ] 選項的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="71698-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="71698-300">關閉 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="71698-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="71698-301">重新開啟 Windows Media Player，並嘗試下載某些內容。</span><span class="sxs-lookup"><span data-stu-id="71698-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="71698-302">確認認證快取存在且正常運作。</span><span class="sxs-lookup"><span data-stu-id="71698-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="71698-303">登出存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="71698-304">關閉 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="71698-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="71698-305">重新開啟 Windows Media Player，並嘗試下載某些內容。</span><span class="sxs-lookup"><span data-stu-id="71698-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="71698-306">確認如果使用者未快取認證，系統會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="71698-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="71698-307">登出再嘗試使用存放區之後，系統應該會提示客戶輸入認證。</span><span class="sxs-lookup"><span data-stu-id="71698-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="71698-308">取得內容</span><span class="sxs-lookup"><span data-stu-id="71698-308">Content Acquisition</span></span>

<span data-ttu-id="71698-309">本節描述取得內容的各種方式，以及如何確認已取得該內容。</span><span class="sxs-lookup"><span data-stu-id="71698-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="71698-310">串流內容</span><span class="sxs-lookup"><span data-stu-id="71698-310">Streaming Content</span></span>

<span data-ttu-id="71698-311">從存放區串流所有可用的內容類型。</span><span class="sxs-lookup"><span data-stu-id="71698-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="71698-312">例如，串流電臺、影片、音訊和預覽內容。</span><span class="sxs-lookup"><span data-stu-id="71698-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="71698-313">**確認串流內容**</span><span class="sxs-lookup"><span data-stu-id="71698-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="71698-314">確認所有可用的內容資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="71698-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="71698-315">確認內容是在 Windows Media Player 中播放，而不是其他玩家或控制項。</span><span class="sxs-lookup"><span data-stu-id="71698-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="71698-316">取得內容</span><span class="sxs-lookup"><span data-stu-id="71698-316">Obtaining Content</span></span>

<span data-ttu-id="71698-317">請先執行下列步驟來購買內容，然後執行遵循初始步驟的步驟來確認購買並確認已下載內容：</span><span class="sxs-lookup"><span data-stu-id="71698-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="71698-318">啟動 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="71698-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="71698-319">登入測試帳戶。</span><span class="sxs-lookup"><span data-stu-id="71698-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="71698-320">流覽至要購買的內容。</span><span class="sxs-lookup"><span data-stu-id="71698-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="71698-321">依照商店專屬程式來購買內容。</span><span class="sxs-lookup"><span data-stu-id="71698-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="71698-322">**確認已購買及下載的內容**</span><span class="sxs-lookup"><span data-stu-id="71698-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="71698-323">確認計算的價格正確。</span><span class="sxs-lookup"><span data-stu-id="71698-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="71698-324">請確認價格正確，特別是當一次購買多個內容，並確認任何帳戶餘額資訊在購買後都會正確更新。</span><span class="sxs-lookup"><span data-stu-id="71698-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="71698-325">有些內容可以當作單一曲目來購買，有些則只做為專輯。</span><span class="sxs-lookup"><span data-stu-id="71698-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="71698-326">確認專輯價格不超過個別曲目的總和。</span><span class="sxs-lookup"><span data-stu-id="71698-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="71698-327">確認購買的內容下載至文件庫。</span><span class="sxs-lookup"><span data-stu-id="71698-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="71698-328">當下載完成時，流覽至 Windows Media Player 程式庫中下載的內容。</span><span class="sxs-lookup"><span data-stu-id="71698-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="71698-329">下載的內容位於目前使用者的文件庫中。</span><span class="sxs-lookup"><span data-stu-id="71698-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="71698-330">若為具有 Windows Media Player 11 的 Windows XP 和 Windows Vista，下載的內容會出現在 [文件庫] 流覽窗格中的 [程式庫]、[連結 **庫** ] 和 [ **歌曲**] 下</span><span class="sxs-lookup"><span data-stu-id="71698-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="71698-331">針對 Windows Media Player 12 的 Windows 7，下載至 Windows Media Player 程式庫的內容會出現在 [ **音樂**] 的 Windows Media Player 流覽窗格中。</span><span class="sxs-lookup"><span data-stu-id="71698-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="71698-332">確認購買的中繼資料已下載。</span><span class="sxs-lookup"><span data-stu-id="71698-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="71698-333">請確認下列資料行出現在 Windows Media Player 程式庫中 (在不) 的情況下新增這些資料行：</span><span class="sxs-lookup"><span data-stu-id="71698-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="71698-334">專輯演出者</span><span class="sxs-lookup"><span data-stu-id="71698-334">Album Artist</span></span>
    -   <span data-ttu-id="71698-335">標題</span><span class="sxs-lookup"><span data-stu-id="71698-335">Title</span></span>
    -   <span data-ttu-id="71698-336">專輯標題</span><span class="sxs-lookup"><span data-stu-id="71698-336">Album Title</span></span>
    -   <span data-ttu-id="71698-337">內容提供者</span><span class="sxs-lookup"><span data-stu-id="71698-337">Content Provider</span></span>
    -   <span data-ttu-id="71698-338">Genre</span><span class="sxs-lookup"><span data-stu-id="71698-338">Genre</span></span>

    <span data-ttu-id="71698-339">前面的資料行必須填入。</span><span class="sxs-lookup"><span data-stu-id="71698-339">The preceding columns must be populated.</span></span> <span data-ttu-id="71698-340">內容應該有專輯封面。</span><span class="sxs-lookup"><span data-stu-id="71698-340">Content should have album art.</span></span> <span data-ttu-id="71698-341">但是，不需要專輯封面就能通過驗證測試。</span><span class="sxs-lookup"><span data-stu-id="71698-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="71698-342">確認媒體許可權是否正確以進行購買。</span><span class="sxs-lookup"><span data-stu-id="71698-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="71698-343">針對每個下載的播放軌，以滑鼠右鍵按一下 **曲目，然後** 選取 [內容]，再選取 [ **媒體許可權** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="71698-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="71698-344">存放區可選擇使用媒體許可權來保護其內容，或者可以選擇不保護內容。</span><span class="sxs-lookup"><span data-stu-id="71698-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="71698-345">[ **媒體許可權** ] 索引標籤會藉由列出限制來反映該狀態，或指出內容不受保護。</span><span class="sxs-lookup"><span data-stu-id="71698-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="71698-346">存放區必須傳達其最新的媒體許可權計畫。</span><span class="sxs-lookup"><span data-stu-id="71698-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="71698-347">您必須根據此預期行為來確認實際的結果。</span><span class="sxs-lookup"><span data-stu-id="71698-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="71698-348">媒體許可權授權必須預先傳遞。</span><span class="sxs-lookup"><span data-stu-id="71698-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="71698-349">客戶不一定需要播放內容，也不需要經過其他程式來取得授權。</span><span class="sxs-lookup"><span data-stu-id="71698-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="71698-350">您必須將特定媒體許可權與存放區已適當地傳達給客戶的資訊進行比較。</span><span class="sxs-lookup"><span data-stu-id="71698-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="71698-351">許可權至少必須可轉讓給其他兩部電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="71698-352">客戶必須能夠燒錄媒體並進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="71698-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="71698-353">下列螢幕擷取畫面顯示受保護檔案的媒體許可權：</span><span class="sxs-lookup"><span data-stu-id="71698-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![顯示受保護檔案之媒體許可權的螢幕擷取畫面](images/media-rights-protected.png)

    <span data-ttu-id="71698-355">如果內容未受保護，[ **媒體許可權** ] 索引標籤會指出這項事實。</span><span class="sxs-lookup"><span data-stu-id="71698-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="71698-356">下列螢幕擷取畫面顯示未受保護檔案的媒體許可權：</span><span class="sxs-lookup"><span data-stu-id="71698-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![顯示未受保護檔案之媒體許可權的螢幕擷取畫面](images/media-rights-not-protected.png)

5.  <span data-ttu-id="71698-358">確認已購買的內容可供播放。</span><span class="sxs-lookup"><span data-stu-id="71698-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="71698-359">確認下載的內容在 Windows Media Player 中播放。</span><span class="sxs-lookup"><span data-stu-id="71698-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="71698-360">播放從商店購買且位於本機文件庫中，或串流預覽的任何內容。</span><span class="sxs-lookup"><span data-stu-id="71698-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="71698-361">請執行下列步驟，以 Windows Media Player 11 在 Windows XP 和 Windows Vista 中購買內容：</span><span class="sxs-lookup"><span data-stu-id="71698-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="71698-362">按一下 [ **立即播放** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="71698-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="71698-363">在 [清單] 窗格中，將滑鼠指標放在專輯封面上方以顯示 [ **購買** ] 連結。</span><span class="sxs-lookup"><span data-stu-id="71698-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="71698-364">按一下 [ **購買**]。</span><span class="sxs-lookup"><span data-stu-id="71698-364">Click **Buy**.</span></span>

    <span data-ttu-id="71698-365">下列螢幕擷取畫面顯示 Windows Media Player 11 中 **購買** 連結的位置：</span><span class="sxs-lookup"><span data-stu-id="71698-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![顯示如何在 windows media player 11 中購買內容的螢幕擷取畫面](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="71698-367">在 Windows 7 中，執行下列步驟以 Windows Media Player 12 購買內容：</span><span class="sxs-lookup"><span data-stu-id="71698-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="71698-368">在 [程式庫] 模式中，按一下 [ **播放** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="71698-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="71698-369">在播放清單中的專輯封面下，按一下 [**購買**]</span><span class="sxs-lookup"><span data-stu-id="71698-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="71698-370">下列螢幕擷取畫面顯示如何在 Windows Media Player 12 中購買內容：</span><span class="sxs-lookup"><span data-stu-id="71698-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![顯示如何在 windows media player 12 中購買內容的螢幕擷取畫面](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="71698-372">確認按一下 [ **購買** ] 或 [ **購物** ] 切換至商店。</span><span class="sxs-lookup"><span data-stu-id="71698-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="71698-373">Windows Media Player 應切換至程式庫視圖中的存放區，並載入商店的購買體驗。</span><span class="sxs-lookup"><span data-stu-id="71698-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="71698-374">然後，您必須繼續購買曲目。</span><span class="sxs-lookup"><span data-stu-id="71698-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="71698-375">按一下 [ **購買** 或 **購物**] 之後，請確認內容已下載。</span><span class="sxs-lookup"><span data-stu-id="71698-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="71698-376">確認媒體許可權適用于已購買的內容和其中繼資料，並確認播放軌是否正常播放。</span><span class="sxs-lookup"><span data-stu-id="71698-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="71698-377">一般來說，這個購買方法的結果應該與其他方法相同。</span><span class="sxs-lookup"><span data-stu-id="71698-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="71698-378">燒錄內容</span><span class="sxs-lookup"><span data-stu-id="71698-378">Burning Content</span></span>

<span data-ttu-id="71698-379">首先，請執行下列步驟來燒錄購買的內容 (將購買的內容複寫到可寫入的 CD 或 DVD) ，然後執行遵循初始步驟的步驟，以確認內容已重新執行：</span><span class="sxs-lookup"><span data-stu-id="71698-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="71698-380">燒錄購買的曲目之前，請記下它的燒錄計數，讓您稍後可以在燒錄曲目之後，確認計數是否遞減。</span><span class="sxs-lookup"><span data-stu-id="71698-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="71698-381">按一下 [ **燒錄** ] 索引標籤</span><span class="sxs-lookup"><span data-stu-id="71698-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="71698-382">將購買的曲目拖曳到 **燒錄清單**。</span><span class="sxs-lookup"><span data-stu-id="71698-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="71698-383">按一下 [ **開始燒錄** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="71698-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="71698-384">下列螢幕擷取畫面顯示畫面右側的 **燒錄清單**，以及 Windows Media Player 11 中 **燒錄清單** 下方的 [**開始燒錄**] 按鈕：</span><span class="sxs-lookup"><span data-stu-id="71698-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![顯示如何在 windows media player 11 中燒錄內容的螢幕擷取畫面](images/wmp11-verify-burn.png)

<span data-ttu-id="71698-386">下列螢幕擷取畫面顯示在您將曲目拖曳至燒錄清單之後，燒錄清單如何出現在 Windows Media Player 12 中，並顯示 [**燒錄**] 索引標籤頂端的 [**開始燒錄**] 按鈕：</span><span class="sxs-lookup"><span data-stu-id="71698-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![顯示如何在 windows media player 12 中燒錄內容的螢幕擷取畫面](images/wmp12-verify-burn.png)

<span data-ttu-id="71698-388">**確認購買的內容可以燒錄**</span><span class="sxs-lookup"><span data-stu-id="71698-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="71698-389">在燒錄完成後播放 CD 或 DVD，確認購買的內容已燒錄。</span><span class="sxs-lookup"><span data-stu-id="71698-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="71698-390">確認已減少燒錄計數。</span><span class="sxs-lookup"><span data-stu-id="71698-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="71698-391">流覽至媒體櫃，並針對已燒錄的曲目開啟媒體許可權。</span><span class="sxs-lookup"><span data-stu-id="71698-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="71698-392">如果播放軌的次數有所限制，請確認這個數位會在燒錄曲目之後減少。</span><span class="sxs-lookup"><span data-stu-id="71698-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="71698-393">傳送內容</span><span class="sxs-lookup"><span data-stu-id="71698-393">Transferring Content</span></span>

<span data-ttu-id="71698-394">將內容傳送到另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-394">Transfer content to another computer.</span></span>

<span data-ttu-id="71698-395">**確認購買的內容可以轉移到另一部電腦**</span><span class="sxs-lookup"><span data-stu-id="71698-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="71698-396">如果存放區允許將內容傳送到另一部電腦，請將內容傳輸到至少兩部電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="71698-397">請先執行下列步驟來同步處理裝置，並將購買的內容傳送至該裝置，然後執行遵循初始步驟的步驟，以確認內容已傳送：</span><span class="sxs-lookup"><span data-stu-id="71698-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="71698-398">在您傳輸已購買的曲目之前，請記下其同步計數，讓您可以在稍後確認計數是否會在您傳輸曲目後遞減。</span><span class="sxs-lookup"><span data-stu-id="71698-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="71698-399">以安全時鐘連接裝置。</span><span class="sxs-lookup"><span data-stu-id="71698-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="71698-400">範例包括使用適用于可攜式裝置之 Windows Media DRM 的裝置，例如 iRiver H10 等便攜媒體中心、創意 Zen 等等。</span><span class="sxs-lookup"><span data-stu-id="71698-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="71698-401">在 Windows Media Player 中，按一下 [ **同步** 處理] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="71698-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="71698-402">將文件庫中的內容拖曳至 [**同步** 處理] 索引標籤上的 [**同步清單**] 區域。</span><span class="sxs-lookup"><span data-stu-id="71698-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="71698-403">按一下 [ **開始同步** 處理] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="71698-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="71698-404">下列螢幕擷取畫面顯示 **同步清單** 區域中的追蹤1，並顯示 Windows Media Player 11 中的 [ **開始同步** 處理] 按鈕：</span><span class="sxs-lookup"><span data-stu-id="71698-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![顯示如何在 windows media player 11 中傳送內容的螢幕擷取畫面](images/wmp11-verify-transfer.png)

<span data-ttu-id="71698-406">下列螢幕擷取畫面顯示 **同步清單** 區域中的追蹤1，並顯示 Windows Media Player 12 中的 [ **開始同步** 處理] 按鈕：</span><span class="sxs-lookup"><span data-stu-id="71698-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![顯示如何在 windows media player 12 中傳送內容的螢幕擷取畫面](images/wmp12-verify-transfer.png)

<span data-ttu-id="71698-408">**確認購買的內容可以轉移到另一部裝置**</span><span class="sxs-lookup"><span data-stu-id="71698-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="71698-409">藉由在裝置上播放內容，確認已購買的內容已傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="71698-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="71698-410">傳送的內容也必須有適當的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="71698-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="71698-411">確認同步處理計數已減少。</span><span class="sxs-lookup"><span data-stu-id="71698-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="71698-412">流覽至程式庫，並開啟已傳輸曲目的媒體許可權。</span><span class="sxs-lookup"><span data-stu-id="71698-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="71698-413">如果追蹤可同步的次數有所限制，請確認此數量會在傳送曲目時減少。</span><span class="sxs-lookup"><span data-stu-id="71698-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="71698-414">存放區功能</span><span class="sxs-lookup"><span data-stu-id="71698-414">Store Features</span></span>

<span data-ttu-id="71698-415">下列各節說明如何測試內部上線線上商店的各種功能。</span><span class="sxs-lookup"><span data-stu-id="71698-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="71698-416">管理帳戶</span><span class="sxs-lookup"><span data-stu-id="71698-416">Managing an Account</span></span>

<span data-ttu-id="71698-417">使用已進行某些購買的帳戶登入，並開啟購買歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="71698-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="71698-418">**確認購買歷程記錄**</span><span class="sxs-lookup"><span data-stu-id="71698-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="71698-419">確認購買歷程記錄會追蹤先前的購買專案。</span><span class="sxs-lookup"><span data-stu-id="71698-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="71698-420">如果存放區或帳戶類型支援這項功能，請嘗試還原已刪除的購買。</span><span class="sxs-lookup"><span data-stu-id="71698-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="71698-421">**確認您可以重新取得先前的購買專案**</span><span class="sxs-lookup"><span data-stu-id="71698-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="71698-422">確認先前的購買可以還原。</span><span class="sxs-lookup"><span data-stu-id="71698-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="71698-423">如果存放區支援將多部電腦與該帳戶搭配使用，請確認此功能提供的任何功能。</span><span class="sxs-lookup"><span data-stu-id="71698-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="71698-424">**使用單一帳戶確認多部電腦管理**</span><span class="sxs-lookup"><span data-stu-id="71698-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="71698-425">確認存放區的功能，以管理多部電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="71698-426">管理 Store-Specific 帳戶</span><span class="sxs-lookup"><span data-stu-id="71698-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="71698-427">存放區可能沒有典型的帳戶類型、限制或內容。</span><span class="sxs-lookup"><span data-stu-id="71698-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="71698-428">例如，出租串流影片的商店需要一些使用者介面來顯示作用中租用，且需要測試使用者介面。</span><span class="sxs-lookup"><span data-stu-id="71698-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="71698-429">雖然 Microsoft 無法認證商店專屬的帳戶功能，但為了確保客戶體驗良好，您應該測試該功能。</span><span class="sxs-lookup"><span data-stu-id="71698-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="71698-430">管理資訊中心</span><span class="sxs-lookup"><span data-stu-id="71698-430">Managing the Info Center</span></span>

<span data-ttu-id="71698-431">首先，請執行下列步驟來準備測試預設狀態，然後執行遵循初始步驟的下一個步驟，以確認資訊中心預設為關閉：</span><span class="sxs-lookup"><span data-stu-id="71698-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="71698-432">播放存放區中的一些內容。</span><span class="sxs-lookup"><span data-stu-id="71698-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="71698-433">切換至 [立即播放] 模式。</span><span class="sxs-lookup"><span data-stu-id="71698-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="71698-434">在具有 Windows Media Player 11 的 Windows XP 或 Windows Vista 中，按一下 [ **立即播放** ] 索引標籤。在具有 Windows Media Player 12 的 Windows 7 中，按一下位於右下角的 [ **立即播放** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="71698-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="71698-435">**確認資訊中心預設為關閉**</span><span class="sxs-lookup"><span data-stu-id="71698-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="71698-436">確認資訊中心預設為關閉。</span><span class="sxs-lookup"><span data-stu-id="71698-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="71698-437">如果存放區提供資訊中心視圖，請播放存放區中的一些內容，並在內容播放時，切換到 [立即播放] 模式，並開啟資訊中心。</span><span class="sxs-lookup"><span data-stu-id="71698-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="71698-438">在具有 Windows Media Player 11 的 Windows XP 或 Windows Vista 中，以滑鼠右鍵按一下 [立即播放] 視窗，然後從內容功能表中選取 [ **資訊中心視圖**]。</span><span class="sxs-lookup"><span data-stu-id="71698-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="71698-439">下列螢幕擷取畫面顯示 Windows Media Player 11 的內容功能表：</span><span class="sxs-lookup"><span data-stu-id="71698-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![顯示如何存取 windows media player 11 中商店資訊中心的螢幕擷取畫面](images/wmp11-info-center.png)

<span data-ttu-id="71698-441">在具有 Windows Media Player 12 的 Windows 7 中，以滑鼠右鍵按一下 [立即播放] 視窗，然後在操作功能表上選取 [ **視覺效果**]，再按一下 [ **資訊中心視圖**]。</span><span class="sxs-lookup"><span data-stu-id="71698-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="71698-442">下列螢幕擷取畫面顯示 Windows Media Player 12 中的內容功能表：</span><span class="sxs-lookup"><span data-stu-id="71698-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![顯示如何在 windows media player 12 中存取商店資訊中心的螢幕擷取畫面](images/wmp12-info-center.png)

<span data-ttu-id="71698-444">**確認資訊中心是否正常運作**</span><span class="sxs-lookup"><span data-stu-id="71698-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="71698-445">確認資訊中心在立即播放的區域中顯示媒體資訊。</span><span class="sxs-lookup"><span data-stu-id="71698-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="71698-446">下列螢幕擷取畫面顯示這類媒體資訊的範例：</span><span class="sxs-lookup"><span data-stu-id="71698-446">The following screen shot shows an example of such media information:</span></span>

    ![顯示商店資訊中心功能的螢幕擷取畫面](images/media-information.png)

<span data-ttu-id="71698-448">如果頁面上出現任何購買連結或其他連結，請按一下連結。</span><span class="sxs-lookup"><span data-stu-id="71698-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="71698-449">**確認資訊中心視圖中的連結**</span><span class="sxs-lookup"><span data-stu-id="71698-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="71698-450">確認連結顯示存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="71698-451">Windows Media Player 應切換至其程式庫中的存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="71698-452">商店互動</span><span class="sxs-lookup"><span data-stu-id="71698-452">Store Interaction</span></span>

<span data-ttu-id="71698-453">下列各節說明如何測試其他存放區與您正在測試之存放區之間的互動。</span><span class="sxs-lookup"><span data-stu-id="71698-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="71698-454">對使用中的存放區產生</span><span class="sxs-lookup"><span data-stu-id="71698-454">Yielding to the Active Store</span></span>

<span data-ttu-id="71698-455">切換至要測試之存放區以外的商店。</span><span class="sxs-lookup"><span data-stu-id="71698-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="71698-456">**若要確認是否已為使用中的存放區產生**</span><span class="sxs-lookup"><span data-stu-id="71698-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="71698-457">確認測試的存放區會產生至使用中的存放區。</span><span class="sxs-lookup"><span data-stu-id="71698-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="71698-458">防止經過測試的存放區接管使用中的存放區</span><span class="sxs-lookup"><span data-stu-id="71698-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="71698-459">選取另一個存放區之後，關閉 Windows Media Player 然後重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="71698-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="71698-460">啟動 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="71698-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="71698-461">**確認測試的存放區不接管**</span><span class="sxs-lookup"><span data-stu-id="71698-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="71698-462">確認最近使用中的存放區出現，而且測試的存放區並未出現。</span><span class="sxs-lookup"><span data-stu-id="71698-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="71698-463">以 High-Contrast 模式存取存放區</span><span class="sxs-lookup"><span data-stu-id="71698-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="71698-464">先按左 SHIFT + 左 ALT + PRINT SCREEN 啟用高對比模式，然後執行下列步驟來確認高對比的存取範圍：</span><span class="sxs-lookup"><span data-stu-id="71698-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="71698-465">**確認可在高對比模式下存取存放區**</span><span class="sxs-lookup"><span data-stu-id="71698-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="71698-466">確認登入的使用者介面未完整且正常運作。</span><span class="sxs-lookup"><span data-stu-id="71698-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="71698-467">確認所有視窗和對話方塊都正確出現。</span><span class="sxs-lookup"><span data-stu-id="71698-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="71698-468">購買媒體。</span><span class="sxs-lookup"><span data-stu-id="71698-468">Purchase media.</span></span> <span data-ttu-id="71698-469">確認 [購買] 和 [下載] 按鈕、下載管理員、價格資訊等都是可見的。</span><span class="sxs-lookup"><span data-stu-id="71698-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="71698-470">確認您可以進行串流、燒錄和同步處理。</span><span class="sxs-lookup"><span data-stu-id="71698-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="71698-471">尋找裁剪的文字和使用者介面元素、無法辨認的文字，以及其他可見的瑕疵。</span><span class="sxs-lookup"><span data-stu-id="71698-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="71698-472">保護存放區</span><span class="sxs-lookup"><span data-stu-id="71698-472">Securing a Store</span></span>

<span data-ttu-id="71698-473">請執行下列步驟來確認帳戶安全性：</span><span class="sxs-lookup"><span data-stu-id="71698-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="71698-474">**確認帳戶安全性**</span><span class="sxs-lookup"><span data-stu-id="71698-474">**To verify account security**</span></span>

1.  <span data-ttu-id="71698-475">在 [登入] 頁面和對話方塊中輸入格式不正確的帳戶資訊，並確認存放區拒絕它。</span><span class="sxs-lookup"><span data-stu-id="71698-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="71698-476">登入、查看帳戶頁面，然後登出。</span><span class="sxs-lookup"><span data-stu-id="71698-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="71698-477">按一下 Windows Media Player 中的 [上一步] 按鈕，並確認您沒有看到先前的使用者帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="71698-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 




