---
description: 讓 capture engine 使用具有使用規定限制的解碼器。
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: 'MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f586325f883595e1336ed946611850b3c51d5443dbd9f6e68830502284a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061065"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>MF \_ CAPTURE \_ ENGINE \_ 解碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性屬性

讓 capture engine 使用具有使用規定限制的解碼器。

## <a name="data-type"></a>資料類型

**IUnknown\***

## <a name="remarks"></a>備註

這個屬性的值是 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 介面的指標，由呼叫端所執行。 呼叫端的這個介面的實作為預期會使用與解碼器的交握，如 [使用限制的欄位](field-of-use-restrictions.md)所述。 Microsoft 媒體基礎不會定義交握，通常會牽涉到某種類型的密碼編譯交換。

就內部而言，capture 引擎會設定解碼器的 [MFT \_ FIELDOFUSE \_ UNLOCK \_ attribute](mft-fieldofuse-unlock-attribute.md)屬性，以設定 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)上的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




