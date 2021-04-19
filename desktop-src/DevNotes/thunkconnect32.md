---
description: ThunkConnect32 函式是由16位設備磁碟機所使用 (用於呼叫32位核心的 MS-DOS) 。
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989276"
---
# <a name="thunkconnect32-function"></a>ThunkConnect32 函式

\[這個函式支援回溯相容性，但不存在於目前的 Windows 版本中。 新的設備磁碟機應該是32或64位，而且不需要此功能。\]

**ThunkConnect32** 函式是由16位設備磁碟機所使用 (用於呼叫32位核心的 MS-DOS) 。

## <a name="syntax"></a>語法


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

忽略。

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

忽略。

</dd> <dt>

*pszDll16* 
</dt> <dd>

忽略。

</dd> <dt>

*pszDll32* 
</dt> <dd>

忽略。

</dd> <dt>

*hInstance* 
</dt> <dd>

忽略。

</dd> <dt>

*dwReason* 
</dt> <dd>

忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




