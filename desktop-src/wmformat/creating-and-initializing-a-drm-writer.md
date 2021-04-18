---
title: 建立和初始化 DRM 寫入器
description: 建立和初始化 DRM 寫入器
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK，DRM 寫入器
- 數位版權管理 (DRM) ，建立 DRM 寫入器
- DRM (數位版權管理) ，建立 DRM 寫入器
- 數位版權管理 (DRM) ，初始化 DRM 寫入器
- DRM (數位版權管理) ，初始化 DRM 寫入器
- DRM 用戶端擴充 Api，DRM 寫入器
- 用戶端擴充 Api，DRM 寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106965872"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="2f519-110">建立和初始化 DRM 寫入器</span><span class="sxs-lookup"><span data-stu-id="2f519-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="2f519-111">必須執行下列步驟，才能初始化 ASF 寫入器物件，以便在 Windows Media DRM 中匯入加密的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="2f519-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="2f519-112">遵循匯 [入授權和金鑰內容](importing-license-and-key-material.md)的步驟1到4。</span><span class="sxs-lookup"><span data-stu-id="2f519-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="2f519-113">使用適當的 Windows Media DRM 金鑰內容，建立及初始化 ASF 寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="2f519-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="2f519-114">如需詳細資訊，請參閱 [啟用 DRM 支援](enabling-drm-support.md)。</span><span class="sxs-lookup"><span data-stu-id="2f519-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="2f519-115">藉由呼叫 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)來設定下列每個屬性：</span><span class="sxs-lookup"><span data-stu-id="2f519-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="2f519-116">DRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="2f519-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="2f519-117">DRM \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="2f519-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="2f519-118">DRM \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="2f519-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="2f519-119">DRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="2f519-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="2f519-120">如果執行軟體的電腦上未安裝 Windows Media Rights Manager 的授權版本，則也必須設定下列四個屬性：</span><span class="sxs-lookup"><span data-stu-id="2f519-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="2f519-121">DRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="2f519-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="2f519-122">DRM \_ LASignatureCert</span><span class="sxs-lookup"><span data-stu-id="2f519-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="2f519-123">DRM \_ LASignatureLicSrvCert</span><span class="sxs-lookup"><span data-stu-id="2f519-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="2f519-124">DRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="2f519-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="2f519-125">您可以填寫 [Windows Media 授權合約 (WMLA) ](https://www.microsoft.com/licensing/default) online，來完成必要加密憑證的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2f519-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="2f519-126">建立工作階段金鑰，並填寫 WMDRM 匯 [**\_ 入 \_ 會話 \_ 金鑰**](wmdrm-import-session-key.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2f519-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="2f519-127">工作階段金鑰將用來加密內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f519-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="2f519-128">如需範例，請參閱 [建立工作階段金鑰範例](create-session-key-example.md)。</span><span class="sxs-lookup"><span data-stu-id="2f519-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="2f519-129">從隨機 RC4 初始化向量建立內容金鑰，並填寫 [**WMDRM 匯 \_ 入 \_ 內容 \_ 金鑰**](wmdrm-import-content-key.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2f519-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="2f519-130">內容金鑰是用來加密媒體範例。</span><span class="sxs-lookup"><span data-stu-id="2f519-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="2f519-131">如需範例，請參閱 [建立內容金鑰範例](create-content-key-example.md)。</span><span class="sxs-lookup"><span data-stu-id="2f519-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="2f519-132">使用 RC4 加密，以工作階段金鑰加密內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f519-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="2f519-133">解壓縮電腦憑證集合金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f519-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="2f519-134">如需範例，請參閱 [取得電腦憑證範例](get-machine-certificate-example.md)。</span><span class="sxs-lookup"><span data-stu-id="2f519-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="2f519-135">使用從憑證解壓縮的公開金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f519-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="2f519-136">填寫 WMDRM 匯 [**\_ 入 \_ INIT \_ 結構**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) 結構。</span><span class="sxs-lookup"><span data-stu-id="2f519-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="2f519-137">呼叫 [**IWMDRMWriter3：： SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) 方法來通知 SDK，進入寫入器的範例已經受到保護，而且應該直接傳送到 WINDOWS Media DRM 用戶端以進行匯入。</span><span class="sxs-lookup"><span data-stu-id="2f519-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="2f519-138">呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)。</span><span class="sxs-lookup"><span data-stu-id="2f519-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="2f519-139">您可以在 Windows Media Format SDK 程式設計指南中記載建立受 DRM 保護之檔案的其餘步驟。</span><span class="sxs-lookup"><span data-stu-id="2f519-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="2f519-140">如需詳細資訊，請參閱 [建立受保護](creating-protected-files.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="2f519-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="2f519-141">下一步是逐一查看每個媒體範例、將其加密，然後將其傳遞至寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="2f519-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="2f519-142">如需詳細資訊，請參閱 [加密和匯入媒體範例](encrypting-and-importing-media-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="2f519-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f519-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f519-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f519-144">**屬性**</span><span class="sxs-lookup"><span data-stu-id="2f519-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="2f519-145">**DRM 匯入**</span><span class="sxs-lookup"><span data-stu-id="2f519-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




