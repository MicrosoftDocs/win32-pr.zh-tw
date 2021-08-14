---
description: 將來源記憶體區塊的內容複寫到目的地記憶體區塊，並支援重迭的來源和目的地記憶體區塊。
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: 'RtlMoveMemory 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: bf4366633de321e27f6d3cdc0396fcdce81b0dac30b0d09a4c2c4675706d939e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161660"
---
# <a name="rtlmovememory-function"></a>RtlMoveMemory 函式

將來源記憶體區塊的內容複寫到目的地記憶體區塊，並支援重迭的來源和目的地記憶體區塊。

## <a name="syntax"></a>語法


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目的地* \[擴展\]
</dt> <dd>

要將位元組複製到其中之目的地記憶體區塊的指標。

</dd> <dt>

*來源* \[在\]
</dt> <dd>

要從中複製位元組之來源記憶體區塊的指標。

</dd> <dt>

*長度* \[在\]
</dt> <dd>

要從來源複製到目的地的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

無

## <a name="remarks"></a>備註

來源記憶體區塊是由 *來源* 和 *長度* 所定義，可以重迭目的地記憶體區塊（由 *目的地* 和 *長度* 所定義）。

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)常式的執行速度比 **RtlMoveMemory** 快，但 **RtlCopyMemory** 需要來源和目的地記憶體區塊不重迭。

如果來源和目的地記憶體區塊是在非分頁系統記憶體中， **RtlMoveMemory** 的呼叫端可以在任何 IRQL 執行。 否則，呼叫端必須在 IRQL <= APC \_ 層級執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                    |
| 目標平台<br/>          | <dl> <dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| 標頭<br/>                   | <dl> <dt>Wdm (包括 Wdm、Ntddk .h 或 Ntifs. h) </dt> </dl>                   |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
