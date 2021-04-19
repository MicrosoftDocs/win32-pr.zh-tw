---
description: 定義顯示光圈，也就是包含有效影像資料的影片框架區域。
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: 'MF_MT_MINIMUM_DISPLAY_APERTURE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972872"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>MF \_ MT \_ 最小 \_ 顯示 \_ 光圈屬性

定義顯示光圈，也就是包含有效影像資料的影片框架區域。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

屬性值是 [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) 結構。

最小顯示光圈是包含信號有效部分的區域。 光圈外面的圖元包含不正確資料，不應該顯示。

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

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[圖片外觀比例](picture-aspect-ratio.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MF \_ MT \_ 幾何 \_ 光圈**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




