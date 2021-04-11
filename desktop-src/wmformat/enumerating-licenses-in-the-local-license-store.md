---
title: 列舉本機授權存放區中的授權
description: 列舉本機授權存放區中的授權
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK，列舉授權
- Windows Media Format SDK，授權
- Windows Media Format SDK，本機授權存放
- 數位版權管理 (DRM) ，列舉授權
- DRM (數位版權管理) ，列舉授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 的本機授權商店
- DRM (數位版權管理) ，本機授權商店
- DRM 用戶端擴充 Api，列舉授權
- 用戶端擴充 Api，列舉授權
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，本機授權存放
- 用戶端擴充 Api，本機授權存放
- 授權，列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372008"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="bf8f2-119">列舉本機授權存放區中的授權</span><span class="sxs-lookup"><span data-stu-id="bf8f2-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="bf8f2-120">「列舉」（Enumeration）是一種程式，可透過逐一逐步執行授權，取得本機授權存放區中授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="bf8f2-121">您可以藉由呼叫 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)來建立授權列舉。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="bf8f2-122">在存放區中列舉授權的最常見原因，是尋找特定授權以解密某些內容。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="bf8f2-123">[**IWMDRMLicense**](iwmdrmlicense.md)介面可作為個別授權結果和列舉值的入口網站。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="bf8f2-124">建立授權列舉時，會將清單中的第一個授權載入 **IWMDRMLicense** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="bf8f2-125">**IWMDRMLicense** 的大部分方法都可讓您取得授權的相關資訊，或根據授權建立物件以加密或解密內容。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="bf8f2-126">不過，有兩種方法可以控制列舉： [**GetNext**](iwmdrmlicense-getnext.md) 和 [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="bf8f2-127">**GetNext** 會將清單中的下一個授權載入介面。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="bf8f2-128">**ResetEnumeration** 會將列舉傳回至第一次建立時的狀態。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="bf8f2-129">重設列舉之後，會將清單中的第一個授權載入回 **IWMDRMLicense** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="bf8f2-130">當您到達清單中的最後一個授權時，下一次的 **GetNext** 呼叫會傳回錯誤，也就是 \_ 沒有 \_ 其他 \_ 專案。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="bf8f2-131">如果您的應用程式使用 DRM 所涵蓋的內容來執行動作，您應該檢查當地授權存放區中的授權，以取得許可權及其他限制因素，例如 (OPLs) 的輸出保護層級。</span><span class="sxs-lookup"><span data-stu-id="bf8f2-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf8f2-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf8f2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf8f2-133">**從本機授權存放中的授權取得資訊**</span><span class="sxs-lookup"><span data-stu-id="bf8f2-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




