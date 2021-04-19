---
description: 說明如何針對 YCbCr 影片媒體類型取樣色度。
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: 'MF_MT_VIDEO_CHROMA_SITING 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996789"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a>MF \_ MT \_ 視頻 \_ 色度 \_ 地點屬性

說明如何針對 Y'Cb'Cr 的影片媒體類型取樣色度。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling)列舉中的位 **or** 旗標。

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
</dt> <dt>

[擴充的色彩資訊](extended-color-information.md)
</dt> </dl>

 

 




