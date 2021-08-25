---
title: Cdrom 播放清單
description: 播放清單物件會抓取播放清單物件，此物件代表 cd 光碟機中目前的曲目，或 DVD 的根層級標題專案。
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom Windows Media Player 的播放清單
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29419b68c50718165e49c0fbe9e75487e9154c19243453981ab352f03e8209a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864178"
---
# <a name="cdromplaylist"></a>Cdrom 播放清單

**播放** 清單物件會抓取 **播放清單** 物件，此物件代表 cd 光碟機中目前的曲目，或 DVD 的根層級標題專案。

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **播放清單** 物件。

## <a name="remarks"></a>備註

一般而言，Dvd 會組織成標題。 每個標題都包含一或多個章節。 每個 DVD 的撰寫方式都不同，因此使用標題和章節的方式是由內容作者決定。

若是 DVD，這個方法會抓取播放清單，其中包含代表 DVD 媒體之 **媒體** 物件的第一個專案。 如果播放專案是在插入新 DVD 之後第一次播放，播放該專案會導致 DVD 播放，或在 DVD 與最後一張 DVD 相同時繼續播放。 在播放期間將這個專案設定為目前的專案，會從一開始就播放 DVD。

播放清單中)  (**媒體** 物件的其他專案，則是以嵌套播放清單表示的 DVD 標題。 當您指定 *控制項* 時。**currentItem** 為等於其中一個嵌套播放清單專案，Windows Media Player 會自動將嵌套播放清單設定為 *播放* 程式。開始進行章節的 **currentPlaylist** 之後。 然後，您可以使用 **currentPlaylist** 物件屬性、方法和事件來處理 DVD 章節，也就是播放清單專案。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個屬性。

## <a name="examples"></a>範例

下列範例會使用 *光碟*。用來填滿 HTML 文字元素的 **播放清單** ，名稱為 myText，而音訊 CD 的標題則是目前位於第一個 CD 光碟機的標題。 使用 *CdromCollection*。用來判斷可用 CD 磁片磁碟機數目的 **計數** 。 使用 ID = "Player" 建立 **player** 物件。


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 版本<br/>                  | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Cdrom 物件**](cdrom-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





