---
description: DV Muxer 濾波器
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV Muxer 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688376"
---
# <a name="dv-muxer-filter"></a>DV Muxer 濾波器

此篩選器結合數位視訊 (DV) 編碼的影片串流與一或兩個音訊串流，以產生交錯的 DV 串流。 若要將資料流程寫入 AVI 檔案，請將此篩選連接到 [Avi mux](avi-mux-filter.md) 篩選器，並將 *AVI mux* 連接至檔案 [寫入](file-writer-filter.md) 器篩選器。 如需詳細資訊，請參閱 [DirectShow 中的數位視訊](digital-video-in-directshow.md)。



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| 輸入 Pin 媒體類型                    | **影片**：媒體媒體 \_ 、MEDIASUBTYPE \_ Dvsd、format \_ VideoInfo **Audio**：媒體媒體 \_ 、MEDIASUBTYPE \_ PCM、format \_ WaveFormatEx |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| 輸出 Pin 媒體類型                   | 媒體 \_ 中交錯、MEDIASUBTYPE \_ DVSD、格式 \_ DvInfo                                                                             |
| 輸出 Pin 介面                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| 篩選 CLSID                             | CLSID \_ DVMux                                                                                                                           |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                       |
| 可執行檔                               | qdv.dll                                                                                                                                |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                                                        |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                          |



 

## <a name="remarks"></a>備註

DV Muxer 可以建立兩個音訊輸入圖釘。 它支援下表所示的音訊格式。



音訊 Pin 1

音訊 Pin 2

輸出格式

取樣率 (kHz) 

位/範例

通道

採樣速率

位/範例

通道

32

16

Mono

無關

SD 2 通道

32

16

立體聲

無關

SD 4 通道

44.1 或48

16

身歷聲或 Mono

無關

SD 2 通道

無關

32

16

身歷聲或 Mono

不允許

無關

44.1 或48

16

Mono

不允許

無關

44.1 或48

16

立體聲

SD 2 通道

32

16

Mono

32

16

Mono

SD 2 通道

32

16

身歷聲或 Mono\*

32

16

身歷聲或 Mono\*

SD 4 通道

44.1

16

Mono

44.1

16

Mono

SD 2 通道

48

16

Mono

48

16

Mono

SD 2 通道

\* 如果至少有一個輸入 pin 是身歷聲。



 

基於此表格的目的，音訊 pin 1 會定義為連接到音訊來源的第一個輸入連接，而音訊 pin 2 則定義為連接到音訊來源的第二個輸入 pin。 連接音訊 pin 之後，除非兩個音訊針腳都已中斷連線，否則此編號配置仍會保持有效。 例如，如果您連接兩個音訊針腳，然後中斷音訊 pin 1 的連線，則剩餘的 pin 仍會被視為 pin 2。

提供給 pin 1 的音訊會記錄至 DV 框架的第一個音訊區塊 (CH1) ，而提供給針腳2的音訊會記錄到第二個音訊區塊 (CH2) 。 例外狀況：如果篩選器的 44.1 kHz 或 48 kHz 有單一的身歷聲輸入，則左側音訊頻道會記錄到第一個音訊區塊，而右邊的音訊頻道會記錄到第二個音訊區塊。

針對 SD 4-通道輸出：如果輸入為身歷聲，則會將左軌記錄到 CHa 或 CHc，並將正確的曲目記錄到 CHb 或 CHd。 如果輸入為 mono，則會將音訊記錄為 CHa 或 CHc，而 CHb 和 CHd 為無訊息。

藉由連接並中斷連接音訊 pin 1，就可以達到不允許的格式。 在此情況下，篩選的 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法會傳回 VFW \_ E \_ 未 \_ 連接。 這項限制可防止第一個音訊區塊沒有音訊，但第二個音訊區塊有音訊的情況。 第二個區塊只有在第一個區塊也有音訊時，才應該有音訊。

DV Muxer 不允許具有不同取樣率的音訊輸入。 不過，圖形建立方法（例如 [**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ）通常會新增「高階 [包裝](acm-wrapper-filter.md) 函式」篩選器，這會將第二個音訊串流轉換成符合第一個資料流程的取樣率。

如果音訊輸入是 48 kHz 或 32 kHz，音訊輸出會被鎖定。  (不能鎖定 44.1-kHz 音訊。 ) 

如果沒有連線音訊 pin，輸出會包含傳入 DV 框架的音訊資料。 這可能是靜音或有效的音訊資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 



