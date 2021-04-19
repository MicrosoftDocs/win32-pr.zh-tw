---
description: GetFrameDstAddressOffset 函式會傳回指定框架之目的地位址的位移。
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: 'GetFrameDstAddressOffset 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973810"
---
# <a name="getframedstaddressoffset-function"></a>GetFrameDstAddressOffset 函式

**GetFrameDstAddressOffset** 函式會傳回指定框架之目的地位址的位移。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。

</dd> <dt>

*AddressType* \[在\]
</dt> <dd>

目的地位址的類型。 指定下列其中一個值：

位址 \_ 類型的 \_ 乙太網路位址類型 \_ IP 位址類型 TOKENRING 網址類別型的 IP 位址類型 \_ \_ \_ \_ \_ \_ \_ \_ \_ XNS 位址 \_ 類型 \_ VINES \_ IP 位址類型的 IP 位址類型 \_ \_ 。

</dd> <dt>

*AddressLength* \[在\]
</dt> <dd>

目的地位址的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是以) 位元組為單位的位移 (測量到要求的網址類別型。

如果函式不成功，則傳回值為減去 1 (-1) 。

## <a name="remarks"></a>備註

如果 *AddressType* 參數設定為 ADDRESS \_ 類型 \_ ETHERNET， **GetFrameDstAddressOffset** 函式的傳回值一律為零。 乙太網路位址的位移一律為零。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameDstAddressOffset** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




