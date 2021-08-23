---
description: 解碼和儲存字串。
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815468"
---
# <a name="cchlszofid2-function"></a>CchLszOfId2 函式

解碼和儲存字串。

## <a name="syntax"></a>語法


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*id* 
</dt> <dd>

要解碼和儲存的資源檔中的字串識別碼。 未驗證字串的有效性。

</dd> <dt>

*lsz* 
</dt> <dd>

長度為 *cbmax* 之緩衝區的指標。 長度超過 *cbmax* 的字串會被截斷。

</dd> <dt>

*cbmax* 
</dt> <dd>

要儲存在 *lsz* 參數中之字串的最大長度。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回已解碼的字串。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
