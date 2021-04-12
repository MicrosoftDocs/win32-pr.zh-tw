---
title: 使用下一個躍點
description: RTMv2 API 可讓用戶端使用與路由和目的地相關聯的下一個躍點清單。
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372560"
---
# <a name="working-with-next-hops"></a>使用下一個躍點

RTMv2 API 可讓用戶端使用與路由和目的地相關聯的下一個躍點清單。 用戶端可以藉由呼叫 [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)來新增或更新下一個躍點。 用戶端可以使用 [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)來刪除下一個躍點。 用戶端可以藉由呼叫 [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)來搜尋下一個躍點。

用戶端也可以直接更新下一個躍點。 若要這樣做，用戶端必須先使用 [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) 函數來鎖定下一個躍點。 然後，用戶端可以使用路由表管理員的 [**RTM \_ NEXTHOP \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) 結構的直接指標進行必要的修改。 最後，用戶端可以解除鎖定下一個躍點。

> [!Note]  
> 下一個躍點中的下一個躍點位址和介面索引欄位可唯一識別下一個躍點，不應該修改。

 

 

 




