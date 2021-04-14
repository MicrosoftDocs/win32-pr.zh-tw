---
UID: ''
title: InterlockedPushListSList 函式
description: 在另一個單一連結清單的前方插入單一連結清單。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2020
ms.locfileid: "104374836"
---
# <a name="interlockedpushlistslist-function"></a>InterlockedPushListSList 函式

## <a name="description"></a>Description

在另一個單一連結清單的前方插入單一連結清單。
系統會在多處理器系統上同步處理清單的存取。

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>參數

### <a name="listhead-in-out"></a>ListHead [in，out]

**SLIST_HEADER** 結構的指標，表示單一連結清單的標頭。
*清單* 和 *ListEnd* 參數所指定的清單會插入此清單的前面。

### <a name="list-in-out"></a>清單 [in，out]

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)結構的指標，代表要插入清單中的第一個專案。

### <a name="listend-in-out"></a>ListEnd [in，out]

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)結構的指標，代表要插入清單中的最後一個專案。

### <a name="count-in"></a>計數 [in]

清單中要插入的專案數目。

## <a name="returns"></a>傳回

傳回值是 *ListHead* 參數所指定清單中的前一個專案。
如果清單之前是空的，則傳回值為 **Null**。

## <a name="remarks"></a>備註

所有清單專案都必須對齊 **MEMORY_ALLOCATION_ALIGNMENT** 界限;否則，此函式將會以無法預期的方式運作。
請參閱 **_aligned_malloc**。

**Windows 8 和 Windows Server 2012：**  此函數已被 [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)取代。
當使用 **NTDDI_VERSION** 設定為 **NTDDI_WIN8** 或更高版本進行編譯時，對 **InterlockedPushListSList** 的呼叫會改為移至 **InterlockedPushListSListEx** 。

## <a name="see-also"></a>另請參閱

[連鎖單向連結清單](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[使用單向連結清單](/windows/desktop/Sync/using-singly-linked-lists)
