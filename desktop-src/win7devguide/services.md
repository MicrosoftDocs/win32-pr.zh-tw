---
title: '服務 (Windows 7 開發人員指南) '
description: Windows 7 提供功能強大、高度可擴充且可管理的平臺，可用於建立及整合未來的 web 服務和應用程式。Windows 7 提供 managed 程式碼 api 和原生 api 來建立和執行 web 服務。
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42fe2a59a69efe7fb34bb4a09c58b2ee03f00ac8b8129c36b1ef5f0f61971c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203861"
---
# <a name="services-windows-7-developer-guide"></a>服務 (Windows 7 開發人員指南) 

Windows 7 提供功能強大、高度可擴充且可管理的平臺，可用於建立及整合未來的 web 服務和應用程式。

Windows 7 提供 managed 程式碼 api 和原生 api 來建立和執行 web 服務。 新的擴充性層級上建有各種新功能，可讓開發人員擴充所有 Api、原生程式碼或 Microsoft .NET Framework 內的應用程式。

Windows 7 還可讓開發人員利用更佳的快取和搜尋功能。 藉由這些增強功能，開發人員可以更快地取出資料，並減少網路頻寬使用量。

## <a name="windows-web-services"></a>WindowsWeb 服務

利用[Windows Web 服務](/windows/desktop/wsw/portal)，您可以建立可與本機電腦或遠端 Web 服務輕鬆通訊的應用程式。 WindowsWeb 服務是 SOAP 的原生程式碼執行，藉由支援一組廣泛的 web 服務 (*WS*) 系列的通訊協定，提供核心網路通訊。 WindowsWeb 服務是對 [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*wcf*、managed 程式碼的 web 服務) ，並提供高效能的 *wcf* 功能子集。 WindowsWeb 服務提供下列優點：

-   在 Windows 用戶端和伺服器中，以 C/c + + 建立機器碼 web 服務的能力。
-   與[Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) services 的廣泛整合。
-   能夠以最短的啟動時間來建立 web 服務。
-   能夠 *根據核心的* 通訊協定系列和 *W3C* 標準來建立服務。
-   在資源受限的環境中使用 web 服務的能力。

如需詳細資訊，請參閱[Windows web 服務 api](../wsw/portal.md) ，以及[使用 Windows web 服務 api 來執行 web 服務](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI)。

## <a name="distributed-routing-table"></a>分散式路由表

Windows 7 可讓您更輕鬆地建立複雜的點對點應用程式，例如分散式檔案系統和使用[分散式路由表](/windows/desktop/P2PSdk/distributed-routing-table-api-reference)的內容散發網路。 分散式路由表提供安全且可擴充的機制，可在對等系統中發佈和搜尋金鑰。 您可以使用它來建立分散式雜湊表，並針對重迭網路建立拓撲。  (參閱 [分散式路由資料表 API](../p2psdk/distributed-routing-table-api.md)。 ) 

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 可改善中央伺服器與分公司電腦之間的應用程式回應性。 在現今的網路中，中央伺服器與分公司之間的通訊通常是擁塞的，這會導致分公司的應用程式效能變慢。 使用 Windows BranchCache 時，用戶端可以從其本身分支中已下載資料的其他用戶端取出資料，而不需要透過遠端伺服器取得資料。 如此一來，廣域網路 (WAN) 連結流量降低，而應用程式的回應能力也會提高。 快取會保留分支中用戶端所要求的所有內容複本，並確保只有由內容伺服器授權的用戶端可以存取要求的資料，同時保留資料的端對端加密。

WindowsBranchCache 已與 HTTP 和伺服器訊息區整合 (SMB) 。 如果應用程式使用上述任一種通訊協定的 WindowsAPIs，Windows BranchCache 可協助提高此應用程式在 Windows 7 的效能，而不需要對其進行任何變更。

如果您的應用程式透過 WAN 連結從伺服器多次抓取相同的資料，而且不會使用 Windows 7 自動優化，則您可以輕鬆地使用 Windows BranchCacheAPIs 來優化您的應用程式，以便在 Windows 7 上更快速地運作，並滿足您的分支使用者。

這些新功能可協助降低 WAN 流量和延遲，同時確保符合安全性規定。  (請參閱 [對等散發](../p2psdk/peer-distribution.md)。 ) 

 

 
