---
title: MediaCollection 方法
description: Remove 方法會從媒體集合中移除專案。
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- 移除方法 Windows Media Player
- remove 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，remove 方法
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574605"
---
# <a name="mediacollectionremove-method"></a>MediaCollection 方法

**Remove** 方法會從媒體集合中移除專案。

## <a name="syntax"></a>語法


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*專案* \[在\]
</dt> <dd>

要移除的 **媒體** 物件。

</dd> <dt>

*刪除* \[在\]
</dt> <dd>

指出是否要移除專案的 **布林值**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會從程式庫中刪除專案。 這個方法不會刪除使用者電腦中的檔案。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例在提示使用者之後，會使用 *MediaCollection* 永久刪除媒體集合中的第一個媒體專案。**移除**。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

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

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection 新增**](mediacollection-add.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





