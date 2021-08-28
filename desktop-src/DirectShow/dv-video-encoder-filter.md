---
description: DV 影片編碼器篩選器
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV 影片編碼器篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14928c937313d056549a348bd255f251354c0ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482634"
---
# <a name="dv-video-encoder-filter"></a>DV 影片編碼器篩選器

此篩選會將未壓縮的影片串流編碼為數位視訊 (DV) 。 它會提供自訂介面 [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)，以設定編碼解析度和格式。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>、 <strong>IPersistStream</strong>、 <strong>ISpecifyPropertyPages</strong> | |輸入 Pin 媒體類型 | <ul><li>主要類型： MEDIATYPE_VideoThe 下列子類型有效：<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>格式類型： FORMAT_VideoInfo</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 | <ul><li>主要類型： MEDIATYPE_Video</li><li>子類型： MEDIASUBTYPE_dvsd</li><li>格式類型： FORMAT_VideoInfo</li></ul> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_DVVideoEnc | |屬性頁 CLSID |CLSID_DVEncPropertiesPage | |可執行檔 |qdv.dll | | <a href="merit.md">業績</a> |MERIT_DO_NOT_USE | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>備註

若為16位的影片 (MEDIASUBTYPE \_ RGB555 或 MEDIASUBTYPE \_ RGB565) ，則輸入必須為 720 x 480 圖元（NTSC）或 720 x 576 圖元（代表 PAL）。 若是24位的影片，輸入上沒有大小限制。

適用于 NTSC 的輸出一律是 720 x 480，或適用于 PAL 的 720 x 576;24位影片會調整成符合這些尺寸。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




