---
title: 關於 BITS
description: 使用背景智慧型傳送服務 (位) 在用戶端與伺服器之間非同步傳送檔案。
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- 背景智慧型傳送服務，說明
- 傳送佇列位
- 傳送佇列位，節流
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b1ac0f587b496692ec1c2e62be06c0e64766a205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092771"
---
# <a name="about-bits"></a>關於 BITS

使用背景智慧型傳送服務 (位) 從檔案下載檔案，或將檔案上傳至 HTTP 網頁伺服器或 SMB 檔案伺服器。 

只要起始傳送的使用者仍處於登入狀態，並維護網路連線，BITS 會在應用程式結束之後繼續傳輸檔案。 BITS 不會強制網路連接。 BITS 會在已中斷的網路連線重新建立之後，或在登出登入的使用者之後，繼續傳輸。 如需詳細資訊，請參閱 [使用者和網路連接](users-and-network-connections.md)。

BITS 會留意目前的網路成本和擁塞，讓背景工作在使用使用者的前景體驗時可能會干擾到最少。 BITS 會使用閒置的 [網路頻寬](network-bandwidth.md) 來傳輸檔案，並根據可用的閒置網路頻寬量來增加或減少傳輸檔案的速率。 如果網路應用程式開始佔用較多頻寬，BITS 便會降低其傳送速率，以保持使用者的互動體驗。 BITS 會使用應用程式指定的 [傳輸原則](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) 來防止檔案在有成本的網路連線上傳輸。

位也會留意電源使用量。 從 Windows 10 2019 年5月更新開始，BITS 會在電腦處於 [新式待命](/windows-hardware/design/device-experiences/modern-standby) 模式且電腦已插入電源時傳輸檔案。

BITS 應用程式可使用不同的位 [優先權層級](/windows/desktop/api/Bits/ne-bits-bg_job_priority) ，讓 bits 以智慧方式挑選要執行的傳送作業。 優先順序較高的工作優先於優先順序較低的工作。 優先順序層級相同的工作則會共用傳送時間，如此可防止傳送佇列中的某個大型工作阻擋其他幾個小型工作。 直到所有優先順序較高的工作都完成或處於錯誤狀態後，優先順序較低的工作才能接收傳送時間。

BITS 會使用 Windows BranchCache 進行對等快取。 如需詳細資訊，請參閱 [BranchCache 總覽](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))。

通用 Windows 平臺 (UWP) 開發人員應該使用 [Windows.networking.backgroundtransfer.contentprefetcher](/uwp/api/Windows.Networking.BackgroundTransfer) API，而不是 BITS api。

有三種類型的 [**傳送作業**](/windows/desktop/api/Bits/ne-bits-bg_job_type)。 下載作業會將檔案下載到用戶端、上傳作業會將檔案上傳到伺服器，而上傳-回復作業會將檔案上傳至伺服器，並從伺服器應用程式接收回複檔案。

下列主題提供更多有關 BITS 的詳細資訊：

-   [驗證](authentication.md)
-   [BITS 工作的生命週期](life-cycle-of-a-bits-job.md)
-   [使用者和網路連接](users-and-network-connections.md)
-   [網路頻寬](network-bandwidth.md)
-   [群組原則](group-policies.md)
-   [服務帳戶和 BITS](service-accounts-and-bits.md)
-   [BITS 傳送工作的協助程式權杖](helper-tokens-for-bits-transfer-jobs.md)
-   [檔案傳輸一致性](file-transfer-consistency.md)
-   [BITS 下載的 HTTP 需求](http-requirements-for-bits-downloads.md)
-   [BITS 上傳的 IIS 需求](iis-requirements-for-bits-uploads.md)
-   [虛擬目錄清理](virtual-directory-cleanup.md)
-   [BITS 和系統還原](bits-and-system-restore.md)
-   [BITS 啟動類型](bits-startup-type.md)
-   [網際網路連線共用](internet-connection-sharing.md)
-   [對等快取](peer-caching.md)
-   [BITS 安全性、權杖和系統管理員帳戶](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

使用 BITS [介面](bits-interfaces.md) 撰寫用來建立和監視傳送作業的應用程式。 如需使用 BITS 介面的詳細資訊，請參閱 [使用 bits](using-bits.md)。