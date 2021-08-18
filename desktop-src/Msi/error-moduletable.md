---
description: 唯讀 ModuleTable 屬性會傳回模組中造成錯誤之資料表的名稱。
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: '錯誤。 ModuleTable 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 47cd9bab5c12230a048da04e60169e1ad21195df2304642f6b656983539f3b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947070"
---
# <a name="errormoduletable-property"></a>錯誤。 ModuleTable 屬性

唯讀 **ModuleTable** 屬性會傳回模組中造成錯誤之資料表的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果值不適用於錯誤的類型，則集合是空的。 您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。

### <a name="c"></a>C++

請參閱 [**get \_ ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

