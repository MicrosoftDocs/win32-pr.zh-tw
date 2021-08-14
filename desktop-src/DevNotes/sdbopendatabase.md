---
description: 開啟指定的填充碼資料庫。
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: df0081d7373bf67d3df1723be7d5beb272ef7ee4c77c54da8a6985dfe250d7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161191"
---
# <a name="sdbopendatabase-function"></a>SdbOpenDatabase 函式

開啟指定的填充碼資料庫。

## <a name="syntax"></a>語法


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszPath* \[在\]
</dt> <dd>

資料庫路徑。 此參數不可以是 **Null**。

</dd> <dt>

*eType* \[在\]
</dt> <dd>

路徑類型。 如需值清單，請參閱 [**路徑 \_ 類型**](path-type.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回填充碼資料庫的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




