---
description: 伺服器 Hyper-v
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: 伺服器 Hyper-v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cab162355e298cbc21c1c43d8b1a0d16b8c23f958e06c7fb28a8ecb6e3309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328708"
---
# <a name="server-hyper-v"></a>伺服器 Hyper-v

## <a name="platforms"></a>平台

 **客戶** 端-Windows XP \| Windows Vista \| Windows 7  
**伺服器**-Windows server 2008 \| Windows server 2008 R2  

## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>描述

伺服器虛擬化可讓您在單一實體電腦上執行多個作業系統，作為虛擬機器 (Vm) ，可讓您將使用量過低之伺服器機器的工作負載合併到較少的充分利用電腦上。 Windows 7 包含 Windows Server 2008 版本的數項增強功能：

-   **即時移轉：** 在 Windows Server 2008 中，我們有快速的遷移。 透過即時移轉，我們改善了遷移速度和儲存彈性。
-   **邏輯處理器支援：** 我們已將邏輯主機處理器從16LP 增加至64LP。
-   **儲存體熱新增：** 現在您可以將額外的 VHD 或傳遞磁片新增至執行中的虛擬機器，而不需要關閉虛擬機器。
-   **新硬體支援：** 我們已新增新處理器所包含的技術支援，以及即將上市的網路卡，包括第二層轉譯 (SLAT) 、TCP 卸載 (煙囪) 和 VMdQ。
-   **終端機服務虛擬化 (TSv) ：** 適用于 Hyper-v 的集中式桌面解決方案。

## <a name="manifestation-of-impact"></a>影響的表現

-   **即時移轉：** 您可能需要變更您的儲存系統架構，才能充分利用此技術。 雖然可能不需要這些變更，但您可以選擇執行這些變更，以充分利用這些優勢。 您可能需要一個管理應用程式來協調即時移轉。
-   **邏輯處理器支援：** 從 Windows Server 2008 遷移至 Windows server 2008 R2 時，此功能不會影響客戶或 isv。
-   **儲存體熱新增：** 從 Windows Server 2008 遷移至 Windows server 2008 R2 時，此功能不會影響客戶或 isv。 設定虛擬機器設定的管理應用程式可能需要更新，才能管理這項新功能。
-   **新硬體支援：** 這些功能僅適用于推出到市場的新硬體。 因為它不支援這些功能的內建支援，所以從 Windows server 2008 遷移至 Windows server 2008 R2 的實體伺服器不太可能會受到影響。 如果要遷移的伺服器上有這些功能，則不會預期直接變更。
-   **終端機服務虛擬化：** 從 Windows Server 2008 遷移至 Windows server 2008 R2 時，此功能不會影響客戶或 isv。 利用終端機服務 (TS) 的應用程式可能會受到影響。 這項功能會直接與 TS 整合，因此設定 TS 的應用程式可能需要更新，才能管理這項新功能。

## <a name="mitigation"></a>降低

-   **即時移轉：** 針對具有儲存體系統設計的最佳作法和建議，為終端使用者提供規範性指導方針。 您必須通知終端使用者關於選項和建議。

## <a name="leveraging-capabilitities"></a>利用 Capabilitities

-   **即時移轉：** 這項功能可啟用動態 IT 環境。 虛擬化管理應用程式開發人員必須修改其應用程式，以利用這項新功能。 Microsoft 會公開提供 WMI 介面，讓開發人員能夠整合應用程式與這項功能。
-   **終端機服務虛擬化：** 這項功能可提供新的虛擬化案例。 利用終端機服務 (TS) 的應用程式可能會受到影響。 這項功能會直接與 TS 整合，因此設定 TS 的應用程式可能需要更新，才能管理這項新功能。

## <a name="links-to-other-resources"></a>其他資源的連結

[Hyper-v v1 的 WMI 管理介面](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)。 雖然此內容大多適用于 hyper-v 的 v2，但是具有 v2 特定資訊的更新版本應可在更接近 Windows 7 啟動時使用。

 

 
