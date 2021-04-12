---
title: 共用函式
description: 網路管理共用功能會控制共用資源。 共用資源是伺服器上的本機資源 (例如，磁碟目錄、列印裝置或具名管道) ，可供使用者和網路上的應用程式存取。
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5034d46e233ebb7ed4de691bd79942a3ecdf5263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382573"
---
# <a name="share-functions"></a>共用函式

網路管理共用功能會控制共用資源。 共用資源是伺服器上的本機資源 (例如，磁碟目錄、列印裝置或具名管道) ，可供使用者和網路上的應用程式存取。

共用函數如下所示。



| 函式                                  | 描述                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | 共用伺服器上的資源。                                       |
| [**NetShareCheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | 查詢伺服器是否正在共用裝置。                        |
| [**NetShareDel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | 從伺服器的共用資源清單中刪除共用名稱。       |
| [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | 抓取伺服器上每個共用資源的共用資訊。  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | 抓取伺服器上指定之共用資源的相關資訊。 |
| [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | 設定共用資源的參數。                                 |



 

這些共用函式僅適用于伺服器訊息區上的共用， (LAN Manager) Server。 這些共用功能不支援 (DFS) 共用分散式檔案系統。 例如， [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) 函式只能取得 SMB 伺服器上指定之共用資源的資訊。 若要使用不同的網路提供者取出共用的資訊 (WebDAV 或 DFS 共用（例如) ），請使用 [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) 函式。

[**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)函式可讓使用者或應用程式使用指定的共用名稱來共用特定類型的資源。 **NetShareAdd** 函式需要共用名稱和本機裝置名稱，才能共用資源。 使用者或應用程式必須具有伺服器上的帳戶，才能存取資源。

您也可以指定要與共享相關聯的安全描述項。 安全描述項會指定允許哪些使用者透過共用存取檔案，以及使用何種類型的存取權。 呼叫 **NetShareAdd** 或 [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo)時，請指定具有 [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)資訊層級的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)。 **NetShareSetInfo** 支援 [**共用 \_ 資訊 \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) 資訊層級。 如需安全描述項的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。

網路管理功能會使用下列特殊的共用名稱來進行處理序間通訊 (IPC) 和伺服器的遠端系統管理：

-   IPC $，保留給處理序間通訊
-   ADMIN $，保留給遠端系統管理
-   $、B $、C $ (和其他本機磁片名稱，後面接著貨幣符號) ，指派給本機磁片裝置

若要列出伺服器上共用資源的所有連線，或列出從特定電腦建立的所有連接，請呼叫 [**NetConnectionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) 函數。 您可以在 [**連接 \_ 資訊 \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0)和 [**連接 \_ 資訊 \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1)資訊層級呼叫 **NetConnectionEnum** 。

您可以在下列資訊層級取得共用函式，不過某些共用層級只適用于某些共用功能：

-   [**共用 \_ 資訊 \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**共用 \_ 資訊 \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**共用 \_ 資訊 \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**共用 \_ 資訊 \_ 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**共用 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**共用 \_ 資訊 \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**共用 \_ 資訊 \_ 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**共用 \_ 資訊 \_ 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**共用 \_ 資訊 \_ 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**共用 \_ 資訊 \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

如需詳細資料，請參閱特定共用功能的檔。

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理共用功能來達成的相同功能。 如需詳細資訊，請參閱 [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)。

 

 