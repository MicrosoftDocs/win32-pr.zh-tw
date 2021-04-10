---
title: 匯入授權和金鑰內容
description: 匯入授權和金鑰內容
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows Media Format SDK，DRM 匯入
- Windows Media Format SDK，匯入
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、金鑰材料
- DRM (數位版權管理) 、金鑰材料
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，金鑰材料
- 用戶端擴充 Api，金鑰材料
- 授權，匯入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184050"
---
# <a name="importing-license-and-key-material"></a><span data-ttu-id="1a535-119">匯入授權和金鑰內容</span><span class="sxs-lookup"><span data-stu-id="1a535-119">Importing License and Key Material</span></span>

<span data-ttu-id="1a535-120">如果您的媒體內容是使用協力廠商內容保護系統進行加密，而您想要將授權和金鑰內容匯入 Windows Media DRM 中，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1a535-120">If you have media content that was encrypted using a third-party content protection system and you want to import the license and key material into Windows Media DRM, follow these steps:</span></span>

1.  <span data-ttu-id="1a535-121">藉由呼叫 [**IWMDRMSecurity：： GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) 方法，來取出 WINDOWS Media DRM 電腦憑證集合。</span><span class="sxs-lookup"><span data-stu-id="1a535-121">Retrieve the Windows Media DRM machine certificate collection by calling the [**IWMDRMSecurity::GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) method.</span></span>
2.  <span data-ttu-id="1a535-122">剖析憑證集合，以確保其已正確簽署，並驗證為已知的 Microsoft 根公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="1a535-122">Parse the certificate collection, ensuring that it is signed correctly and is validated to a known Microsoft root public key.</span></span> <span data-ttu-id="1a535-123">憑證集合符合 XMR 架構。</span><span class="sxs-lookup"><span data-stu-id="1a535-123">The certificate collection conforms to the XMR schema.</span></span> <span data-ttu-id="1a535-124">如需詳細資訊，請參閱 [建立 XMR 授權](building-an-xmr-license.md)。</span><span class="sxs-lookup"><span data-stu-id="1a535-124">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>
3.  <span data-ttu-id="1a535-125">選擇性：藉由呼叫 [**IWMDRMSecurity：： GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) 方法，將撤銷清單解壓縮。</span><span class="sxs-lookup"><span data-stu-id="1a535-125">Optional: Extract the revocation list by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
4.  <span data-ttu-id="1a535-126">選擇性：確定未撤銷集合中的任何憑證。</span><span class="sxs-lookup"><span data-stu-id="1a535-126">Optional: Insure that no certificate in the collection is revoked.</span></span> <span data-ttu-id="1a535-127">如需詳細資訊，請參閱 [檢查憑證撤銷](checking-certificate-revocation.md)。</span><span class="sxs-lookup"><span data-stu-id="1a535-127">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
5.  <span data-ttu-id="1a535-128">產生 XMR 格式的授權，以代表匯入內容的原則需求，並包含適當的 Windows Media DRM 金鑰內容。</span><span class="sxs-lookup"><span data-stu-id="1a535-128">Generate a license in the XMR format that represents the policy requirements for the import content and contains the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="1a535-129">如需詳細資訊，請參閱 [建立 XMR 授權](building-an-xmr-license.md)的主題。</span><span class="sxs-lookup"><span data-stu-id="1a535-129">For more information, see the topic [Building an XMR License](building-an-xmr-license.md).</span></span>
6.  <span data-ttu-id="1a535-130">使用 [**IWMDRMLicenseManagement：： StoreLicense**](iwmdrmlicensemanagement-storelicense.md) 方法，將 XMR 授權傳遞給 WINDOWS Media DRM 系統進行處理。</span><span class="sxs-lookup"><span data-stu-id="1a535-130">Pass the XMR license to the Windows Media DRM system for processing, by using the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="1a535-131">當您授權 Windows Media DRM 時，將會為您提供 XMR 架構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1a535-131">Details about the XMR schema will be provided to you when you license Windows Media DRM.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1a535-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a535-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a535-133">**檢查憑證撤銷**</span><span class="sxs-lookup"><span data-stu-id="1a535-133">**Checking Certificate Revocation**</span></span>](checking-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="1a535-134">**建立 XMR 授權**</span><span class="sxs-lookup"><span data-stu-id="1a535-134">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="1a535-135">**DRM 匯入**</span><span class="sxs-lookup"><span data-stu-id="1a535-135">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




