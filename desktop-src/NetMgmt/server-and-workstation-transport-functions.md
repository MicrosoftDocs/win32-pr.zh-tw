---
title: 伺服器和工作站傳輸功能
description: 網路管理伺服器和工作站傳輸功能可處理傳輸通訊協定與伺服器和重新導向程式之間的系結和解除系結。
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967416"
---
# <a name="server-and-workstation-transport-functions"></a>伺服器和工作站傳輸功能

網路管理伺服器和工作站傳輸功能可處理傳輸通訊協定與伺服器和重新導向程式之間的系結和解除系結。 伺服器傳輸功能會處理由伺服器管理的傳輸通訊協定;工作站傳輸功能會處理由重新導向程式管理的傳輸通訊協定。

傳輸裝置與伺服器之間的檔案共用有兩個元件：

-   檔案所在的伺服器電腦
-   存取檔案 (SMB) 用戶端的伺服器訊息區

用戶端電腦會使用傳輸通訊協定，透過區域網路與伺服器電腦進行通訊;例如，TCP 或 XNS。 用戶端會將要求傳送到伺服器以取得資料。 用戶端電腦上產生檔案要求的軟體稱為重新導向器， *因為它* 會將本機檔案要求重新導向至伺服器電腦。 電腦上接收和操作檔案要求的軟體稱為「 *伺服器* 」，因為它會為用戶端提供服務。 這些要求的特定格式稱為 SMB 通訊協定。

伺服器傳輸函數如下所示。



| 函式                                                     | 描述                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | 將模擬的伺服器名稱系結至伺服器使用中的每個傳輸通訊協定。  (結合 [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) 函式和 [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) 函數的功能。 )                                             |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | 將每個網路傳輸通訊協定與先前呼叫 **NetServerComputerNameAdd** 函式所設定的模擬伺服器名稱中斷連線。                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | 將指定的伺服器系結至傳輸通訊協定。  (此函式只支援 [**伺服器 \_ 傳輸 \_ 資訊 \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) 資訊層級。 )                                                                                                                                                 |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | 將指定的伺服器系結至傳輸通訊協定。  (此擴充功能可支援 [**伺服器 \_ 傳輸 \_ 資訊 \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)、 [**伺服器 \_ 傳輸 \_ 資訊 \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)和 [**伺服器 \_ 傳輸資訊 \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) 資訊層級。 )  |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | 中斷傳輸通訊協定與伺服器的連線。                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | 列舉伺服器所管理的傳輸通訊協定。                                                                                                                                                                                                                                                                   |



 

您可以從下列資訊層級取得伺服器傳輸功能：

-   [**伺服器 \_ 傳輸 \_ 資訊 \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [**伺服器 \_ 傳輸 \_ 資訊 \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [**伺服器 \_ 傳輸 \_ 資訊 \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [**伺服器 \_ 傳輸 \_ 資訊 \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

工作站傳輸功能會對工作站執行對等的作業。

**Windows Server 2003 和 WINDOWS XP/2000：** 重新導向器不支援 [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) 函數或 [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) 函數。 您可以透過 [**網路和撥號連線**] 資料夾中的 [**本機區域** 線上內容] 對話方塊，手動變更傳輸通訊協定的預設設定。

工作站傳輸功能如下所示。



| 函式                                               | 描述                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | 將重新導向程式連接至傳輸通訊協定。                |
| [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | 中斷傳輸通訊協定與重新導向器的連線。           |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | 列出由重新導向程式管理的傳輸通訊協定。 |



 

工作站傳輸功能可在一個資訊層級使用：

-   [**WKSTA \_ 傳輸 \_ 資訊 \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




