---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: 能源效率的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975320"
---
# <a name="best-practices-for-energy-efficiency"></a>能源效率的最佳作法

## <a name="platform"></a>平台

 **用戶端** – windows XP \| windows Vista \| windows 7  

## <a name="description"></a>Description

以 Windows 為基礎的膝上型電腦必須符合能源效率法規需求，例如美國環境保護機構的 (EPA) 能源之星方案。 此外，問卷已顯示較長的電池壽命，會持續成為取用者最需要和膝上型電腦所需的時間。 為了滿足消費者的需求，Windows 膝上型電腦必須持續前進到下欄區域：

-   所有使用案例的能源效率，包括閒置、生產力工作負載、DVD 和媒體播放，以及產業基準測試
-   行動電腦電池壽命—適用于硬體平臺和 Windows

Windows 平臺高度可靠，可提供快速的開啟和關閉效能。 不過，隨行動電腦系統提供的擴充功能（例如服務、系統匣 applet、驅動程式和其他軟體）可能會大幅影響效能、可靠性和能源效率。

能源效率是一個複雜的問題，其中的因素會受到影響並影響電腦生態系統的所有元素。 跨多個案例的小型增強功能可以提升能源效率，但是單一效能不良的應用程式、裝置或系統功能可能會大幅增加能源耗用量。

硬體和裝置形成能源效率的基礎。 不過，應用程式和服務軟體也必須有效率，才能讓系統達到最佳的電池壽命。 系統上的每個軟體元件（包括作業系統和附加價值的應用程式和服務）都必須符合基本的效率指導方針。 單一不正常的應用程式或服務可以消除最新處理器、裝置或平臺硬體達成的任何能源效益。 如需有關電池壽命和能源效率的詳細資訊，請參閱 [電池壽命解決方案指南](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)。

影響行動電腦電池壽命的原則問題和元件包括：

**電池特性**

-   電池容量的大小、類型和品質會影響電池壽命
-   電池愈大，電源供應器愈大
-   較大的電池成本更高，使用者偏好較輕的系統

**硬體元件**

-   硬體可進入較低電源狀態的頻率和深度
-   較低電源狀態的硬體支援
-   能源效率的驅動程式優化

**作業系統–導向的電源管理**

-   負載和閒置時的 Windows 程式碼效率
-   具有 Windows 導向電源管理的所有元件合作層級
-   適當的作業系統設定，以透過電源原則設定優化電源管理

**應用程式軟體和服務**

-   負載和閒置時的應用程式、驅動程式和服務的效率
-   應用程式與 Windows 的合作等級-導向的電源管理
-   要進入低電源閒置狀態的系統或裝置的軟體額度

單一應用程式或服務元件可能會讓系統無法達到最佳的電池壽命。 雖然 Windows 提供許多電源設定選項，但在許多系統上預先安裝的軟體或電源原則設定都不會針對主機硬體平臺進行優化。

評估預先安裝軟體之電池生命影響的常見方法，是將系統的電源耗用量與 windows 的全新安裝（包括加值軟體和服務的 Windows 安裝）進行比較。 雖然全新安裝不代表 Oem 傳送給客戶的一般平臺，但耗電量比較可讓您深入瞭解預先安裝軟體的能源效率。

## <a name="best-practices"></a>最佳做法

若要確保您的應用程式已在 Windows 平臺上優化，請在設計應用程式或服務時遵循下列最佳作法：

-   **避免使用高解析度的定期計時器**

<dl> 使用高解析度定期計時器 (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **投資效能優化**

<dl> 每個效能優化都是電池壽命優化。 減少必要的資源，例如使用較少的處理器時間或批次處理/叢集磁片讀取，可讓系統硬體變成閒置並進入低電源模式。  
</dl>

-   **調整為使用者電源原則**

<dl> Windows Vista 和更新版本可讓使用者輕鬆地選擇系統的整體省電或效能行為。 您的應用程式應該回應電源原則的變更，並據此減少資源使用量或提升效能。 例如，應用程式應該在使用者選取省電電源計劃時停用背景活動，例如編制索引或掃描系統。  
</dl>

-   **當系統使用電池電源時減少資源使用量**

<dl> 當系統使用電池電源時，您的應用程式應該會降低其資源使用量（例如背景更新頻率）。  
</dl>

-   **當關閉時，不要轉譯為顯示**

<dl> 系統顯示器可能會關閉電源節約。 當顯示器關閉時，您的應用程式不應該執行不必要的圖形轉譯，因為這會浪費系統資源和電源。  
</dl>

-   **避免在緊密迴圈中進行輪詢和旋轉**

<dl> 大量處理器使用量可降低處理器電源管理技術（例如處理器閒置狀態和處理器效能狀態）的效率。  
</dl>

-   **請勿防止系統關閉顯示器或閒置進入睡眠狀態**

<dl> 您的應用程式應該對 SetThreadExecutionState API 提出明智的電源要求。 只有當重要作業必須延遲系統關閉顯示器的電源或自動進入睡眠狀態時，系統才會提出這些要求。  
</dl>

-   **回應常見的電源管理事件**

<dl> 您的應用程式應該註冊並回應常見的電源管理事件，例如系統電源來源變更和顯示器的電源開啟和關閉通知。  
</dl>

-   **請勿預設啟用 debug 記錄;改為使用 Windows 事件追蹤**

<dl> 週期性 debug 記錄可能會導致磁片無法向下微調。  
</dl>

## <a name="links-to-other-resources"></a>其他資源的連結

-   [電池壽命解決方案指南](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [能源效益入口網站](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



