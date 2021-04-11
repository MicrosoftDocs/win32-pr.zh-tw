---
description: Winsock 追蹤事件詳細資料。
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Winsock 追蹤事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112988"
---
# <a name="winsock-tracing-events"></a>Winsock 追蹤事件

本節說明特定 Winsock 追蹤事件詳細資料的詳細資訊。

Winsock 追蹤是一項疑難排解功能，可以在零售二進位檔中啟用，以追蹤某些 Windows 通訊端事件的額外負荷。 這項功能可讓開發人員和產品支援獲得更佳的診斷功能。 Winsock 網路事件追蹤支援 IPv4 和 IPv6 應用程式的追蹤通訊端作業。 Winsock 目錄變更追蹤支援追蹤對 Winsock 類別目錄所做的變更， (Lsp) 的分層服務提供者。

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

Winsock 追蹤會使用 Windows 的事件追蹤 (ETW) 是作業系統所提供的一般用途高速追蹤功能。 ETW 針對使用者模式應用程式和核心模式設備磁碟機所引發的事件，提供追蹤機制。 ETW 可以動態啟用和停用記錄，讓您輕鬆地在生產環境中執行詳細追蹤，而不需要重新開機或重新開機應用程式。 Windows Vista 和更新版本已新增使用 ETW 進行 Winsock 追蹤的支援。 如需 ETW 的一般資訊，請參閱 [使用 Etw 改善偵錯工具和效能微調](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)。

下列清單提供每個 Winsock 追蹤事件的詳細資訊。 如需任何事件的詳細資訊，請按一下事件名稱。



| 活動名稱                                                            | Description                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AFD \_ 事件 \_ 建立**](afd-event-create.md)                        | 適用于通訊端建立作業的 Winsock 網路追蹤事件。                            |
| [**AFD \_ 事件 \_ 關閉**](afd-event-close.md)                          | 適用于通訊端關閉操作的 Winsock 網路追蹤事件。                                 |
| [**WINSOCK \_ WS2HELP \_ LSP \_ 安裝**](winsock-ws2help-lsp-install.md) | 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 安裝作業。 |
| [**WINSOCK \_ WS2HELP \_ LSP \_ 移除**](winsock-ws2help-lsp-remove.md)   | 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 移除作業。      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ DISABLE**](winsock-ws2help-lsp-disable.md) | 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 停用作業。      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ 重設**](winsock-ws2help-lsp-reset.md)     | Winsock 類別目錄重設作業的 winsock 目錄變更事件。                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 ETW 改善偵錯和效能調整](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock 網路事件追蹤詳細資料](winsock-tracing-event-details.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
