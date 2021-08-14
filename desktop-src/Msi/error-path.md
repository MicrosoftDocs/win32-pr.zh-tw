---
description: 在 Windows Installer 1.0 和1.1 版中，Path 屬性一律為空字串。 未來的版本可能會使用這個值，傳回無法建立之檔案或目錄的路徑。
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: '錯誤。 Path 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7787fcd5bad5550b933b2a866308c1d5b77dd24f60fce23ebc3b227829528307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378149"
---
# <a name="errorpath-property"></a>錯誤。 Path 屬性

在 Windows Installer 1.0 和1.1 版中，Path 屬性一律為空字串。 未來的版本可能會使用這個值，傳回無法建立之檔案或目錄的路徑。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

此值只對 msmErrorFileCreate 或 msmErrorDirCreate 類型的錯誤有效。 您可以藉由呼叫 [**error**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。

### <a name="c"></a>C++

請參閱 [**get \_ Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

