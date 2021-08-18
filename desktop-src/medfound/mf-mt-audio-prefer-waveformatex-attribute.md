---
description: 指定轉換音訊媒體類型時要使用的慣用舊版格式結構。
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: 'MF_MT_AUDIO_PREFER_WAVEFORMATEX 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035296"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>MF \_ MT \_ 音訊 \_ 偏好 \_ WAVEFORMATEX 屬性

指定轉換音訊媒體類型時要使用的慣用舊版格式結構。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性會提供 [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) 函數的提示。 如果屬性為 **TRUE**，則函式會盡可能將音訊媒體類型轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，而不是將它轉換成 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構。

[**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)函式會設定這個屬性。 您可以覆寫這個屬性的值，但是將此屬性設定為 **TRUE** 並不保證音訊媒體類型可以轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 形式。

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

 

 
