---
title: 設定 SAP 和 RPC
description: Novell NetWare network 伺服器使用 (SAP) 的服務廣告通訊協定，將網路上可用服務的相關資訊廣播至其他網路裝置。
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf75a9ab45e97a66f1fc8d796b1d288367bb1c8d0e04b2ace4a90de7e21cbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931681"
---
# <a name="configuring-sap-and-rpc"></a>設定 SAP 和 RPC

Novell NetWare network 伺服器使用 (SAP) 的服務廣告通訊協定，將網路上可用服務的相關資訊廣播至其他網路裝置。 伺服器可能會每隔60秒傳送一次 SAP 廣播，以通知其他網路裝置所提供的服務。 工作站會使用 Sap 來尋找網路上所需的服務。

Windows 包含 SAP 代理程式服務，可讓 Windows 型伺服器與 NetWare 伺服器互動。 SAP 代理程式服務會在伺服器上安裝並執行的 IPX 服務，接聽網路用戶端的 SAP 要求。

設計成透過網路以服務方式公告的軟體（透過 SAP 廣播）將會每隔60秒發出 SAP 公告，而不會安裝 SAP 代理程式。 不過，為了讓網路用戶端快速找出 IPX 網路服務，維護服務資料庫的伺服器必須可在網路上使用，以回應服務位置要求。 此服務資料庫通常由 Novell NetWare 或受 NetWare 相容的伺服器維護。 適用于 NetWare 的 Microsoft 檔案和列印服務也會維護一個 IPX network service 資料庫。

在執行 Windows Server 的電腦上，如果已安裝適用于 NetWare 的閘道服務 (GSNW) ，則 SAP 類型640會在遠端程序呼叫 (RPC) 服務時，每隔60秒廣播一次。 即使使用者停用 GSNW 和 SAP 代理程式服務，也會繼續進行此 SAP 廣播。

如果用戶端服務 for NetWare (CSNW) 和 SAP 代理程式服務已安裝，RPC 服務將會進行 SAP 廣播。 即使使用者停用 SAP 代理程式，也會繼續進行此 SAP 廣播。

根據預設，RPC 服務會檢查是否有適用于 NetWare 的閘道服務，以及執行 Windows Server 之電腦上的 SAP 代理程式服務。 安裝適用于 NetWare 的檔案和列印服務，會安裝 SAP 代理程式。

在使用 CSNW 執行用戶端版本 Windows 的電腦上，RPC 服務會檢查 SAP 代理程式服務。 如果服務存在，RPC 將會啟動自己的執行緒，每分鐘都會進行 SAP 廣播類型640。

> [!NOTE]
> 如果您不想要在網路上每隔60秒進行 SAP 廣播，則可以使用登錄編輯程式停用 SAP 廣播。 請注意，使用登錄編輯程式不正確可能會導致嚴重問題，而可能需要您重新安裝作業系統。 Microsoft 無法保證可以解決因不當使用登錄編輯程式所造成的問題。 您必須自行負擔使用「登錄編輯程式」的風險。 您應該先備份登錄，然後再進行編輯。

 

**若要設定 SAP**

1.  執行登錄編輯程式 (Regedt32.exe) 並移至登錄中的下列機碼：

    **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ RPC**

2.  在 [ **編輯** ] 功能表上，按一下 [ **新增值**]，然後使用下列專案：
    1.  值名稱： AdvertiseRpcService
    2.  資料類型： REG \_ SZ
    3.  字串：否
3.  針對字串使用 No 會關閉 RPC SAP 廣播。 針對字串使用 Yes 可將 RPC SAP 廣播開啟。
4.  重新開機電腦，登錄變更才會生效。
    > [!NOTE]
    > 如果在遵循這些步驟之後，SAP 廣播繼續進行，您可能會想要嘗試進行疑難排解步驟。 刪除下列登錄機碼中的 **Ncacn \_ spx** 字串值：
    >
    > **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Rpc \\ ServerProtocols\\**

     

> [!NOTE]  
> 這應該只用來作為疑難排解步驟。 刪除此字串值會完全停用 SAP 廣播，而某些程式可能需要這些廣播才能正常運作。