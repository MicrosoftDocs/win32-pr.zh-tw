---
description: 指定影片媒體類型的色彩主要複本。
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: 'MF_MT_VIDEO_PRIMARIES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b4e1c99dc9a4f288ebab36d413f7eed7c74881e7c10d3c7e9a8a4fe3f0bcf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876708"
---
# <a name="mf_mt_video_primaries-attribute"></a>MF \_ MT \_ 影片 \_ 主要複本屬性

指定影片媒體類型的色彩主要複本。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) 列舉的成員。

[**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries)列舉會識別與特定常見影片標準相關聯的色彩主要複本。 如果媒體類型使用 **MFVideoPrimaries** 列舉中未識別的色彩主要複本，請設定 [ [**MF \_ MT \_ 自訂 \_ 影片 \_ 主要複本**](mf-mt-custom-video-primaries-attribute.md) ] 屬性，而不要設定此屬性。

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
</dt> <dt>

[擴充的色彩資訊](extended-color-information.md)
</dt> </dl>

 

 




