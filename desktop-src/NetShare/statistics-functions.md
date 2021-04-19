---
description: Windows 作業系統會從工作站或伺服器服務啟動時，累積工作站和伺服器的一組操作統計資料。
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Statistics 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979959"
---
# <a name="statistics-functions"></a><span data-ttu-id="8cfe8-103">Statistics 函數</span><span class="sxs-lookup"><span data-stu-id="8cfe8-103">Statistics Functions</span></span>

<span data-ttu-id="8cfe8-104">Windows 作業系統會從工作站或伺服器服務啟動時，累積工作站和伺服器的一組操作統計資料。</span><span class="sxs-lookup"><span data-stu-id="8cfe8-104">The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.</span></span> <span data-ttu-id="8cfe8-105">若要取得這些統計資料，您可以呼叫下列網路管理統計資料函數。</span><span class="sxs-lookup"><span data-stu-id="8cfe8-105">To retrieve these statistics, you can call the following network management statistics function.</span></span>



| <span data-ttu-id="8cfe8-106">函式</span><span class="sxs-lookup"><span data-stu-id="8cfe8-106">Function</span></span>                                     | <span data-ttu-id="8cfe8-107">描述</span><span class="sxs-lookup"><span data-stu-id="8cfe8-107">Description</span></span>                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cfe8-108">**NetStatisticsGet**</span><span class="sxs-lookup"><span data-stu-id="8cfe8-108">**NetStatisticsGet**</span></span>](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | <span data-ttu-id="8cfe8-109">捕獲服務的作業統計資料;支援工作站和伺服器服務。</span><span class="sxs-lookup"><span data-stu-id="8cfe8-109">Retrieves operating statistics for a service; supports the workstation and server services.</span></span> |



 

<span data-ttu-id="8cfe8-110">要求工作站統計資料時， **NetStatisticsGet** 函式會傳回 [**stat \_ 工作站 \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) 結構; 當要求伺服器統計資料時，此函數會傳回 [**stat \_ server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) 結構。</span><span class="sxs-lookup"><span data-stu-id="8cfe8-110">The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) structure when server statistics are requested.</span></span>

 

 



