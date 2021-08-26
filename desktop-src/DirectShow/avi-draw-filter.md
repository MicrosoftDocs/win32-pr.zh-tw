---
description: AVI 繪製篩選
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: AVI 繪製篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003336a68bdc1591e6e9a3f8af139f4bf27ddc4d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471274"
---
# <a name="avi-draw-filter"></a>AVI 繪製篩選

當影片輸出到外部 NTSC 電視監視器時，會自動將 AVI 繪圖篩選器提取到播放圖形，而不是 [Avi 解壓縮](avi-decompressor-filter.md) 程式。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | |輸入 Pin 媒體類型 |主要類型： MEDIATYPE_VideoSubtypes：<br /><ul><li>MEDIASUBTYPE_MJPG</li><li>MEDIASUBTYPE_TVMJ</li><li>MEDIASUBTYPE_WAKE</li><li>MEDIASUBTYPE_CFCC</li><li>MEDIASUBTYPE_IJPG</li><li>MEDIASUBTYPE_Plum</li><li>MEDIASUBTYPE_DVCS</li><li>MEDIASUBTYPE_DVSD</li><li>MEDIASUBTYPE_MDVF</li><li>格式類型： FORMAT_VideoInfo</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |MEDIATYPE_Video，MEDIASUBTYPE_Null | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_AVIDraw | |屬性頁 CLSID |沒有屬性頁。 | |可執行檔 |quartz.dll | | <a href="merit.md">業績</a> |MERIT_NORMAL + 100 | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

由於 AVI Draw 篩選和 [VFW Capture 篩選器](vfw-capture-filter.md) 都連接到相同的硬體，因此它們不能在相同的篩選圖形中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




