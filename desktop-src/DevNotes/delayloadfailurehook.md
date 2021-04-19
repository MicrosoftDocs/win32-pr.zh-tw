---
description: 傳回指定之 DLL 和進程的延遲載入失敗回呼函式的位址。
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993492"
---
# <a name="delayloadfailurehook-function"></a>DelayLoadFailureHook 函式

傳回指定之 DLL 和進程的延遲載入失敗回呼函式的位址。

## <a name="syntax"></a>語法


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszDllName* \[在\]
</dt> <dd>

DLL 的名稱。

</dd> <dt>

*pszProcName* \[在\]
</dt> <dd>

處理序的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼函式的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[失敗攔截](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




