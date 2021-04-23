---
description: AVI 分隔器篩選
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI 分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909656"
---
# <a name="avi-splitter-filter"></a>AVI 分隔器篩選

AVI 分隔器篩選器是用來播放 AVI 檔。 它接受 AVI 格式的資料，並將其分割成其組成的資料流程，以進行進一步的處理和/或轉譯。



| 標籤 | 值 |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Avi                                                                                                                                |
| 輸入 Pin 介面                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| 輸出 Pin 媒體類型                   | 通常是媒體或 **媒體 \_** 媒體的 **媒體 \_** 。 確切的類型取決於檔案的內容、是否壓縮檔案，以及使用何種編解碼器。 |
| 輸出 Pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、IPropertyBag、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| 篩選 CLSID                             | CLSID \_ AviSplitter                                                                                                                                                  |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                                   |
| 可執行檔                               | quartz.dll                                                                                                                                                          |
| [優點](merit.md)                       | 一般的業績 \_                                                                                                                                                       |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                       |



 

## <a name="remarks"></a>備註

此篩選通常會連接到其輸入 pin 的 [非同步檔案來源](file-source--async--filter.md) 篩選。 它可以連線到輸出 pin 支援 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 的任何篩選器，並提供正確的媒體類型給 AVI 分隔器篩選的輸入圖釘。

AVI 分隔器上的輸出圖釘支援 IPropertyBag：： Read 方法，以便從個別資料流程讀取屬性。 目前已定義下列屬性。



| 屬性 | 描述                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME     | 傳回從 AVI 檔案中的區塊取得的資料流程名稱 `'strn'` 。 如果這個區塊不存在，Read 方法會傳回 E \_ INVALIDARG。 |



 

IPropertyBag：： Write 方法會傳回 E \_ FAIL。 [Avi Mux](avi-mux-filter.md)篩選支援 IPropertyBag：： Write，可將資料流程屬性儲存到 AVI 檔案中。

AVI 分隔器不允許下游篩選器使用自己的配置器。

檔案中交錯的持續時間會決定 AVI 分隔器將配置多少記憶體來處理它。 交錯在一個第二個區塊中的檔案需要更多的記憶體來處理，而不是將交錯期間設定為一或兩個畫面格的檔案。 在新式電腦上，除非您同時執行 AVI 分隔器的多個實例，否則這通常不是問題。

### <a name="seeking"></a>尋求

如果檔案包含影片資料流程，AVI 分隔器支援依框架編號搜尋。 若要啟用以框架為基礎的搜尋，請在 [篩選圖形管理員](filter-graph-manager.md)上以值 **時間 \_ 格式 \_ 框架** 呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。

如果檔案包含音訊串流，AVI 分隔器支援依樣本數進行搜尋。 若要啟用以範例為基礎的搜尋，請使用值 **時間 \_ 格式 \_ 範例**，在篩選圖形管理員上呼叫 [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。

在這兩種情況下，該資料流程的輸出圖釘都必須連接到轉譯器篩選器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



