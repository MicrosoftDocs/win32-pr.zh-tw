---
description: DV 影片解碼篩選
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: DV 影片解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12131aa09f8e3f7dbef56504ad55410af11ffcbe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466045"
---
# <a name="dv-video-decoder-filter"></a>DV 影片解碼篩選

此篩選器會將數位視訊解碼 (DV) 串流轉換成未壓縮的影片。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>、 <strong>IPersistStream</strong>、 <strong>ISpecifyPropertyPages</strong> | |輸入 Pin 媒體類型 | <ul><li>MEDIATYPE_Video</li><li>MEDIASUBTYPE_dvsd</li><li>FORMAT_VideoInfo，FORMAT_DvInfo</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 | <strong>主要類型</strong>： MEDIATYPE_Video<strong>子</strong>類型：<br /><ul><li>MEDIASUBTYPE_YUY2</li><li>MEDIASUBTYPE_UYVY</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li><li>MEDIASUBTYPE_ARGB32</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_Y41P</li></ul><strong>格式類型</strong>：<br /> Format_VideoInfo，Format_VideoInfo2<br /> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_DVVideoCodec | |屬性頁 CLSID |CLSID_DVDecPropertiesPage | |可執行檔 |qdv.dll | | <a href="merit.md">業績</a> |MERIT_NORMAL | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

您可以使用 [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) 介面，將解碼解析度設定為 [完整]、[半大小]、[季大小] 或 [一到八個大小]。

**交錯**：較早版本的解碼器一律會將影片進行逐行掃描。 從 DirectX 9.0，DV Video 解碼器可以保留交錯。 這可讓 (VMR) 的影片混合轉譯器 deinterlaced 交錯式影片，以改善轉譯品質。 若要使用這項功能，下游篩選器必須支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)格式，並 \_ 以 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **formattype** 成員中的該值格式 VideoInfo2 表示。 在完整解析輸出中， **VIDEOINFOHEADER2** 結構中 (**dwInterlace**) 的去交錯旗標會設為 `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` ，表示交錯的欄位。 在半解析度或較低的情況下， **dwInterlace** 會設為零，表示漸進式框架。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




