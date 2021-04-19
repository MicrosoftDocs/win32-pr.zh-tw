---
description: 指定 h.264 影片串流的最大巨大區塊處理速率。
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: 'MF_MT_H264_MAX_MB_PER_SEC 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974181"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>MF \_ MT \_ H264 \_ \_ 每秒最大 MB \_ \_ 屬性

指定 h.264 影片串流的最大巨大區塊處理速率。

## <a name="data-type"></a>資料類型

**\[ UINT32 \]** 儲存為 **UINT8 \[ \]**

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。 屬性的值是 UINT32 值的陣列，對應至 UVC 1.5 h.264 影片格式描述項中的下欄欄位。

| Array 元素 | 描述項欄位                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwMaxMBperSecOneResolutionNoScalability**                |
| 1             | **dwMaxMBperSecTwoResolutionsNoScalability**               |
| 2             | **dwMaxMBperSecThreeResolutionsNoScalability**             |
| 3             | **dwMaxMBperSecFourResolutionsNoScalability**              |
| 4             | **dwMaxMBperSecOneResolutionTemporalScalability**          |
| 5             | **dwMaxMBperSecTwoResolutionsTemporalScalablility**        |
| 6             | **dwMaxMBperSecThreeResolutionsTemporalScalability**       |
| 7             | **dwMaxMBperSecFourResolutionsTemporalScalability**        |
| 8             | **dwMaxMBperSecOneResolutionTemporalQualityScalability**   |
| 9             | **dwMaxMBperSecTwoResolutionsTemporalQualityScalability**  |
| 10            | **dwMaxMBperSecThreeResolutionsTemporalQualityScalablity** |
| 11            | **dwMaxMBperSecFourResolutionsTemporalQualityScalability** |
| 12            | **dwMaxMBperSecOneResolutionFullScalability**              |
| 13            | **dwMaxMBperSecTwoResolutionsFullScalability**             |
| 14            | **dwMaxMBperSecThreeResolutionsFullScalability**           |
| 15            | **dwMaxMBperSecFourResolutionsFullScalability**            |



 

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




