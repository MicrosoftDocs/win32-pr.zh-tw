---
title: 使用 Microsoft 定位器
description: Microsoft 定位器是預設的名稱服務。 RPC 執行時間程式庫會使用它來尋找伺服器主機系統上的伺服器程式。
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- 使用 Microsoft 定位器的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64a5c54c09ee344ffdba46f9f44a546ab866557bc861b206868ad6d3992896b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010736"
---
# <a name="using-microsoft-locator"></a>使用 Microsoft 定位器

Microsoft 定位器是預設的名稱服務。 RPC 執行時間程式庫會使用它來尋找伺服器主機系統上的伺服器程式。

**注意** Windows Vista 和更新版本的作業系統不支援 Microsoft RPC 定位器。

在 Windows 2000 之前，Microsoft 定位器未提供持續性的名稱服務專案。 名稱服務中的所有專案都儲存在伺服器程式的主機電腦上的記憶體快取中。 定位器使用廣播機制來探索用戶端所要求的伺服器位置。 當主機系統關機時，所有名稱服務專案都會遺失。

從 Windows 2000 的版本開始，Microsoft 定位器現在支援持續性名稱服務專案。 為了達成此目的，系統採用分散式目錄服務來儲存名稱服務專案。 這項機制有幾個優點：

-   **堅持。** 伺服器程式在每次啟動時，都不再需要將其系結資訊匯出至名稱服務。 名稱服務現在會儲存資訊，直到網路系統管理員上的伺服器程式明確移除該資訊為止。
-   **效率。** 藉由排除名稱服務專案的大部分廣播，定位器可減少網路流量。 它也能更快速地找到名稱服務專案。
-   **跨網域互通性。** 用戶端現在可以跨多個網域提出名稱服務要求。

Microsoft 定位器的目前版本具有回溯相容性。 例如，執行隨附于 Windows 2000 之定位器的伺服器主機系統可以在包含執行 Windows NT 4.0 隨附之定位器的伺服器主機系統的網路上正確運作。

在2000版的 Windows 中，Microsoft 定位程式現在支援使用者群組的名稱服務專案。 它也能讓您建立使用者設定檔。

此外，目前版本的 Microsoft 定位器支援在名稱服務專案中使用存取控制清單。 這項功能可增強網路的安全性。

Microsoft 定位器現在已包含隨插即用支援。 因此，它可以透明地處理隨插即用事件，例如網域變更。 如需詳細資訊，請參閱 [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) 和 [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa)。

 

 




