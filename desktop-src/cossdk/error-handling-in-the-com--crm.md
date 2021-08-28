---
description: COM + CRM 中的錯誤處理
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: COM + CRM 中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a470aa1d386c28d5f1fe67d308b8bb46d23636dc3411906e07184e6ddce923
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128720"
---
# <a name="error-handling-in-the-com-crm"></a>COM + CRM 中的錯誤處理

COM + 伺服器應用程式會執行 failfast 原則。 如果偵測到嚴重的內部錯誤，伺服器應用程式進程會結束，並將錯誤訊息寫入 Windows 事件記錄檔。 這可讓您快速偵測問題，而且可能是因為交易處理的應用程式資料受到保護。 請一律檢查 Windows 事件記錄檔中是否有任何來自 CRM 的錯誤，無論是在開發期間或在最終部署期間。

使用 CRM 介面的基本錯誤，例如不正確引數或順序錯誤 (例如，嘗試在註冊 CRM 補償器) 之前寫入記錄檔記錄、傳回錯誤碼，且不應觸發 failfast。 針對 CRM 開發，您可以選擇設定 VTRACE1 登錄機碼 (請參閱[com + CRM 登錄設定](com--crm-registry-settings.md)) ，讓訊息出現在每個錯誤的偵錯工具輸出視窗中。

也可能發生暫時性錯誤。 這些錯誤通常是由計時條件所造成，而且會導致傳回錯誤碼。 CRM 開發人員應該確保這些錯誤狀況都已處理。 例如，寫入記錄檔記錄時，交易可能會因為超時而中止。方法接著會傳回錯誤，呼叫端應該檢查並適當地處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



