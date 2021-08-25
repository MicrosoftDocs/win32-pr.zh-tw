---
title: BeginNextGroup 方法
description: BeginNextGroup 方法會開始新的條件群組。 |BeginNextGroup 方法
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- beginNextGroup 方法 Windows Media Player
- beginNextGroup 方法 Windows Media Player，查詢類別
- 查詢類別 Windows Media Player，beginNextGroup 方法
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d12f8e37c32b83afb3e518deda09643033c7f396d8c52a2898893a01dc930d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861848"
---
# <a name="querybeginnextgroup-method"></a>BeginNextGroup 方法

**BeginNextGroup** 方法會開始新的條件群組。

## <a name="syntax"></a>語法


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

開始新的條件群組即表示您已完成目前的條件群組。 新的條件群組一律會使用或邏輯串連至先前的條件群組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Query 物件**](query-object.md)
</dt> <dt>

[**AddCondition**](query-addcondition.md)
</dt> </dl>

 

 





