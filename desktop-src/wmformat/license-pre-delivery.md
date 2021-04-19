---
title: 授權預先傳遞
description: 授權預先傳遞
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media Format SDK，預先傳遞的授權
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、預先傳遞的授權
- DRM (數位版權管理) 、預先傳遞的授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api、預先傳遞的授權
- 用戶端擴充的 Api，預先傳遞的授權
- 預先傳遞的授權
- 授權、預先傳遞的授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968923"
---
# <a name="license-pre-delivery"></a><span data-ttu-id="4c52a-113">授權預先傳遞</span><span class="sxs-lookup"><span data-stu-id="4c52a-113">License Pre-Delivery</span></span>

<span data-ttu-id="4c52a-114">授權預先傳遞是用來將授權提取至用戶端電腦事先的流程。</span><span class="sxs-lookup"><span data-stu-id="4c52a-114">License pre-delivery is the process used to pull licenses to a client computer preemptively.</span></span> <span data-ttu-id="4c52a-115">使用預先傳遞的常見案例是當使用者訂閱音樂服務時。</span><span class="sxs-lookup"><span data-stu-id="4c52a-115">A common scenario for using pre-delivery is when a user subscribes to a music service.</span></span> <span data-ttu-id="4c52a-116">若未在需要的情況下傳遞授權，使用者就必須等候每個新歌曲的授權取得。</span><span class="sxs-lookup"><span data-stu-id="4c52a-116">Without delivering licenses before they are needed, the user would have to wait for license acquisition for each new song.</span></span>

<span data-ttu-id="4c52a-117">由於未在嘗試存取的情況下傳遞預先傳遞，因此通常只會由內容擁有者執行。</span><span class="sxs-lookup"><span data-stu-id="4c52a-117">Because pre-delivery is not done as a response to attempted access, it is typically performed only by the content owner.</span></span> <span data-ttu-id="4c52a-118">也就是說，您只能針對您所控制的內容預先提供授權。</span><span class="sxs-lookup"><span data-stu-id="4c52a-118">That is, you can only pre-deliver licenses for content that you control.</span></span> <span data-ttu-id="4c52a-119">預先傳遞程式是用戶端元件與使用 Windows Media 數位 Rights Management SDK 的物件所建立的授權伺服器之間的協調。</span><span class="sxs-lookup"><span data-stu-id="4c52a-119">The pre-delivery process is a coordination between a client component and a license server built by using the objects of the Windows Media Digital Rights Management SDK.</span></span>

<span data-ttu-id="4c52a-120">授權預先傳遞與 [非無訊息授權](non-silent-license-acquisition.md)取得類似。</span><span class="sxs-lookup"><span data-stu-id="4c52a-120">License pre-delivery is similar to [Non-Silent License Acquisition](non-silent-license-acquisition.md).</span></span> <span data-ttu-id="4c52a-121">遵循相同的步驟，但您沒有要傳遞至 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)的 DRM 標頭。</span><span class="sxs-lookup"><span data-stu-id="4c52a-121">Follow the same steps, except that you don't have a DRM header to pass to [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md).</span></span> <span data-ttu-id="4c52a-122">方法將會產生不是內容特定的挑戰，您可以傳送給授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="4c52a-122">The method will generate a challenge that is not content-specific that you can send to your license server.</span></span>

<span data-ttu-id="4c52a-123">或者，您可以使用 [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) 來預先傳遞授權。</span><span class="sxs-lookup"><span data-stu-id="4c52a-123">Alternatively you can use the [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) to pre-deliver licenses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c52a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c52a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c52a-125">**取得授權**</span><span class="sxs-lookup"><span data-stu-id="4c52a-125">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="4c52a-126">**使用媒體基礎事件模型**</span><span class="sxs-lookup"><span data-stu-id="4c52a-126">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 