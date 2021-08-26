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
ms.openlocfilehash: 512e180549c246a5504bc14675d61082c68904aa767d98deca5111d9a275dc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984098"
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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




