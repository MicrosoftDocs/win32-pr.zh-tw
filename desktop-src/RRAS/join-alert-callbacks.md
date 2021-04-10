---
title: 加入警示回呼
description: 當多播群組管理員收到介面上群組有新的接收者存在時，多播群組管理員會叫用 PMGM \_ 聯結 \_ 警示 \_ 回呼回呼。
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021664"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="cc9ae-103">加入警示回呼</span><span class="sxs-lookup"><span data-stu-id="cc9ae-103">Join Alert Callbacks</span></span>

<span data-ttu-id="cc9ae-104">當多播群組管理員收到介面上群組有新的接收者存在時，多播群組管理員會 [**叫用 PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="cc9ae-105">此回呼會通知路由通訊協定新的主機已加入指定的群組。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="cc9ae-106">因此，路由通訊協定必須要求回呼所指定之群組的多播資料。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="cc9ae-107">多播群組管理員會使用一組預先定義的規則，用來判斷叫用此回呼的時間。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="cc9ae-108">這組規則是根據用戶端傳送的聯結要求類型，以及接收聯結要求的順序。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="cc9ae-109">萬用字元加入要求</span><span class="sxs-lookup"><span data-stu-id="cc9ae-109">Wildcard Join Requests</span></span>

<span data-ttu-id="cc9ae-110">當群組的萬用字元聯結 (時 \* ，會從第一個用戶端收到 g) ，多播群組管理員會叫用 [**PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) 回呼給所有其他已註冊的用戶端。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="cc9ae-111">從第二個用戶端收到群組的萬用字元聯結時，多播群組管理員會叫用此回呼給第一個用戶端以加入群組。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="cc9ae-112">Source-Specific 加入要求</span><span class="sxs-lookup"><span data-stu-id="cc9ae-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="cc9ae-113">多播群組管理員不會對群組的任何後續聯結叫用此回呼。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="cc9ae-114">當收到群組 (s、g) 的來源特定聯結時，多播群組管理員只會針對擁有來源 s 連入介面的用戶端叫用 [**PMGM \_ 聯結 \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="cc9ae-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




