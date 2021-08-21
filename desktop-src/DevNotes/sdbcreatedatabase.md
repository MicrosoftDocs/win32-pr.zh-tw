---
description: 建立新的填充碼資料庫。
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161552"
---
# <a name="sdbcreatedatabase-function"></a>SdbCreateDatabase 函式

建立新的填充碼資料庫。

## <a name="syntax"></a>語法


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszPath* \[在\]
</dt> <dd>

應儲存資料庫的路徑。 此參數不可以是 **Null**。

</dd> <dt>

*eType* \[在\]
</dt> <dd>

路徑類型。 如需值清單，請參閱 [**路徑 \_ 類型**](path-type.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回填充碼資料庫的控制碼，或在失敗時傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




