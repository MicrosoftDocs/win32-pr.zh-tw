---
description: 報告背景分割遮罩的中繼資料和遮罩緩衝區，以區分影片框架的背景和前景。
title: 'MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK 屬性 (Mfapi) '
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 1c9cf48235483f13cfa6f9fc04aace5baaf030cf1eb2597b86e9361176a0b9b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973977"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>MF \_ CAPTURE \_ 中繼資料 \_ 框架 \_ 背景 \_ 遮罩屬性

報告背景分割遮罩的中繼資料和遮罩緩衝區，以區分影片框架的背景和前景。

## <a name="data-type"></a>資料類型

**BLOB**

## <a name="remarks"></a>備註

這個屬性所傳送的資料是 [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) 結構，其中包含背景遮罩的維度及其推斷來源框架的涵蓋範圍的相關資訊，也就是資料流程輸出的框架。 它也會攜帶一個連續的緩衝區，代表取用應用程式所要使用的遮罩，以定義哪些圖元被視為前景或背景的一部分。 與框架相關之遮罩的縮放和影像座標相互關聯是由取用應用程式所處理。 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows組建22000t<br/>                          |
| 最低支援的伺服器<br/> | Windows組建22000<br/>                      |
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

 




