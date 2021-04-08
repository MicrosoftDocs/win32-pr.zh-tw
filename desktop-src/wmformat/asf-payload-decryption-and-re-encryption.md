---
title: ASF 承載解密和重新加密
description: ASF 承載解密和重新加密
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows Media 格式 SDK、ASF 承載解密和重新加密
- Windows Media Format SDK、承載解密和重新加密
- Windows Media Format SDK，解密
- Windows Media Format SDK，重新加密
- 數位版權管理 (DRM) 、ASF 承載解密和重新加密
- DRM (數位版權管理) 、ASF 承載解密和重新加密
- 數位版權管理 (DRM) 、承載解密和重新加密
- DRM (數位版權管理) 、承載解密和重新加密
- 數位版權管理 (DRM) 、解密
- DRM (數位版權管理) 、解密
- 數位版權管理 (DRM) ，重新加密
- DRM (數位版權管理) ，重新加密
- DRM 用戶端擴充 Api、ASF 承載解密和重新加密
- 用戶端擴充 Api、ASF 承載解密和重新加密
- DRM 用戶端擴充 Api、承載解密和重新加密
- 用戶端擴充 Api、承載解密和重新加密
- DRM 用戶端擴充 Api，解密
- 用戶端擴充 Api，解密
- DRM 用戶端擴充 Api，重新加密
- 用戶端擴充 Api，重新加密
- Advanced Systems Format (ASF) 、重新加密
- ASF (Advanced Systems Format) ，重新加密
- Advanced Systems Format (ASF) 、解密
- ASF (Advanced Systems Format) 、解密
- Advanced Systems Format (ASF) 、承載解密和重新加密
- ASF (Advanced 系統格式) 、承載解密和重新加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671444"
---
# <a name="asf-payload-decryption-and-re-encryption"></a><span data-ttu-id="ee0cf-129">ASF 承載解密和重新加密</span><span class="sxs-lookup"><span data-stu-id="ee0cf-129">ASF Payload Decryption and Re-encryption</span></span>

<span data-ttu-id="ee0cf-130">下列步驟描述應用程式必須完成才能解密和重新加密每個承載的動作：</span><span class="sxs-lookup"><span data-stu-id="ee0cf-130">The steps below describe the actions that an application must complete to decrypt and re-encrypt each payload:</span></span>

1.  <span data-ttu-id="ee0cf-131">遞增 salt 值。</span><span class="sxs-lookup"><span data-stu-id="ee0cf-131">Increment the salt value.</span></span>
2.  <span data-ttu-id="ee0cf-132">傳遞 (以 Windows Media DRM) 加密的承載，並將 salt 值傳遞給解密函式 [**IWMDRMDecrypt：:D ecrypt**](iwmdrmdecrypt-decrypt.md)，這會傳回使用 RC4 公開金鑰加密的承載。</span><span class="sxs-lookup"><span data-stu-id="ee0cf-132">Pass the payload (encrypted with Windows Media DRM) and the salt value to the decryption function, [**IWMDRMDecrypt::Decrypt**](iwmdrmdecrypt-decrypt.md), which will return the payload, encrypted using the RC4 public key.</span></span>
3.  <span data-ttu-id="ee0cf-133">藉由套用與 salt 值串連之初始化向量的 SHA-1 雜湊，來衍生暫時性的 RC4 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ee0cf-133">Derive a transitory RC4 key by applying an SHA-1 hash of the initialization vector concatenated with the salt value.</span></span>
4.  <span data-ttu-id="ee0cf-134">使用您的暫時性金鑰來解密承載。</span><span class="sxs-lookup"><span data-stu-id="ee0cf-134">Use your transitory key to decrypt the payload.</span></span>
5.  <span data-ttu-id="ee0cf-135">根據 Windows Media DRM 匯出合規性和穩定性規則，以授權的內容保護設定立即重新加密承載。</span><span class="sxs-lookup"><span data-stu-id="ee0cf-135">Immediately re-encrypt the payload with the authorized content protection scheme according to the Windows Media DRM export compliance and robustness rules.</span></span>
6.  <span data-ttu-id="ee0cf-136">找出下一個承載。</span><span class="sxs-lookup"><span data-stu-id="ee0cf-136">Locate the next payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee0cf-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee0cf-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee0cf-138">**匯出壓縮的內容**</span><span class="sxs-lookup"><span data-stu-id="ee0cf-138">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




