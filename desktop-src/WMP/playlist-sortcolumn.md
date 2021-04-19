---
title: 播放清單。 sortColumn
description: SortColumn 方法會排序指定之資料行中的資料。
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- 播放清單. sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979620"
---
# <a name="playlistsortcolumn"></a>播放清單。 sortColumn

**SortColumn** 方法會排序指定之資料行中的資料。

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*列*
</dt> <dd>

**Number** (**Long**) ，表示要排序的資料行索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會將指定的資料行排序，其方式與 **播放清單** 元素中的資料行標頭按鈕相同。 如果資料行尚未排序，則會依英數位元順序排序。 如果已排序，則會反轉其順序。

若要讓此方法運作， **allowColumnSorting** 屬性必須設定為 true。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





