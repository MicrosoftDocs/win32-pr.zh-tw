---
description: 包含適用于影片媒體類型的 MPEG-2 或 MPEG-2 序列標頭。
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: 'MF_MT_MPEG_SEQUENCE_HEADER 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e988a5b64b7b1c99d3c84de7441f492cebe07f0b473ee3f5256c732fbb7697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035146"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>MF \_ MT \_ MPEG \_ SEQUENCE \_ 標頭屬性

包含適用于影片媒體類型的 MPEG-2 或 MPEG-2 序列標頭。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

這個屬性會對應至 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)結構的 **dwSequenceHeader** 成員，或 [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)結構的 **bSequenceHeader** 成員。

針對 h264 和 h265 video，blob 包含附錄 B 格式的串連 [NAL 單位](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) 以及其起始程式碼。 具體來說，針對 h264 video，它們是 SPS & PPS NAL 單位。 針對 h265，它們是 VPS，SPS & PPS。

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

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 
