---
description: 本節說明 NPP 方法所使用的 NPP 結構。
ms.assetid: f0729dc5-6b5f-4f24-85d6-47c45f1bf9be
title: NPP 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b514bded37450f6a7c33a016b231bb38f0c1812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973680"
---
# <a name="npp-structures"></a><span data-ttu-id="3c557-103">NPP 結構</span><span class="sxs-lookup"><span data-stu-id="3c557-103">NPP Structures</span></span>

<span data-ttu-id="3c557-104">本節說明 NPP 方法所使用的 NPP 結構。</span><span class="sxs-lookup"><span data-stu-id="3c557-104">This section describes the NPP structures used by NPP methods.</span></span> <span data-ttu-id="3c557-105">這些結構是用來取出統計資料、提供系統狀態和統計資訊，以及指出哪些電腦正在執行網路監視器。</span><span class="sxs-lookup"><span data-stu-id="3c557-105">These structures are used to retrieve statistics, provide system status and statistical information, and indicate which computers are running Network Monitor.</span></span> <span data-ttu-id="3c557-106">下表描述這些結構。</span><span class="sxs-lookup"><span data-stu-id="3c557-106">The following tables describes these structures.</span></span>



| <span data-ttu-id="3c557-107">NPP 結構</span><span class="sxs-lookup"><span data-stu-id="3c557-107">NPP Structures</span></span>                     | <span data-ttu-id="3c557-108">Description</span><span class="sxs-lookup"><span data-stu-id="3c557-108">Description</span></span>                                                                                                                      |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c557-109">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="3c557-109">SESSIONSTATS</span></span>](sessionstats.md)   | <span data-ttu-id="3c557-110">提供抓取交談統計資料時的會話資訊。</span><span class="sxs-lookup"><span data-stu-id="3c557-110">Provides session information when conversation statistics are retrieved.</span></span>                                                         |
| [<span data-ttu-id="3c557-111">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="3c557-111">STATIONSTATS</span></span>](stationstats.md)   | <span data-ttu-id="3c557-112">提供特定 [*工作站*](s.md)的相關統計資料。</span><span class="sxs-lookup"><span data-stu-id="3c557-112">Provides statistics about a specific [*station*](s.md).</span></span>                                                     |
| [<span data-ttu-id="3c557-113">統計</span><span class="sxs-lookup"><span data-stu-id="3c557-113">STATISTICS</span></span>](statistics.md)       | <span data-ttu-id="3c557-114">提供在抓取統計資料和目前的捕獲暫停或停止時的網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="3c557-114">Provides network statistics when total statistics are retrieved and when the current capture has paused or stopped.</span></span>              |
| [<span data-ttu-id="3c557-115">透視</span><span class="sxs-lookup"><span data-stu-id="3c557-115">QUERYTABLE</span></span>](querytable.md)       | <span data-ttu-id="3c557-116">指出哪些電腦正在使用網路監視器。</span><span class="sxs-lookup"><span data-stu-id="3c557-116">Indicates which computers are using Network Monitor.</span></span>                                                                             |
| [<span data-ttu-id="3c557-117">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="3c557-117">STATIONQUERY</span></span>](stationquery.md)   | <span data-ttu-id="3c557-118">提供使用網路監視器之電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c557-118">Provides information about a computer that is using Network Monitor.</span></span> <span data-ttu-id="3c557-119">此 **結構是由 NPP 的** 工作方式結構所使用。</span><span class="sxs-lookup"><span data-stu-id="3c557-119">This structure is used by the NPP **QUERYTABLE** structure.</span></span> |
| [<span data-ttu-id="3c557-120">>NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="3c557-120">NETWORKSTATUS</span></span>](networkstatus.md) | <span data-ttu-id="3c557-121">根據系統狀態提供目前的網路狀態。</span><span class="sxs-lookup"><span data-stu-id="3c557-121">Provides current network status in terms of system state.</span></span>                                                                        |



 

 

 



