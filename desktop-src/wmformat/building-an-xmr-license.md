---
title: 建立 XMR 授權
description: 建立 XMR 授權
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK，DRM 匯入
- Windows Media Format SDK，匯入
- Windows Media Format SDK，XMR 授權
- Windows Media Format SDK，授權
- 'Windows Media Format SDK，可延伸媒體許可權 (XMR) '
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、XMR 授權
- DRM (數位版權管理) 、XMR 授權
- '數位版權管理 (DRM) 的可延伸媒體許可權 (XMR) '
- 'DRM (數位版權管理) 、可延伸的媒體許可權 (XMR) '
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api、XMR 授權
- 用戶端擴充 Api、XMR 授權
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- 'DRM 用戶端擴充 Api、可擴充媒體許可權 (XMR) '
- '用戶端擴充 Api，可延伸媒體許可權 (XMR) '
- 授權，XMR
- '可擴充媒體許可權 (XMR) '
- 'XMR (可擴充媒體許可權) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371860"
---
# <a name="building-an-xmr-license"></a><span data-ttu-id="d7f3e-127">建立 XMR 授權</span><span class="sxs-lookup"><span data-stu-id="d7f3e-127">Building an XMR License</span></span>

<span data-ttu-id="d7f3e-128">若要產生 Windows Media DRM 的授權以進行處理，您必須使用可延伸媒體許可權 (XMR) 二進位架構。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-128">To generate a license for Windows Media DRM to process, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="d7f3e-129">XMR 是用來傳達媒體許可權和限制的架構，而且需要個別授權。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-129">XMR is a schema for conveying media usage rights and restrictions and needs to be licensed separately.</span></span>

<span data-ttu-id="d7f3e-130">授權中的重要資料會使用 Windows Media DRM 憑證集合中的公開金鑰進行加密，因此只有 Windows Media DRM 用戶端擴充 API 子系統才能看到此內容。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-130">The important material in a license is encrypted using the public key in the Windows Media DRM certificate collection, so it is visible only to the Windows Media DRM Client Extended API subsystem.</span></span> <span data-ttu-id="d7f3e-131">.</span><span class="sxs-lookup"><span data-stu-id="d7f3e-131">.</span></span>

<span data-ttu-id="d7f3e-132">您必須負責確保授權結構和原則設定有效，且與授權簽發者的意圖一致，而且它們符合合規性規則。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-132">It is your responsibility to ensure that the license structure and policy settings are valid and consistent with the license issuer's intent, and that they conform to the compliance rules.</span></span>

<span data-ttu-id="d7f3e-133">您應該閱讀 Windows Media DRM 匯入合規性規則，以瞭解必須存在於授權中的一組完整 XMR 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-133">You should read the Windows Media DRM import compliance rules to learn the complete set of XMR objects that must be present in the license.</span></span>

<span data-ttu-id="d7f3e-134">若要將 XMR 授權傳遞至 DRM 子系統，請呼叫 [**IWMDRMLicenseManagement：： StoreLicense**](iwmdrmlicensemanagement-storelicense.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-134">To pass the XMR license to the DRM subsystem, call the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span> <span data-ttu-id="d7f3e-135">使用下列格式，在 *bstrLicenseResponse* 參數中傳遞授權：</span><span class="sxs-lookup"><span data-stu-id="d7f3e-135">Use the following format to pass the license in the *bstrLicenseResponse* parameter:</span></span>


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



<span data-ttu-id="d7f3e-136">此字串必須是 Unicode 格式 (UTF-16) 。</span><span class="sxs-lookup"><span data-stu-id="d7f3e-136">This string must be in Unicode format (UTF-16).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7f3e-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7f3e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7f3e-138">**DRM 匯入**</span><span class="sxs-lookup"><span data-stu-id="d7f3e-138">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




