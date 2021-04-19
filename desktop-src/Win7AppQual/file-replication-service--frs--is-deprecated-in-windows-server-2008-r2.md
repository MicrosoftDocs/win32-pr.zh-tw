---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Windows Server 2008 R2 中的檔案複寫服務 (FRS) 已淘汰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971818"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>Windows Server 2008 R2 中的檔案複寫服務 (FRS) 已淘汰

## <a name="platform"></a>平台

 **伺服器-** Windows Server 2008 R2  

## <a name="feature-impact"></a>功能影響

 **嚴重性-** 高  
**頻率-** 高  


## <a name="description"></a>Description

在 Windows Server 2008 R2 中， (FRS) 的檔案複寫服務無法用於複寫分散式檔案系統 (DFS) 資料夾或自訂 (非 SYSVOL) 資料。 Windows Server 2008 R2 網域控制站仍可使用 FRS 來複寫網域中使用 FRS 來複寫網域控制站之間 SYSVOL 共用的 SYSVOL 共用內容。 不過，Windows Server 2008 R2 伺服器無法使用 FRS 來複寫 SYSVOL 共用以外的任何複本集的內容。 DFS 複寫服務是 FRS 的替代方案，可用來複寫 SYSVOL 共用、DFS 資料夾，以及其他自訂 (非 SYSVOL) 資料的內容。 將所有非 SYSVOL 的 FRS 複本集遷移至 DFS 複寫。 我們也強烈建議您將 SYSVOL 共用的複寫從 FRS 遷移至 DFS 複寫，因為 DFS 複寫更健全、可調整規模，且複寫效能比 FRS 更好。

## <a name="manifestation"></a>表現

自訂資料的 FRS 複寫會在就地升級時中斷將失效。 從這種情況復原的唯一方法是在伺服器上重新安裝較舊的作業系統，然後重新初始化 FRS 複寫。 升級至 Windows Server 2008 R2 的伺服器不能參與現有的 FRS 複寫群組。

## <a name="mitigation-of-impact"></a>影響緩和措施

為了避免因這些變更而發生的問題，請將自訂的 FRS 複寫集遷移至 DFS 複寫。 DFS 複寫服務在 FRS 方面有許多優點，包括改良的管理工具、更高的效能和委派的管理。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [分散式檔案系統複寫：常見問題集](/windows-server/storage/dfs-replication/dfsr-faq)
-   [SYSVOL 複寫遷移指南： FRS 至 DFS 複寫](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
