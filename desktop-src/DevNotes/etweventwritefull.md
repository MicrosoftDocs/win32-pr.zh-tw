---
description: 將完整事件寫入至會話。
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936399"
---
# <a name="etweventwritefull-function"></a>EtwEventWriteFull 函式

[EtwEventWriteFull 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個版本。]

將完整事件寫入至會話。

## <a name="syntax"></a>語法

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
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

*EventProperty*
</dt> <dd>

使用者指定的旗標。

</dd> <dt>

*ActivityId*
</dt> <dd>

活動識別碼。

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

相關的活動識別碼。

</dd> <dt>

*UserDataCount*
</dt> <dd>

使用者資料項目的數目。

</dd> <dt>

*UserData*
</dt> <dd>

使用者資料項目陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

Win32 錯誤碼。

## <a name="remarks"></a>備註

EtwEventWriteFull 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個。 若要維持應用程式的相容性，最好改為使用公用函數。


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
