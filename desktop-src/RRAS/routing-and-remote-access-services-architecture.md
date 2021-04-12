---
title: 路由及遠端存取服務架構
description: 下圖顯示 Windows 2000 路由器的一般架構觀點。
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- 路由及遠端存取服務 RRAS、路由及遠端存取服務架構 RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462344"
---
# <a name="routing-and-remote-access-services-architecture"></a>路由及遠端存取服務架構

下圖顯示 Windows 2000 路由器的一般架構觀點。

IP 通訊協定系列特定的元件會以淺灰色顯示。 IPX 通訊協定系列特定的元件會以暗灰色顯示。 所有通訊協定系列通用的元件都是 unshaded。

「路由及遠端存取」服務提供用來管理和設定服務的 Api。 這些 Api 包括 IP 和 IPX 的 SNMP 代理程式。

RRAS 包含 IP 和 IPX 的路由通訊協定。 針對 IP，RRAS 會提供路由資訊通訊協定 (RIP) 和開放式最短路徑 First (OSPF) 路由通訊協定。 針對 IPX，RRAS 提供 (SAP) 的 IPX RIP 和服務廣告通訊協定。

RRAS 會針對 IP 和 IPX 使用一個路由表管理員 (RTM) 。 不過，每個通訊協定系列都有自己的路由器管理員。 RRAS 也有個別的元件，可用於管理多播群組。

動態介面管理員 (將) 介面與 PPP 和 TAPI 服務互動，以便管理某些路由所使用的 PPP 介面。

![windows 2000 路由器的一般架構視圖](images/rtarch.png)

 

 




