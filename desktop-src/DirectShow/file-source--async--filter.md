---
description: 檔案來源 (Async) 篩選
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: 檔案來源 (Async) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909696"
---
# <a name="file-source-async-filter"></a>檔案來源 (Async) 篩選

非同步檔案來源篩選會開啟並讀取許多不同資料格式的本機檔案，並將資料傳遞至剖析器篩選器。

若要透過 HTTP 從 web 下載媒體檔案，請使用檔案 [來源 (URL) ](file-source--url--filter.md) 篩選。 若要讀取 ASF 檔案，請使用 [ [WM Asf 讀取](wm-asf-reader-filter.md) 器] 篩選器。



| 標籤 | 值 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| 輸入 Pin 媒體類型                    | 不適用                                                                                                                       |
| 輸入 Pin 介面                     | 不適用                                                                                                                       |
| 輸出 Pin 媒體類型                   | **媒體媒體 \_資料流程**。 子類型相依于媒體格式。 如果篩選無法辨識格式， (**MEDIASUBTYPE \_ Null** 。 )  |
| 輸出 Pin 介面                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)、 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| 篩選 CLSID                             | **CLSID \_ AsyncReader**                                                                                                               |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                     |
| 可執行檔                               | quartz.dll                                                                                                                           |
| [優點](merit.md)                       | **不 \_ 太可能**                                                                                                                  |
| [篩選準則分類](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



