---
title: 匯出壓縮的內容
description: 匯出壓縮的內容
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK，DRM 匯出
- Windows Media 格式 SDK，匯出
- Windows Media Format SDK，壓縮的內容
- 數位版權管理 (DRM) 、匯出
- DRM (數位版權管理) ，匯出
- 數位版權管理 (DRM) ，壓縮的內容
- DRM (數位版權管理) ，壓縮的內容
- DRM 用戶端擴充 Api，壓縮的內容
- 用戶端擴充的 Api，壓縮的內容
- DRM 用戶端擴充 Api，匯出
- 用戶端擴充 Api，匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839803"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="fcc52-114">匯出壓縮的內容</span><span class="sxs-lookup"><span data-stu-id="fcc52-114">Exporting Compressed Content</span></span>

<span data-ttu-id="fcc52-115">本節說明如何在應用程式接收壓縮數位媒體資料的 Windows Media 檔案上，匯出 Windows Media 受 DRM 保護的媒體。</span><span class="sxs-lookup"><span data-stu-id="fcc52-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="fcc52-116">若要這樣做，您的應用程式必須在 ASF 檔案中執行所有 Windows Media DRM 加密承載的內嵌解密。</span><span class="sxs-lookup"><span data-stu-id="fcc52-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="fcc52-117">系統會提供 ASF 剖析程式庫，作為 Windows Media DRM 匯出合約的一部分。</span><span class="sxs-lookup"><span data-stu-id="fcc52-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="fcc52-118">匯出壓縮內容所涉及的主要步驟如下：</span><span class="sxs-lookup"><span data-stu-id="fcc52-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="fcc52-119">視需要執行 DRM 的個人化。</span><span class="sxs-lookup"><span data-stu-id="fcc52-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="fcc52-120">確認已明確允許目標內容保護設定。</span><span class="sxs-lookup"><span data-stu-id="fcc52-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="fcc52-121">建立解密器物件來解密每個 ASF 承載。</span><span class="sxs-lookup"><span data-stu-id="fcc52-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="fcc52-122">DRM 系統會先將 Windows Media DRM 的每個 ASF 承載 transcrypts 至 RC4，再將其傳遞至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fcc52-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="fcc52-123">如果您的應用程式在 transcryption 期間變更了 ASF 承載的大小，您也必須 remultiplex ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fcc52-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="fcc52-124">傳遞給存根程式庫 Windows Media DRM 匯出應用程式憑證。</span><span class="sxs-lookup"><span data-stu-id="fcc52-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="fcc52-125">憑證經過驗證，如果有效，DRM 系統會產生初始化向量，並使用 RSA OAEP 進行加密。</span><span class="sxs-lookup"><span data-stu-id="fcc52-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="fcc52-126">藉由串連初始化向量和 salt 值，為每個承載建立 RC4 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="fcc52-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="fcc52-127">您將 salt 值提供給解密 API，您必須為每個承載將它遞增為非零的正整數值。</span><span class="sxs-lookup"><span data-stu-id="fcc52-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="fcc52-128">您將在 Windows Media DRM 匯出合約中提供 Microsoft 所提供的工具，可讓您產生自己的 RSA 公開/私密金鑰組。</span><span class="sxs-lookup"><span data-stu-id="fcc52-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="fcc52-129">您會將公開金鑰傳送給 Microsoft，Microsoft 會將它併入已簽署的 Windows Media DRM 應用程式憑證，並將其傳回。</span><span class="sxs-lookup"><span data-stu-id="fcc52-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="fcc52-130">每個裝載在使用 RC4 解密金鑰進行解密之後，都必須立即加密至輸出 CPS。</span><span class="sxs-lookup"><span data-stu-id="fcc52-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="fcc52-131">在 Windows Media DRM 匯出合約隨附的健全狀況與合規性規則中，處理未加密的承載有其他限制。</span><span class="sxs-lookup"><span data-stu-id="fcc52-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcc52-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcc52-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcc52-133">**ASF 承載解密和重新加密**</span><span class="sxs-lookup"><span data-stu-id="fcc52-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="fcc52-134">**DRM 匯出**</span><span class="sxs-lookup"><span data-stu-id="fcc52-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="fcc52-135">**執行 DRM 的個人化**</span><span class="sxs-lookup"><span data-stu-id="fcc52-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="fcc52-136">**驗證與初始化**</span><span class="sxs-lookup"><span data-stu-id="fcc52-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 




