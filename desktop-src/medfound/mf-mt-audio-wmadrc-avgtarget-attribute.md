---
description: 以 Windows Media 音訊檔的平均磁片區層級為目標。
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: 'MF_MT_AUDIO_WMADRC_AVGTARGET 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a05ef07966313d9b06bec57ec09af068f385bbc869cba7fab33e42e786dc63b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940628"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>MF \_ MT \_ 音訊 \_ WMADRC \_ AVGTARGET 屬性

以 Windows Media 音訊檔的平均磁片區層級為目標。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此屬性適用于 Windows Media 音訊編解碼器的音訊媒體類型。 它會指定內容的目標平均音量層級。 此解碼器可以使用此值來執行動態範圍控制。

如果 ASF 標頭包含 [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md)屬性， [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)方法會將此屬性新增至媒體類型。 此屬性記載于 Windows 媒體格式 SDK 檔中。

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

 

 
