---
description: 播放卡拉卡拉的音訊串流
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: 播放卡拉卡拉的音訊串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10912761034feb9ed82c85625324cd3091514b2c492c66b4e49af711d7d2152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213298"
---
# <a name="playing-karaoke-audio-streams"></a>播放卡拉卡拉的音訊串流

DVD 導覽器可以播放具有卡拉卡拉 DVD-Video 光碟的視頻串流，但卡拉 ok 播放也需要支援多重通道卡拉器混合的解碼器。 具體而言，解碼器必須支援 [**DVD 卡拉 Ok 屬性集**](dvd-karaoke-property-set.md) (AM \_ 屬性 \_ DVDKARAOKE) 。

卡拉 ok 光碟是一種 DVD-Video 光碟，具有相同的導覽結構。 歌曲通常會格式化為標題，且標題可根據執行者、音樂樣式或其他準則分組為標題組。 「卡拉」和「其他」 DVD-Videos 類型的主要差異在於音訊串流。 卡拉卡拉的所有磁片都包含多頻道音訊，通常是杜比 AC-3。 頻道0和1永遠包含背景的對音樂，而頻道2到5則各自都包含了節目表人聲、指南 melodies 和音效效果的任何組合。 卡拉卡拉（卡拉）應用程式可以控制每個輔助通道的音量和目的地喇叭。

當 DVD 導覽器偵測到光碟上的卡拉 ok 內容，並進入 [卡拉 ok] 模式時，它會通知該解碼器，然後將前三個通道的上方靜音 (輔助通道) ，直到應用程式明確開啟任何或所有通道為止。 「卡拉卡拉」應用程式的基本工作是：

1.  使用 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 方法來判斷輔助通道的數目及其內容。
2.  提供可顯示通道內容的使用者介面，並可讓使用者隨時使用 [**IDvdControl2：： SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode)來開啟或關閉任何輔助通道。

這些步驟會在 **GetAudioAttributes** 方法的 DVDCore .cpp 中的 DVD 範例應用程式中說明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 



