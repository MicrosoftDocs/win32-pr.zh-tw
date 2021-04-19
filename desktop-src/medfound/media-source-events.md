---
description: 媒體來源事件
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: 媒體來源事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106976405"
---
# <a name="media-source-events"></a>媒體來源事件

本主題列出媒體來源和媒體資料流程所傳送的事件。 媒體來源也可以傳送此處未列出的自訂事件。

## <a name="media-source-events"></a>媒體來源事件



| 事件                                                                      | 描述                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation 事件](meendofpresentation.md)                       | 簡報結束。 簡報中的所有資料流程都已達到資料流程的結尾。      |
| [MENewStream 事件](menewstream.md)                                       | 已建立新的資料流程。 事件包含資料流程的指標。                            |
| [MESourceCharacteristicsChanged 事件](mesourcecharacteristicschanged.md) | 來源的特性已變更。 (選擇性。)                                      |
| [MESourceMetadataChanged 事件](mesourcemetadatachanged.md)               | 來源的中繼資料已變更。 (選擇性。)                                                   |
| [MESourcePaused 事件](mesourcepaused.md)                                 | 來源已暫停。 並非所有來源都支援暫停。                                          |
| [MESourceRateChanged 事件](mesourceratechanged.md)                       | 來源的播放率已變更。  (選用;適用于來源是否支援速率控制。 )  |
| [MESourceRateChangeRequested 事件](mesourceratechangerequested.md)       | 來源正在要求新的播放速率。 (選擇性。)                                        |
| [MESourceSeeked 事件](mesourceseeked.md)                                 | 來源已 seeked。 並非所有來源都支援搜尋。                                          |
| [MESourceStarted 事件](mesourcestarted.md)                               | 來源已啟動。                                                                          |
| [MESourceStopped 事件](mesourcestopped.md)                               | 來源已停止。                                                                          |
| [MEUpdatedStream 事件](meupdatedstream.md)                               | 現有的資料流程已 seeked 或重新開機。 事件包含資料流程的指標。         |



 

## <a name="media-stream-events"></a>媒體串流事件



| 事件                                                    | 描述                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfStream 事件](meendofstream.md)                 | 資料流程已結束。                                                                                                              |
| [MEError 事件](meerror.md)                             | 串流期間發生錯誤。 如果錯誤與此處所列的任何其他事件無關，請使用此事件。 |
| [MEMediaSample 事件](memediasample.md)                 | 資料流程已產生新的範例。                                                                                         |
| [MEStreamFormatChanged 事件](mestreamformatchanged.md) | 媒體類型已變更。 (選擇性。)                                                                                        |
| [MEStreamPaused 事件](mestreampaused.md)               | 資料流程已暫停。                                                                                                         |
| [MEStreamSeeked 事件](mestreamseeked.md)               | 資料流程已 seeked。                                                                                                         |
| [MEStreamStarted 事件](mestreamstarted.md)             | 資料流程已啟動。                                                                                                        |
| [MEStreamStopped 事件](mestreamstopped.md)             | 資料流程已停止。                                                                                                        |
| [MEStreamThinMode 事件](mestreamthinmode.md)           | Thinning 模式已啟動或停止。 (選擇性。)                                                                              |
| [MEStreamTick 事件](mestreamtick.md)                   | 資料流程中有一個間距。 (選擇性。)                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源](media-sources.md)
</dt> </dl>

 

 



