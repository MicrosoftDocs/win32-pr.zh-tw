---
description: Windows Media 音訊檔案的參考平均音量層級。
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: 'MF_MT_AUDIO_WMADRC_AVGREF 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdde0bfb4c2993580d73981e9e121d1f7f18612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191888"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a>MF \_ MT \_ 音訊 \_ WMADRC \_ AVGREF 屬性

Windows Media 音訊檔案的參考平均音量層級。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此屬性適用于 Windows Media 音訊編解碼器的音訊媒體類型。 它會指定內容的原始平均音量層級。 此解碼器可以使用此值來執行動態範圍控制。

如果 ASF 標頭包含 [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md)屬性， [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)方法會將此屬性新增至媒體類型。 此屬性記載于 Windows Media Format SDK 檔中。

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

 

 
