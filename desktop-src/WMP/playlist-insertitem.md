---
title: InsertItem 方法
description: InsertItem 方法會將媒體專案插入播放清單中指定的位置。
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- insertItem 方法 Windows Media Player
- insertItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，insertItem 方法
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995698"
---
# <a name="playlistinsertitem-method"></a>InsertItem 方法

**InsertItem** 方法會將媒體專案插入播放清單中指定的位置。

## <a name="syntax"></a>語法


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**Number** (**Long**) ，其中包含要在其中加入專案的索引。

</dd> <dt>

*專案* \[在\]
</dt> <dd>

要插入的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

插入專案之後的所有專案都會以1遞增其索引編號。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**播放清單。專案**](playlist-item.md)
</dt> <dt>

[**播放清單。 removeItem**](playlist-removeitem.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





