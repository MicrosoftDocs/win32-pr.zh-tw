---
description: 服務控制程式會啟動並控制服務。
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: 服務控制程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847923"
---
# <a name="service-control-programs"></a><span data-ttu-id="b6e00-103">服務控制程式</span><span class="sxs-lookup"><span data-stu-id="b6e00-103">Service Control Programs</span></span>

<span data-ttu-id="b6e00-104">服務控制程式會啟動並控制服務。</span><span class="sxs-lookup"><span data-stu-id="b6e00-104">A service control program starts and controls services.</span></span> <span data-ttu-id="b6e00-105">其會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="b6e00-105">It performs the following actions:</span></span>

-   <span data-ttu-id="b6e00-106">啟動服務或驅動程式服務（如果啟動類型是服務 \_ 需求 \_ 開始）。</span><span class="sxs-lookup"><span data-stu-id="b6e00-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="b6e00-107">將控制要求傳送至執行中的服務。</span><span class="sxs-lookup"><span data-stu-id="b6e00-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="b6e00-108">查詢正在執行之服務的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b6e00-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="b6e00-109">這些動作需要服務物件的開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="b6e00-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="b6e00-110">若要取得控制碼，服務控制程式必須：</span><span class="sxs-lookup"><span data-stu-id="b6e00-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="b6e00-111">您可以使用 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式來取得指定電腦上之 SCM 資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b6e00-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="b6e00-112">使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) 或 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數來取得服務物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b6e00-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="b6e00-113">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="b6e00-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b6e00-114">服務啟動</span><span class="sxs-lookup"><span data-stu-id="b6e00-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="b6e00-115">服務控制要求</span><span class="sxs-lookup"><span data-stu-id="b6e00-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="b6e00-116">使用 SC 控制服務</span><span class="sxs-lookup"><span data-stu-id="b6e00-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 



