---
description: Winsock 目錄變更追蹤詳細資料
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Winsock 目錄變更追蹤詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114288"
---
# <a name="winsock-catalog-change-tracing-details"></a>Winsock 目錄變更追蹤詳細資料

> [!Note]  
> 已淘汰分層服務提供者。 從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。

 

適用于多層式服務提供者 (Lsp) 的 Winsock 目錄變更事件追蹤，與 LSP 安裝、LSP 移除、LSP 停用和 Winsock 類別目錄重設作業有關。 下列所有事件都會寫入至 *Microsoft windows-Winsock-WS2HELP/Operational* 通道，這與記錄在 Windows Vista 和更新版本上的其他 Winsock 網路事件追蹤不同。

以下將詳細說明每個可追蹤的 Winsock LSP 事件，以及描述所記錄的參數和資訊。

## <a name="lsp-install"></a>LSP 安裝

事件識別碼 = 1

層級 = 4 (資訊) 

針對 LSP 安裝作業，會追蹤下列 Winsock LSP 事件：

-   通訊協定專案會安裝到 Winsock 目錄。

系統會針對 LSP 安裝事件記錄下列參數：



| 參數                                                                                                | Description                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP 名稱<br/>     | 從所安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄<br/>         | Winsock 目錄 (32 位或64位) 安裝 LSP 的位置。 這是一個整數值，也就是32或64。<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>安裝<br/> | 讓 LSP 安裝呼叫的應用程式模組檔案名。<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | 要在其中安裝 LSP 之 Winsock 傳輸提供者的 GUID 值。<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別<br/>     | 要安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。<br/>                                |



 

## <a name="lsp-uninstall"></a>LSP 卸載

事件識別碼 = 2

層級 = 4 (資訊) 

針對 LSP 卸載作業，會追蹤下列 Winsock LSP 事件：

-   從 Winsock 目錄移除通訊協定專案。

系統會針對 LSP 卸載事件記錄下列參數：



| 參數                                                                                                | Description                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP 名稱<br/>     | 從要移除的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄<br/>         | Winsock 目錄 (32 位或64位) ，其中 LSP 正在移除。 這是一個整數值，也就是32或64。<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>安裝<br/> | 讓 LSP 移除呼叫的應用程式模組檔案名。<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | 將 LSP 移除的 Winsock 傳輸提供者的 GUID 值。<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別<br/>     | 要移除的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。<br/>                                |



 

## <a name="lsp-disable"></a>LSP 停用

事件識別碼 = 3

層級 = 4 (資訊) 

針對 LSP 停用作業，會追蹤下列 Winsock LSP 事件：

-   Winsock 目錄中的通訊協定專案已停用。

針對 LSP 停用事件，會記錄下列參數：



| 參數                                                                                                | Description                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP 名稱<br/>     | 針對正在停用的 LSP，從 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄<br/>         | Winsock 目錄 (32 位或64位) 在 LSP 正在停用的位置。 這是一個整數值，也就是32或64。<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>安裝<br/> | 讓 LSP 停用呼叫的應用程式模組檔案名。<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | 要停用 LSP 之 Winsock 傳輸提供者的 GUID 值。<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別<br/>     | 正在停用的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Winsock 目錄重設

事件識別碼 = 4

層級 = 4 (資訊) 

Winsock 類別目錄重設作業會追蹤下列 Winsock LSP 事件：

-   Winsock 類別目錄已重設。

Winsock 類別目錄重設事件會記錄下列參數：



| 參數                                                                                        | Description                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>目錄<br/> | 要重設的 (32 位或64位) 的 Winsock 目錄。 這是一個整數值，也就是32或64。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> <dt>

[Winsock 網路事件追蹤詳細資料](winsock-tracing-event-details.md)
</dt> </dl>

 

 
