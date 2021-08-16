---
description: 關閉搜尋控制碼。
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 862159ed74d6c7c9ddbe4d6f97bede37bab7dca949e6d3259715737de07b8df5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758718"
---
# <a name="cscfindclose-function"></a>CSCFindClose 函式

\[這項功能不受支援，因此不應該使用。\]

關閉搜尋控制碼。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFind* \[在\]
</dt> <dd>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)函數所傳回的搜尋控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)
</dt> </dl>

 

 
