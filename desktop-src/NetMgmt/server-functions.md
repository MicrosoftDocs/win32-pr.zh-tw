---
title: " (網路管理) 的伺服器功能"
description: Network management server 函式會在本機或遠端伺服器上執行管理工作。 伺服器函數如下所示。
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024496"
---
# <a name="server-functions-network-management"></a> (網路管理) 的伺服器功能

Network management server 函式會在本機或遠端伺服器上執行管理工作。 伺服器函數如下所示。



| 函式                                       | 描述                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | 傳回伺服器上的本機磁片磁碟機清單。                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | 列出特定類型的所有可見伺服器 (或指定網域中) 的類型。 |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | 傳回指定伺服器的設定資訊。                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | 設定伺服器的指令引數。                                        |



 

只有在本機或遠端伺服器上具有系統管理員群組成員資格的使用者或應用程式，才能在該伺服器上執行系統管理工作，以控制伺服器的作業、使用者存取和資源分享。 您可以藉由呼叫 [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) 和 [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) 函數來檢查和修改影響伺服器作業的低層級參數。 這些參數是在伺服器的 LANMAN.INI 檔案中定義。

大部分的網路管理伺服器功能只會在遠端伺服器上執行。 [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)函式是在本機工作站或遠端伺服器上執行。 如果您嘗試在本機工作站上執行其他伺服器函式，這些函式會傳回錯誤 NERR \_ RemoteOnly。

您可以在下列層級取得伺服器特定的資訊：

-   [**伺服器 \_ 資訊 \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**伺服器 \_ 資訊 \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**伺服器 \_ 資訊 \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**伺服器 \_ 資訊 \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**伺服器 \_ 資訊 \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**伺服器 \_ 資訊 \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**伺服器 \_ 資訊 \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**伺服器 \_ 資訊 \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**伺服器 \_ 資訊 \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**伺服器 \_ 資訊 \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**伺服器 \_ 資訊 \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**伺服器 \_ 資訊 \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**伺服器 \_ 資訊 \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**伺服器 \_ 資訊 \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**伺服器 \_ 資訊 \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**伺服器 \_ 資訊 \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**伺服器 \_ 資訊 \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**伺服器 \_ 資訊 \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**伺服器 \_ 資訊 \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**伺服器 \_ 資訊 \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**伺服器 \_ 資訊 \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**伺服器 \_ 資訊 \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**伺服器 \_ 資訊 \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**伺服器 \_ 資訊 \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**伺服器 \_ 資訊 \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**伺服器 \_ 資訊 \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**伺服器 \_ 資訊 \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**伺服器 \_ 資訊 \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**伺服器 \_ 資訊 \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**伺服器 \_ 資訊 \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**伺服器 \_ 資訊 \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理伺服器功能達成的相同功能。 如需詳細資訊，請參閱 [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)。

如需詳細資訊，請參閱 [伺服器和工作站傳輸功能](server-and-workstation-transport-functions.md)。

 

 
