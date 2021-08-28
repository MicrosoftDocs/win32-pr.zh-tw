---
description: MPEG-2 影片解碼篩選器
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: MPEG-2 影片解碼篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468225"
---
# <a name="mpeg-1-video-decoder-filter"></a>MPEG-2 影片解碼篩選器

解碼 MPEG 1 影片。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong> | |輸入 Pin 媒體類型 |MEDIATYPE_Video，FORMAT_MPEGVideo<br /> 下列子類型有效：<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a> | |輸出釘選媒體類型 |主要類型： <strong>MEDIATYPE_Video</strong>、<br /> 格式類型： <strong>FORMAT_VideoInfo</strong> 或 <strong>FORMAT_VideoInfo2</strong><br /> 亞：<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID | <strong>CLSID_CMpegVideoCodec</strong> | |屬性頁 CLSID | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | |可執行檔 |quartz.dll | | <a href="merit.md">業績</a> |0x40000001 | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>備註

此篩選器可以解碼成 DirectDraw 表面。 如果電腦支援 MMX，則篩選器會使用 MMX。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




