---
description: 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 安裝作業。
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 561dec21f08b5e8ad06ade54427789ece877d79af4c1b5412bb995b1ff25d065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860598"
---
# <a name="winsock_ws2help_lsp_install-event"></a>WINSOCK \_ WS2HELP \_ LSP \_ 安裝事件

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用[Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

**Winsock \_ WS2HELP \_ lsp \_ 安裝** 事件是多層式服務提供者的 winsock 目錄變更事件， (LSP) 安裝作業。


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>參數

<dl> <dt>

*LSP 名稱* 
</dt> <dd>

從所安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。

</dd> <dt>

*目錄* 
</dt> <dd>

Winsock 目錄 (32 位或64位) 安裝 LSP 的位置。 這是一個整數值，也就是32或64。

</dd> <dt>

*安裝程式* 
</dt> <dd>

讓 LSP 安裝呼叫的應用程式模組檔案名。

</dd> <dt>

*GUID* 
</dt> <dd>

要在其中安裝 LSP 之 Winsock 傳輸提供者的 GUID 值。

</dd> <dt>

*類別* 
</dt> <dd>

要安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。

</dd> </dl>

## <a name="remarks"></a>備註

當通訊協定專案安裝到 Winsock 類別目錄時，系統會針對 LSP 安裝作業追蹤 **WINSOCK \_ WS2HELP \_ lsp \_ 安裝** 事件。

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

 

 
