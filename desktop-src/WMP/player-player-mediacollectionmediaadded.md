---
title: MediaCollectionMediaAdded 事件
description: 當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。 |MediaCollectionMediaAdded 事件
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- MediaCollectionMediaAdded 事件 Windows Media Player
- MediaCollectionMediaAdded 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionMediaAdded 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000471"
---
# <a name="playermediacollectionmediaadded-event"></a>MediaCollectionMediaAdded 事件

當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。

## <a name="syntax"></a>語法


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdispMedia* 
</dt> <dd>

已新增的 **媒體** 物件。

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

 

 





