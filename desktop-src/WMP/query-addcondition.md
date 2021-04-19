---
title: AddCondition 方法
description: AddCondition 方法會使用和邏輯，將條件加入至查詢物件。
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- addCondition 方法 Windows Media Player
- addCondition 方法 Windows Media Player，查詢類別
- 查詢類別 Windows Media Player，addCondition 方法
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994212"
---
# <a name="queryaddcondition-method"></a>AddCondition 方法

**AddCondition** 方法會使用和邏輯，將條件加入至 **查詢** 物件。

## <a name="syntax"></a>語法


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。

</dd> <dt>

*運算子* \[在\]
</dt> <dd>

包含運算子的 **字串**。 如需支援的值，請參閱備註。

</dd> <dt>

*值* \[在\]
</dt> <dd>

包含屬性值的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

使用 **查詢** 的複合查詢不區分大小寫。

您可以在 [[字母屬性參考](alphabetical-attribute-reference.md)] 區段中找到 *屬性* 參數值的清單。

**查詢** 物件中包含的條件會組織成條件群組。 條件群組內的多個條件一律會使用和邏輯串連。 條件群組一律會使用或邏輯互相串連。 若要啟動新的條件群組，請呼叫 **beginNextGroup**。

下表列出 *運算子* 支援的值。



| 運算子            | 適用於     |
|---------------------|----------------|
| BeginsWith          | 字串        |
| 包含            | 字串        |
| 等於              | 所有類型      |
| GreaterThan         | 數位、日期 |
| GreaterThanOrEquals | 數位、日期 |
| LessThan            | 數位、日期 |
| LessThanOrEquals    | 數位、日期 |
| NotBeginsWith       | 字串        |
| NotContains         | 字串        |
| NotEquals           | 所有類型      |



 

## <a name="examples"></a>範例

下列 JScript 範例會使用 **addCondition** 和 **beginNextGroup** 來執行範例查詢。


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



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

[**BeginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





