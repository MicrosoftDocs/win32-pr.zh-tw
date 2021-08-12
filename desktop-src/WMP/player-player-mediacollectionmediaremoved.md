---
title: MediaCollectionMediaRemoved 事件
description: 從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。 |MediaCollectionMediaRemoved 事件
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- MediaCollectionMediaRemoved 事件 Windows Media Player
- MediaCollectionMediaRemoved 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionMediaRemoved 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 009432040deace140dd3cf4d7d7da1246c0a38dbd9fc0da028832af137cefa83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572848"
---
# <a name="playermediacollectionmediaremoved-event"></a>MediaCollectionMediaRemoved 事件

從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。

## <a name="syntax"></a>語法


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdispMedia* 
</dt> <dd>

已移除的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

只有本機程式庫才會發生此事件。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**MediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





