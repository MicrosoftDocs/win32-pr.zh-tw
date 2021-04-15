---
description: 下列範例可用來作為支援單一服務之服務程式的進入點。
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: 撰寫服務程式 Main 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511200"
---
# <a name="writing-a-service-programs-main-function"></a><span data-ttu-id="ae34a-103">撰寫服務程式的 main 函數</span><span class="sxs-lookup"><span data-stu-id="ae34a-103">Writing a Service Program's main Function</span></span>

<span data-ttu-id="ae34a-104">[服務程式](service-programs.md)的 **main** 函式會呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)函式，以連接至 [服務控制管理員](service-control-manager.md) (SCM) 並啟動控制發送器執行緒。</span><span class="sxs-lookup"><span data-stu-id="ae34a-104">The **main** function of a [service program](service-programs.md) calls the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function to connect to the [service control manager](service-control-manager.md) (SCM) and start the control dispatcher thread.</span></span> <span data-ttu-id="ae34a-105">發送器執行緒會迴圈，等候分派資料表中指定之服務的傳入控制項要求。</span><span class="sxs-lookup"><span data-stu-id="ae34a-105">The dispatcher thread loops, waiting for incoming control requests for the services specified in the dispatch table.</span></span> <span data-ttu-id="ae34a-106">當發生錯誤或進程中的所有服務都已結束時，這個執行緒就會傳回。</span><span class="sxs-lookup"><span data-stu-id="ae34a-106">This thread returns when there is an error or when all of the services in the process have terminated.</span></span> <span data-ttu-id="ae34a-107">當進程中的所有服務都已結束時，SCM 會將控制項要求傳送給發送器執行緒，告知其結束。</span><span class="sxs-lookup"><span data-stu-id="ae34a-107">When all services in the process have terminated, the SCM sends a control request to the dispatcher thread telling it to exit.</span></span> <span data-ttu-id="ae34a-108">此執行緒接著會從 **StartServiceCtrlDispatcher** 呼叫傳回，而且進程可以終止。</span><span class="sxs-lookup"><span data-stu-id="ae34a-108">This thread then returns from the **StartServiceCtrlDispatcher** call and the process can terminate.</span></span>

<span data-ttu-id="ae34a-109">此範例中使用下列全域定義。</span><span class="sxs-lookup"><span data-stu-id="ae34a-109">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="ae34a-110">下列範例可用來作為支援單一服務之服務程式的進入點。</span><span class="sxs-lookup"><span data-stu-id="ae34a-110">The following example can be used as the entry point for a service program that supports a single service.</span></span> <span data-ttu-id="ae34a-111">如果您的服務程式支援多個服務，請將其他服務的名稱新增至分派資料表，以便發送器執行緒監視這些服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae34a-111">If your service program supports multiple services, add the names of the additional services to the dispatch table so they can be monitored by the dispatcher thread.</span></span>

<span data-ttu-id="ae34a-112">Tmain 函式 \_ 是進入點。</span><span class="sxs-lookup"><span data-stu-id="ae34a-112">The \_tmain function is the entry point.</span></span> <span data-ttu-id="ae34a-113">SvcReportEvent 函數會將參考用訊息和錯誤寫入事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="ae34a-113">The SvcReportEvent function writes informational messages and errors to the event log.</span></span> <span data-ttu-id="ae34a-114">如需撰寫 SvcMain 函式的詳細資訊，請參閱 [撰寫 ServiceMain 函數](writing-a-servicemain-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ae34a-114">For information about writing the SvcMain function, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span> <span data-ttu-id="ae34a-115">如需 SvcInstall 函數的詳細資訊，請參閱 [安裝服務](installing-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="ae34a-115">For more information about the SvcInstall function, see [Installing a Service](installing-a-service.md).</span></span> <span data-ttu-id="ae34a-116">如需撰寫 SvcCtrlHandler 函式的詳細資訊，請參閱 [撰寫控制項處理常式函數](writing-a-control-handler-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ae34a-116">For information about writing the SvcCtrlHandler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span> <span data-ttu-id="ae34a-117">如需完整的範例服務，包括 SvcReportEvent 函數的來源，請參閱 [.svc](svc-cpp.md)。</span><span class="sxs-lookup"><span data-stu-id="ae34a-117">For the complete example service, including the source for the SvcReportEvent function, see [Svc.cpp](svc-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



<span data-ttu-id="ae34a-118">以下是訊息編譯器所產生的範例 .h 範例。</span><span class="sxs-lookup"><span data-stu-id="ae34a-118">The following is an example Sample.h as generated by the message compiler.</span></span> <span data-ttu-id="ae34a-119">如需詳細資訊，請參閱 [Sample.mc](sample-mc.md)。</span><span class="sxs-lookup"><span data-stu-id="ae34a-119">For more information, see [Sample.mc](sample-mc.md).</span></span>

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a><span data-ttu-id="ae34a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae34a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae34a-121">服務進入點</span><span class="sxs-lookup"><span data-stu-id="ae34a-121">Service Entry Point</span></span>](service-entry-point.md)
</dt> <dt>

[<span data-ttu-id="ae34a-122">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="ae34a-122">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



