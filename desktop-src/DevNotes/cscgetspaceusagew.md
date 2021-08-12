---
description: 抓取離線檔案快取所使用之空間的相關資訊。
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667951"
---
# <a name="cscgetspaceusagew-function"></a>CSCGetSpaceUsageW 函式

\[這項功能不受支援，因此不應該使用。\]

抓取離線檔案快取所使用之空間的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lptzLocation* \[in、out\]
</dt> <dd>

快取的目錄位置。

</dd> <dt>

*dwSize* \[在\]
</dt> <dd>

*LptzLocation* 緩衝區的大小（以字元為單位）。

</dd> <dt>

*lpdwMaxSpaceHigh* \[in、out\]
</dt> <dd>

快取中可用的最大位元組數目的高序位 **DWORD** 。

</dd> <dt>

*lpdwMaxSpaceLow* \[in、out\]
</dt> <dd>

快取中可用的最大位元組數目的低序位 **DWORD** 。

</dd> <dt>

*lpdwCurrentSpaceHigh* \[in、out\]
</dt> <dd>

快取中目前可用位元組數目的高序位 **DWORD** 。

</dd> <dt>

*lpdwCurrentSpaceLow* \[in、out\]
</dt> <dd>

快取中目前可用位元組數目的低序位 **DWORD** 。

</dd> <dt>

*lpcntTotalFiles* \[in、out\]
</dt> <dd>

快取中的檔案總數。

</dd> <dt>

*lpcntTotalDirs* \[in、out\]
</dt> <dd>

快取中的目錄總數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
