---
description: GetFrameSrcAddressOffset 函式會傳回框架來源位址的位移。
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: 'GetFrameSrcAddressOffset 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5c8c2315b53d336a06a73e63019daee842439f65aa53e3fb7d34d4944dcab9cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366092"
---
# <a name="getframesrcaddressoffset-function"></a>GetFrameSrcAddressOffset 函式

**GetFrameSrcAddressOffset** 函式會傳回框架來源位址的位移。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* 
</dt> <dd>

框架的控制碼。

</dd> <dt>

*AddressType* 
</dt> <dd>

來源網址類別型。 參數值可以是下列其中一項：

-   位址 \_ 類型 \_ ETHERNET
-   位址 \_ 類型 \_ IP
-   位址 \_ 類型的 \_ IPX
-   位址 \_ 類型 \_ TOKENRING
-   位址 \_ 類型的 \_ FDDI
-   位址 \_ 類型 \_ XNS
-   位址 \_ 類型 \_ VINES \_ IP
-   位址 \_ 類型的 \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

**DWORD** 的指標，它會在傳回時包含位址的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為來源位址的位移。

如果函式不成功，則傳回值為減去 1 (-1) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




