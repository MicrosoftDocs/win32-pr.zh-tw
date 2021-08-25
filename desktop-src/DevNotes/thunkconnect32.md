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
ms.openlocfilehash: 3f754d4c0e88ee860d112a6fb99d15c2690af0014951e77425d425b65ad16e39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929108"
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



 

 




