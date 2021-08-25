---
description: 取消註冊指定的資料庫，使其無法再使用。
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2ea0cfeedbf74bea02af60b8c01d04b9e0e02f527ba35c0478da801253687b8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815308"
---
# <a name="sdbunregisterdatabase-function"></a>SdbUnregisterDatabase 函式

取消註冊指定的資料庫，使其無法再使用。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pguidDB* \[在\]
</dt> <dd>

資料庫的 GUID。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




