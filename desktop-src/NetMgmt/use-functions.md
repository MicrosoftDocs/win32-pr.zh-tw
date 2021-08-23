---
title: 使用函式
description: 網路管理使用功能檢查和管理連線 (在工作站和伺服器之間使用) 。 使用函數如下所示。
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61019f6c6e2785f03eb4e2e9a47ed1953e14662c5664dca41465bc83d7c683d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779508"
---
# <a name="use-functions"></a>使用函式

網路管理使用功能檢查和管理連線 (在工作站和伺服器之間使用) 。 使用函數如下所示。



| 函式                               | 描述                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | 在本機電腦與伺服器之間建立連線。                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | 結束共用資源的連接。                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | 列出本機電腦與遠端伺服器上的資源之間的所有目前連接。 |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | 傳回共用資源連接的相關資訊。                              |



 

這些函式只適用于 (LAN Manager 工作站) 用戶端的伺服器訊息區。 **NetUseGetInfo** 函數不支援 (DFS) 共用分散式檔案系統。 若要使用不同的網路提供者來抓取共用資源的連接資訊 (WebDAV 或 DFS 共用（例如) ），請使用 [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) 函式。

連接會從會話辨別：當工作站第一次建立與伺服器上共用資源的連接時，就會建立 *會話* 。 在會話結束之前，工作站和伺服器之間的所有其他連線都是此相同會話的一部分。 您可以建立兩種類型的連線：裝置名稱連接 (只能是明確的) 和通用命名慣例 (UNC) 連接 (可以是明確或隱含的) 。

*連接* 是以每個使用者為基礎進行。 當使用者登出時，就會刪除使用者所建立的連接。 基於這個理由，網路管理使用的功能只在本機，因為任何其他使用者都無法存取由遠端使用者設定的連線，即使是以互動方式登入該電腦的使用者也是如此。

[**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)函式會將本機裝置名稱重新導向至遠端伺服器資源的共用名稱（ (\\ \\ *servername* \\ *共用*) ），藉此在本機電腦和伺服器上共用的資源之間建立明確的連接。 建立裝置名稱連接之後，使用者或應用程式可以藉由指定本機裝置名稱，來使用遠端資源。

隱含 UNC 連接是由負責連接的函式所組成。 若要建立隱含的 UNC 連接，應用程式會將資源的共用名稱傳遞給接受 UNC 路徑的任何函式。 此函式會接受 UNC 名稱，並連接到指定的共用名稱。 此連接上的所有進一步要求都需要完整的共用名稱。

使用函式適用于下列資訊層級：

-   [**使用 \_ 資訊 \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**使用 \_ 資訊 \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**使用 \_ 資訊 \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 