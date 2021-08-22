---
description: IP Helper 提供管理網路路由的功能。 使用下列功能管理 IP 路由表，以及取得其他路由資訊。
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: 管理路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3b351882e08be3d09615acd033e0fb86192aee8675e8f52c4812a1eba398ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146641"
---
# <a name="managing-routing"></a>管理路由

IP Helper 提供管理網路路由的功能。 使用下列功能管理 IP 路由表，以及取得其他路由資訊。

藉由呼叫 [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) 函數來取出 IP 路由表的內容。 使用 [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry)、 [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)和 [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) 函數來操作 IP 路由表中的特定專案。 使用 **CreateIpForwardEntry** 函式來加入新的路由表專案。 使用 **DeleteIpForwardEntry** 函數來移除現有的專案。 **SetIpForwardEntry** 函式會修改現有的專案。

IP 協助程式的路由器管理功能可以用來取得有關如何透過網路路由傳送資料包的資訊。 [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)函式會取得指定之目的地位址的最佳路由。 [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface)函式會將最佳路由所使用的介面索引，捕獲到指定的目的地位址。 最後， [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) 函式會 (RTT) 和躍點數目，以指定的目的地位址抓取來回時間。

 

 



