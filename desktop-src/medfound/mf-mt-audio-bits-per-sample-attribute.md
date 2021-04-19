---
description: 音訊媒體類型的每個音訊樣本位數。
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: 'MF_MT_AUDIO_BITS_PER_SAMPLE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969268"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>\_每個樣本的 MF MT \_ 音訊 \_ 位數 \_ \_ 屬性

音訊媒體類型的每個音訊樣本位數。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會對應至 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **wBitsPerSample** 成員。

如果某些位包含填補，請設定每個樣本屬性的 [**MF \_ MT \_ 音訊 \_ 有效 \_ 位數 \_ \_**](mf-mt-audio-valid-bits-per-sample-attribute.md) ，以指定每個樣本中的有效音訊資料位數。

如果音訊包含每個樣本8個位，則音訊樣本為不帶正負號的值。  (每個音訊樣本的範圍為0–255。 ) 如果音訊包含每個樣本或更高的16個位，則音訊樣本為帶正負號的值。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 
