---
title: PlaylistCollection. getByName 方法
description: GetByName 方法會抓取 PlaylistArray 物件，其中包含具有指定名稱的播放清單（如果有的話）。
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- getByName 方法 Windows Media Player
- getByName 方法 Windows Media Player，PlaylistCollection 類別
- PlaylistCollection 類別 Windows Media Player，getByName 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300307ff011abf8b28c645901422291ccab4cf7c66a7a3ba81121ffe1c22e573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334639"
---
# <a name="playlistcollectiongetbyname-method"></a>PlaylistCollection. getByName 方法

**GetByName** 方法會抓取 **PlaylistArray** 物件，其中包含具有指定名稱的播放清單（如果有的話）。

## <a name="syntax"></a>語法


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含要抓取之播放清單名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **PlaylistArray** 物件。

## <a name="remarks"></a>備註

使用 *PlaylistArray*。判斷播放清單是否存在的 **計數** 。 如果 **count** 為零，則不存在播放清單。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *playlistCollection*。**getByName** ，檢查名為 "ThreeList" 的播放清單的 **playlistCollection** 物件。 如果 "Threelist" 播放清單存在， **getByName** 會將 "Threelist" 設定為目前的播放清單。 使用 ID = "Player" 建立 **player** 物件。


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlaylistArray 物件**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray 計數**](playlistarray-count.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





