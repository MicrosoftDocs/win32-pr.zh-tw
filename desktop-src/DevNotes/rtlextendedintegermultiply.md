---
description: 將擴展的整數相乘。
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 0048da80026029274a89d089f5c232311a481a6010c0aad32d8b1a6ae6cc6786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571468"
---
# <a name="rtlextendedintegermultiply-function"></a>RtlExtendedIntegerMultiply 函式

\[**RtlExtendedIntegerMultiply** 函式會匯出以支援現有的驅動程式二進位檔，並已淘汰。 為了獲得更好的效能，請使用編譯器支援64位的整數作業。\]

將擴展的整數相乘。

## <a name="syntax"></a>語法


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*被乘數* \[在\]
</dt> <dd>

被乘數.

</dd> <dt>

*乘數* \[在\]
</dt> <dd>

乘數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回乘法結果。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
