---
description: 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 停用作業。
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733128"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>WINSOCK \_ WS2HELP \_ LSP \_ 停用事件

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用[Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

**Winsock \_ WS2HELP \_ lsp \_ 停** 用事件是多層式服務提供者的 winsock 目錄變更事件， (lsp) 停用作業。


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>參數

<dl> <dt>

*LSP 名稱* 
</dt> <dd>

針對正在停用的 LSP，從 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。

</dd> <dt>

*目錄* 
</dt> <dd>

Winsock 目錄 (32 位或64位) 在 LSP 正在停用的位置。 這是一個整數值，也就是32或64。

</dd> <dt>

*安裝程式* 
</dt> <dd>

讓 LSP 停用呼叫的應用程式模組檔案名。

</dd> <dt>

*GUID* 
</dt> <dd>

要停用 LSP 之 Winsock 傳輸提供者的 GUID 值。

</dd> <dt>

*類別* 
</dt> <dd>

正在停用的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。

</dd> </dl>

此事件沒有任何參數。

## <a name="remarks"></a>備註

Winsock **\_ WS2HELP \_ lsp \_ 停** 用事件是在 winsock 類別目錄中停用通訊協定專案時，針對 LSP 停用作業進行追蹤。

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

 

 
