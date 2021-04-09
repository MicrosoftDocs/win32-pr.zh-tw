---
title: 服務的指導方針
description: 服務應遵守這些指導方針，以確保重新開機管理員可以在必要時關閉和重新開機服務，以安裝更新。 應用程式可以使用應用程式指導方針中所述的指導方針。
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51374c0a4c6fc561b8259aadf15e3d5487e12483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023817"
---
# <a name="guidelines-for-services"></a><span data-ttu-id="62808-104">服務的指導方針</span><span class="sxs-lookup"><span data-stu-id="62808-104">Guidelines for Services</span></span>

<span data-ttu-id="62808-105">服務應遵守這些指導方針，以確保重新開機管理員可以在必要時關閉和重新開機服務，以安裝更新。</span><span class="sxs-lookup"><span data-stu-id="62808-105">Services should adhere to these guidelines to ensure that the Restart Manager can shut down and restart services if necessary to install updates.</span></span> <span data-ttu-id="62808-106">應用程式可以使用 [應用程式指導方針](guidelines-for-applications.md)中所述的指導方針。</span><span class="sxs-lookup"><span data-stu-id="62808-106">Applications can use the guidelines that are described in [Guidelines for Applications](guidelines-for-applications.md).</span></span>

-   <span data-ttu-id="62808-107">服務應該能夠使用 [服務控制管理員](/windows/desktop/Services/service-control-manager) 來關閉和重新開機，而不需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="62808-107">Services should be capable of being shut down and restarted using the [Service Control Manager](/windows/desktop/Services/service-control-manager) without requiring a system restart.</span></span> <span data-ttu-id="62808-108">此指導方針的例外狀況是在 lsass.exe 或 services.exe 內容中執行的重要系統進程。</span><span class="sxs-lookup"><span data-stu-id="62808-108">The exceptions to this guideline are critical system processes that run in the context of lsass.exe or services.exe.</span></span>
-   <span data-ttu-id="62808-109">重新開機管理員會接受服務相關性。</span><span class="sxs-lookup"><span data-stu-id="62808-109">Restart Manager honors service dependencies.</span></span> <span data-ttu-id="62808-110">當服務關閉並重新啟動時，其相依服務會關閉並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="62808-110">When a service is shut down and restarted, its dependent services are shut down and restarted.</span></span>
-   <span data-ttu-id="62808-111">服務應該會在 [服務控制管理員 (SCM) ](/windows/desktop/Services/service-control-manager)中指定復原間隔和重設期間。</span><span class="sxs-lookup"><span data-stu-id="62808-111">Services should specify the recovery interval and reset period in the [Service Control Manager (SCM)](/windows/desktop/Services/service-control-manager).</span></span> <span data-ttu-id="62808-112">復原間隔是 SCM 在取得復原動作之前等候的最後一次失敗之後的時間（以毫秒為間隔）。</span><span class="sxs-lookup"><span data-stu-id="62808-112">The recovery interval is the time, in msecs, after the last failure that the SCM waits before taking the recovery action.</span></span> <span data-ttu-id="62808-113">重設期間是在最後一次失敗之後，服務控制管理員在將失敗計數重設為0之前等候的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="62808-113">The reset period is the time, in seconds, after the last failure that the Service Control Manager waits before resetting the failure count to 0.</span></span> <span data-ttu-id="62808-114">服務可以使用 [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) 函數來變更設定。</span><span class="sxs-lookup"><span data-stu-id="62808-114">Services can use [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) function to change the configuration settings.</span></span>

    <span data-ttu-id="62808-115">[重要服務](critical-system-services.md) 應該使用下列復原設定，指定在第一次失敗之後重新開機服務、在第二次失敗後重新開機兩分鐘，以及在第三次失敗之後重新開機電腦一分鐘。</span><span class="sxs-lookup"><span data-stu-id="62808-115">[Critical services](critical-system-services.md) should use the following recovery settings to specify that the service be restarted one minute after the first failure to restart the service, restarted two minutes after the second failure, and that the computer be restarted one minute after the third failure.</span></span> <span data-ttu-id="62808-116">失敗計數會在300秒後重設為0。</span><span class="sxs-lookup"><span data-stu-id="62808-116">The failure count is reset to 0 after 300 seconds.</span></span>

    <dl> <span data-ttu-id="62808-117">復原動作：重新開機/60000/重新開機/120000/重新開機/60000 & 重設 = 300</span><span class="sxs-lookup"><span data-stu-id="62808-117">Recovery Actions: Restart/60000/Restart/120000/Reboot/60000 & Reset =300</span></span>  
    </dl>

    <span data-ttu-id="62808-118">[重要服務](critical-system-services.md) 應該在非關鍵服務之前啟動。</span><span class="sxs-lookup"><span data-stu-id="62808-118">[Critical services](critical-system-services.md) should be started before non-critical services.</span></span> <span data-ttu-id="62808-119">非關鍵服務的服務應該使用下列復原設定，指定在第一次失敗之後，重新開機服務兩分鐘。</span><span class="sxs-lookup"><span data-stu-id="62808-119">Services that are not critical services should use the following recovery settings to specify that the service be restarted two minutes after the first failure to restart the service.</span></span> <span data-ttu-id="62808-120">這項服務不會在第二次失敗之後重新開機，而且系統管理員必須在這種情況下介入。</span><span class="sxs-lookup"><span data-stu-id="62808-120">The service is not restarted after the second failure, and an administrator would need to intervene in this case.</span></span> <span data-ttu-id="62808-121">失敗計數會在900秒後重設為0。</span><span class="sxs-lookup"><span data-stu-id="62808-121">The failure count is reset to 0 after 900 seconds.</span></span>

    <dl> <span data-ttu-id="62808-122">復原動作： Restart/120000/Restart/300000/None/0 & Reset = 900</span><span class="sxs-lookup"><span data-stu-id="62808-122">Recovery Actions: Restart/120000/Restart/300000/None/0 & Reset = 900</span></span>  
    </dl>

 

 