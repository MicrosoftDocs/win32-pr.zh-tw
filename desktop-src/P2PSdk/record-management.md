---
description: 若要記錄管理，您可以使用儲存在對等記錄結構中的資訊 \_ 。
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: 記錄管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977070"
---
# <a name="record-management"></a><span data-ttu-id="88265-103">記錄管理</span><span class="sxs-lookup"><span data-stu-id="88265-103">Record Management</span></span>

<span data-ttu-id="88265-104">若要記錄管理，您可以使用儲存在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record) 結構中的資訊。</span><span class="sxs-lookup"><span data-stu-id="88265-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="88265-105">當記錄建立、更新或刪除時，對圖表所做的變更會複寫到所有節點。</span><span class="sxs-lookup"><span data-stu-id="88265-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="88265-106">下表將識別更新和自動重新整理記錄的規則。</span><span class="sxs-lookup"><span data-stu-id="88265-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="88265-107">管理工作</span><span class="sxs-lookup"><span data-stu-id="88265-107">Management Task</span></span>     | <span data-ttu-id="88265-108">規則</span><span class="sxs-lookup"><span data-stu-id="88265-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88265-109">更新記錄</span><span class="sxs-lookup"><span data-stu-id="88265-109">Updating a record</span></span>   | <span data-ttu-id="88265-110">將到期時間保持不變或增加。</span><span class="sxs-lookup"><span data-stu-id="88265-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="88265-111">您無法縮短到期時間。</span><span class="sxs-lookup"><span data-stu-id="88265-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="88265-112">重新整理記錄</span><span class="sxs-lookup"><span data-stu-id="88265-112">Refreshing a record</span></span> | <span data-ttu-id="88265-113">使用 [**對等 \_ 記錄 \_ 旗標 \_ 自動重新整理**](/windows/desktop/api/P2P/ns-p2p-peer_record) 旗標來自動重新整理記錄。</span><span class="sxs-lookup"><span data-stu-id="88265-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="88265-114">只有當發行記錄的節點在線上時，才使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="88265-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="88265-115">否則，請不要使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="88265-115">Otherwise, do not use this flag.</span></span> |



 

 

 



