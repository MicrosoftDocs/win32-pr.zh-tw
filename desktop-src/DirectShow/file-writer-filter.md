---
description: 檔案寫入器篩選
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: 檔案寫入器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187540"
---
# <a name="file-writer-filter"></a>檔案寫入器篩選

檔案寫入器篩選器可以用來將檔案寫入光碟，而不管格式為何。 篩選器只會寫入其輸入 pin 所收到的光碟，因此必須將上游連接到可正確格式化檔案的多工器。 您可以使用檔案寫入器建立新的輸出檔，或指定現有的檔案;如果檔案已存在，則會以新資料完全覆寫該檔案。

檔案寫入器篩選器會使用輸入資料流程的時間戳記做為檔案位移，並提供檔案的隨機存取。 它支援 **IStream** ，以允許在圖形停止之後讀取和寫入檔案標頭。 為了改善效能，它也支援未緩衝的重迭寫入，並處理對應的緩衝區協商。

> [!Note]  
> 若要寫入 ASF 檔案，請使用 [WM Asf 寫入](wm-asf-writer-filter.md) 器篩選器。

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter)、 [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)、 **IPersistStream** |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                              |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 **IStream**                                                                                |
| 輸出 Pin 媒體類型                   | 不適用                                                                                                                                                                                     |
| 輸出 Pin 介面                    | 不適用                                                                                                                                                                                     |
| 篩選 CLSID                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                                                                                   |
| 可執行檔                               | qcap.dll                                                                                                                                                                                           |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



