---
description: MacTypeToAddressType 函式會將指定的 MAC 型別轉換為網址類別型。
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: 'MacTypeToAddressType 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848161"
---
# <a name="mactypetoaddresstype-function"></a>MacTypeToAddressType 函式

**MacTypeToAddressType** 函式會將指定的 MAC 型別轉換為網址類別型。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MacType* \[在\]
</dt> <dd>

要轉換的 MAC 類型。 指定下列其中一個值：

MAC \_ 類型 \_ ETHERNET MAC \_ 類型 \_ TOKENRING MAC \_ 類型的 \_ FDDI

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是下列其中一種網址類別型。

位址 \_ 類型 \_ 乙太網路位址類型 \_ \_ TOKENRING 位址 \_ 類型 \_ FDDI

如果函式不成功，則 MAC 類型未知，傳回值為-1。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **MacTypeToAddressType** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




