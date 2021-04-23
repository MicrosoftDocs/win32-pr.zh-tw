---
description: AVI 解壓縮程式篩選
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: AVI 解壓縮程式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910096"
---
# <a name="avi-decompressor-filter"></a>AVI 解壓縮程式篩選

AVI 解壓縮程式篩選器可讓影片壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器來聯結篩選圖形。 應用程式不需要將篩選新增至篩選圖形;篩選圖形管理員會在需要時自動提取。

當篩選圖形管理員建立圖形來轉譯 AVI 檔案時，它會檢查檔案的 AVI 標頭中的 FOURCC，以判斷影片資料流程是否已壓縮。 如果是，則篩選圖形管理員會新增 AVI 解壓縮程式，然後在登錄中搜尋可處理檔案的已安裝解壓縮程式。

> [!Note]  
> MPEG decompressors 絕不會實作為 BC-VCM-LVM-HYPERV 編解碼器，而只會實作為原生的 DirectShow 篩選。

 

在其上游釘選上，AVI 解壓縮器通常會連接到 [Avi 分隔器](avi-splitter-filter.md)。 在其輸出釘選上，通常會連接到 [影片](video-renderer-filter.md) 轉譯 [器或 AVI Mux 篩選器](avi-mux-filter.md)。



| 標籤 | 值 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| 輸入 Pin 媒體類型                    | 主要類型：媒體類型 \_ VideoSubtype：必須對應到壓縮類型的 FOURCC 程式碼。 如需詳細資訊，請參閱 [FOURCC 代碼](fourcc-codes.md)。<br/> 格式類型： \_ VIDEOINFO 格式<br/> |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null、FORMAT \_ VideoInfo                                                                                                                                                            |
| 輸出 Pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| 篩選 CLSID                             | CLSID \_ AVIDec                                                                                                                                                                                                      |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                                                                                  |
| 可執行檔                               | quartz.dll                                                                                                                                                                                                         |
| [優點](merit.md)                       | 一般的業績 \_                                                                                                                                                                                                      |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 




