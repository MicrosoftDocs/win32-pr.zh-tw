---
title: 如何針對應用程式封裝簽章錯誤進行疑難排解
description: 應用程式部署失敗的原因可能是無法驗證應用程式套件的數位簽章。 瞭解如何辨識這些失敗，以及該怎麼做。
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6f50dc5ff428e74f4928fc20775b13de7c3be9
ms.sourcegitcommit: 784b5954a1646e2406cd4ee27a9e4f50e28ee9b7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106976309"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a><span data-ttu-id="622a5-104">如何針對應用程式封裝簽章錯誤進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="622a5-104">How to troubleshoot app package signature errors</span></span>

<span data-ttu-id="622a5-105">應用程式部署失敗的原因可能是無法驗證應用程式套件的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="622a5-105">An app deployment failure can be caused by a failure to validate the digital signature of the app package.</span></span> <span data-ttu-id="622a5-106">瞭解如何辨識這些失敗，以及該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="622a5-106">Learn how to recognize these failures, and what to do about them.</span></span>

<span data-ttu-id="622a5-107">當您部署已封裝的 Windows 應用程式時，Windows 一律會嘗試驗證應用程式套件上的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="622a5-107">When you deploy a packaged Windows app, Windows always attempts to validate the digital signature on the app package.</span></span> <span data-ttu-id="622a5-108">簽章驗證期間的失敗會封鎖封裝的部署。</span><span class="sxs-lookup"><span data-stu-id="622a5-108">Failures during signature validation block deployment of the package.</span></span> <span data-ttu-id="622a5-109">但是，為什麼封裝未進行驗證可能並不明顯。</span><span class="sxs-lookup"><span data-stu-id="622a5-109">But why the package didn't validate might not be obvious.</span></span> <span data-ttu-id="622a5-110">尤其是，如果您使用私人憑證簽署套件以進行本機測試，您通常也必須管理這些憑證的信任。</span><span class="sxs-lookup"><span data-stu-id="622a5-110">In particular, if you sign your packages with private certificates for local testing, you often must manage the trust for those certificates as well.</span></span> <span data-ttu-id="622a5-111">不正確的憑證信任設定可能會導致簽章驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="622a5-111">An incorrect certificate trust configuration can lead to signature validation failures.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="622a5-112">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="622a5-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="622a5-113">技術</span><span class="sxs-lookup"><span data-stu-id="622a5-113">Technologies</span></span>

