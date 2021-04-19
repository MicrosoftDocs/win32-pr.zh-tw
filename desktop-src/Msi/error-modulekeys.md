---
description: Error 物件的唯讀 ModuleKeys 屬性會傳回字串集合的指標，其中包含模組中資料列的主鍵，而該資料列會造成錯誤，也就是集合中每個專案的一個索引鍵。
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: '錯誤。 ModuleKeys 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999164"
---
# <a name="errormodulekeys-property"></a>錯誤。 ModuleKeys 屬性

[**Error**](error-object.md)物件的唯讀 **ModuleKeys** 屬性會傳回字串集合的指標，其中包含模組中資料列的主鍵，而該資料列會造成錯誤，也就是集合中每個專案的一個索引鍵。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

當不再需要時，用戶端會負責釋放字串集合。

如果值不適用於錯誤的類型，則集合是空的。 您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。

### <a name="c"></a>C++

請參閱 [**get \_ ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

