---
description: IP 多播落在 nonrooted 資料平面和 nonrooted 控制平面的類別中。
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: IP 多播
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b80441826f490fedc3dac3dba405ddd0d9f09d57bfd0243a66cae320c76b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051496"
---
# <a name="ip-multicast"></a>IP 多播

IP 多播落在 nonrooted 資料平面和 nonrooted 控制平面的類別中。 所有應用程式都扮演分葉角色。 目前，大部分的 IP 多播採用都是由 Steve Deering 提供的一組通訊端選項， (IETF) 的網際網路工程任務推動力。 因此有五個作業可供使用：

-   IP \_ 多播 \_ TTL —設定存留時間、控制多播會話的範圍。
-   IP \_ 多播 \_ IF-決定要用於多播的介面。
-   IP \_ 新增 \_ MEMBERSHI：聯結指定的多播會話。
-   IP \_ 捨棄 \_ 成員資格-捨棄多播會話。
-   IP \_ 多播 \_ 迴圈-控制多播流量的回送。

設定 IP 多播通訊端的存留時間時，會直接對應到 \_ 針對 WSAIoctl 使用 SIO 多播 \_ 領域命令的程式碼[](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)。

判斷要用於多播的 IP 介面的方法是透過 tcp/ip 特定通訊端選項，如 Windows 通訊端 2 Protocol-Specific 附錄中所述。 剩下的三項作業會在此涵蓋 Windows 通訊端2語義，如下所述。

應用程式會使用 WSASocket 中的 c 分 \_ 葉/d 分 \_ 葉旗標[](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)來開啟通訊端。 它會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 將本身新增至預設介面（指定給多播作業）的多播群組。 如果 **WSAJoinLeaf** 中的旗標指出這個通訊端只是傳送者，則聯結作業基本上是無作業，而且不需要傳送任何 IGMP 訊息。 否則，會將 IGMP 封包傳送給路由器，以指出接收傳送到指定多播位址的封包的興趣。 由於應用程式建立了專門用來執行多播的特殊 c 分 \_ 葉/d 分 \_ 葉通訊端，因此會使用標準 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式來捨棄多播會話。 適用于 \_ WSAIoctl 的 SIO MULTIPOINT \_ 回[](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)送命令程式碼提供了一般控制機制，用來判斷在 nonrooted MULTIPOINT 配置的 d 分葉通訊端上傳送的資料是否 \_ 也可以在相同的通訊端上接收。

> [!Note]  
> ip 多播迴圈選項的 Winsock 版本在 \_ \_ 語義上不同于 ip \_ 多播迴圈選項的 UNIX 版本 \_ ：

 

-   在 Winsock 中，IP \_ 多播 \_ 迴圈選項只會套用到接收路徑。
-   在 UNIX 版本中，IP \_ 多播 \_ 迴圈選項會套用到傳送路徑。

例如，開啟和關閉應用程式 (比 X 和 Y 更容易追蹤) 在相同介面上加入相同群組;上的應用程式會在上設定 IP \_ 多播 \_ 迴圈選項，應用程式 OFF 將 ip \_ 多播 \_ 迴圈選項設為關閉。 如果 ON 和 OFF 是 Winsock 應用程式，OFF 可以傳送至 ON，但無法傳送到 OFF。 相反地，如果 on 和 OFF 是 UNIX 的應用程式，則上的可以傳送至 off，但無法傳送至。

 

 



