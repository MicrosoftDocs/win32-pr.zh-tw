---
description: MJPEG 解壓縮程式篩選器
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910016"
---
# <a name="mjpeg-decompressor-filter"></a>MJPEG 解壓縮程式篩選器

此篩選會將影片串流從動畫 JPEG 解碼成未壓縮的影片。 有些數位攝影機會產生運動 JPEG 影片串流。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ MJPG                                                                                                               |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                               |
| 輸出 Pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                                   |
| 可執行檔                               | quartz.dll                                                                                                                                         |
| [優點](merit.md)                       | 一般的業績 \_                                                                                                                                      |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>備註

此篩選與使用 FOURCC 碼 ' MJPG ' 的動畫 JPEG 影片相容。 它無法解碼其他各種不同的動畫 JPEG。 在這些情況下，您將需要使用協力廠商的解碼篩選器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



