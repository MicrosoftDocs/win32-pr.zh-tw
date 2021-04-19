---
description: Merge 物件的 CloseDatabase 方法會關閉目前開啟的 Windows Installer 資料庫。
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: 'CloseDatabase 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974907"
---
# <a name="mergeclosedatabase-method"></a>Merge. CloseDatabase 方法

[**Merge**](merge-object.md)物件的 **CloseDatabase** 方法會關閉目前開啟的 Windows Installer 資料庫。

## <a name="syntax"></a>語法


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bCommit* 
</dt> <dd>

若應儲存變更，**則為 TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

關閉資料庫會清除所有相依性資訊，但不會影響任何未取出的錯誤。

### <a name="c"></a>C++

請參閱 [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