-   [<span data-ttu-id="622a5-114">封裝、部署及查詢 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="622a5-114">Packaging, deployment, and query of Windows apps</span></span>](appx-portal.md)
-   [<span data-ttu-id="622a5-115">憑證信任驗證</span><span class="sxs-lookup"><span data-stu-id="622a5-115">Certificate Trust Verification</span></span>](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a><span data-ttu-id="622a5-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="622a5-116">Prerequisites</span></span>

-   <span data-ttu-id="622a5-117">用來診斷安裝失敗的[Windows 事件記錄](/windows/desktop/WES/windows-event-log)檔。</span><span class="sxs-lookup"><span data-stu-id="622a5-117">[Windows Event Log](/windows/desktop/WES/windows-event-log) to diagnose installation failures.</span></span>
-   <span data-ttu-id="622a5-118">[用於](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) 在疑難排解期間管理憑證存放區操作之憑證的 Certutil 工作</span><span class="sxs-lookup"><span data-stu-id="622a5-118">[Certutil tasks for managing certificates](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) for certificate store manipulation during troubleshooting</span></span>

## <a name="instructions"></a><span data-ttu-id="622a5-119">指示</span><span class="sxs-lookup"><span data-stu-id="622a5-119">Instructions</span></span>

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a><span data-ttu-id="622a5-120">步驟1：檢查事件記錄檔中的診斷資訊</span><span class="sxs-lookup"><span data-stu-id="622a5-120">Step 1: Examine event logs for diagnostic information</span></span>

<span data-ttu-id="622a5-121">根據您嘗試部署應用程式的方式而定，您可能並未收到有意義的錯誤碼來部署失敗。</span><span class="sxs-lookup"><span data-stu-id="622a5-121">Depending on how you attempted to deploy your app, you might not have received a meaningful error code for the deployment failure.</span></span> <span data-ttu-id="622a5-122">在此情況下，您通常可以直接從事件記錄檔取得錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="622a5-122">In this case, you can usually get the error code directly from the event logs.</span></span>

<span data-ttu-id="622a5-123">**若要從事件記錄檔取得錯誤碼**</span><span class="sxs-lookup"><span data-stu-id="622a5-123">**To get the error code from the event logs**</span></span>

1.  <span data-ttu-id="622a5-124">執行 **eventvwr.msc services.msc**。</span><span class="sxs-lookup"><span data-stu-id="622a5-124">Run **eventvwr.msc**.</span></span>
2.  <span data-ttu-id="622a5-125">移至 **事件檢視器 (本機)**  >  **應用程式和服務記錄**  >  **Microsoft**  >  **Windows**。</span><span class="sxs-lookup"><span data-stu-id="622a5-125">Go to **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3.  <span data-ttu-id="622a5-126">第一個要檢查的記錄是 **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**。</span><span class="sxs-lookup"><span data-stu-id="622a5-126">The first log to check is **AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**.</span></span>
4.  <span data-ttu-id="622a5-127">部署相關錯誤會記錄在 **appxdeployment-server-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational** 中。</span><span class="sxs-lookup"><span data-stu-id="622a5-127">Deployment-related errors are recorded in **AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**.</span></span>

    <span data-ttu-id="622a5-128">針對部署錯誤，請搜尋最新的錯誤事件404。</span><span class="sxs-lookup"><span data-stu-id="622a5-128">For deployment errors, search for the most recent error event 404.</span></span> <span data-ttu-id="622a5-129">此錯誤事件會為您提供錯誤碼，以及部署失敗原因的說明。</span><span class="sxs-lookup"><span data-stu-id="622a5-129">This error event provides you with the error code and a description of why the deployment failed.</span></span> <span data-ttu-id="622a5-130">如果錯誤事件465之前是404事件，開啟封裝時發生問題。</span><span class="sxs-lookup"><span data-stu-id="622a5-130">If an error event 465 preceded the 404 event, there was a problem opening the package.</span></span>

<span data-ttu-id="622a5-131">如果未發生465錯誤，請參閱一般針對 [封裝、部署及查詢 Windows 應用程式進行疑難排解](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="622a5-131">If the 465 error didn't occur, see general [Troubleshooting packaging, deployment, and query of Windows apps](troubleshooting.md).</span></span> <span data-ttu-id="622a5-132">否則，請參閱此表格，以取得可在錯誤事件465的錯誤字串中顯示的常見錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="622a5-132">Otherwise, refer to this table for common error codes that can show up in the error string for error event 465:</span></span>

| <span data-ttu-id="622a5-133">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="622a5-133">Error code</span></span> | <span data-ttu-id="622a5-134">錯誤</span><span class="sxs-lookup"><span data-stu-id="622a5-134">Error</span></span>                                 | <span data-ttu-id="622a5-135">描述</span><span class="sxs-lookup"><span data-stu-id="622a5-135">Description</span></span>                                                                                                          | <span data-ttu-id="622a5-136">建議</span><span class="sxs-lookup"><span data-stu-id="622a5-136">Suggestion</span></span>                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622a5-137">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="622a5-137">0x80073CF0</span></span> | <span data-ttu-id="622a5-138">\_安裝 \_ 開啟 \_ 套件 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="622a5-138">ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED</span></span> | <span data-ttu-id="622a5-139">無法開啟應用程式封裝。</span><span class="sxs-lookup"><span data-stu-id="622a5-139">The app package could not be opened.</span></span>                                                                                 | <span data-ttu-id="622a5-140">此錯誤通常表示套件有問題。</span><span class="sxs-lookup"><span data-stu-id="622a5-140">This error typically indicates a problem with the package.</span></span> <span data-ttu-id="622a5-141">您必須重新建立並簽署封裝。</span><span class="sxs-lookup"><span data-stu-id="622a5-141">You need to build and sign the package again.</span></span> <span data-ttu-id="622a5-142">如需詳細資訊，請參閱 [使用應用程式封裝程式](make-appx-package--makeappx-exe-.md)。</span><span class="sxs-lookup"><span data-stu-id="622a5-142">For more info, see [Using App Packager](make-appx-package--makeappx-exe-.md).</span></span> |
| <span data-ttu-id="622a5-143">0x80080205</span><span class="sxs-lookup"><span data-stu-id="622a5-143">0x80080205</span></span> | <span data-ttu-id="622a5-144">APPX \_ E \_ 不正確 \_ BLOCKMAP</span><span class="sxs-lookup"><span data-stu-id="622a5-144">APPX\_E\_INVALID\_BLOCKMAP</span></span>            | <span data-ttu-id="622a5-145">應用程式套件已遭篡改，或具有不正確區塊對應。</span><span class="sxs-lookup"><span data-stu-id="622a5-145">The app package has been tampered with or has an invalid block map.</span></span>                                                  | <span data-ttu-id="622a5-146">封裝已損毀。</span><span class="sxs-lookup"><span data-stu-id="622a5-146">The package is corrupted.</span></span> <span data-ttu-id="622a5-147">您必須重新建立並簽署封裝。</span><span class="sxs-lookup"><span data-stu-id="622a5-147">You need to build and sign the package again.</span></span> <span data-ttu-id="622a5-148">如需詳細資訊，請參閱 [使用應用程式封裝程式](make-appx-package--makeappx-exe-.md)。</span><span class="sxs-lookup"><span data-stu-id="622a5-148">For more info, see [Using App Packager](make-appx-package--makeappx-exe-.md).</span></span>                                  |
| <span data-ttu-id="622a5-149">0x800B0004</span><span class="sxs-lookup"><span data-stu-id="622a5-149">0x800B0004</span></span> | <span data-ttu-id="622a5-150">信任 \_ 電子 \_ 主體 \_ 不 \_ 受信任</span><span class="sxs-lookup"><span data-stu-id="622a5-150">TRUST\_E\_SUBJECT\_NOT\_TRUSTED</span></span>       | <span data-ttu-id="622a5-151">應用程式套件已遭修改。</span><span class="sxs-lookup"><span data-stu-id="622a5-151">The app package has been tampered with.</span></span>                                                                              | <span data-ttu-id="622a5-152">套件內容不再符合其數位簽章。</span><span class="sxs-lookup"><span data-stu-id="622a5-152">The package contents no longer match its digital signature.</span></span> <span data-ttu-id="622a5-153">您必須重新簽署封裝。</span><span class="sxs-lookup"><span data-stu-id="622a5-153">You need to sign the package again.</span></span> <span data-ttu-id="622a5-154">如需詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="622a5-154">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>  |
| <span data-ttu-id="622a5-155">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="622a5-155">0x800B0100</span></span> | <span data-ttu-id="622a5-156">信任 \_ 電子 \_ NOSIGNATURE</span><span class="sxs-lookup"><span data-stu-id="622a5-156">TRUST\_E\_NOSIGNATURE</span></span>                 | <span data-ttu-id="622a5-157">應用程式套件未簽署。</span><span class="sxs-lookup"><span data-stu-id="622a5-157">The app package is unsigned.</span></span>                                                                                         | <span data-ttu-id="622a5-158">只能部署已簽署的 Windows 應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="622a5-158">Only signed Windows app packages can be deployed.</span></span> <span data-ttu-id="622a5-159">如需簽署應用程式套件的相關資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="622a5-159">For info about signing an app package, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>                  |
| <span data-ttu-id="622a5-160">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="622a5-160">0x800B0109</span></span> | <span data-ttu-id="622a5-161">CERT \_ E 未 \_ 受信任的 \_ 根</span><span class="sxs-lookup"><span data-stu-id="622a5-161">CERT\_E\_UNTRUSTED\_ROOT</span></span>              | <span data-ttu-id="622a5-162">用來簽署應用程式套件的憑證鏈會以不受信任的根憑證結尾。</span><span class="sxs-lookup"><span data-stu-id="622a5-162">The certificate chain that was used to sign the app package ends in a root certificate that isn't trusted.</span></span>           | <span data-ttu-id="622a5-163">繼續進行步驟2以疑難排解憑證信任。</span><span class="sxs-lookup"><span data-stu-id="622a5-163">Continue to Step 2 to troubleshoot the certificate trust.</span></span>                                                                                                                                                  |
| <span data-ttu-id="622a5-164">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="622a5-164">0x800B010A</span></span> | <span data-ttu-id="622a5-165">CERT \_ E \_ 連結</span><span class="sxs-lookup"><span data-stu-id="622a5-165">CERT\_E\_CHAINING</span></span>                     | <span data-ttu-id="622a5-166">從用來簽署應用程式套件的憑證中，無法將任何憑證鏈建立至信任的根授權單位。</span><span class="sxs-lookup"><span data-stu-id="622a5-166">No certificate chain could be built to a trusted root authority from the cert that was used to sign the app package.</span></span> | <span data-ttu-id="622a5-167">繼續進行步驟2以疑難排解憑證信任。</span><span class="sxs-lookup"><span data-stu-id="622a5-167">Continue to Step 2 to troubleshoot the certificate trust.</span></span>                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a><span data-ttu-id="622a5-168">步驟2：判斷用來簽署應用程式套件的憑證鏈</span><span class="sxs-lookup"><span data-stu-id="622a5-168">Step 2: Determine the certificate chain used to sign the app package</span></span>

<span data-ttu-id="622a5-169">若要找出本機電腦必須信任的憑證，您可以在應用程式套件上檢查憑證鏈中的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="622a5-169">To figure out the certificates that the local computer must trust, you can examine the certificate chain for the digital signature on the app package.</span></span>

<span data-ttu-id="622a5-170">**判斷憑證鏈**</span><span class="sxs-lookup"><span data-stu-id="622a5-170">**To determine the certificate chain**</span></span>

1.  <span data-ttu-id="622a5-171">在檔案總管中，以滑鼠右鍵按一下應用程式套件，然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="622a5-171">In File Explorer, right-click on the app package and select **Properties**.</span></span>
2.  <span data-ttu-id="622a5-172">在 [ **屬性** ] 對話方塊中，選取 [ **數位簽章** ] 索引標籤，此索引標籤也會顯示是否可以驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="622a5-172">In the **Properties** dialog, select the **Digital Signatures** tab, which also displays whether the signature can be validated.</span></span>
3.  <span data-ttu-id="622a5-173">在 [簽章] 清單中選取簽章，然後按一下 [ **詳細資料** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="622a5-173">In the Signature list, select the signature and then click the **Details** button.</span></span>
4.  <span data-ttu-id="622a5-174">在 [ **數位簽章詳細資料** ] 對話方塊中，按一下 [ **視圖憑證** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="622a5-174">In the **Digital Signature Details** dialog, click the **View Certificate** button.</span></span>
5.  <span data-ttu-id="622a5-175">在 [ **憑證** ] 對話方塊中，選取 [ **憑證路徑** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="622a5-175">In the **Certificate** dialog, select the **Certification Path** tab.</span></span>

<span data-ttu-id="622a5-176">鏈中的最上層憑證是根憑證，而底部的憑證則是簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="622a5-176">The top certificate in the chain is the root certificate and the bottom certificate is the signing certificate.</span></span> <span data-ttu-id="622a5-177">如果鏈中只有單一憑證，則簽署憑證也是自己的根憑證。</span><span class="sxs-lookup"><span data-stu-id="622a5-177">If only a single certificate is in the chain, the signing certificate is also its own root certificate.</span></span> <span data-ttu-id="622a5-178">您可以為每個使用 [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))的憑證判斷序號：</span><span class="sxs-lookup"><span data-stu-id="622a5-178">You can determine the serial number for each certificate that you then use with [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)):</span></span>

<span data-ttu-id="622a5-179">**判斷每個憑證的序號**</span><span class="sxs-lookup"><span data-stu-id="622a5-179">**To determine the serial number for each certificate**</span></span>

1.  <span data-ttu-id="622a5-180">在 [憑證路徑] 窗格中，選取憑證，然後按一下 [ **View certificate**]。</span><span class="sxs-lookup"><span data-stu-id="622a5-180">In the Certification path pane, select the certificate and then click **View Certificate**.</span></span>
2.  <span data-ttu-id="622a5-181">在 [憑證] 對話方塊中，選取 [ **詳細資料** ] 索引標籤，此索引標籤會顯示憑證的序號和其他有用的屬性。</span><span class="sxs-lookup"><span data-stu-id="622a5-181">In the Certificate dialog, select the **Details** tab, which displays the serial number and other useful properties of the certificate.</span></span>

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a><span data-ttu-id="622a5-182">步驟3：判斷本機電腦所信任的憑證</span><span class="sxs-lookup"><span data-stu-id="622a5-182">Step 3: Determine the certificates trusted by the local machine</span></span>

<span data-ttu-id="622a5-183">若要能夠部署應用程式套件，它不僅能在使用者的內容中受信任，也不能在本機電腦內容中受到信任。</span><span class="sxs-lookup"><span data-stu-id="622a5-183">To be able to deploy an app package, it must not only be trusted in the user’s context but also the local computer context.</span></span> <span data-ttu-id="622a5-184">如此一來，當您在上一個步驟的 [數位簽章] 索引標籤中查看時，數位簽章可能會顯示為有效，但在應用程式套件部署期間仍無法通過驗證。</span><span class="sxs-lookup"><span data-stu-id="622a5-184">As a result, the digital signature can appear valid when viewed in the Digital Signatures tab from the previous step but still fail validation during deployment of the app package.</span></span>

<span data-ttu-id="622a5-185">**判斷用來簽署應用程式套件的憑證鏈是否由本機電腦明確信任**</span><span class="sxs-lookup"><span data-stu-id="622a5-185">**To determine if the certificate chain used to sign the app package is specifically trusted by the local computer**</span></span>

1.  <span data-ttu-id="622a5-186">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="622a5-186">Run this command:</span></span>

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  <span data-ttu-id="622a5-187">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="622a5-187">Run this command:</span></span>

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

<span data-ttu-id="622a5-188">如果您未指定憑證序號， [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) 會列出該存放區的本機電腦所信任的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="622a5-188">If you don't specify the certificate serial number, [Certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) lists all certificates that are trusted by the local computer for that store.</span></span>

<span data-ttu-id="622a5-189">封裝可能會因為憑證鏈錯誤而無法安裝，即使簽署憑證不是自我簽署的憑證，以及根憑證在本機電腦的根存放區中。</span><span class="sxs-lookup"><span data-stu-id="622a5-189">The package may fail to install due to certificate chaining errors, even if the signing certificate is not self-signed and the root certificate is in the root store of the local computer.</span></span> <span data-ttu-id="622a5-190">在此情況下，可能會有中繼憑證授權單位單位的信任問題。</span><span class="sxs-lookup"><span data-stu-id="622a5-190">In this case, there might be an issue with trust for the intermediate certificate authorities.</span></span> <span data-ttu-id="622a5-191">如需此問題的詳細資訊，請參閱 [使用憑證](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="622a5-191">For more info about this issue, see [Working with Certificates](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="622a5-192">備註</span><span class="sxs-lookup"><span data-stu-id="622a5-192">Remarks</span></span>

<span data-ttu-id="622a5-193">如果您決定因為簽署憑證不受信任而無法部署封裝，除非您知道它的來源，並信任它，否則請勿安裝套件。</span><span class="sxs-lookup"><span data-stu-id="622a5-193">If you determined that the package couldn't be deployed because the signing certificate isn't trusted, don't install the package unless you know where it originated and you trust it.</span></span>

<span data-ttu-id="622a5-194">如果您想要以手動方式信任安裝的應用程式 (例如，安裝您自己的測試簽署應用程式套件) ，您可以從應用程式套件手動將憑證新增至本機電腦憑證信任。</span><span class="sxs-lookup"><span data-stu-id="622a5-194">If you want to manually trust the app for install (for example, to install your own test-signed app package), you can manually add the certificate to the local computer certificate trust from the app package.</span></span>

<span data-ttu-id="622a5-195">**手動將憑證新增至本機電腦憑證信任**</span><span class="sxs-lookup"><span data-stu-id="622a5-195">**To manually add the certificate to the local computer certificate trust**</span></span>

1.  <span data-ttu-id="622a5-196">在檔案總管中，以滑鼠右鍵按一下應用程式套件，然後在快顯功能表中選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="622a5-196">In File Explorer, right-click on the app package, and in the pop-up context menu select **Properties**.</span></span>
2.  <span data-ttu-id="622a5-197">在 [ **屬性** ] 對話方塊中，選取 [ **數位簽章** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="622a5-197">In the **Properties** dialog, select the **Digital Signatures** tab.</span></span>
3.  <span data-ttu-id="622a5-198">在 [簽章] 清單中選取簽章，然後按一下 [ **詳細資料** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="622a5-198">In the Signature list, select the signature and then click the **Details** button.</span></span>
4.  <span data-ttu-id="622a5-199">在 [ **數位簽章詳細資料** ] 對話方塊中，按一下 [ **視圖憑證** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="622a5-199">In the **Digital Signature Details** dialog, click the **View Certificate** button.</span></span>
5.  <span data-ttu-id="622a5-200">在 [**憑證**] 對話方塊中，按一下 [**安裝憑證 ...** ]。</span><span class="sxs-lookup"><span data-stu-id="622a5-200">In the **Certificate** dialog, click the **Install Certificate…**</span></span> <span data-ttu-id="622a5-201">按鈕。</span><span class="sxs-lookup"><span data-stu-id="622a5-201">button.</span></span>
6.  <span data-ttu-id="622a5-202">在 [憑證匯入] 嚮導中選取 [ **本機電腦** ]，然後按 **[下一步]**。</span><span class="sxs-lookup"><span data-stu-id="622a5-202">In the Certificate Import Wizard, select **Local Machine** and then click **Next**.</span></span> <span data-ttu-id="622a5-203">您將需要授與系統管理員許可權才能繼續。</span><span class="sxs-lookup"><span data-stu-id="622a5-203">You will need to grant administrator privileges to continue.</span></span>
7.  <span data-ttu-id="622a5-204">選取 **[將所有憑證放入以下的存放區** ]，然後流覽至 [ **受信任的人** ] 存放區。</span><span class="sxs-lookup"><span data-stu-id="622a5-204">Select **Place all certificates in the following store** and browse to the **Trusted People** store.</span></span>
8.  <span data-ttu-id="622a5-205">按 **[下一步**]，然後按一下 **[完成** ] 以完成 wizard。</span><span class="sxs-lookup"><span data-stu-id="622a5-205">Click **Next**, then click **Finish** to complete the wizard.</span></span>

<span data-ttu-id="622a5-206">在此手動新增之後，您可以在 [ **憑證** ] 對話方塊中看到憑證現在是受信任的。</span><span class="sxs-lookup"><span data-stu-id="622a5-206">After this manual addition, you can see that the certificate is now trusted in the **Certificate** dialog.</span></span>

<span data-ttu-id="622a5-207">您可以在不再需要憑證之後，將它移除。</span><span class="sxs-lookup"><span data-stu-id="622a5-207">You can remove the certificate after you no longer need it.</span></span>

<span data-ttu-id="622a5-208">**移除憑證**</span><span class="sxs-lookup"><span data-stu-id="622a5-208">**To remove the certificate**</span></span>

1.  <span data-ttu-id="622a5-209">以系統管理員身分執行 **Cmd.exe** 。</span><span class="sxs-lookup"><span data-stu-id="622a5-209">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="622a5-210">在系統管理員命令提示字元中，執行此命令：</span><span class="sxs-lookup"><span data-stu-id="622a5-210">In the administrator command prompt, run this command:</span></span>

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  <span data-ttu-id="622a5-211">尋找您所安裝之憑證的序號。</span><span class="sxs-lookup"><span data-stu-id="622a5-211">Look for the serial number of the certificate that you installed.</span></span> <span data-ttu-id="622a5-212">這個數位是 *certID*。</span><span class="sxs-lookup"><span data-stu-id="622a5-212">This number is the *certID*.</span></span>
4.  <span data-ttu-id="622a5-213">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="622a5-213">Run this command:</span></span>

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

<span data-ttu-id="622a5-214">建議您避免手動將根憑證新增至本機電腦的「 [受信任的根憑證授權單位」憑證存放區](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)。</span><span class="sxs-lookup"><span data-stu-id="622a5-214">We recommend that you avoid manually adding root certificates to the local machine [Trusted Root Certification Authorities Certificate Store](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store).</span></span> <span data-ttu-id="622a5-215">如果有多個應用程式是以連結至相同根憑證的憑證來簽署，例如企業營運應用程式，則會比將個別憑證安裝至受信任的人存放區更有效率。</span><span class="sxs-lookup"><span data-stu-id="622a5-215">Having several applications that are signed with certificates that chain to the same root certificate, such as line of business applications, can be more efficient than installing individual certificates to the Trusted People store.</span></span> <span data-ttu-id="622a5-216">[受信任的人] 存放區包含預設視為受信任的憑證，因此不會由較高的授權單位或憑證信任清單或鏈進行驗證。</span><span class="sxs-lookup"><span data-stu-id="622a5-216">The Trusted People store contains certificates that are considered trusted by default and so aren't verified by higher authorities or certificate trust lists or chains.</span></span> <span data-ttu-id="622a5-217">如需將憑證新增至「信任的根憑證授權單位」憑證存放區的考慮，請參閱程式 [代碼簽署最佳做法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="622a5-217">For considerations around adding certificates to the Trusted Root Certification Authorities certificate store, see [Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85)).</span></span>

## <a name="security-considerations"></a><span data-ttu-id="622a5-218">安全性考量</span><span class="sxs-lookup"><span data-stu-id="622a5-218">Security Considerations</span></span>

<span data-ttu-id="622a5-219">藉由將認證新增至[本機電腦憑證存放區](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores) (英文)，您會對電腦上所有使用者的憑證信任造成影響。</span><span class="sxs-lookup"><span data-stu-id="622a5-219">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="622a5-220">建議您將任何要用於測試應用程式套件的程式碼簽署憑證，安裝到 [受信任的人] 憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="622a5-220">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="622a5-221">當不再需要時，請立即移除這些憑證，以防止它們被用來危害系統信任。</span><span class="sxs-lookup"><span data-stu-id="622a5-221">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span> <span data-ttu-id="622a5-222">如果您建立自己的測試憑證來簽署應用程式套件，我們也建議您限制與測試憑證相關聯的許可權。</span><span class="sxs-lookup"><span data-stu-id="622a5-222">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges that are associated with the test certificate.</span></span> <span data-ttu-id="622a5-223">如需建立測試憑證以簽署應用程式套件的相關資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。</span><span class="sxs-lookup"><span data-stu-id="622a5-223">For info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="622a5-224">相關主題</span><span class="sxs-lookup"><span data-stu-id="622a5-224">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="622a5-225">**範例**</span><span class="sxs-lookup"><span data-stu-id="622a5-225">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="622a5-226">建立應用程式套件範例</span><span class="sxs-lookup"><span data-stu-id="622a5-226">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="622a5-227">**概念**</span><span class="sxs-lookup"><span data-stu-id="622a5-227">**Concepts**</span></span>
</dt> <dt>

[<span data-ttu-id="622a5-228">對 Windows 應用程式的封裝、部署及查詢進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="622a5-228">Troubleshooting packaging, deployment, and query of Windows apps</span></span>](troubleshooting.md)
</dt> <dt>

<span data-ttu-id="622a5-229">[用於管理憑證的 Certutil 工作](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="622a5-229">[Certutil tasks for managing certificates](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))</span></span>
</dt> </dl>

 

 
