---
title: 使用計時層級
description: 使用計時層級
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- 視覺效果，計時事件
- 自訂視覺效果，計時事件
- 視覺效果、頻率陣列
- 自訂視覺效果、頻率陣列
- 視覺效果、波形陣列
- 自訂視覺效果、波形陣列
- 視覺效果，狀態變數
- 自訂視覺效果，狀態變數
- 視覺效果、時間戳記變數
- 自訂視覺效果，timeStamp 變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021473"
---
# <a name="using-timed-levels"></a>使用計時層級

**TimedLevel** 結構是由 2 2 維度陣列、狀態值和時間戳記值所組成。

## <a name="frequency-array"></a>頻率陣列

頻率陣列是二維陣列。 每個陣列的第一個維度會對應到身歷聲音訊頻道 (左或右) ，而第二個維度對應到快照集的頻率層級 (（以位元組為單位) ），其中的音訊頻譜會分成1024個區域。

您可以透過下列方式取得從 Windows Media Player 提供的頻率陣列資料：


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



Snapshot 的值適用于左邊的通道，且包含 frequency 頻譜的最小部分值。 例如，如果快照集有很大的值，則會指出頻率頻譜的最低1024th 部分在頻率方面很豐富。 值為零表示左方頻道的範圍內沒有低頻率值。 如果您有單聲道信號，則只有第一個維度具有有效的值。

如果信號為非身歷聲，則第二個數組將包含 mono 信號的複本。 也就是說，frequency \[ 0 \] \[ *n* \] 和 frequency \[ 1 \] \[ *n* \] 會包含相同的資料，其中 *n* 是特定資料格的索引。

## <a name="waveform-array"></a>波形陣列

波形陣列也是二維陣列。 陣列的第一個維度會對應至通道 (左或右) ，而第二個維度對應到快照集的電源等級 (（以位元組為單位）) ，其中音訊電源會分成1024個連續的時間區段。

您可以利用下列方式，從 Windows Media Player 取得波形陣列資料：


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



Snapshot 的值適用于左邊通道，並且包含電源值的量化快照的第一個值。 建立快照集時，它是由1024的微小遞增量值所組成。 陣列的最小值是由音訊電源的第一次遞增量值所產生。 請注意，乘冪的值是從-128 到 + 127，但陣列中的值範圍從0到255。 如果您有單聲道 wave，則只有第一個維度會有有效的值。

如果信號為非身歷聲，則第二個數組將包含 mono 信號的複本。 也就是說，波形 \[ 0 \] \[ *n* \] 和波形 \[ 1 \] \[ *n* \] 將包含相同的資料，其中 *n* 是特定資料格的索引。

## <a name="state"></a>狀態

狀態變數會反映 Windows Media Player 的音訊播放狀態。 PlayerState 列舉值為


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



您可以使用此變數來採取不同的動作，視音訊播放狀態而定。 例如，您可以在播放音訊時播放一種視覺效果，並在停止時播放另一種視覺效果。

## <a name="time-stamp"></a>時間戳記

時間戳記變數會反映拍攝快照集的目前時間。 這可以用來測量拍攝快照集的頻率。

您可以使用此變數來時間動畫。 如果快照集太頻繁，您可以正常地降低影像，使其以您選擇的方式顯示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行轉譯**](implementing-render.md)
</dt> </dl>

 

 




