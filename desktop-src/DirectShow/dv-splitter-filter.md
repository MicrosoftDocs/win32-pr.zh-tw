---
description: DV 分隔器篩選
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: DV 分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ca8e856f1a49ff22ee05f7dc0ae341fad6aa91
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908406"
---
# <a name="dv-splitter-filter"></a>DV 分隔器篩選

此篩選器會將交錯數位視訊 (DV) stream 分割成其元件的影片和音訊串流。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| 輸入 Pin 媒體類型                    | 媒體 \_ 中交錯、MEDIASUBTYPE \_ DVSD、格式 \_ DvInfo                                                                                         |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| 輸出 Pin 媒體類型                   | **影片**：媒體媒體 \_ ，格式 \_ DvInfo<br/> **音訊**：媒體媒體 \_ 、MEDIASUBTYPE \_ PCM、格式 \_ WaveFormatEx<br/>             |
| 輸出 Pin 介面                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| 篩選 CLSID                             | CLSID \_ DVSplitter                                                                                                                                  |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                  |
| 可執行檔                               | qdv.dll                                                                                                                                            |
| [優點](merit.md)                       | 一般的業績 \_                                                                                                                                      |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>備註

DV 框架在相同的框架中包含音訊和影片。 DV 分隔器篩選器會將音訊資料解壓縮，並以一或兩個音訊串流的形式從音訊輸出圖釘傳遞。 原始的 DV 框架是從影片輸出圖釘以影片框架的形式傳遞。 影片畫面上的媒體類型已從 [媒體媒體類型] 變更為 [媒體類型] \_ \_ 影片，否則不會修改資料。 媒體類型會變更，以表示應忽略畫面中的音訊資料。 DV 分隔器不會在其輸出範例上設定媒體時間;如果您要撰寫需要媒體時間的下游篩選器，則可以從框架計數衍生時間。

一次只有一個輸出圖釘會公開 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面。

DV 分隔器篩選器可以接受音訊資料流程中的動態格式變更。 但是，如果 [AVI Mux](avi-mux-filter.md) 篩選器是下游的，則會拒絕格式變更。 如果發生這種情況，DV 分隔器會停止產生音訊串流。 這項限制只會影響類型2的檔案捕捉。 針對類型1檔案，交錯資料流程不會在第一個位置進行分割。 若為預覽版本，則不會下游有 AVI Mux 篩選。

如果 DV 來源是即時攝影機，則通常不會有變更音訊格式的原因。 但是，如果您從包含數個異類來源的 VTR 磁帶進行傳輸，格式可能會變更。

除了音訊和影片資料之外，每個 DV 框架還包含中繼資料。 此中繼資料可以從框架變更為框架。 應用程式可以藉由檢查輸入範例或影片輸出範例來剖析中繼資料。 但是，DirectShow 並不提供任何直接支援來剖析 DV 中繼資料。 如需詳細資訊，請參閱 IEC 61834-4。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 




