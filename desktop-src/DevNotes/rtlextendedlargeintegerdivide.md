---
description: 分割擴充的整數。
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994997"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>RtlExtendedLargeIntegerDivide 函式

\[**RtlExtendedLargeIntegerDivide** 函式會匯出以支援現有的驅動程式二進位檔，並已淘汰。 為了獲得更好的效能，請使用編譯器支援64位的整數作業。\]

分割擴充的整數。

## <a name="syntax"></a>語法


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>參數

<dl> <dt>

被 *除數* \[在\]
</dt> <dd>

股利。

</dd> <dt>

*除數* \[在\]
</dt> <dd>

因數。

</dd> <dt>

*餘數* \[in、out\]
</dt> <dd>

除法餘數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回除法運算的結果。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
