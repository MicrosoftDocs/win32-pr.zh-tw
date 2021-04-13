---
description: MJPEG 解壓縮程式篩選器
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510275"
---
# <a name="mjpeg-decompressor-filter"></a>MJPEG 解壓縮程式篩選器

此篩選會將影片串流從動畫 JPEG 解碼成未壓縮的影片。 有些數位攝影機會產生運動 JPEG 影片串流。



|                                          |                                                                                                                                                    |
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

 

 



