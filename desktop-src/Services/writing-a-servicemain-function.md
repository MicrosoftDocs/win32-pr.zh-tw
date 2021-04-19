---
description: 下列範例中的 SvcMain 函數是範例服務的 ServiceMain 函式。
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: 撰寫 ServiceMain 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997082"
---
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="da2d8-103">撰寫 ServiceMain 函式</span><span class="sxs-lookup"><span data-stu-id="da2d8-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="da2d8-104">下列範例中的 SvcMain 函數是範例服務的 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函式。</span><span class="sxs-lookup"><span data-stu-id="da2d8-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="da2d8-105">SvcMain 可讓您存取服務的命令列引數，就像是主控台應用程式的 **主要** 功能一樣。</span><span class="sxs-lookup"><span data-stu-id="da2d8-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="da2d8-106">第一個參數包含在第二個參數中傳遞至服務的引數數目。</span><span class="sxs-lookup"><span data-stu-id="da2d8-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="da2d8-107">一律會有至少一個引數。</span><span class="sxs-lookup"><span data-stu-id="da2d8-107">There will always be at least one argument.</span></span> <span data-ttu-id="da2d8-108">第二個參數是字串指標陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="da2d8-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="da2d8-109">陣列中的第一個專案一律是服務名稱。</span><span class="sxs-lookup"><span data-stu-id="da2d8-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="da2d8-110">SvcMain 函式會先呼叫 [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) 函式，將 SvcCtrlHandler 函式註冊為服務的 [**處理**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 函式，並開始初始化。</span><span class="sxs-lookup"><span data-stu-id="da2d8-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="da2d8-111">**RegisterServiceCtrlHandler** 應該是 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)中的第一個 nonfailing 函式，因此，如果發生錯誤，服務可以使用此函 [](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)式所傳回的狀態控制碼來呼叫具有服務 \_ 停止狀態的 >setservicestatus。</span><span class="sxs-lookup"><span data-stu-id="da2d8-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="da2d8-112">接下來，SvcMain 函式會呼叫 ReportSvcStatus 函式，以指出其初始狀態為 \_ 「服務開始暫止」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="da2d8-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="da2d8-113">當服務處於這種狀態時，就不會接受任何控制項。</span><span class="sxs-lookup"><span data-stu-id="da2d8-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="da2d8-114">若要簡化服務的邏輯，建議服務在執行初始化時，不接受任何控制項。</span><span class="sxs-lookup"><span data-stu-id="da2d8-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="da2d8-115">最後，SvcMain 函式會呼叫 SvcInit 函式來執行服務特定的初始化，並開始服務所要執行的工作。</span><span class="sxs-lookup"><span data-stu-id="da2d8-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="da2d8-116">範例初始化函式 SvcInit 是非常簡單的範例;它不會執行更複雜的初始化工作，例如建立額外的執行緒。</span><span class="sxs-lookup"><span data-stu-id="da2d8-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="da2d8-117">它會建立一個事件，讓服務控制處理常式可以表示服務應該停止，然後呼叫 ReportSvcStatus 來指出服務已進入執行中的服務 \_ 狀態。</span><span class="sxs-lookup"><span data-stu-id="da2d8-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="da2d8-118">此時，服務已完成初始化，並已準備好接受控制項。</span><span class="sxs-lookup"><span data-stu-id="da2d8-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="da2d8-119">為了達到最佳的系統效能，您的應用程式應在25-100 毫秒內進入執行狀態。</span><span class="sxs-lookup"><span data-stu-id="da2d8-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="da2d8-120">因為此範例服務不會完成任何實際工作，SvcInit 只會等候服務停止事件透過呼叫 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) 函式來發出信號、呼叫 ReportSvcStatus 以表示服務已進入服務 \_ 停止狀態，然後傳回。</span><span class="sxs-lookup"><span data-stu-id="da2d8-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="da2d8-121"> (請注意，函式必須傳回，而不是呼叫 [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) 函式，因為傳回可讓您清除配置給引數的記憶體。 ) 您可以使用 [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) 函數來執行其他清除工作，而不是 **WaitForSingleObject**。</span><span class="sxs-lookup"><span data-stu-id="da2d8-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="da2d8-122">正在執行 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函式的執行緒會終止，但服務本身會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="da2d8-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="da2d8-123">當服務控制處理常式對事件發出信號時，執行緒集區中的執行緒會執行您的回呼來執行其他清除，包括將狀態設定為 [ \_ 已停止]。</span><span class="sxs-lookup"><span data-stu-id="da2d8-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="da2d8-124">請注意，此範例會使用 SvcReportEvent 將錯誤事件寫入事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="da2d8-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="da2d8-125">如需 SvcReportEvent 的原始程式碼，請參閱 [.svc .cpp](svc-cpp.md)。</span><span class="sxs-lookup"><span data-stu-id="da2d8-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="da2d8-126">如需範例控制項處理常式函式，請參閱 [撰寫控制項處理常式函數](writing-a-control-handler-function.md)。</span><span class="sxs-lookup"><span data-stu-id="da2d8-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="da2d8-127">此範例中使用下列全域定義。</span><span class="sxs-lookup"><span data-stu-id="da2d8-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="da2d8-128">下列範例片段取自完整的服務範例。</span><span class="sxs-lookup"><span data-stu-id="da2d8-128">The following sample fragment is taken from the complete service sample.</span></span>


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a><span data-ttu-id="da2d8-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="da2d8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da2d8-130">服務 ServiceMain 函式</span><span class="sxs-lookup"><span data-stu-id="da2d8-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="da2d8-131">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="da2d8-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
