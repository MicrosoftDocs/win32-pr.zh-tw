---
title: 啟動應用程式
description: 啟動應用程式
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- 啟動應用程式
- 背景工作
- 執行金鑰
- RunOnce
- 開機檔案夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc2dc2a73a08c3aebd265c209b407646e50a6cb1b7cba630884cf719330b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815048"
---
# <a name="startup-apps"></a>啟動應用程式

## <a name="platform"></a>平台

**用戶端** Windows 8     


## <a name="description"></a>描述

Windows 的其中一個 big，就是能夠從傳統的桌上型電腦和膝上型電腦到低電源的平板電腦，來照亮各種外型規格。 為了確保我們的相互客戶在使用 Windows 所選擇的任何外型規格上有絕佳的體驗，需要解決的兩個關鍵成功計量會提高電池壽命和絕佳的電腦回應能力。 為了達成這些目的，已在 Windows 的多個領域進行改進，包括處理生命週期、睡眠狀態和啟動應用程式， (應用程式在電腦開機) 之後自動啟動。 本主題將重點放在 Windows 裝置上啟動應用程式的一些影響，並為開發人員提供 (ISV/IHV) 的指引，以及 oem 重新思考啟動應用程式的使用模式，以改善我們的共同客戶的電池壽命和回應能力。 它也會說明 Windows 中的變更，讓使用者能夠決定實際要執行的啟動應用程式。

Windows商店應用程式的設計是為了遵守新的電池耗用量和回應性標準，Windows 藉由暫停和/或終止它們來管理其生命週期。 不過，針對先前的 Windows 版本所設計的桌面應用程式不一定是設計來維持電池壽命或對使用者活動敏感，而且可能會影響系統回應性 (例如，當應用程式傳送一般1秒的心跳來檢查是否有更新時，或預先配置記憶體，以在稍後) 時預先配置記憶體。 如此一來，如果使用者購買的 Windows tablet PC 的電池壽命很長，且待命時間很長，但卻發現平板電腦的電池壽命無法達到這些目標。 此外，由於啟動應用程式會在背景執行，因此在系統上執行的應用程式數目可能會比使用者察覺的還多，而且會影響系統的回應性。 啟動應用程式會分類為包含利用這些機制來啟動的應用程式：

-   執行 (HKLM、HKCU、wow64 節點所包含的登錄機碼) 
-   RunOnce 登錄機碼
-   每個使用者和公用位置的 [開始] 功能表下的 [啟動] 資料夾

已將新功能新增至 Windows，以確保終端使用者一律能夠控制其系統上執行的應用程式。 工作管理員中的 [啟動] 索引標籤會顯示啟動應用程式的清單，以及可讓使用者停用啟動應用程式的控制項。 為了協助使用者判斷要停用的內容，工作管理員會顯示每個啟動應用程式影響的量值。 系統會根據應用程式在啟動時的 CPU 和磁片使用量來評估影響。 影響值取決於套用下列準則：

-   **高影響力**   在啟動時使用超過1秒 CPU 時間或超過 3 MB 磁片 i/o 的應用程式
-   **中度影響**   使用 300 ms-1000 ms CPU 時間或 300 KB-3 MB 磁片 i/o 的應用程式
-   **低影響**   使用小於 300 ms CPU 時間和小於 300 KB 磁片 i/o 的應用程式

Microsoft 提供的工具可協助應用程式開發人員評估、分析和採取步驟，以降低啟動的影響並改善使用者體驗。 評定及部署套件提供執行開機效能評估的能力，以及測量在啟動時執行的應用程式所造成的影響。 評量結果包含詳細的分析和補救資訊（適用時），適用于 Windows 啟動的最受影響的元件。 應用程式開發人員可以使用 Windows Performance Analyzer 來執行深入分析，以找出效能影響的根本原因，並提升 Windows 的啟動效能。 從[這裡](/previous-versions/windows/hh825494(v=win.10))安裝 Windows ADK。

## <a name="guidance"></a>指引

啟動應用程式涵蓋多個類別，如下表所述。 一組適用于開發人員的建議會對應至啟動應用程式的類別，以符合上述的 Windows 功能變更。



