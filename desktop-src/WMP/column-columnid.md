---
title: ColumnID
description: ColumnID 屬性會指定或抓取播放清單控制項中的資料行識別碼。
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- ColumnID Windows Media Player 的資料行
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993433"
---
# <a name="columncolumnid"></a>ColumnID

**ColumnID** 屬性會指定或抓取 **播放清單** 控制項中的資料行識別碼。

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

**ColumnID** 值與 **媒體** 物件上的 **getItemInfo** 方法所使用的值相同。 您可以使用 *媒體* 取得清單。**attributeCount** 屬性，用來判斷指定之 **媒體** 物件的可用屬性數目。 然後，您可以將索引號碼與 *媒體* 搭配使用。**getAttributeName** 方法，可決定屬性的名稱，然後再傳遞給 *媒體*。**getItemInfo**。 **ColumnID** 屬性只能設定為這些值，但可能不會由 *媒體* 傳回的某些值除外。**getAttributeName**。 下面會列出這些值。



| 值     | 描述                                                                        |
|-----------|------------------------------------------------------------------------------------|
| NAME      | 顯示 **媒體** 物件的名稱。                                         |
| duration  | 顯示 **媒體** 物件的持續時間。                                     |
| sourceURL | 顯示 **媒體** 物件的 URL。                                          |
| status    | 顯示覆制檔案的狀態。                                              |
| {1}size{2}      | 顯示 **媒體** 物件所代表之檔案的大小。                |
| 擴充功能 | 顯示 **媒體** 物件所代表之檔案的副檔名。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COLUMN 元素**](column-element.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**AttributeCount**](media-attributecount.md)
</dt> <dt>

[**GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**GetItemInfo**](media-getiteminfo.md)
</dt> </dl>

 

 





