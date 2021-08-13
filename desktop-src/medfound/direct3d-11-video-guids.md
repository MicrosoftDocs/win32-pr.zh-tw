---
description: 下列 Guid 支援 Direct3D 11 Video Api。
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: 'Direct3D 11 Video Guid (D3d11 .h) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905621e26edcc149d456d5d7b4ef7294ae39c80ae35955e9a19902484d5ff5eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346468"
---
# <a name="direct3d-11-video-guids"></a>Direct3D 11 影片 Guid

下列 Guid 支援 Direct3D 11 Video Api。

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ 金鑰 \_ 交換 \_ HW \_ 保護**
</dt> <dd> <dl> <dt>



指出此解碼器將從硬體型 DRM 元件接收資料

**D3D11 \_您 \_ 可以 \_ \_** 在 [**ID3D11VideoDevice：： CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession)函式的 *pKeyExchangeType* 參數中指定金鑰交換 HW 保護，以指出 [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)介面將純粹用於使用者模式 DRM 元件與安全執行環境之間的通訊。

指定此 GUID 時，不應該呼叫下列方法：

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoCoNtext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoCoNtext：:D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoCoNtext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoCoNtext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoCoNtext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ 解碼器 \_ 加密 \_ HW \_ CENC**
</dt> <dd> <dl> <dt>



指出此解碼器將從硬體型 DRM 元件接收資料

在傳遞給 [**ID3D11VideoDevice：： CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API 之 [**D3D11 \_ VIDEO \_ 解碼器 \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config)設定結構的 **guidConfigBitstreamEncryption** 成員中設定此 GUID，表示下列參數將會傳遞至 [**ID3D11VideoDevice：:D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)呼叫：



| 值                 | 描述                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | 包含 [**D3D11 \_ 影片 \_ 解碼器 \_ 開始 \_ 畫面格 \_ 加密 \_ 會話**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) 結構的大小。                                                                                                  |
| *pContentKey*    | [**D3D11 \_ 影片 \_ 解碼器 \_ 開始 \_ 畫面 \_ \_**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)格密碼編譯會話的指標，提供 [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)和解密框架所需的金鑰資訊。 |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>D3d11。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 11 影片 Api](direct3d-11-video-apis.md)
</dt> </dl>

 

 




