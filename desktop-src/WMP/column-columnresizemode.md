---
title: ColumnResizeMode
description: ColumnResizeMode 屬性會指定或抓取此資料行的調整大小模式。
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- ColumnResizeMode Windows Media Player 的資料行
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59046aa76c01a1439e5db8f0fb6850e7df74d874cba555d1f9c3829f09d9598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763998"
---
# <a name="columncolumnresizemode"></a>ColumnResizeMode

**ColumnResizeMode** 屬性會指定或抓取此資料行的調整大小模式。

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>可能的值

這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。



| 值          | 描述                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | 預設值。 資料行調整大小以容納資料行和標頭中的所有資料。                         |
| AutosizeData   | 資料行調整大小以容納資料行中的所有資料。                                                 |
| 固定式          | 此資料行是固定的大小。                                                                                    |
| 延伸      | 當所有其他資料行調整大小之後，資料行調整大小以使用 **播放清單** 控制項中的剩餘空間。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COLUMN 元素**](column-element.md)
</dt> </dl>

 

 





