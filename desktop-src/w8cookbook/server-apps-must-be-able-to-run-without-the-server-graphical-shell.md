---
title: 伺服器圖形化 Shell 限制
description: 伺服器應用程式必須能夠在沒有伺服器圖形化 Shell 的情況下執行
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1742b87d0cb4ece4ac05b38b0ac2644967eee256931df5dfc8ec838574db33ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773181"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>伺服器應用程式必須能夠在沒有伺服器圖形化 Shell 的情況下執行

## <a name="platform"></a>平台

**伺服器**– Windows Server 2012 

## <a name="description"></a>描述

伺服器圖形化介面（包含 Windows 檔案總管和 Internet Explorer 的功能）預設會安裝在 Windows Server 2012 的「Server 含 GUI」安裝中。 您可以卸載伺服器圖形化介面功能，以降低潛在的服務和效能，進而限制伺服器可能產生的重新開機次數，同時仍允許在伺服器本機上執行管理工具。

當系統管理員卸載伺服器圖形化介面之後，伺服器會在基本伺服器介面設定中：

![伺服器圖形化 shell 介面設定](images/minimalserverinterface.png)

接著，系統管理員可以選擇在最基本的伺服器介面設定中執行 (其中包含一組本機管理工具) （預設值），而不是在伺服器上設定 GUI。 這可允許本機監視和管理，同時降低服務的資源使用量和頻率。

系統管理員可以在稍後需要它的功能時，重新安裝伺服器圖形化 Shell。  (系統管理員也可以從 Server Core 安裝開始，並使用功能隨選功能將「建立」至基本伺服器介面設定。 ) 

伺服器應用程式必須能夠在最基本的伺服器介面設定中執行，才能利用降低的資源使用率和服務使用量。 這項功能的達成方式是讓系統管理員選擇不安裝需要伺服器圖形化 Shell 的部分應用程式，或偵測伺服器圖形化 Shell 的存在，並停用應用程式的某些層面。

基本伺服器介面具有降低的資源和服務使用量，因為伺服器圖形化介面中包含的許多 Api 和二進位檔無法在此設定中使用。 在適當的情況下，伺服器應用程式也應該允許遠端系統管理 (最好透過另一個 Windows 伺服器或 Windows 用戶端安裝 Windows PowerShell 遠端) 。 這可讓您更妥善地集中管理基本伺服器介面設定中的一部或多部電腦，或較低使用量設定（例如 Server Core）中的電腦。

## <a name="manifestation"></a>表現

如果應用程式需要基本伺服器介面設定中未提供的任何 Api 或二進位檔，可能不會在畫面上正確顯示，也可能無法使用。

## <a name="mitigation"></a>降低

伺服器應用程式開發人員應該找出需要任何移除的 Api 或二進位檔的應用程式部分，並包含伺服器系統管理員的資訊，以識別使用基本伺服器介面時無法正確執行的應用程式元件。 如果應用程式的這些部分可以選擇性地安裝或不是產品功能的絕對必要元件，則仍可在基本伺服器介面設定下安裝並執行應用程式。

如果應用程式完全無法在沒有伺服器圖形化介面的情況下使用，則應記錄這項限制，並指示伺服器系統管理員安裝伺服器圖形化介面。  (如果新增至 Server Core 安裝，這可能需要使用隨選功能來新增功能。 ) 此外，應用程式應該在啟動時檢查是否有所有必要的檔案可供使用，因為伺服器圖形化介面可以在安裝應用程式之前或之後卸載。

## <a name="solution"></a>解決方案

依賴最小的一組相依性，以及模組化應用程式，讓核心應用程式功能可以運作，而不需要安裝更多重量級使用者介面元件。 開發不需要任何已移除之 Api 或二進位檔的應用程式，而是改為依賴基本伺服器介面或 Server Core 內所含的功能。 這樣可減少維護需求，同時提高效能和使用者滿意度。

當伺服器圖形化介面可用時，應用程式的某些部分可能會新增重要的功能，應用程式開發人員可以：

-   允許這些額外的功能，讓您可以選擇性地安裝使用伺服器圖形化介面，以便在基本伺服器介面設定上從安裝中省略
-   偵測伺服器圖形化 Shell 是否存在，並調整應用程式行為

應用程式開發人員也應該確保伺服器應用程式能夠在適當的情況下遠端系統管理。

## <a name="detecting-minimal-server-interface-and-server-core"></a>偵測基本伺服器介面和 Server Core

Windows伺服器將會為安裝的每個伺服器層級安裝對應的登錄值。 您可以查詢這些機碼是否存在，以判斷是否已安裝並啟用伺服器圖形化 Shell 或基本伺服器介面功能。

HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels：



|   &nbsp;         | Server Core | 基本伺服器介面 | 伺服器圖形化 Shell |
|------------------|-------------|--------------------------|------------------------|
| ServerCore = 1     | X           | X                        | X                      |
| 伺服器-GuiMgmt = 1 |             | X                        | X                      |
| ServerGuiShell = 1 |             |                          | X                      |



 

上表中的 "X" 代表安裝對應的功能時，將會出現登錄機碼。

請注意，這些伺服器層級是加法。如果已安裝伺服器圖形化介面，則為基本伺服器介面和 Server Core。 在此情況下，這兩個登錄機碼都將存在。

## <a name="tests"></a>測試

檢查您的應用程式程式碼中是否有使用任何已移除 Api 和二進位檔的需求。 從「核心應用程式」二進位檔移除任何這些實例之後，請在不包含伺服器圖形化介面的環境中測試您的應用程式。 進程監視器等工具可能有助於解決此情況。

如果您無法完全停止使用這些 Api 和二進位檔，請確定您的應用程式在基本伺服器介面或 Server Core 上執行時，正常地失敗。

## <a name="resources"></a>資源

-   [MSDN 上的現有伺服器核心檔](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 