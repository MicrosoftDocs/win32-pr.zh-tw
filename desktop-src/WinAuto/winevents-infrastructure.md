---
title: WinEvents 基礎結構
description: Microsoft Windows 作業系統包含稱為 WinEvents 的功能，可讓在 Windows 桌面上執行的進程和應用程式交換特定類型的資訊。
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8662cdcbfa9546ce04dc787e7089f68ba1c03137c41067c20792f7da111cf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563283"
---
# <a name="winevents"></a>WinEvents

Microsoft Windows 作業系統包含稱為 *WinEvents* 的功能，可讓在 Windows 桌面上執行的進程和應用程式交換特定類型的資訊。 使用 Microsoft 消費者介面自動化和 Microsoft Active Accessibility 的協助工具工具是 WinEvents 的主要使用者。

在協助工具的內容中，消費者介面自動化提供者和 Microsoft Active Accessibility 伺服器會使用 WinEvents 來通知用戶端應用程式 UI 中的變更，例如當 UI 元素建立或終結時，或專案名稱、狀態或值變更時。

本節提供的建議、指導方針和範例可協助用戶端處理 WinEvents，以及協助伺服器判斷何時觸發適當的 New-winevent。

## <a name="in-this-section"></a>本節內容

-   [什麼是 WinEvents？](what-are-winevents.md)
-   [註冊攔截函式](registering-a-hook-function.md)
-   [系統層級和 Object-Level 事件](system-level-and-object-level-events.md)
-   [內容內部和跨內容攔截函式](in-context-and-out-of-context-hook-functions.md)
-   [防止在攔截函式中重新進入](guarding-against-reentrancy-in-hook-functions.md)
-   [配置 New-winevent 識別碼](allocation-of-winevent-ids.md)

如需 Microsoft Active Accessibility 中事件通知程式的總覽，請參閱[技術總覽](technical-overview.md)中的[WinEvents](winevents-overview.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一般基礎結構](common-infrastructure.md)
</dt> </dl>

 

 




