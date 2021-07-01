---
description: 下列 Guid 支援 Direct3D 11 Video Api。
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: 'Direct3D 11 Video Guid (D3d11 .h) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f5277123c3d174427debc3f0ad5e184e49a6c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118633"
---
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="1fded-103">Direct3D 11 影片 Guid</span><span class="sxs-lookup"><span data-stu-id="1fded-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="1fded-104">下列 Guid 支援 Direct3D 11 Video Api。</span><span class="sxs-lookup"><span data-stu-id="1fded-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="1fded-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ 金鑰 \_ 交換 \_ HW \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="1fded-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1fded-106">指出此解碼器將從硬體型 DRM 元件接收資料</span><span class="sxs-lookup"><span data-stu-id="1fded-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="1fded-107">**D3D11 \_您 \_ 可以 \_ \_** 在 [**ID3D11VideoDevice：： CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession)函式的 *pKeyExchangeType* 參數中指定金鑰交換 HW 保護，以指出 [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)介面將純粹用於使用者模式 DRM 元件與安全執行環境之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="1fded-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="1fded-108">指定此 GUID 時，不應該呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="1fded-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="1fded-109">**ID3D11CryptoSession::GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="1fded-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="1fded-110">**ID3D11CryptoSession::GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="1fded-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="1fded-111">**ID3D11VideoCoNtext::EncryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="1fded-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="1fded-112">**ID3D11VideoCoNtext：:D ecryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="1fded-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="1fded-113">**ID3D11VideoCoNtext::StartSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="1fded-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="1fded-114">**ID3D11VideoCoNtext::FinishSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="1fded-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="1fded-115">**ID3D11VideoCoNtext::GetEncryptionBltKey**</span><span class="sxs-lookup"><span data-stu-id="1fded-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fded-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ 解碼器 \_ 加密 \_ HW \_ CENC**</span><span class="sxs-lookup"><span data-stu-id="1fded-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1fded-117">指出此解碼器將從硬體型 DRM 元件接收資料</span><span class="sxs-lookup"><span data-stu-id="1fded-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="1fded-118">在傳遞給 [**ID3D11VideoDevice：： CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API 之 [**D3D11 \_ VIDEO \_ 解碼器 \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config)設定結構的 **guidConfigBitstreamEncryption** 成員中設定此 GUID，表示下列參數將會傳遞至 [**ID3D11VideoDevice：:D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)呼叫：</span><span class="sxs-lookup"><span data-stu-id="1fded-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



| <span data-ttu-id="1fded-119">值</span><span class="sxs-lookup"><span data-stu-id="1fded-119">Value</span></span>                 | <span data-ttu-id="1fded-120">描述</span><span class="sxs-lookup"><span data-stu-id="1fded-120">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fded-121">*ContentKeySize*</span><span class="sxs-lookup"><span data-stu-id="1fded-121">*ContentKeySize*</span></span> | <span data-ttu-id="1fded-122">包含 [**D3D11 \_ 影片 \_ 解碼器 \_ 開始 \_ 畫面格 \_ 加密 \_ 會話**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="1fded-122">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="1fded-123">*pContentKey*</span><span class="sxs-lookup"><span data-stu-id="1fded-123">*pContentKey*</span></span>    | <span data-ttu-id="1fded-124">[**D3D11 \_ 影片 \_ 解碼器 \_ 開始 \_ 畫面 \_ \_**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)格密碼編譯會話的指標，提供 [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)和解密框架所需的金鑰資訊。</span><span class="sxs-lookup"><span data-stu-id="1fded-124">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fded-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fded-125">Requirements</span></span>



| <span data-ttu-id="1fded-126">需求</span><span class="sxs-lookup"><span data-stu-id="1fded-126">Requirement</span></span> | <span data-ttu-id="1fded-127">值</span><span class="sxs-lookup"><span data-stu-id="1fded-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fded-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fded-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1fded-129">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fded-129">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fded-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fded-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1fded-131">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fded-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1fded-132">標頭</span><span class="sxs-lookup"><span data-stu-id="1fded-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fded-133"><dt>D3d11。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fded-133"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fded-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fded-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fded-135">Direct3D 11 影片 Api</span><span class="sxs-lookup"><span data-stu-id="1fded-135">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




