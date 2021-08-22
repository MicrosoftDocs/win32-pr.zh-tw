---
description: 對等群組和圖形基礎結構會使用雲端。
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: 雲端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c5ecbeee1f5b69d120c5f351f8a5bb200b6e3e5f60e4bacca5a4f5484f402dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932690"
---
# <a name="clouds"></a>雲端

對等 [群組](grouping-api.md) 和 [圖形](graphing-api.md) 基礎結構會使用雲端。 [對等名稱解析通訊協定 (PNRP) ](pnrp-namespace-provider-api.md)將雲端識別為可在相同 IPv6 範圍內進行通訊的一組對等。 雲端與 IPv6 範圍密切相關。 下列清單指出一些獨特的雲端功能：

-   雲端是以名稱來識別，而可用的雲端則可以使用 [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md)來列舉。
-   如果電腦已連線到網際網路，則它是全域雲端的一部分，以字串 "Global \_ " 識別。
-   如果電腦連線到一或多個區域網路 (LAN) ，則每個連結都可使用個別的雲端。
-   您可以透過多個網路介面卡或使用虛擬私人網路 (VPN) ，將一部電腦連線到許多網路，這表示在許多雲端中都可以看到具有一個介面的電腦。
-   您可以使用 PNRP 來註冊和解析特定雲端中的對等名稱。

 

 



