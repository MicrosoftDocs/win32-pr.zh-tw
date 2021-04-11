---
description: CompareFrameSourceAddress 函式會比較位址與框架的來源位址。
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: 'CompareFrameSourceAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194083"
---
# <a name="compareframesourceaddress-function"></a>CompareFrameSourceAddress 函式

**CompareFrameSourceAddress** 函式會比較位址與框架的來源位址。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。

</dd> <dt>

*lpAddress* \[在\]
</dt> <dd>

位址的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果位址相同，則傳回值為 **TRUE**。

如果位址不同，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

若要讓 **CompareFrameSourceAddress** 函式成功，來源網址類別型必須符合 *lpAddress* 參數中指定的網址類別型。

網路監視器提供兩個其他函數來比較位址： [CompareFrameDestAddress](compareframedestaddress.md) 和 [CompareAddresses](compareaddresses.md)。 **CompareFrameDestAddress** 函式會比較指定的位址與框架的目的地位址，而 **CompareAddress** 函式會比較兩個指定的位址。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **CompareFrameSourceAddress** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> </dl>

 

 




