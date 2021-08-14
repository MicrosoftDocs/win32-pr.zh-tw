---
title: AppendItem 方法
description: AppendItem 方法會將媒體專案新增至播放清單的結尾。
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- appendItem 方法 Windows Media Player
- appendItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，appendItem 方法
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79361ebcf2ea23b754a7bc86cb6fa4a0af465e4e6619ed692c027bc28eb7aa87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747117"
---
# <a name="playlistappenditem-method"></a>AppendItem 方法

**AppendItem** 方法會將媒體專案新增至播放清單的結尾。

## <a name="syntax"></a>語法


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*專案* \[在\]
</dt> <dd>

要加入的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *播放清單*。**appendItem** 將目前的媒體專案新增至名為 "ThreeList" 的播放清單。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





