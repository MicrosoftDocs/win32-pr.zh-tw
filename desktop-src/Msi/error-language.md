---
description: Error 物件的唯讀語言屬性會傳回目前錯誤的 LANGID。
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: '錯誤。 Language 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082888"
---
# <a name="errorlanguage-property"></a>錯誤。語言屬性

[**Error**](error-object.md)物件的唯讀 **語言** 屬性會傳回目前錯誤的 **LANGID** 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

除非錯誤的類型為 msmErrorLanguageUnsupported 或 msmErrorLanguageFailed，否則 **Language** 屬性的值為-1。 您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。

### <a name="c"></a>C++

請參閱 [**取得 \_ Language Function (Error 物件)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

