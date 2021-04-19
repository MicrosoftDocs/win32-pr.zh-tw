---
description: Error 物件的唯讀 DatabaseKeys 屬性會傳回字串集合，其中包含造成錯誤之資料庫資料列的主鍵。 集合中的每個專案都有一個金鑰。
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: '錯誤。 DatabaseKeys 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989247"
---
# <a name="errordatabasekeys-property"></a>錯誤。 DatabaseKeys 屬性

[**Error**](error-object.md)物件的唯讀 **DatabaseKeys** 屬性會傳回字串集合，其中包含造成錯誤之資料庫資料列的主鍵。 集合中的每個專案都有一個金鑰。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

當不再需要時，用戶端會負責釋放字串集合。

如果值不適用於錯誤的類型，則集合是空的。 您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。

### <a name="c"></a>C++

請參閱 [**get \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

