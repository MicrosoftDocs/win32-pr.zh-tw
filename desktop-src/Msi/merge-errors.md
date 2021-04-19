---
description: Merge 物件的唯讀錯誤屬性會傳回錯誤物件的集合，這些是一組目前的錯誤。
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: 'Merge。 Errors 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995290"
---
# <a name="mergeerrors-property"></a>Merge。 Errors 屬性

[**Merge**](merge-object.md)物件的唯讀 **錯誤** 屬性會傳回 [**錯誤**](error-object.md)物件的集合，這些是一組目前的錯誤。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

抓取是非破壞性的。 重複呼叫這個方法，即可抓取錯誤集合的多個實例。

### <a name="c"></a>C++

請參閱 [**取得 \_ 錯誤**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
