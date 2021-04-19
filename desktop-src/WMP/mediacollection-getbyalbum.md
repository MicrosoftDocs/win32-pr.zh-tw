---
title: MediaCollection. getByAlbum 方法
description: GetByAlbum 方法會從指定的專輯抓取包含媒體專案的播放清單。
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- getByAlbum 方法 Windows Media Player
- getByAlbum 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAlbum 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000422"
---
# <a name="mediacollectiongetbyalbum-method"></a>MediaCollection. getByAlbum 方法

**GetByAlbum** 方法會從指定的專輯抓取包含媒體專案的播放清單。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*專輯* \[在\]
</dt> <dd>

包含專輯名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 *MediaCollection*。**getByAlbum** 以取得媒體專案的播放清單。 播放清單中包含使用者在名為 GetAlbum 的 HTML 文字輸入元素中所指定之專輯的專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
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

 

 





