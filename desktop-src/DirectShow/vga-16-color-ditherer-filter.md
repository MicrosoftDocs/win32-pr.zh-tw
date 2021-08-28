---
description: VGA 16 色 Ditherer 濾波器
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA 16 色 Ditherer 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36aed289a800a992bc061dc9822209bf4c2b5133647d995dfb675c7d5523bd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071942"
---
# <a name="vga-16-color-ditherer-filter"></a>VGA 16 色 Ditherer 濾波器

VGA 16 色 Ditherer 濾波器會從 RGB 色彩類型轉換成4位色彩，讓 AVI 和 MPEG 視頻資料流程可以顯示在較舊的16色監視器上。 此篩選器會在解壓縮程式篩選器和影片轉譯器篩選器之間的圖形中插入。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ RGB8                                                                                                               |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ RGB4                                                                                                               |
| 輸出 Pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ 遞色                                                                                                                                      |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                  |
| 可執行檔                               | quartz.dll                                                                                                                                         |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                                                                    |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



