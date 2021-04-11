---
title: 剪除警示回呼
description: 當多播群組管理員收到通知接收者將群組留在介面上時，多播群組管理員會叫用 PMGM 剪除 \_ \_ 警示 \_ 回呼回呼。
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021982"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="848a3-103">剪除警示回呼</span><span class="sxs-lookup"><span data-stu-id="848a3-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="848a3-104">當多播群組管理員收到通知接收者將群組留在介面上時，多播群組管理員會叫用 PMGM 剪除 [**\_ \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="848a3-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="848a3-105">此回呼會通知路由通訊協定，用戶端不再屬於指定的群組。</span><span class="sxs-lookup"><span data-stu-id="848a3-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="848a3-106">因此，路由通訊協定必須停止要求指定群組的多播資料。</span><span class="sxs-lookup"><span data-stu-id="848a3-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="848a3-107">多播群組管理員有一組預先定義的規則，用來判斷叫用此回呼的時間。</span><span class="sxs-lookup"><span data-stu-id="848a3-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="848a3-108">這些規則是根據用戶端所傳送的剪除要求類型，以及在中收到剪除要求的順序。</span><span class="sxs-lookup"><span data-stu-id="848a3-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="848a3-109">萬用字元剪除要求</span><span class="sxs-lookup"><span data-stu-id="848a3-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="848a3-110">當針對群組 (的萬用字元剪除時 \* ，會收到 g) ，而且會為第二個用戶端移除最後一個介面 (也就是說，當只有單一用戶端的介面保持) 時，多播群組管理員會叫用 PMGM 剪除 [**\_ \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) 回呼至剩餘的用戶端。</span><span class="sxs-lookup"><span data-stu-id="848a3-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="848a3-111">移除最後一個用戶端的最終介面之後 (也就是，當沒有其他介面仍) 時，就會針對已向多播群組管理員註冊的所有其他用戶端叫用此回呼。</span><span class="sxs-lookup"><span data-stu-id="848a3-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="848a3-112">Source-Specific 剪除要求</span><span class="sxs-lookup"><span data-stu-id="848a3-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="848a3-113">當群組的來源特定剪除 (s，會收到 g) ，多播群組管理員只會針對擁有來源 s 傳入介面的用戶端叫用 [**PMGM 剪除 \_ \_ 警示 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="848a3-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




