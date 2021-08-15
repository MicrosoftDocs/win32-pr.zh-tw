---
description: 每個音訊樣本中音訊資料的有效位數。
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: 'MF_MT_AUDIO_VALID_BITS_PER_SAMPLE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f84fa3938e4d74473da70bd28e5ccbb1bab71441c694b670cdb8b54bead31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973577"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>\_ \_ \_ \_ \_ 每個 \_ 樣本屬性的 MF MT 音訊有效位數

每個音訊樣本中音訊資料的有效位數。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

每個樣本屬性的 **MF \_ MT \_ 音訊 \_ 有效 \_ 位數 \_ \_** ，會用於在每個音訊樣本之後包含填補的音訊格式。 每個音訊樣本的總大小（包括填補位）都會提供給每個範例屬性的 [**MF \_ MT \_ 音訊 \_ 位 \_ \_**](mf-mt-audio-bits-per-sample-attribute.md) 。

如果未設定 [ **\_ \_ \_ \_ \_ 每個 \_ 範例的 mf mt 音訊有效位數** ] 屬性，請使用 [ [**\_ \_ \_ \_ 每個 \_ 樣本的 mf mt 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md) ] 屬性來尋找每個樣本的有效位數數目。

如果音訊格式未包含任何填補位，則不應設定這個屬性，或將其設定為與 [**\_ \_ \_ \_ 每個 \_ 範例的 MF MT 音訊位**](mf-mt-audio-bits-per-sample-attribute.md) 相同的值。

這個屬性會對應至 [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)結構的 **wValidBitsPerSample** 成員。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
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

 

 
