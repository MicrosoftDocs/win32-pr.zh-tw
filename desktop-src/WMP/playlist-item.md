---
title: 播放清單. item 方法
description: Item 方法會抓取位於指定之索引處的媒體專案。
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player、item 方法
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995476"
---
# <a name="playlistitem-method"></a>播放清單. item 方法

**Item** 方法會抓取位於指定之索引處的媒體專案。

## <a name="syntax"></a>語法


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**Number** (**Long**) ，其中包含要抓取之專案的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **媒體** 物件。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *播放清單*。用來根據使用者選取專案從目前播放清單取出媒體專案的 **專案** 。 使用名稱 "weblist" 建立的 HTML SELECT 元素，並填入目前播放清單中的標題。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**播放清單。 insertItem**](playlist-insertitem.md)
</dt> <dt>

[**播放清單。 removeItem**](playlist-removeitem.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





