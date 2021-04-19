---
description: Error 物件的唯讀 DatabaseTable 屬性會傳回資料庫中造成錯誤之資料表的名稱。
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: '錯誤。 DatabaseTable 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989246"
---
# <a name="errordatabasetable-property"></a>錯誤。 DatabaseTable 屬性

[**Error**](error-object.md)物件的唯讀 **DatabaseTable** 屬性會傳回資料庫中造成錯誤之資料表的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果值不適用於錯誤的類型，則集合是空的。 您可以藉由呼叫 [**error**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。

### <a name="c"></a>C++

請參閱 [**get \_ DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

