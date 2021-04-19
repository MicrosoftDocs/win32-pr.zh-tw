---
title: MediaCollection. isDeleted 方法
description: IsDeleted 方法會抓取值，指出指定的媒體專案是否位於 [刪除的專案] 資料夾中。
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- isDeleted 方法 Windows Media Player
- isDeleted 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，isDeleted 方法
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989780"
---
# <a name="mediacollectionisdeleted-method"></a>MediaCollection. isDeleted 方法

**IsDeleted** 方法會抓取值，指出指定的媒體專案是否位於 [刪除的專案] 資料夾中。

## <a name="syntax"></a>語法


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*專案* \[在\]
</dt> <dd>

可能會刪除的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：這個方法一律會傳回 **false**。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *MediaCollection*。**isDeleted** ，測試儲存在名為 mediaObject 的變數中的特定媒體專案是否在 [刪除的專案] 資料夾中。 如果媒體專案尚未刪除，則會移至 [已刪除的專案] 資料夾。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 的 Windows Media Player 7.0 版、Windows Media Player 7.1 版或 Windows Media Player。 Windows Media Player 9 系列或更新版本不支援這個方法。<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.setDeleted**](mediacollection-setdeleted.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





