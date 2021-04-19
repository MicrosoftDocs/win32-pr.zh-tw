---
description: Merge 物件的 OpenLog 方法會開啟記錄檔，以接收進度和錯誤訊息。 如果記錄檔已經存在，安裝程式會附加新的訊息。 如果記錄檔不存在，安裝程式會建立記錄檔。
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: 'OpenLog 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979624"
---
# <a name="mergeopenlog-method"></a>Merge. OpenLog 方法

[**Merge**](merge-object.md)物件的 **OpenLog** 方法會開啟記錄檔，以接收進度和錯誤訊息。 如果記錄檔已經存在，安裝程式會附加新的訊息。 如果記錄檔不存在，安裝程式會建立記錄檔。

## <a name="syntax"></a>語法


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名稱* 
</dt> <dd>

指向要開啟或建立之檔案的完整檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

用戶端可以透過 [**log**](merge-log.md) 方法將自己的訊息傳送至此記錄檔。

### <a name="c"></a>C++

請參閱 [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
