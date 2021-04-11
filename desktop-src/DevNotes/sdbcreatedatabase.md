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
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936272"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




