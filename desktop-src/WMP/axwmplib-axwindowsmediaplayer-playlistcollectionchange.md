---
title: AxWindowsMediaPlayer 物件的 PlaylistCollectionChange 事件
description: 當播放清單集合中的某個專案發生變更時，就會發生 PlaylistCollectionChange 事件。 |AxWindowsMediaPlayer 物件的 PlaylistCollectionChange 事件
ms.assetid: 868ee1c6-b740-4614-90ac-961c59091f0f
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistCollectionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7dd88b558bb13b8835be1a8f840df8f8316706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980197"
---
# <a name="playlistcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 PlaylistCollectionChange 事件

當播放清單集合中的某個專案發生變更時，就會發生 PlaylistCollectionChange 事件。

``` syntax
[C#]
private void player_PlaylistCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_PlaylistCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.PlaylistCollectionChange
```

## <a name="event-data"></a>事件資料

此事件不包含資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





