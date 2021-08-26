---
description: On/Off 效能的最佳作法
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: On/Off 效能的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef9e10b0a6fc82be138951d45f811ce1ccf0dbe2222b620cf73d0c272570c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031048"
---
# <a name="best-practices-for-onoff-performance"></a>On/Off 效能的最佳作法

## <a name="platform"></a>平台

**用戶端-** Windows Vista \| Windows 7  
**伺服器-** Windows server 2008 \| Windows server 2008 R2  

## <a name="description"></a>描述

系統電源狀態 (或 S 狀態) （如 Advanced Computer 電源介面 (ACPI) 規格中所定義）堆疊稱為「開啟/關閉」狀態，因為最常見的 S 狀態轉換是電腦開啟和關閉。 在執行 Windows Vista 或 Windows 7 的系統上，不同的開啟/關閉狀態轉換是開機、睡眠 (acpi S3) 、休眠 (acpi S4) 和關機。

在這些開啟/關閉轉換期間的良好效能不僅能改善電腦的認知品質，也會大幅影響每日電腦使用模式和系統可靠性。 客戶可能會因為開機或關機時間太長的系統而感到挫折。 具有冗長睡眠和休眠轉換的行動系統可能會不必要地耗盡電池壽命。 較長的關機時間也會對行動系統的可靠性造成負面影響。 例如，它們會增加非預期電源減少的風險。

系統擴充功能（例如驅動程式、應用程式和服務）可能會對轉換時間有顯著的影響。 本節將討論應用程式和服務開發人員可以遵循的一些最佳作法，以避免開機、待命和關機期間的延遲，並確保開機後和後續恢復的使用者體驗。 如需如何使用 Windows 效能工具組找出/關閉效能問題的詳細資訊，並針對您的應用程式或服務執行下列建議，請參閱「其他資源的連結」一節中的白皮書。

## <a name="best-practices"></a>最佳做法

-   使用 Windows 效能工具組，在所有的開啟/關閉轉換期間測量效能。
-   以受控制的方式執行測試，並針對有效的基準進行比較：
    -   以最少的系統擴充功能在系統上取得基準量測
    -   一次新增一個應用程式和服務
    -   測試處於開啟/關閉轉換時間的無法接受的回歸
-   避免針對重要開機路徑上的應用程式使用 managed 程式碼。
-   確定所有應用程式都能快速回應 (WM \_ QUERYENDSESSION 和 wm \_ ENDSESSION 訊息) 的關機通知。
-   藉由將 CPU、磁片和網路活動降至最低，以回應關機通知，減少服務和應用程式關閉路徑的延遲。
-   避免處理暫停通知 (WM \_ POWERBROADCAST 訊息) 的延遲。
-   快速回應以繼續事件，並將恢復後的 CPU、磁片和網路使用量降至最低。
-   減少開機後的應用程式資源耗用量。
-   請勿在每次開機時從 RunOnce 索引鍵啟動應用程式。
-   將所有不必要的服務轉換為需求開始或觸發程式開始，以便讓系統資源在開機期間可供使用。
-   避免使用載入順序群組來表示服務相依性。
-   請確定所有執行中的服務都在開機期間儘快回報此狀態，以避免封鎖服務控制管理員 (SCM) 。
-   避免在啟動路徑上使用服務的 managed 程式碼。
-   除非絕對必要，否則不允許服務選擇接收 (服務 \_ 控制 \_ PRESHUTDOWN 和服務 \_ 控制 \_ 關閉控制代碼的預先關閉和關閉通知) 。
-   確定已選擇接收關機通知的所有服務，都能快速回應 SCM。
-   確認除非絕對必要，否則服務不會選擇接收暫停通知。
-   確定所有服務都能快速回應以繼續事件，並將恢復後的 CPU、磁片和網路使用量降至最低。

## <a name="links-to-other-resources"></a>其他資源的連結

-   -   [Windows開啟/關閉轉換解決方案指南](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Windows Vista 的開啟/關閉轉換效能分析](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Windows效能分析](https://msdn.microsoft.com/performance/default.aspx)
-   [WindowsMSDN 上的效能工具組檔](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Windows效能分析論壇](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [MSDN 上的 Windows 事件追蹤](../etw/event-tracing-portal.md)

 

 
