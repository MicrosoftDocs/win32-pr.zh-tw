---
title: 刪除授權
description: 刪除授權
ms.assetid: f941efeb-145d-48a1-a3e2-d12f66b7fdcf
keywords:
- Windows Media Format SDK，授權
- Windows Media Format SDK，刪除授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) ，刪除授權
- DRM (數位版權管理) ，刪除授權
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，刪除授權
- 用戶端擴充 Api，刪除授權
- 授權，刪除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f297db679ac2c8afe2c836d032fa045d6955665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967623"
---
# <a name="license-deletion"></a><span data-ttu-id="0c582-114">刪除授權</span><span class="sxs-lookup"><span data-stu-id="0c582-114">License Deletion</span></span>

<span data-ttu-id="0c582-115">您可以藉由呼叫 [**IWMDRMLicenseManagement：:P rocesslicensedeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) 方法來刪除在本機建立的任何協力廠商授權（例如透過 DRM 匯入）。</span><span class="sxs-lookup"><span data-stu-id="0c582-115">Any third-party licenses created locally, for example through DRM import, can be deleted by calling the [**IWMDRMLicenseManagement::ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md) method.</span></span> <span data-ttu-id="0c582-116">您傳遞給這個方法的字串將會是 XMR 授權，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0c582-116">The string you pass to this method will be an XMR license that resembles the following:</span></span>


```C++
<response type="LRB">
  <DATA>
    <LICENSEDATA>
      <DATA>
        <KID>include Key ID here to revoke certain keys</KID>
        <LID>rights ID</LID
        <META>
          <LGPUBKEY>
            <PublicKey>
              <Modulus>base64 encoded public key</Modulus>
              <Exponent>Exponent in network byte order</Exponent>
            </PublicKey>
          </LGPUBKEY>
          <UID>content-owner-specific user ID</UID>
        </META>
      </DATA>
    </LICENSEDATA>
  </DATA>
</response>
```



<span data-ttu-id="0c582-117">擁有者特定的使用者識別碼 (UID) 欄位是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0c582-117">The owner specific user ID (UID) field is optional.</span></span> <span data-ttu-id="0c582-118">如果沒有任何相關聯的資料，則不一定要在授權回應中包含選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="0c582-118">Optional fields must not be included in the license response if there is not any data associated with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c582-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c582-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c582-120">**建立 XMR 授權**</span><span class="sxs-lookup"><span data-stu-id="0c582-120">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> <dt>

[<span data-ttu-id="0c582-121">**DRM 匯入**</span><span class="sxs-lookup"><span data-stu-id="0c582-121">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="0c582-122">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="0c582-122">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




