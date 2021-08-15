---
description: 無限圖釘指標篩選
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: 無限圖釘指標篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28edb67da9d6aae01786cece43b45dfcd33d571b82bdbab21ecf82a2473ff0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818783"
---
# <a name="infinite-pin-tee-filter"></a>無限圖釘指標篩選

此篩選器會將傳遞給其輸入圖釘的樣本傳遞給變數的輸出接點數目。 當篩選準則的實例建立時，它會有一個輸出圖釘。 每次連線輸出連接時，篩選器會建立另一個輸出圖釘。 所有輸出圖釘都會共用與輸入 pin 相同的媒體類型。

此篩選器的版本也會以 SDK 範例的形式提供。 請參閱 [InfTee 篩選範例](inftee-filter-sample.md)。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| 輸入 Pin 媒體類型                    | 任何媒體類型                                                                                                                                     |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| 輸出 Pin 媒體類型                   | 任何媒體類型。 輸出類型永遠符合輸入類型，適用于所有輸出釘選                                                                 |
| 輸出 Pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                                   |
| 可執行檔                               | qcap.dll                                                                                                                                           |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



