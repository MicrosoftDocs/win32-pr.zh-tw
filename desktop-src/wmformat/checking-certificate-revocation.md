---
title: 檢查憑證撤銷
description: 檢查憑證撤銷
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows Media Format SDK，DRM 匯入
- Windows Media Format SDK，匯入
- Windows Media Format SDK，憑證撤銷
- Windows Media Format SDK，撤銷憑證
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) ，憑證撤銷
- DRM (數位版權管理) ，憑證撤銷
- 數位版權管理 (DRM) ，撤銷憑證
- DRM (數位版權管理) ，撤銷憑證
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，憑證撤銷
- 用戶端擴充 Api，憑證撤銷
- DRM 用戶端擴充 Api，撤銷憑證
- 用戶端擴充的 Api，撤銷憑證
- 憑證，撤銷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673023"
---
# <a name="checking-certificate-revocation"></a><span data-ttu-id="7797a-120">檢查憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="7797a-120">Checking Certificate Revocation</span></span>

<span data-ttu-id="7797a-121">將內容匯入 Windows Media DRM 時，您必須確認此集合中沒有任何憑證存在於撤銷清單中，以確定憑證集合中沒有任何憑證遭到撤銷。</span><span class="sxs-lookup"><span data-stu-id="7797a-121">When importing content into Windows Media DRM, you must ensure that no certificate in a certificate collection has been revoked by verifying that no certificate in the collection is in the revocation list.</span></span> <span data-ttu-id="7797a-122">撤銷清單是使用 [**IWMDRMSecurity：： GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) 方法來解壓縮。</span><span class="sxs-lookup"><span data-stu-id="7797a-122">The revocation list is extracted by using the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>

<span data-ttu-id="7797a-123">然後，您可以使用 [**IWMDRMSecurity：： CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) 方法來確認憑證未被撤銷。</span><span class="sxs-lookup"><span data-stu-id="7797a-123">You then use the [**IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) method to verify that the certificate is not revoked.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7797a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="7797a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7797a-125">**DRM 匯入**</span><span class="sxs-lookup"><span data-stu-id="7797a-125">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




