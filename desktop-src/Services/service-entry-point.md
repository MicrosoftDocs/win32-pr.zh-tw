---
description: 服務通常會撰寫為主控台應用程式。
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: 服務進入點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943360"
---
# <a name="service-entry-point"></a><span data-ttu-id="7acad-103">服務進入點</span><span class="sxs-lookup"><span data-stu-id="7acad-103">Service Entry Point</span></span>

<span data-ttu-id="7acad-104">服務通常會撰寫為主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="7acad-104">Services are generally written as console applications.</span></span> <span data-ttu-id="7acad-105">主控台應用程式的進入點是它的 **主要** 功能。</span><span class="sxs-lookup"><span data-stu-id="7acad-105">The entry point of a console application is its **main** function.</span></span> <span data-ttu-id="7acad-106">**Main** 函數會從服務的登錄機碼接收 **ImagePath** 值的引數。</span><span class="sxs-lookup"><span data-stu-id="7acad-106">The **main** function receives arguments from the **ImagePath** value from the registry key for the service.</span></span> <span data-ttu-id="7acad-107">如需詳細資訊，請參閱 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="7acad-107">For more information, see the Remarks section of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="7acad-108">當 SCM 啟動服務程式時，它會等候它呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 函數。</span><span class="sxs-lookup"><span data-stu-id="7acad-108">When the SCM starts a service program, it waits for it to call the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function.</span></span> <span data-ttu-id="7acad-109">使用下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="7acad-109">Use the following guidelines.</span></span>

-   <span data-ttu-id="7acad-110">服務 \_ WIN32 專屬進程的服務 \_ \_ 應該立即從其主執行緒呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 。</span><span class="sxs-lookup"><span data-stu-id="7acad-110">A service of type SERVICE\_WIN32\_OWN\_PROCESS should call [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) immediately, from its main thread.</span></span> <span data-ttu-id="7acad-111">您可以在服務啟動後執行任何初始化，如 [服務 ServiceMain](service-servicemain-function.md)函式中所述。</span><span class="sxs-lookup"><span data-stu-id="7acad-111">You can perform any initialization after the service starts, as described in [Service ServiceMain Function](service-servicemain-function.md).</span></span>
-   <span data-ttu-id="7acad-112">如果服務類型是服務 \_ WIN32 \_ 共用進程， \_ 而且程式中的所有服務都有一般的初始化，您可以在呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)之前，在主執行緒中執行初始化，只要它花費的時間不超過30秒。</span><span class="sxs-lookup"><span data-stu-id="7acad-112">If the service type is SERVICE\_WIN32\_SHARE\_PROCESS and there is common initialization for all services in the program, you can perform the initialization in the main thread before calling [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), as long as it takes less than 30 seconds.</span></span> <span data-ttu-id="7acad-113">否則，您必須建立另一個執行緒來進行一般初始化，而主執行緒會呼叫 **StartServiceCtrlDispatcher**。</span><span class="sxs-lookup"><span data-stu-id="7acad-113">Otherwise, you must create another thread to do the common initialization, while the main thread calls **StartServiceCtrlDispatcher**.</span></span> <span data-ttu-id="7acad-114">在服務啟動之後，您仍然應該執行任何服務特定的初始化。</span><span class="sxs-lookup"><span data-stu-id="7acad-114">You should still perform any service-specific initialization after the service starts.</span></span>

<span data-ttu-id="7acad-115">[**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)函式會針對進程中包含的每個服務，使用 [**服務 \_ 資料表 \_ 專案**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya)結構。</span><span class="sxs-lookup"><span data-stu-id="7acad-115">The [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function takes a [**SERVICE\_TABLE\_ENTRY**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) structure for each service contained in the process.</span></span> <span data-ttu-id="7acad-116">每個結構會指定服務的服務名稱和進入點。</span><span class="sxs-lookup"><span data-stu-id="7acad-116">Each structure specifies the service name and the entry point for the service.</span></span> <span data-ttu-id="7acad-117">如需範例，請參閱 [撰寫服務程式的主要功能](writing-a-service-program-s-main-function.md)。</span><span class="sxs-lookup"><span data-stu-id="7acad-117">For an example, see [Writing a Service Program's main Function](writing-a-service-program-s-main-function.md).</span></span>

<span data-ttu-id="7acad-118">如果 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) 成功，則在進程中的所有執行中服務都進入服務停止狀態之前，呼叫的執行緒不會傳回 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7acad-118">If [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) succeeds, the calling thread does not return until all running services in the process have entered the SERVICE\_STOPPED state.</span></span> <span data-ttu-id="7acad-119">SCM 會透過具名管道將控制項要求傳送至此執行緒。</span><span class="sxs-lookup"><span data-stu-id="7acad-119">The SCM sends control requests to this thread through a named pipe.</span></span> <span data-ttu-id="7acad-120">執行緒會作為控制項發送器，執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="7acad-120">The thread acts as a control dispatcher, performing the following tasks:</span></span>

-   <span data-ttu-id="7acad-121">建立新的執行緒，以在新服務啟動時呼叫適當的進入點。</span><span class="sxs-lookup"><span data-stu-id="7acad-121">Create a new thread to call the appropriate entry point when a new service is started.</span></span>
-   <span data-ttu-id="7acad-122">呼叫適當的 [處理常式](service-control-handler-function.md) 函式來處理服務控制要求。</span><span class="sxs-lookup"><span data-stu-id="7acad-122">Call the appropriate [handler function](service-control-handler-function.md) to handle service control requests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7acad-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="7acad-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7acad-124">撰寫服務程式的 main 函數</span><span class="sxs-lookup"><span data-stu-id="7acad-124">Writing a Service Program's main Function</span></span>](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



