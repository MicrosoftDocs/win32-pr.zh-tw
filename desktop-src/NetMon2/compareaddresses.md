---
description: CompareAddresses 函式會比較兩個位址，表示其中一個位址大於、小於或等於其他位址。
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: 'CompareAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323afb66d251d58bf13670fd335da2bd26ad2193ce03d5aa799ddb0f28e875fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744718"
---
# <a name="compareaddresses-function"></a>CompareAddresses 函式

**CompareAddresses** 函式會比較兩個位址，表示其中一個位址大於、小於或等於其他位址。

## <a name="syntax"></a>語法


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpAddress1* \[在\]
</dt> <dd>

第一個位址的指標。

</dd> <dt>

*lpAddress2* \[在\]
</dt> <dd>

第二個位址的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果位址相同，則函數會傳回零。

如果 *lpAddress1* 參數指定的位址小於 *lpAddress2* 參數指定的位址，則傳回值為負數。

如果 *lpAddress1* 參數指定的位址大於 *lpAddress2* 參數指定的位址，則傳回值為正數。

## <a name="remarks"></a>備註

小於另一個位址的位址表示先前的畫面格。 大於另一個位址的位址表示較新的畫面格。

網路監視器提供兩個其他函式： [CompareFrameDestAddress](compareframedestaddress.md) 和 [CompareFrameSourceAddress](compareframesourceaddress.md)，可供您用來比較位址。 **CompareFrameDestAddress** 函式會比較指定的位址與框架的目的地位址，而 **CompareFrameSourceAddress** 函式會比較指定的位址與框架的來源位址。

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




