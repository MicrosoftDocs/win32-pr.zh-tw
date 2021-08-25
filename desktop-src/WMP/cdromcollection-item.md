---
title: CdromCollection 專案方法
description: Item 方法會在指定的索引處，捕獲 Cdrom 物件。
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，CdromCollection 類別
- CdromCollection 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f700a17c29c382e96a5601bd9bbfabf3c4ede1b253d9f271b1d37ab1106ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864078"
---
# <a name="cdromcollectionitem-method"></a>CdromCollection 專案方法

**Item** 方法會在指定的索引處，捕獲 **Cdrom** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

包含索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回一個 **Cdrom** 物件。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *CdromCollection*。用來從電腦上每一張 CD 列印播放清單名稱的 **專案**。 如果磁片磁碟機實際包含 DVD 內容，則需要 Windows XP 或更新版本。 使用 ID = "播放清單" 建立的 HTML TextArea 元素。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DriveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**CdromCollection 物件**](cdromcollection-object.md)
</dt> <dt>

[**CdromCollection 計數**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





