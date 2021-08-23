---
title: MediaCollection 新增方法
description: Add 方法會將新的媒體專案或播放清單新增至程式庫。 |MediaCollection 新增方法
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- 新增方法 Windows Media Player
- 新增方法 Windows Media Player、MediaCollection 類別
- MediaCollection 類別 Windows Media Player，add 方法
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b26d21f67496f345324efdca93dbf85e59947f1616e0c5620faead2807a6ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647908"
---
# <a name="mediacollectionadd-method"></a>MediaCollection 新增方法

**Add** 方法會將新的媒體專案或播放清單新增至程式庫。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

包含路徑的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **媒體** 物件。

## <a name="remarks"></a>備註

這個方法會將現有的媒體專案或播放清單載入至程式庫，並提供檔案的路徑。 這個方法不會移動或變更檔案。 如果指定了不正確本機路徑，這個方法將會失敗，但在將數位媒體檔案新增至程式庫之前，不會檢查數位媒體檔案的有效性。

這個方法會接受靜態和自動播放清單檔案。 *PlaylistCollection*。**importPlaylist** 方法也可以用來將靜態播放清單新增至程式庫。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 Microsoft JScript 範例將三個媒體物件新增至 Windows Media Player 媒體集合。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection。移除**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





