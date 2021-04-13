---
title: 管理託管服務的基礎結構
description: Windows 遠端管理 2.0 (WinRM) 引進了裝載架構。 為了使用此架構，會撰寫 WinRM 外掛程式，以公開 WinRM 基礎結構內應用程式的管理資料。
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311307"
---
# <a name="infrastructure-for-managing-hosted-services"></a>管理託管服務的基礎結構

Windows 遠端管理 2.0 (WinRM) 引進了裝載架構。 為了使用此架構，會撰寫 WinRM 外掛程式，以公開 WinRM 基礎結構內應用程式的管理資料。 支援兩種裝載模型。 其中一個是 Internet Information Services (IIS) 「基礎」，另一個則是「以服務為基礎的 WinRMâ」。 以 WinRM 為基礎的模型會使用 HTTP.sys，且不會相依于 IIS。

下列各節說明裝載模型：

-   [WinRM IIS 擴充功能裝載模型](#winrm-iis-extension-hosting-model)
    -   [WinRM IIS 擴充功能裝載模型中的負載平衡](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [WinRM IIS 擴充功能裝載模型中的 HTTP 重新導向](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [WinRM 服務裝載模型](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>WinRM IIS 擴充功能裝載模型

WinRM IIS 延伸模組是使用 **伺服器管理員** 安裝的選用元件。 WinRM IIS 延伸模組是用來從 IIS 服務內建立 WinRMâ€「啟用的端點」。 您可以在網站或虛擬目錄層級啟用此模組。 其運作方式是攔截連入要求，並將其重新導向至關聯的網站或虛擬目錄。 系統會將要求重新導向至可分析內容的 WinRM 模組，然後判斷哪些 WinRM 外掛程式設定為處理每個要求。 如需詳細資訊，請參閱 [IIS 主機外掛程式](iis-host-plug-in-configuration.md)設定。

WinRM IIS 擴充功能裝載模型是設計來處理大量的要求。 如果以 IIS 為基礎的模型做為裝載架構，則可使用下列功能：

-   標準 IIS 驗證模組。
-   裝載所有外掛程式的 IIS 應用程式集區進程。
-   節流管理系統的大量使用者。 如需詳細資訊，請參閱 [遠端 shell 的配額管理](quotas.md)。
-   Shell 外掛程式模型。 請參閱 [WinRM 用戶端 SHELL API](client-shell-api.md)。
-   彈性的授權模型。 請參閱 [WinRM 外掛程式 API](winrm-plugin-api.md)。

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>WinRM IIS 擴充功能裝載模型中的負載平衡

大部分的負載平衡器 (磅) 支援以 cookie 為基礎的粘性模型。 LB 會將 cookie 插入至用戶端的第一個要求的回應中。 針對所有後續的要求，cookie 會在要求中傳輸，而 LB 會使用 cookie 將要求路由傳送至適當的伺服器。

在將 WinRM 2.0 裝載于 LB 後方的環境中，LB 應設定為以 MS-WSMAN 作為 cookie 的名稱。 此外，您必須設定 LB，讓 cookie 的存留期成為無限的，因為 WinRM 用戶端應該控制 cookie 的有效時間長度。

以下是 cookie 名稱的範例：

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>WinRM IIS 擴充功能裝載模型中的 HTTP 重新導向

WinRM 2.0 可處理 HTTP 重新導向。 建議所有重新導向都使用安全通訊端層 (SSL) ，而且所有應用程式會在建立新的會話之前驗證重新導向的 URI。

## <a name="winrm-service-hosting-model"></a>WinRM 服務裝載模型

以 WinRM 服務為基礎的模型會在 HTTP.sys 上執行。 WinRM 服務是向 WinRM 用戶端處理要求的網路面向服務。 服務會判斷要求是否會路由至在主要服務中執行的外掛程式，或是透過執行協力廠商外掛程式的主機進行路由傳送。 此模型適用于受管理節點上的負載偏低的案例。 此外，此模型適用于 IIS 裝載不是選項的情況。 如需詳細資訊，請參閱 [WinRM 服務外掛程式](wsman-service-plug-in-configuration.md)設定。

 

 




