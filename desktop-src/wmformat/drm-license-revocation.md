---
title: " (Microsoft Windows Media DRM 用戶端) 的授權撤銷"
description: " (Microsoft Windows Media DRM 用戶端) 的授權撤銷"
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK，授權
- Windows Media Format SDK，授權撤銷
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、授權撤銷
- DRM (數位版權管理) 、授權撤銷
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，授權撤銷
- 用戶端擴充 Api，授權撤銷
- 授權，撤銷
- 授權撤銷，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195672"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="65c2f-115"> (Microsoft Windows Media DRM 用戶端) 的授權撤銷</span><span class="sxs-lookup"><span data-stu-id="65c2f-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="65c2f-116">授權撤銷是指移除本機授權存放區中的授權。</span><span class="sxs-lookup"><span data-stu-id="65c2f-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="65c2f-117">當服務提供者（例如，音樂訂閱服務）必須停用使用者電腦上的服務時，就會發生授權撤銷的常見案例。</span><span class="sxs-lookup"><span data-stu-id="65c2f-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="65c2f-118">授權撤銷程式是由授權簽發者所提供的服務所起始。</span><span class="sxs-lookup"><span data-stu-id="65c2f-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="65c2f-119">您的應用程式可以裝載此服務，也可以是 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="65c2f-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="65c2f-120">無論是哪一種情況，您的應用程式都必須能夠收到服務所建立的授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="65c2f-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="65c2f-121">若要移除授權存放區的授權，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="65c2f-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="65c2f-122">收到授權簽發者的授權挑戰時，請使用 [**IWMDRMLicenseManagement：： CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) 方法建立撤銷挑戰。</span><span class="sxs-lookup"><span data-stu-id="65c2f-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="65c2f-123">這個方法會配置包含撤銷挑戰資料的緩衝區，此資料會透過 *ppbChallengeOutput* 參數傳遞至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="65c2f-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="65c2f-124">將授權撤銷挑戰傳送到授權撤銷服務。</span><span class="sxs-lookup"><span data-stu-id="65c2f-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="65c2f-125">伺服器將會產生 (LRB) 的授權撤銷 BLOB 以回應。</span><span class="sxs-lookup"><span data-stu-id="65c2f-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="65c2f-126">使用 [**IWMDRMLicenseManagement：:P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) 方法來移除本機存放區中的授權，並傳遞授權伺服器所傳回的 LRB。</span><span class="sxs-lookup"><span data-stu-id="65c2f-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="65c2f-127">使用 **CoTaskMemFree** 函數，將 **CreateLicenseRevocationChallenge** 所配置的緩衝區解除配置。</span><span class="sxs-lookup"><span data-stu-id="65c2f-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="65c2f-128">如需有關授權撤銷的運作方式或如何撰寫撤銷服務的詳細資訊，請參閱 [實施授權撤銷](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)。</span><span class="sxs-lookup"><span data-stu-id="65c2f-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="65c2f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="65c2f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c2f-130">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="65c2f-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="65c2f-131">**本機授權商店**</span><span class="sxs-lookup"><span data-stu-id="65c2f-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="65c2f-132">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="65c2f-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 