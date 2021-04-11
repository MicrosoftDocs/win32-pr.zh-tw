---
title: 群組原則
description: 背景智慧型傳送服務 (位) 會使用下列群組原則來設定 BITS 傳輸和設定。 如需不同版本的 Windows 所使用之位版本的詳細資訊，請參閱新功能主題。
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183053"
---
# <a name="group-policies"></a>群組原則

> [!NOTE]
> 如需如何使用行動裝置管理 (MDM) 為背景智慧型傳送服務 (BITS) 設定原則的詳細資訊，請參閱 [原則 CSP](/windows/client-management/mdm/policy-configuration-service-provider)。

背景智慧型傳送服務 (位) 會使用下列群組原則來設定 BITS 傳輸和設定。 如需不同版本的 Windows 所使用之位版本的詳細資訊，請參閱 [新功能](what-s-new.md) 主題。

> [!NOTE]  
> 如果未設定原則值，BITS 會使用預設原則值。

**啟用 BITS 原則**

1.  在 [**執行**] 視窗或命令提示字元中，于 CMD 視窗中輸入 **gpedit.msc/Gpcomputer： "***ComputerName***"** 來開啟群組原則。
2.  BITS 原則位於 [ **電腦** 設定]、[ **系統管理範本**]、[ **網路**] **背景智慧型傳送服務**。
3.  以滑鼠右鍵按一下原則，然後選取 [ **編輯**]。
4.  遵循啟用和設定原則的指示。

BITS 的群組原則位於 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **BITS** 的登錄中。 請注意，只有設定的原則會列在登錄中。

|原則|Description|
|-|-|
|JobInactivityTimeout<br/>BITS 1。0|依預設，BITS 會維護作業的相關資訊達90天。 如果在這段時間內沒有針對作業的活動，BITS 會取消作業。 傳輸進度或屬性變更會重設計時器。<br/> 如果使用者未登入或維護長時間的網路連接，您可能需要調整此原則。|
|MaxInternetBandwidth<br/>BITS 2。0|限制 BITS 用於背景傳送的網路頻寬 (此原則不會影響) 的前景傳輸。<br/>指定要在特定時間間隔期間使用的限制，以及其他任何時候使用的限制。 例如，將網路頻寬的使用量限制為每秒 10 kb， (Kbps) 上午8:00 到下午5:00 並在剩餘的時間內使用所有可用的未使用頻寬。<br/>**注意**：變更系統時鐘並不會影響頻寬限制時間間隔。 例如，如果目前的時間是 2:00 P.M。 頻寬限制間隔從下午3:00 開始，將系統時鐘往前移動一小時不表示 BITS 將在一小時內仍會持續發生頻寬限制的一小時內強制頻寬限制。 若要反映系統時鐘變更（以位為單位），您必須重新開機電腦或 BITS 服務。<br/>指定限制（以每秒 kb 數為單位）。 以網路連結的大小為基礎，而不是電腦的網路介面卡大小限制 (NIC) 。 如果您指定的值小於兩個 kb，則位大約會使用兩個千位。 若要防止 BITS 傳輸發生，請指定零的限制。 如果您指定的限制為零，則 BITS 會將所有背景工作置於暫時性錯誤狀態。  (錯誤碼設定為 BG_E_BLOCKED_BY_POLICY。 ) 位會在時間間隔到期之後，將工作置於佇列狀態。<br/> 如果您停用或未設定此原則，BITS 會使用所有可用的未使用頻寬。<br/> 一般來說，當用戶端具有快速網路介面卡 (10 Mbps) 但是透過低速連結連接到網路 (56 Kbps) 時，您就可以使用此原則來防止 BITS 從競爭網路頻寬的情況下傳輸。<br/> 如需有關 BITS 如何使用網路頻寬的詳細資訊，請參閱 [網路頻寬](network-bandwidth.md)。|
|MaxDownloadTime<br/>BITS 3。0|決定 BITS 可在作業中主動傳輸檔案的時間長度。 預設值為 90 天。<br/> 若要針對特定作業覆寫此原則，請呼叫 [**IBackgroundCopyJob4：： SetMaximumDownloadTime**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime) 方法。|
|MaxJobsPerMachine<br/>BITS 3。0|限制使用者可在電腦上建立的作業數目。 預設值為300工作。 此原則不適用於具有系統管理員許可權或服務帳戶的使用者。|
|MaxJobsPerUser<br/>BITS 3。0|限制使用者可在電腦上建立的作業數目。 預設為每位使用者60個工作。 此原則不適用於具有系統管理員許可權或服務帳戶的使用者。|
|MaxFilesPerJob<br/>BITS 3。0|限制使用者可新增至作業的檔案數目。 預設為每個作業200個檔案。 此原則不適用於具有系統管理員許可權或服務帳戶的使用者。|
|MaxRangesPerFile<br/>BITS 3。0|限制使用者可以為檔案指定的範圍數目。 預設值為500範圍。 此原則不適用於具有系統管理員許可權或服務帳戶的使用者。|

BITS 會使用下列群組原則來啟用和設定 BITS 與 BranchCache 的互動方式。

|原則|Description|
|-|-|
|DisableBranchCache<br/>BITS 4。0|預設會啟用 Windows BranchCache 功能。 設定此原則以防止 BITS 用戶端使用 Windows BranchCache 傳送內容。<br/>**注意**：這項設定不會影響應用程式以外的應用程式使用 Windows BranchCache。 此原則不適用於透過伺服器訊息區 (SMB) 的 BITS 傳輸。 如果 Windows 分支快取的電腦系統管理設定完全停用其使用，則此設定不會有任何作用。|

BITS 會使用下列群組原則來設定頻寬節流設定。

|原則|Description|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4。0|限制 BITS 在維護天數和小時期間用於背景傳輸的網路頻寬。 維護排程會進一步限制用於背景傳送的網路頻寬。<br/> 指定維護排程期間用於背景工作的限制。 例如，如果一般優先順序作業目前在工作排程上限制為 256 Kbps，您可以進一步將一般優先順序作業的網路頻寬限制為 0 Kbps （上午8:00）。 變成上午 10:00。 維護排程。<br/>**注意**：針對維護期間所設定的頻寬限制，會取代針對工作和其他排程所定義的任何限制。|
|EnableBandwidthLimits<br/>BITS 4。0|限制 BITS 在工作和非工作天和時數中用於背景傳輸的網路頻寬。 工作排程會使用每週行事歷來定義，其中包含一周中的天數和一天中的小時。 在工作排程中未定義的所有時數和天數都會視為非工作時間。<br/> 指定在工作排程期間用於背景工作的限制。 例如，您可以將低優先順序作業的網路頻寬限制為 128 Kbps （上午8:00）。 到下午5:00 從星期一到星期五，然後將 [限制為 512 Kbps] 設定為 [非工作時間]。|


## <a name="related-topics"></a>相關主題
* [原則 CSP](/windows/client-management/mdm/policy-configuration-service-provider)
