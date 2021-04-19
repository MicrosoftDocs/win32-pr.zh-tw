---
title: StringCollectionChange 事件
description: 當字串集合變更時，就會發生 StringCollectionChange 事件。 |StringCollectionChange 事件
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- StringCollectionChange 事件 Windows Media Player
- StringCollectionChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，StringCollectionChange 事件
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983971"
---
# <a name="playerstringcollectionchange-event"></a>StringCollectionChange 事件

當字串集合變更時，就會發生 StringCollectionChange 事件。

## <a name="syntax"></a>語法


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdispStringCollection* 
</dt> <dd>

**StringCollection** 已變更的物件。

</dd> <dt>

*change* 
</dt> <dd>

Number (long) 表示字串集合發生的變更類型。 包含下列其中一個值。



|        |                                    |
|--------|------------------------------------|
| Number | 描述                        |
| 0      | 不明。  (不是有效的值)        |
| 1      | 已插入專案。              |
| 2      | 字串集合已變更。     |
| 3      | 已刪除專案。               |
| 4      | 已清除字串集合。 |
| 5      | 大量更新即將開始。        |
| 6      | 大量更新已結束。           |



 

</dd> <dt>

*lCollectionIndex* 
</dt> <dd>

Number (long) ，其中包含已變更之字串收集項目的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**StringCollection 物件**](stringcollection-object.md)
</dt> </dl>

 

 





