---
description: MJPEG 壓縮程式篩選器
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG 壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7891a85aa32b0ec7572a8c3be08f216c75f8655a7782261a675521aa952bf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791388"
---
# <a name="mjpeg-compressor-filter"></a>MJPEG 壓縮程式篩選器

此篩選器會使用動畫 JPEG 壓縮來壓縮未壓縮的影片串流。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 **IPersistStream**                                                                                                                                                                                             |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| 輸出 Pin 介面                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                                                                                                                                   |
| 可執行檔                               | quartz.dll                                                                                                                                                                                                                                         |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                                                                |
| [篩選準則分類](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>備註

此篩選準則會使用 \_ 對應至 FOURCC 碼 ' MJPG ' 的媒體子類型 MEDIASUBTYPE MJPG 來進行編碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



