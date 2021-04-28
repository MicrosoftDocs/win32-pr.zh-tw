---
description: 從伺服器作業系統移除 UDDI 服務
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: 從伺服器作業系統移除 UDDI 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116326"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>從伺服器作業系統移除 UDDI 服務

## <a name="affected-platform"></a>受影響的平臺

**伺服器** -Windows Server 2008 R2  



## <a name="feature-impact"></a>功能影響

**嚴重性** -中  
**頻率** -低  

## <a name="description"></a>Description

Microsoft 已從 Windows Server 2008 R2 移除 UDDI (通用描述、探索與整合) 服務伺服器角色。 未來的 UDDI 服務版本將會是 Microsoft BizTalk 產品的一部分。 這種產品重做和匯總可定位 Microsoft，以提供服務導向架構 (SOA) 市場。

「UDDI 服務」的第一版 Windows Server 2008 版將會符合「UDDI v3.0 標準」。 它會隨附于 BizTalk Server 2009 版本中。 為了符合我們的承諾，提供令人滿意的使用者體驗，我們將提供適用于 Windows Server 2008 R2 的 UDDI 服務 v3 安裝套件。

## <a name="manifestation"></a>表現

如果系統上有舊版的 UDDI 服務元件，則會封鎖升級至 Windows Server 2008 R2。

## <a name="mitigation-of-impact"></a>影響緩和措施

從 Windows Server 2003 或 Windows Server 2008 部署「UDDI 服務」網站的使用者可以選擇不要將執行「UDDI 服務」的伺服器升級為 Windows Server 2008 R2。 如果他們必須升級目前的「UDDI 服務」方塊，也可以將「UDDI 服務」移至專用的 Windows Server 2003 或 Windows Server 2008 方塊。

## <a name="solution"></a>解決方法

建議的解決方法是將 UDDI 服務 v3.0 從 BizTalk Server 2009 部署到 Windows Server 2008 R2 電腦，然後將舊的網站遷移到新的網站。 UDDI 服務 v3.0 提供與 UDDI 服務2.0 的回溯相容性，因此任何使用 UDDI 服務的應用程式都不會受到影響。

若要這樣做，請遵循下列步驟：

1.  在已載入 Windows Server 2008 R2 的電腦上設定新的 UDDI 服務 v3.0 網站。  (注意：在分散式安裝中，UDDI v3.0 網站可由一個以上的 Windows Server 2008 R2 電腦群組成。 ) 
2.  使用 UDDI 資料移轉工具，將舊的「UDDI 服務」資料庫中的資料移轉至新的資料庫。
3.  備份舊的 UDDI 服務資料庫，以確保復原功能。
4.  卸載舊的「UDDI 服務」軟體，然後將這些方塊升級至 Windows Server 2008 R2。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [Microsoft UDDI 服務網站](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [UDDI 規格](http://uddi.xml.org/specification)
-   [適用于 Windows Server 2008 R2 的 UDDI 服務 v3.0 下載](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



