---
description: 註冊指定的資料庫。
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510497"
---
# <a name="sdbregisterdatabaseex-function"></a>SdbRegisterDatabaseEx 函式

註冊指定的資料庫。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszDatabasePath* \[在\]
</dt> <dd>

資料庫路徑。 此參數不可以是 **Null**。

</dd> <dt>

*dwDatabaseType* \[在\]
</dt> <dd>

資料庫類型。 如需值清單，請參閱 [填充碼資料庫類型](shim-database-types.md) 。

</dd> <dt>

*pTimeStamp* \[在中，選擇性\]
</dt> <dd>

資料庫的時間戳記。 如果此參數為 **Null**，則會使用系統時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="remarks"></a>備註

您必須先註冊資料庫，才能使用任何其他的 SDB 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