啟動應用程式類別

描述

建議

**更新程式**

監視和更新線上更新的使用者

**維護工作**

> [!Note]  
> 所有更新都應該是維護工作，不需要任何 UI 互動需求。 應用程式應該直接以安靜的方式更新，並在失敗時回復

<br/>

$ {ROWSPAN2} $**硬體協助**$ {移除} $  

替代存取點

提供可透過 Windows 中其他存取點存取 Windows 功能和應用程式的存取權

**移除**

> [!Note]  
> 關鍵是減少存在於 Windows 中的重複功能

<br/>

通告

為使用者提供有關其裝置的通知

**移除**

> [!Note]  
> Windows 為使用者提供其裝置的通知

<br/>

**預先啟動器**

在使用者登入期間，應用程式所需的一些初步活動會卸載至啟動應用程式

**移除**

> [!Note]  
> Windows 8 已針對應用程式啟動的快速體驗進行優化。

<br/>

$ {ROWSPAN4} $**Utility**$ {REMOVE} $  

電腦同步

跨多個系統提供同步處理功能

Beta 版中的 **啟動** (可能的更新) 

備份 & 復原

儲存及還原檔案、設定或整個系統狀態的進入點

**Windows用來與使用者互動的商店應用程式**

遙測

收集和傳送使用者體驗和環境的相關資訊

**維護工作**

電腦監視

提供重複的現有收件匣功能的未經要求系統狀態監視和通知

**移除**

> [!Note]  
> 關鍵是減少存在於 Windows 中的重複功能

<br/>

$ {ROWSPAN2} $**Security**$ {REMOVE} $  

家長監護 & 篩選

強制執行為網際網路存取和使用所建立的規則和限制

**啟動**

設定和管理

允許使用者控制系統安全性監視的診斷和修復選項，以通知使用者發現和安全性動作

**Windows用來與使用者互動的商店應用程式**

**通訊 & 網際網路** (IM & VoIP) 

傳送和接收訊息和呼叫

**WindowsStore 應用程式**

**音樂 & MP3**

播放、儲存和管理音樂

**WindowsStore 應用程式**

**相片 & 影片**

偵測、錄製、轉譯、儲存及管理相片和影片

**WindowsStore 應用程式**

**電腦遊戲**

跨不同網域啟動遊戲

**WindowsStore 應用程式**

**銷售 & 公告**

特別注意可供購買的商品和服務

**移除**



 

> [!Note]  
> 協助工具應用程式指導方針是與 Isv 的個別直接合作所涵蓋。 如需詳細資訊，請參閱輕鬆存取的程式 [*設計*](../winauto/ease-of-access---assistive-technology-registration.md) 。

 

**Windows 市集應用程式**

WindowsStore apps 藉由引進 Windows 空間與新的座標來增強使用者體驗：新的應用程式模型、新的使用者介面，以及 Windows 存放區。 這些語言和 presentation framework 選項適用于開發 Windows Store 應用程式：

-   HTML/JavaScript/CSS
-   XAML/C#
-   XAML/C + +

您可以在[Windows 開發人員中心](https://msdn.microsoft.com/windows/apps/)取得開發 Windows Store 應用程式的匯總資訊。

範例：

-   [開發 Windows 店的遊戲](/previous-versions/windows/apps/hh452744(v=win.10))
-   [開發使用媒體的 Windows Store 應用程式](/previous-versions/windows/apps/hh465132(v=win.10))

**自動維護工作**

定期背景活動應設計為自動維護工作。 這些會在系統閒置時間排程，以增加 Windows 電腦的回應能力和能源效率。 您可以使用桌面 SDK，在安裝期間由傳統型應用程式建立和設定維護工作。 如需詳細資訊，請參閱下面的自動維護主題。

## <a name="resources"></a>資源

-   [協助工具指導方針](../winauto/ease-of-access---assistive-technology-registration.md)
-   [Windows 開發人員中心](https://msdn.microsoft.com/windows/apps/)
-   [Windows ADK](/previous-versions/windows/hh825494(v=win.10))

 

