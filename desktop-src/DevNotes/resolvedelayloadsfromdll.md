---
description: 將解決延遲載入的匯入工作從父二進位檔轉送到目標二進位檔。
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984754"
---
# <a name="resolvedelayloadsfromdll-function"></a>ResolveDelayLoadsFromDll 函式

將解決延遲載入的匯入工作從父二進位檔轉送到目標二進位檔。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ParentBase* \[在\]
</dt> <dd>

延遲載入另一個二進位檔之模組的基底位址。

</dd> <dt>

*TargetDllName* \[在\]
</dt> <dd>

目標 DLL 的名稱。

</dd> <dt>

*旗標* 
</dt> <dd>

保護必須是0。

</dd> </dl>

## <a name="return-value"></a>傳回值

延遲載入描述項的位址（如果找到的話）。否則 **為 Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Delay-Loaded Dll 的連結器支援](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




