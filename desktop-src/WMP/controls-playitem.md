---
title: PlayItem 方法
description: PlayItem 方法會播放指定的媒體專案。 |PlayItem 方法
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- playItem 方法 Windows Media Player
- playItem 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，playItem 方法
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000943"
---
# <a name="controlsplayitem-method"></a>PlayItem 方法

**PlayItem** 方法會播放指定的媒體專案。

## <a name="syntax"></a>語法


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*theMediaItem* \[在\]
</dt> <dd>

要播放的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

無論 *設定* 的值為何，都會自動載入並播放媒體專案。**autoStart** 屬性。 若要載入專案而不自動播放，請 *設定 [設定]*。**自動啟動** 至 false，並將值指派給 *Player*。**URL**，之後可以呼叫 **播放** 來開始播放專案。

注意

**playItem** 僅適用于 *currentPlaylist* 中的專案。 不支援使用已儲存媒體專案的參考來呼叫 **playItem** 。

## <a name="examples"></a>範例

下列 JScript 範例會使用 **playItem** 來播放目前播放清單中的媒體專案。 您可以根據播放清單中的位置，選擇要播放的專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**播放清單。專案**](playlist-item.md)
</dt> </dl>

 

 





