---
title: 自動化元件撤銷和更新
description: 自動化元件撤銷和更新
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK、自動撤銷和更新
- Windows Media Format SDK，撤銷
- Windows Media Format SDK，續約
- 數位版權管理 (DRM) 、自動化撤銷和更新
- DRM (數位版權管理) 、自動化撤銷和更新
- 數位版權管理 (DRM) ，撤銷
- DRM (數位版權管理) ，撤銷
- 數位版權管理 (DRM) ，續約
- DRM (數位版權管理) ，續約
- DRM 用戶端擴充 Api、自動化撤銷和更新
- 用戶端擴充 Api、自動化撤銷和更新
- DRM 用戶端擴充 Api，撤銷
- 用戶端擴充 Api，撤銷
- DRM 用戶端擴充 Api，更新
- 用戶端擴充 Api，續約
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316000"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="7e642-118">自動化元件撤銷和更新</span><span class="sxs-lookup"><span data-stu-id="7e642-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="7e642-119">Microsoft 會撤銷被視為遭入侵的軟體應用程式或元件。</span><span class="sxs-lookup"><span data-stu-id="7e642-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="7e642-120">Windows Media Format 用戶端擴充 API 提供自動撤銷和更新元件的機制。</span><span class="sxs-lookup"><span data-stu-id="7e642-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="7e642-121">撤銷的元件會列在由 Microsoft 發佈的憑證撤銷清單中。</span><span class="sxs-lookup"><span data-stu-id="7e642-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="7e642-122">撤銷元件時，會將其憑證新增到憑證撤銷清單中，並在 Microsoft 伺服器上更新撤銷資訊 BLOB (REV \_ 資訊) 。</span><span class="sxs-lookup"><span data-stu-id="7e642-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="7e642-123">若要在使用者嘗試處理 Windows Media 受 DRM 保護的內容時執行自動撤銷和更新，您的應用程式必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7e642-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="7e642-124">\_從授權中解壓縮 REV INFO 版本。</span><span class="sxs-lookup"><span data-stu-id="7e642-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="7e642-125">REV \_ INFO 版本號碼位於 XMR 授權中的下列位置：</span><span class="sxs-lookup"><span data-stu-id="7e642-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="7e642-126">藉 \_ \_ 由呼叫 [**IWMDRMSecurity：： GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) 方法，將授權的修訂資訊版本號碼與本機存放區中的 rev info 版本號碼進行比較。</span><span class="sxs-lookup"><span data-stu-id="7e642-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="7e642-127">如果 REV \_ 資訊版本不是最新版本，請呼叫 [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 方法，並 \_ \_ \_ \_ 在 *dwFlags* 參數中傳遞 WMDRM 安全性執行撤銷重新整理旗標。</span><span class="sxs-lookup"><span data-stu-id="7e642-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="7e642-128">藉由呼叫 [**IWMDRMSecurity：： GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) 方法，從本機存放區取出憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="7e642-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="7e642-129">剖析撤銷清單，並檢查 Windows Media DRM 撤銷。</span><span class="sxs-lookup"><span data-stu-id="7e642-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="7e642-130">如需詳細資訊，請參閱 [檢查憑證撤銷](checking-certificate-revocation.md)。</span><span class="sxs-lookup"><span data-stu-id="7e642-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="7e642-131">如果有任何 Windows Media DRM 撤銷：</span><span class="sxs-lookup"><span data-stu-id="7e642-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="7e642-132">藉由呼叫 [**IWMDRMSecurity：： GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) 方法，建立內容啟用程式以更新撤銷的元件。</span><span class="sxs-lookup"><span data-stu-id="7e642-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="7e642-133">呼叫 **IMFContentEnabler：： AutomaticEnable** ，以將使用者導向包含元件續約資訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="7e642-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="7e642-134">此方法記載于 [媒體基礎 SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx) 。</span><span class="sxs-lookup"><span data-stu-id="7e642-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="7e642-135">您必須使用隱私權聲明來向使用者說明此程式，因為更新程式會將用戶端電腦的資訊傳送至 Microsoft 網站。</span><span class="sxs-lookup"><span data-stu-id="7e642-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="7e642-136">如果可能的話，使用者將會自動或依照特定指示，從 URL 更新元件。</span><span class="sxs-lookup"><span data-stu-id="7e642-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="7e642-137">在某些情況下，元件無法更新。</span><span class="sxs-lookup"><span data-stu-id="7e642-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="7e642-138">請嘗試再次存取內容，直到沒有其他撤銷，或由於某些原因而停止進程。</span><span class="sxs-lookup"><span data-stu-id="7e642-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e642-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e642-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e642-140">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="7e642-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 