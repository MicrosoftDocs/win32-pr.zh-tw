---
description: KaraokeAudioPresentationMode 屬性會設定或抓取輔助的卡拉卡拉板頻道的向左喇叭混合。
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: KaraokeAudioPresentationMode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972513"
---
# <a name="karaokeaudiopresentationmode-property"></a>KaraokeAudioPresentationMode 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`KaraokeAudioPresentationMode`屬性會設定或抓取輔助的卡拉卡拉板頻道的向左喇叭混合。

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>傳回值

傳回整數值，其中包含一組位旗標，指出輔助的卡拉標頻道如何 downmixed 至左右喇叭。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，預設值為零。

音訊頻道是以零為基礎，因此通道0和1通常代表右邊和左邊的喇叭頻道，而頻道2到4則是三個輔助的卡拉卡拉。 當 MSWebDVD 物件進入卡拉 ok 模式時，它會自動靜音通道2和更新版本。 使用位 **or** 運算設定適當的位，以便將輔助通道傳送給左邊的喇叭、右邊的喇叭、兩位喇叭都 () 上的兩個位，或是沒有任何喇叭 () 的兩個位。 只要 DVD 導覽器進入 [卡拉 ok] 模式，這些位都預設為關閉。 下表提供了位的值及其對應的動作。



| 值  | 描述                            |
|--------|----------------------------------------|
| 0x0004 | Downmix Channel 2 至左方喇叭  |
| 0x0008 | Downmix Channel 3 至左方喇叭  |
| 0x0010 | Downmix Channel 4 至左方喇叭  |
| 0x0400 | Downmix Channel 2 到右邊的喇叭 |
| 0x0800 | Downmix Channel 3 到右邊的喇叭 |
| 0x1000 | Downmix Channel 4 到右邊的喇叭 |



 

 

 



