---
title: 對等快取
description: 從背景智慧型傳送服務 (位) 4.0 開始，BITS 服務已擴充為允許使用 Windows BranchCache 下載的 URL 資料的子網層級對等快取。
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965437"
---
# <a name="peer-caching"></a>對等快取

從背景智慧型傳送服務 (位) 4.0 開始，BITS 服務已擴充為允許使用 Windows BranchCache 下載的 URL 資料的子網層級對等快取。 BITS 用戶端可以從自己的子網中已下載資料的其他電腦抓取資料，而不是從遠端伺服器取得資料。 如需 Windows BranchCache 的詳細資訊，請參閱 [BranchCache 總覽](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))。

如果系統管理員透過群組原則或本機設定設定，在組織中的用戶端和伺服器電腦上啟用 Windows BranchCache，BITS 將會使用 Windows BranchCache 進行資料傳輸。

-   [BITS 4.0 對等快取的設定](#configuration-for-bits-40-peer-caching)
-   [停用 Windows BranchCache](#disabling-windows-branchcache)
-   [驗證和監視](#verification-and-monitoring)
-   [BITS 3.0 中的對等快取](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>BITS 4.0 對等快取的設定

需要下列設定，BITS 4.0 中的對等快取才能運作：

-   您必須透過群組原則或本機設定，在用戶端上啟用 Windows BranchCache。 如需詳細資訊，請參閱 [BranchCache 用戶端](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10))設定。
    > [!Note]  
    > Windows BranchCache 功能預設為停用。

     

-   Windows BranchCache 功能是必須安裝在伺服器上的選擇性元件。 如需詳細資訊，請參閱 [BranchCache server configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10))。
-   伺服器也必須透過群組原則或本機設定來啟用 Windows BranchCache 功能。 如需詳細資訊，請參閱 [BranchCache server configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10))。
    > [!Note]  
    > Windows BranchCache 功能預設為停用。

     

預設的 BITS 群組原則允許對等快取。 如果電腦上的 Windows BranchCache 是全域啟用的，則也會啟用 BITS 傳送工作的這項功能。 如需有關 BITS 特定群組原則的詳細資訊，請參閱 [群組原則](group-policies.md)。

## <a name="disabling-windows-branchcache"></a>停用 Windows BranchCache

系統管理員可以使用群組原則來停用 Windows BranchCache。  (請參閱 [群組原則](group-policies.md)。 ) 如果已停用 Windows BRANCHCACHE，BITS 用戶端只會從遠端伺服器取出資料。

應用程式也可以藉由呼叫 [**IBackgroundCopyJob4：： SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) 方法並設定 **BG \_ 停用 \_ 分支 \_** 快取旗標，以每個作業為基礎停用 Windows BranchCache。

> [!Note]  
> 這些設定不會影響 BITS 以外的應用程式使用 Windows BranchCache。 這些設定不適用於透過 SMB 的 BITS 傳輸。 BITS 不會控制 Windows BranchCache 透過 SMB 傳送的任何設定。

 

## <a name="verification-and-monitoring"></a>驗證和監視

有幾種方式可以驗證和監視對等快取統計資料。 系統管理員可以呼叫 [**IBackgroundCopyFile4：： GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) 方法，以查詢從對等和源伺服器下載的資料量。 系統管理員也可以檢查事件記錄檔中的事件 [識別碼 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10))，以提供作業特定的資訊。

Windows BranchCache 功能也提供一些機制來驗證和監視對等快取統計資料。 如需詳細資訊，請參閱 [驗證和監視](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) 和 [效能計數器](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10))。

使用 Windows BranchCache 的對等快取模型會取代 BITS 3.0 中使用的對等快取模型。 如需 Windows BranchCache 的詳細資訊，請參閱下列各項：

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [BranchCache 概觀](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Windows 7 服務](../win7devguide/services.md)
-   [對等散發 API](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>BITS 3.0 中的對等快取

> [!Note]  
> 從 Windows 7 開始，BITS 3.0 對等快取模型已被取代。 如果已安裝 BITS 4.0，BITS 3.0 對等快取模型就無法使用。

 

如果系統管理員啟用對等快取，而作業允許從對等下載內容，BITS 將會嘗試從一或多個對等電腦下載內容。 從對等下載比從網際網路下載內容快很多。 依預設會停用對等快取，且工作必須明確允許從對等下載內容。 系統管理員可以使用群組原則來啟用對等快取。 啟用對等快取之後，系統管理員可以停用從對等下載，或將內容提供給對等。

應用程式也可以藉由呼叫 [**IBitsPeerCacheAdministration：： SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) 方法來啟用對等快取。 但是，如果設定，則會由群組原則設定覆寫這些設定。

啟用對等快取時，BITS 會建立位於相同子網且屬於相同網域的對等清單。 此清單不會包含來自受信任網域的對等。 對等快取只能在網域環境中啟用。

BITS 會執行下列動作來探索對等：

-   接聽宣告本身的對等伺服器。 對等伺服器會在啟動時自行宣告。 如果用戶端在其清單中需要更多對等，則 BITS 會將對等伺服器新增至清單。
-   當對等伺服器在其對等清單中需要更多對等時，廣播要求。 可用來提供內容回應要求的對等伺服器。

如果伺服器執行下列動作，則 BITS 會從對等清單中移除對等伺服器：

-   驗證失敗
-   離線 (無法使用) 太長
-   提供有錯誤的憑證

當作業向對等要求內容時，BITS 會從對等清單中隨機播放對等的子集，並詢問其是否有內容。 BITS 只能從已驗證的對等伺服器下載內容。 用戶端和伺服器一開始會使用 Kerberos 進行驗證，然後在內容探索和下載期間交換自我簽署憑證以進行驗證。

BITS 會從第一個經過驗證的對等下載內容，以回應要求。 如果其中一個對等不包含所有內容，BITS 將會從源伺服器下載其餘部分之前，從一或多個對等下載它。 如果任何對等都沒有內容，或從對等下載時發生錯誤，BITS 會從源伺服器下載內容。

只有在應用程式驗證檔案內容之後，才可以將下載的內容提供給其他對等。 如果應用程式未明確驗證檔案，則會在應用程式完成工作時，以隱含方式驗證檔案。

根據預設，對等伺服器只能將內容提供給三個用戶端。 如果伺服器目前忙於提供三個用戶端，則回應其他要求會有延遲。 BITS 會限制用來將內容提供給 1 Mbps 的頻寬。 您可以使用 [MaxBandwidthServed](group-policies.md) 群組原則來變更限制。

> [!Note]  
> 只有網域網路才支援這項功能;工作組或家用網路不支援對等快取。

另請參閱[管理對等](/windows/desktop/Bits/administering-the-peer-cache)快取
 

 

 