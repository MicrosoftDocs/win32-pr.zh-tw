---
description: ConfigurableItem 物件的 Format 屬性會從 ModuleConfiguration 資料表的 Format 資料行傳回值。
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: 'ConfigurableItem： Format 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000804"
---
# <a name="configurableitemformat-property"></a>ConfigurableItem 格式屬性

[**ConfigurableItem**](configurableitem-object.md)物件的 **format** 屬性會從 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 format 資料行傳回值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這個屬性只能包含下列值。



| 常數                        | 值 |
|---------------------------------|-------|
| **msmConfigurableItemText**     | 0     |
| **msmConfigurableItemKey**      | 1     |
| **msmConfigurableItemInteger**  | 2     |
| **msmConfigurableItemBitfield** | 3     |



 

### <a name="c"></a>C++

請參閱 [**取得 \_ 格式**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




