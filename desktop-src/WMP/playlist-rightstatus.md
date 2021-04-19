---
title: 播放清單。 rightStatus
description: RightStatus 屬性會指定或抓取播放清單元素右側和底部顯示的狀態文字。
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- 播放清單. rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989760"
---
# <a name="playlistrightstatus"></a>播放清單。 rightStatus

**RightStatus** 屬性會指定或抓取 **播放清單** 元素右側和底部顯示的狀態文字。

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

這個屬性可以將任何文字與特定關鍵字合併，以顯示所需的資訊，例如播放清單的總持續時間。 關鍵字會以百分比符號括住 (% ) ，以保持與一般文字不同。

您可以使用下列關鍵字。



| 關鍵字               | 描述                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | 播放清單中的專案數。                                                                                                                                                                             |
| {1}size{2}                  | 播放清單的總大小。                                                                                                                                                                                  |
| duration              | 播放清單的總持續時間。                                                                                                                                                                              |
| *Xxx*                 | 在具有 *XXX* 的播放清單上執行 **getItemInfo** ，這是要接收的專案。                                                                                                                                 |
| Suitablesize          | 播放清單中所選取專案的總大小。                                                                                                                                                          |
| Selectedcount 個         | 播放清單中選取的專案總數。                                                                                                                                                            |
| SelectedDuration      | 播放清單中所選取專案的總持續時間。                                                                                                                                                      |
| CheckedCount          | 播放清單中的已檢查曲目總數。                                                                                                                                                              |
| CheckedDuration       | 播放清單中已檢查曲目的總持續時間。                                                                                                                                                        |
| CheckedSize           | 播放清單中已檢查曲目的總大小。                                                                                                                                                            |
| DurationString        | 根據是否知道總計值，顯示將持續時間描述為「總時間」或「估計時間」的文字。 此文字後面接著 "% duration%"。                                       |
| CheckedDurationString | 根據是否知道總計值，顯示描述播放清單中所有已核取專案之持續時間的文字（以「總時間」或「估計時間」為依據）。 此文字後面接著 "% duration%"。 |



 

若播放清單中包含七分鐘的總持續時間，則其值為 "Total Time：% duration%"，將會顯示 "Total Time： 07:00"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> </dl>

 

 





