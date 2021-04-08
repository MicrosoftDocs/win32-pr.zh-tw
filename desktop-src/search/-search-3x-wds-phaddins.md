---
description: 本節提供執行、擴充和測試通訊協定處理常式所需的概念資訊。
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: 開發 Windows Search 的通訊協定處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689891"
---
# <a name="developing-protocol-handlers-for-windows-search"></a>開發 Windows Search 的通訊協定處理常式

本節提供執行、擴充和測試通訊協定處理常式所需的概念資訊。

-   [瞭解通訊協定處理常式](-search-3x-wds-extidx-prot-implementing.md)
-   [通知索引變更](-search-3x-wds-notifyingofchanges.md)
-   [新增圖示和快顯功能表](-search-3x-wds-ph-ui-extensions.md)
-   [程式碼範例：通訊協定處理常式的 Shell 擴充功能](-search-3x-wds-ph-ui-samplecode.md)
-   [安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)
-   [建立通訊協定處理常式的搜尋連接器](-search-3x-wds-ph-search-connector.md)
-   [偵錯工具通訊協定處理常式](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a>其他資源

如需編制索引的概念背景，請參閱下列主題：

-   如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
-   若要擴充 Windows Search 以編制新檔案格式和資料存放區的內容和屬性的索引，請參閱 [擴充索引](-search-3x-wds-extidx-overview.md)。
-   如需目錄管理員和目錄搜尋管理員 (CSM) 的總覽，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 以及 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。

如需檔案類型和處理常式的概念背景，請參閱下列主題：

-   若要使用檔案類型處理常式來擴充 Shell，請參閱 [建立 Shell 擴充處理常式](../shell/handlers.md)。
-   如需篩選處理常式的概念資訊，請參閱 [開發篩選處理常式](-search-ifilter-conceptual.md)。
-   如需建立處理常式的相關資訊，請參閱檔案 [關聯簡介](../shell/fa-intro.md)、 [註冊 shell 擴充](../shell/reg-shell-exts.md)功能、 [建立 shell 延伸模組處理常式](../shell/handlers.md)、操作 [功能表](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))和 [預覽處理常式](../shell/preview-handlers.md)。

如需相關技術及如何執行資料存放區的背景資訊，請參閱下列主題：

-   Windows Search 通訊協定處理常式會使用與 SharePoint Server 類似的設計規格，而且通常可以交換使用。 如需詳細資訊，請參閱 [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs)。
-   在 Windows 7 和更新版本中，SharePoint Search Server 2008 和 MOSS 2007 SP2 也支援同盟搜尋。 如需有關使用 Office SharePoint Server 2007 部署同盟搜尋和搜尋伺服器2008的詳細資訊，請參閱[聯合搜尋 \[ 搜尋伺服器 2008 \] ](/previous-versions/office/bb931109(v=office.14))。
-   若要建立 Shell 資料存放區，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

如需程式碼範例，請參閱下列入口網站頁面：

-   如需搜尋程式碼範例，請參閱 [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)。
-   針對 Shell 程式碼範例，請參閱 [SHELL SDK 範例](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85))。

 

 
