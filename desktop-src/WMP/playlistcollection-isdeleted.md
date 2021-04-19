---
title: PlaylistCollection. isDeleted 方法
description: IsDeleted 方法會抓取值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- isDeleted 方法 Windows Media Player
- isDeleted 方法 Windows Media Player，PlaylistCollection 類別
- PlaylistCollection 類別 Windows Media Player，isDeleted 方法
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990266"
---
# <a name="playlistcollectionisdeleted-method"></a>PlaylistCollection. isDeleted 方法

**IsDeleted** 方法會抓取值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。

## <a name="syntax"></a>語法


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*播放清單* \[在\]
</dt> <dd>

要搜尋的 **播放清單** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

**Windows Media Player 10** 行動裝置版：此方法一律會傳回 **false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 的 Windows Media Player 7.0 版、Windows Media Player 7.1 版或 Windows Media Player。 Windows Media Player 9 系列或更新版本不支援這個方法。<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> </dl>

 

 





