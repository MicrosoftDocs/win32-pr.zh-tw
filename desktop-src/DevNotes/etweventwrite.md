---
description: 深入瞭解： EtwEventWrite 函數
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: b8e06c2a0922038e37766f44c0b9fcd7c85bbb7fd4fa4bd0841192be9e4e9087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162099"
---
# <a name="etweventwrite-function"></a>EtwEventWrite 函式

[EtwEventWrite 函式和它所傳回的結構是作業系統的內部，而且可能會從一個 Windows 版本變更為另一個版本。]

將基本事件寫入至會話。

## <a name="syntax"></a>語法

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>參數

<dl> <dt>

*RegHandle*
</dt> <dd>

提供者的 RegHandle。

</dd> <dt>

*EventDescriptor*
</dt> <dd>

要記錄之事件的事件描述項。

</dd> <dt>

*UserDataCount*
</dt> <dd>

使用者資料項目數目。

</dd> <dt>

*UserData*
</dt> <dd>

使用者資料項目陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

Win32 錯誤碼。


## <a name="remarks"></a>備註

EtwEventWrite 函式及其傳回的結構都是作業系統的內部，而且可能會從一個 Windows 版本變更為另一個版本。 若要維持應用程式的相容性，最好改為使用公用函數。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | ntetw。h |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
