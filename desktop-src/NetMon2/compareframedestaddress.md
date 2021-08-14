---
description: CompareFrameDestAddress 函式會比較位址與框架的目的位址。
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: 'CompareFrameDestAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 153d1a5768791a33fd4f7629e071a125a4ee2ee46feaae366e2c1a21d8118f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367386"
---
# <a name="compareframedestaddress-function"></a>CompareFrameDestAddress 函式

**CompareFrameDestAddress** 函式會比較位址與框架的目的位址。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CompareFrameDestAddress(
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

若要讓 **CompareFrameDestAddress** 函式成功傳回，目的地網址類別型必須符合 *lpAddress* 參數中指定的網址類別型。

網路監視器提供兩個其他函式： [CompareFrameSourceAddress](compareframesourceaddress.md) 和 [CompareAddresses](compareaddresses.md)，可供您用來比較位址。 **CompareFrameSourceAddress** 函式會比較指定的位址與框架的來源位址，而 **CompareAddress** 函數則會比較兩個指定的位址。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **CompareFrameDestAddress** 函數。

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

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




