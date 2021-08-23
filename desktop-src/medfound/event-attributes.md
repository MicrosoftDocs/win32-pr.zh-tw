---
description: 事件屬性
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: '事件屬性 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36d64efbc4ed36569ef85514d38563fe09a01902218833b029455c48e2c6e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600508"
---
# <a name="event-attributes-microsoft-media-foundation"></a>事件屬性 (Microsoft 媒體基礎) 

下列屬性適用于事件。



| 屬性                                                                                                        | 描述                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ DO \_ THINNING**](mf-event-do-thinning-attribute.md)                                                | 當媒體來源要求新的播放速率時，會指定來源是否也要求 thinning。                |
| [**MF \_ 事件 \_ 輸出 \_ 節點**](mf-event-output-node-attribute.md)                                                | 識別資料流程接收的拓撲節點。                                                                       |
| [**MF \_ 事件 \_ 呈現 \_ 時間 \_ 位移**](mf-event-presentation-time-offset-attribute.md)                     | 呈現時間與媒體來源時間戳記之間的位移。                                              |
| [**MF \_ 事件 \_ SCRUBSAMPLE \_ 時間**](mf-event-scrubsample-time-attribute.md)                                      | 在清除時轉譯之樣本的呈現時間。                                                     |
| [**MF \_ 事件 \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)                                                 | 包含根據目前的簡報定義媒體會話功能的旗標。                  |
| [**MF \_ 事件 \_ SESSIONCAPS \_ 差異**](mf-event-sessioncaps-delta-attribute.md)                                    | 包含旗標，這些旗標會根據目前的簡報，指出媒體會話中的哪些功能已變更。 |
| [**MF \_ 事件 \_ 來源 \_ 實際 \_ 開始**](mf-event-source-actual-start-attribute.md)                               | 包含媒體來源從其目前位置重新開機的開始時間。                                       |
| [**MF \_ 事件 \_ 來源 \_ 特性**](mf-event-source-characteristics-attribute.md)                          | 指定媒體來源的目前特性。                                                            |
| [**MF \_ 事件 \_ 來源 \_ 特性 \_ 舊**](mf-event-source-characteristics-old-attribute.md)                 | 指定媒體來源的先前特性。                                                           |
| [**MF \_ 事件 \_ 來源 \_ 假 \_ 開始**](mf-event-source-fake-start-attribute.md)                                   | 指定目前區段拓撲是否為空白。                                                              |
| [**MF \_ 事件 \_ 來源 \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)                                | 指定區段拓撲的開始時間。                                                                      |
| [**\_已取消 MF 事件 \_ 來源 \_ 拓撲 \_**](mf-event-source-topology-canceled-attribute.md)                     | 指定 sequencer 來源是否取消拓撲。                                                           |
| [**MF \_ 事件 \_ 開始 \_ 簡報 \_ 時間**](mf-event-start-presentation-time-attribute.md)                       | 簡報的開始時間，以 100-納秒為單位，以呈現時鐘測量。               |
| [**MF \_ 事件 \_ \_ \_ \_ 在輸出時開始展示時間 \_**](mf-event-start-presentation-time-at-output-attribute.md) | 媒體接收器轉譯新拓撲第一個樣本的呈現時間。                      |
| [**MF \_ 事件 \_ 拓撲 \_ 狀態**](mf-event-topology-status-attribute.md)                                        | 指定播放期間拓撲的狀態。                                                                   |
| [**MF \_ 會話 \_ 大約 \_ 發生事件 \_ 發生 \_ 時間**](mf-session-approx-event-occurrence-time-attribute.md)        | 媒體會話引發事件的大約時間。                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 



