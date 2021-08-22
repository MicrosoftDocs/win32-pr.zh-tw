---
description: Winsock 類別目錄重設作業的 winsock 目錄變更事件。
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051286"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>WINSOCK \_ WS2HELP \_ LSP \_ 重設事件

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用[Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

Winsock **\_ WS2HELP \_ LSP \_ reset** 事件是 winsock 目錄重設作業的 winsock 目錄變更事件。


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>參數

<dl> <dt>

*目錄* 
</dt> <dd>

要重設的 (32 位或64位) 的 Winsock 目錄。 這是一個整數值，也就是32或64。

</dd> </dl>

## <a name="remarks"></a>備註

在重設 Winsock 類別目錄時，會追蹤 winsock 多層式服務提供者 (LSP) 作業的 **winsock \_ WS2HELP \_ LSP \_ 重設** 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
