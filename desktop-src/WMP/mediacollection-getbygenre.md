---
title: MediaCollection. getByGenre 方法
description: GetByGenre 方法會使用指定的類型，來抓取媒體專案的播放清單。
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- getByGenre 方法 Windows Media Player
- getByGenre 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByGenre 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997656"
---
# <a name="mediacollectiongetbygenre-method"></a>MediaCollection. getByGenre 方法

**GetByGenre** 方法會使用指定的類型，來抓取媒體專案的播放清單。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>參數

<dl> <dt>

內容類型 \[在\]
</dt> <dd>

包含類型名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *MediaCollection*。**getByGenre** 以取得媒體專案的播放清單。 播放清單中包含使用者在名為 GetGenre 的 HTML 文字輸入元素中所指定之類型的專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





