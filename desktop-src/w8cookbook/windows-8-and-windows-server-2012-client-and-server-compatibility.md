---
title: 用戶端與伺服器相容性-Windows 8
description: Windows 8 和 Windows Server 2012 用戶端和伺服器相容性
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313970"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a>Windows 8 和 Windows Server 2012 用戶端和伺服器相容性

本節描述作業系統中的變更，您應該特別注意，因為現有的應用程式可能會受到影響，以及如何在用戶端、伺服器或用戶端和伺服器上設計新的應用程式。 以下是本節所涵蓋的主題清單（依功能區域分組）：

**AppCompat**

-   安全性應用程式偵測規則更新
-   判斷填充碼狀態
-   伺服器應用程式必須能夠在沒有伺服器圖形化 Shell 的情況下執行
-   RDS 伺服器元件會從 Windows 8 中移除
-   檔案類型和通訊協定關聯模型
-   桌面活動仲裁者
-   .NET Framework 4.5 是預設值，.NET Framework 3.5 是選擇性的
-   啟動預設的網頁瀏覽器之後，可能看不到桌面應用程式
-   高對比模式
-   應用程式 (可執行檔) 資訊清單
-   已取代佇列的目前模型
-   Windows 8 的程式相容性助理案例
-   已移除桌面小工具

**儲存體和檔案系統**

-   Advanced format (4K) 磁片相容性更新
-   精簡布建邏輯單元
-   針對 Windows 預先安裝環境 (WinPE) 和伺服器 SKU，現在可選擇增強的儲存體
-   虛擬磁碟服務正在轉換至 Windows Management Instrumentation (WMI) 型 Windows 儲存體管理 API
-   已移除本機磁片區的舊版 UI
-   StorAHCI 取代 MSAHCI
-   Windows 7 備份及還原已淘汰
-   卸載資料傳輸

**其他**

-   桌面視窗管理員一律開啟
-   Direct2D 不支援在 Internet Explorer 9 中轉譯為 "rich" 中繼檔
-   DX9 舊版硬體支援的變更
-   MSAA 無法供 Windows Store 應用程式使用
-   NDIS 6.30 驅動程式的埠3已淘汰

 

 
