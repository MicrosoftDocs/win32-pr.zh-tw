---
title: MediaCollection. getByAuthor 方法
description: GetByAuthor 方法會依指定的作者來抓取媒體專案的播放清單。
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- getByAuthor 方法 Windows Media Player
- getByAuthor 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAuthor 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985956"
---
# <a name="mediacollectiongetbyauthor-method"></a>MediaCollection. getByAuthor 方法

**GetByAuthor** 方法會依指定的作者來抓取媒體專案的播放清單。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*作者* \[在\]
</dt> <dd>

包含作者名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *MediaCollection*。**getByAuthor** 以取得媒體專案的播放清單。 播放清單包含的專案符合使用者在名為 GetAuthor 的 HTML 文字輸入元素中所指定的作者。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
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

 

 





