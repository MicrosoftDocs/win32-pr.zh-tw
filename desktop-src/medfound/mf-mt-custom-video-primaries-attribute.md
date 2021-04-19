---
description: 指定影片媒體類型的自訂色彩主要複本。
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: 'MF_MT_CUSTOM_VIDEO_PRIMARIES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980686"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>MF \_ MT \_ 自訂 \_ 影片 \_ 主要複本屬性

指定影片媒體類型的自訂色彩主要複本。

## <a name="data-type"></a>資料類型

**UINT32**

位元組陣列

## <a name="remarks"></a>備註

屬性資料是 [**MT \_ 自訂 \_ 影片 \_ 主要複本**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) 結構。

這個屬性會指定內容的實際色彩量或顯示。 CEA-861.3/SMPTE ST. 2006 色彩磁片區主控資訊是由解碼器儲存在這個屬性中。 請注意，此屬性不會取代 [**MF \_ MT \_ 影片 \_ 主要複本**](mf-mt-video-primaries-attribute.md)屬性。 此屬性描述內容之色彩量的提示，而 [ **MF \_ MT \_ 影片 \_ 主要複本** ] 則描述內容實際上的編碼方式的色彩主要複本 (例如：浮點數標記法之 R/g/B 通道中的1.0 意義) 。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




