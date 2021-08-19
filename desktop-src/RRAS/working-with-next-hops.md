---
title: 使用下一個躍點
description: RTMv2 API 可讓用戶端使用與路由和目的地相關聯的下一個躍點清單。
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f629bb5f43298c2cada3759ea3ab9c7bb71f0ca47a3c4158028d923646662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024708"
---
# <a name="working-with-next-hops"></a>使用下一個躍點

RTMv2 API 可讓用戶端使用與路由和目的地相關聯的下一個躍點清單。 用戶端可以藉由呼叫 [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)來新增或更新下一個躍點。 用戶端可以使用 [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)來刪除下一個躍點。 用戶端可以藉由呼叫 [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)來搜尋下一個躍點。

用戶端也可以直接更新下一個躍點。 若要這樣做，用戶端必須先使用 [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) 函數來鎖定下一個躍點。 然後，用戶端可以使用路由表管理員的 [**RTM \_ NEXTHOP \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) 結構的直接指標進行必要的修改。 最後，用戶端可以解除鎖定下一個躍點。

> [!Note]  
> 下一個躍點中的下一個躍點位址和介面索引欄位可唯一識別下一個躍點，不應該修改。

 

 

 




