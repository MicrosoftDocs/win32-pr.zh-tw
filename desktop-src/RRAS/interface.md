---
title: " (RRAS) 的介面"
description: 介面是與網路的邏輯連接。 每個介面都是由唯一索引來識別。 多播路由通訊協定 (例如 MOSPF) 處理所有類型的介面。
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933814"
---
# <a name="interface-rras"></a> (RRAS) 的介面

介面是與網路的邏輯連接。 每個介面都是由唯一索引來識別。 多播路由通訊協定 (例如 MOSPF) 處理所有類型的介面。

如果是 LAN 介面，介面會對應到電腦中的實際實體裝置， (LAN 介面卡) 。 如果是 WAN 介面，則在建立連線時，介面會對應至埠。 WAN 介面可以是以通道為基礎，而埠可能是虛擬私人網路 (VPN) 埠。

Windows 2000 和更新版本的作業系統支援「點對 multipoint」介面。 這種類型的介面可以視為共用單一終止點的點對點連結集合。

若要在點對點介面中唯一識別確切的連結，MGM API 會使用介面識別碼的下一個躍點位址。 為了支援此識別，MGM API 會使用擴充的介面識別碼，其中包含 [下一個躍點](next-hop.md) 位址。

 

 




