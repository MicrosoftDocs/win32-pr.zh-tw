---
title: MediaCollection. setDeleted 方法
description: SetDeleted 方法會將指定的媒體專案移到 [刪除的專案] 資料夾。 |MediaCollection. setDeleted 方法
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- setDeleted 方法 Windows Media Player
- setDeleted 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，setDeleted 方法
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997688"
---
# <a name="mediacollectionsetdeleted-method"></a>MediaCollection. setDeleted 方法

**SetDeleted** 方法會將指定的媒體專案移到 [刪除的專案] 資料夾。

## <a name="syntax"></a>語法


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*專案* \[在\]
</dt> <dd>

正在移動的 **媒體** 物件。

</dd> <dt>

*true* \[在\]
</dt> <dd>

一律指定此值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法不會將檔案從使用者的電腦移除。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *MediaCollection*。**setDeleted** ，將儲存在名為 mediaObject 的變數中的特定媒體專案移至 [已刪除的專案] 資料夾。 *MediaCollection*。**isDeleted** 方法會先測試是否已刪除專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

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

[**MediaCollection. isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





