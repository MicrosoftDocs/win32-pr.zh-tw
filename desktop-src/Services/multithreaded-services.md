---
description: 服務控制管理員 (SCM) 會將服務控制事件傳送至服務控制處理常式常式，藉以控制服務。
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: 多執行緒服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991907"
---
# <a name="multithreaded-services"></a><span data-ttu-id="6cecc-103">多執行緒服務</span><span class="sxs-lookup"><span data-stu-id="6cecc-103">Multithreaded Services</span></span>

<span data-ttu-id="6cecc-104">服務控制管理員 (SCM) 會將服務控制事件傳送至服務的控制處理常式常式，藉以控制服務。</span><span class="sxs-lookup"><span data-stu-id="6cecc-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="6cecc-105">服務必須及時地回應控制事件，讓 SCM 可以追蹤服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="6cecc-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="6cecc-106">此外，服務的狀態必須符合 SCM 所接收之狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="6cecc-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="6cecc-107">由於服務與 SCM 之間的通訊機制，在服務中使用多個執行緒時，您必須特別小心。</span><span class="sxs-lookup"><span data-stu-id="6cecc-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="6cecc-108">當服務指示由 SCM 停止時，它必須等待所有線程結束，然後再向 SCM 報表服務已停止。</span><span class="sxs-lookup"><span data-stu-id="6cecc-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="6cecc-109">否則，SCM 可能會混淆服務的狀態，而且可能無法正確關閉。</span><span class="sxs-lookup"><span data-stu-id="6cecc-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="6cecc-110">SCM 必須收到通知，表示服務正在回應停止控制事件，且正在停止服務。</span><span class="sxs-lookup"><span data-stu-id="6cecc-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="6cecc-111">如果 [**)  (**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 服務在 **>setservicestatus** 的前一次呼叫中所指定的時間內 (wait 提示) 所指定的時間內，且檢查點更新為大於先前呼叫 **>setservicestatus** 所指定的檢查點，則 SCM 會假設服務正在進行中。</span><span class="sxs-lookup"><span data-stu-id="6cecc-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="6cecc-112">如果服務向 SCM 回報在所有線程都結束之前已停止，則 SCM 可能會將其解釋為衝突。</span><span class="sxs-lookup"><span data-stu-id="6cecc-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="6cecc-113">這可能會導致無法停止或重新開機服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="6cecc-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 



