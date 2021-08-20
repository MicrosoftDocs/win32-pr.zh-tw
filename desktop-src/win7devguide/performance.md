---
title: '效能 (Windows 7 開發人員指南) '
description: Windows 7 可將硬體能源效率和擴充性最大化，同時維持高效能。
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5636b6cb7178fa660381196f44b811c905478c1bcd31e0580ea631955b13c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032048"
---
# <a name="performance-windows-7-developer-guide"></a>效能 (Windows 7 開發人員指南) 

Windows 7 可將硬體能源效率和擴充性最大化，同時維持高效能。 透過減少背景活動，以及啟動系統服務觸發程式的新支援，來改善能源效率。 Windows 7 也提供 Windows 核心的增強功能，可讓應用程式和服務在各平臺之間有效率地調整規模。 在 Windows 7 和 Windows Vista 中，許多功能和 api 的效能已獲得改善。 例如，伺服器上的驅動程式效能是透過新的使用者模式和核心模式拓撲 Api 進行優化。 圖形轉譯的速度更平滑且更快速。 協助工具效能的速度也會比之前快很多。

## <a name="building-power-efficient-applications"></a>建立 Power-Efficient 應用程式

建立節能的應用程式，利用最新的電源管理技術，是開發人員目前面臨的重大挑戰。 一般來說，處理器和裝置製造商會在其最新的供應專案經過測量和基準測試時，獲得最新的注意力。 不過，單一應用程式很容易就能防止最新一代的硬體實現其能源效率的潛力。 例如，增加平臺計時器解析度的單一應用程式可能會將電池壽命減少10%。

使用電池電力的擴充作業和能源效率技術，是現今開發人員的關鍵需求。 Windows 7 可大幅減少作業系統執行的活動數目，以防止使用省電模式。 它也支援啟動系統服務的觸發程式，以讓處理器更頻繁地變成閒置狀態，並持續維持閒置狀態，以降低耗電量。 此外，Windows 7 還會利用最新的節能硬體，包括網路介面卡、存放裝置和圖形卡。

Windows 7 提供基礎結構和工具，可讓開發人員輕鬆地判斷其應用程式的能源衝擊。 一組事件回呼可讓應用程式在系統使用電池電源時減少其活動，並在系統處於 *AC* 電源時自動擴大。 針對牽涉到背景程式或服務的應用程式，Windows 7 提供新的基礎結構，以在最適當的情況下自動啟用背景工作，以將能源效率最大化。  (請參閱 Windows 7 的[WHDC 效能核心](https://www.microsoft.com/whdc/system/sysperf/default.mspx)和[電源管理的總覽](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf)。 ) 

## <a name="service-control-manager"></a>服務控制管理員

Windows 的 7Service Control Manager (SCM) 已經過擴充，因此當系統發生特定的系統事件或觸發程式時，就可以自動啟動和停止服務。 觸發程式啟動功能可移除在電腦啟動時自動啟動服務的需求，然後輪詢或等候事件發生，例如裝置抵達。 服務的一般觸發程式事件包括：

-   裝置類別介面抵達：只有在有特定類型的裝置存在或連接到系統時，才會啟動服務。
-   網域加入：只有當系統加入 Windows 網域時，才會啟動服務。
-   群組原則變更：當系統上的群組原則重新整理時，就會自動啟動服務。
-   IP 位址抵達：只有當系統連線到網路時，才會啟動服務。

軟體發展人員可以使用 Windows 7 的預先定義觸發程式類型，以及啟用觸發程式啟動功能的設定選項。 Windows 7SCM 會公開一組新的 api，讓服務註冊特定的自訂觸發程式事件。  (請參閱 [服務控制管理員](../services/service-control-manager.md)。 ) 

## <a name="windows-troubleshooting-platform"></a>Windows疑難排解平臺

Windows 7 提供完整且可延伸的疑難排解平臺，它使用以 PowerShell 為基礎的機制來進行疑難排解並解決問題。 疑難排解平臺的主要元件包括疑難排解套件、疑難排解引擎和疑難排解 wizard。 疑難排解套件是 PowerShell 腳本和相關中繼資料的集合。 疑難排解引擎會啟動 PowerShell 執行時間來執行疑難排解套件，並公開一組介面來控制疑難排解套件的執行。

疑難排解 wizard 可提供一致的疑難排解套件體驗，與疑難排解引擎進行通訊，以疑難排解並解決疑難排解套件中所指定的問題。 您也可以透過一組 PowerShell *commandlet* 來控制疑難排解套件的執行。

疑難排解平臺與 Windows 7PC 解決方案中心緊密整合，讓其他應用程式能夠以與電腦管理擬訂規則一部分類似的方式來執行診斷。 IT 專業人員可透過 *群組原則* 在企業內使用來設定疑難排解平臺，也可以使用 Windows 疑難排解工具組，讓開發人員撰寫疑難排解套件。  (參閱[Windows 疑難排解 Platform](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal)。 ) 

![針對平臺 ui 進行疑難排解](images/windows7-devguide-troubleshoot.jpg)

疑難排解平臺與 Windows 7PC 解決方案中心緊密整合

 

 
