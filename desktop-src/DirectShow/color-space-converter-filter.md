---
description: 色彩空間轉換器篩選
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: 色彩空間轉換器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cadc3f980116f6745d578a06220639b181fe13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477364"
---
# <a name="color-space-converter-filter"></a>色彩空間轉換器篩選

這項轉換篩選會從一種 RGB 色彩類型轉換成另一種 RGB 類型，例如24位和8位 RGB 色彩。 由於這種類型的轉換在影片解壓縮程式中通常會更有效率地處理，因此當資料流程來源包含未壓縮的 RGB 框架時，就會使用色彩空間轉換器的主要用途。




| | |篩選介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | |輸入 Pin 媒體類型 |MEDIATYPE_Video，FORMAT_VideoInfo。<br /> 下列子類型有效：<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | |輸入 Pin 介面 | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |輸出釘選媒體類型 |MEDIATYPE_Video，FORMAT_VideoInfo。<br /> 下列子類型有效：<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | |輸出 Pin 介面 | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | |篩選 CLSID |CLSID_Colour | |屬性頁 CLSID |沒有屬性頁。 | |可執行檔 |quartz.dll | | <a href="merit.md">業績</a> |MERIT_UNLIKELY | | <a href="filter-categories.md">篩選準則類別</a> |CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




