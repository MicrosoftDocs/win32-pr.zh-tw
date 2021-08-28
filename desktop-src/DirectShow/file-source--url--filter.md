---
description: 檔案來源 (URL) 篩選
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: 檔案來源 (URL) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a096d25e5e04246385ece9662ed93e209115756491b1a3581cbb01de38225e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685618"
---
# <a name="file-source-url-filter"></a>檔案來源 (URL) 篩選

URL 檔案來源篩選器是一般的非同步來源篩選，可搭配可透過統一資源定位器識別的任何原始程式檔 (URL) ，以及其媒體主要類型為 stream。 這包括 AVI、MOV、MPEG 和 WAV 檔案。 下游篩選器需要是剖析器，例如 [MPEG 1 串流分隔](mpeg-1-stream-splitter-filter.md)器、 [AVI 分隔器](avi-splitter-filter.md)或 [QuickTime Movie](quicktime-movie-parser-filter.md)剖析器。



| 標籤 | 值 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| 輸入 Pin 媒體類型                    | 不適用                                                                                                                       |
| 輸入 Pin 介面                     | 不適用                                                                                                                       |
| 輸出 Pin 媒體類型                   | 媒體 \_ 的串流。 子類型相依于媒體格式。 \_如果篩選無法辨識格式， (MEDIASUBTYPE Null。 )          |
| 輸出 Pin 介面                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)、 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| 篩選 CLSID                             | CLSID \_ URLReader                                                                                                                     |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                     |
| 可執行檔                               | quartz.dll                                                                                                                           |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                                                      |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                        |



 

## <a name="remarks"></a>備註

此篩選器會使用 Urlmon.dll，並支援字碼頁。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



