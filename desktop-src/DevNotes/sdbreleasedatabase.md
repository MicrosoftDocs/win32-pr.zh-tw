---
description: 關閉使用 SdbInitDatabase 函數初始化的填充碼資料庫。
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 82a7cf785927a5ef14e3e033c29233afcc4a49cf89d610757d110583bce4eff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815328"
---
# <a name="sdbreleasedatabase-function"></a>SdbReleaseDatabase 函式

關閉使用 [**SdbInitDatabase**](sdbinitdatabase.md) 函數初始化的填充碼資料庫。

## <a name="syntax"></a>語法


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSDB* \[在\]
</dt> <dd>

[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




