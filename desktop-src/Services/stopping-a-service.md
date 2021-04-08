---
description: 服務控制程式可以使用 ControlService 函式來傳送服務 \_ 控制停止要求，藉以停止服務 \_ 。
ms.assetid: fe16d2a8-3e66-49cc-b9c7-fffbc206e8d3
title: 停止服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb9625dd674623823341c1465964095de7efaf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852059"
---
# <a name="stopping-a-service"></a><span data-ttu-id="cce10-103">停止服務</span><span class="sxs-lookup"><span data-stu-id="cce10-103">Stopping a Service</span></span>

<span data-ttu-id="cce10-104">[服務控制程式](service-control-programs.md)可以使用 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)函式來傳送服務 \_ 控制停止要求，藉以停止服務 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cce10-104">A [service control program](service-control-programs.md) can stop a service by using the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to send a SERVICE\_CONTROL\_STOP request.</span></span> <span data-ttu-id="cce10-105">如果 [服務控制管理員](service-control-manager.md) (SCM) 接收服務的服務 \_ 控制 \_ 停止要求，則會將要求轉送至服務的 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函式，藉此指示服務停止。</span><span class="sxs-lookup"><span data-stu-id="cce10-105">If the [service control manager](service-control-manager.md) (SCM) receives a SERVICE\_CONTROL\_STOP request for a service, it instructs the service to stop by forwarding the request to the service's [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function.</span></span> <span data-ttu-id="cce10-106">但是，如果 SCM 判斷其他執行中的服務相依于指定的服務，它就不會轉寄停止要求。</span><span class="sxs-lookup"><span data-stu-id="cce10-106">However, if the SCM determines that other running services are dependent on the specified service, it will not forward the stop request.</span></span> <span data-ttu-id="cce10-107">相反地，它會傳回執行 \_ 的錯誤相依 \_ 服務 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cce10-107">Instead, it returns ERROR\_DEPENDENT\_SERVICES\_RUNNING.</span></span> <span data-ttu-id="cce10-108">因此，若要以程式設計方式停止這類服務，您必須先列舉和停止其相依的服務。</span><span class="sxs-lookup"><span data-stu-id="cce10-108">Therefore, to programmatically stop such a service, you must first enumerate and stop its dependent services.</span></span>

<span data-ttu-id="cce10-109">下列範例中的 DoStopSvc 函數示範如何停止服務和任何相依的服務。</span><span class="sxs-lookup"><span data-stu-id="cce10-109">The DoStopSvc function in the following example shows how to stop a service and any dependent services.</span></span> <span data-ttu-id="cce10-110">SzSvcName 變數是全域變數，其中包含要停止之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="cce10-110">The szSvcName variable is a global variable that contains the name of the service to be stopped.</span></span> <span data-ttu-id="cce10-111">如需設定此變數的完整範例，請參閱 [SvcControl .cpp](svccontrol-cpp.md)。</span><span class="sxs-lookup"><span data-stu-id="cce10-111">For the complete example that sets this variable, see [SvcControl.cpp](svccontrol-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Stops the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoStopSvc()
{
    SERVICE_STATUS_PROCESS ssp;
    DWORD dwStartTime = GetTickCount();
    DWORD dwBytesNeeded;
    DWORD dwTimeout = 30000; // 30-second time-out
    DWORD dwWaitTime;

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,         // SCM database 
        szSvcName,            // name of service 
        SERVICE_STOP | 
        SERVICE_QUERY_STATUS | 
        SERVICE_ENUMERATE_DEPENDENTS);  
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Make sure the service is not already stopped.

    if ( !QueryServiceStatusEx( 
            schService, 
            SC_STATUS_PROCESS_INFO,
            (LPBYTE)&ssp, 
            sizeof(SERVICE_STATUS_PROCESS),
            &dwBytesNeeded ) )
    {
        printf("QueryServiceStatusEx failed (%d)\n", GetLastError()); 
        goto stop_cleanup;
    }

    if ( ssp.dwCurrentState == SERVICE_STOPPED )
    {
        printf("Service is already stopped.\n");
        goto stop_cleanup;
    }

    // If a stop is pending, wait for it.

    while ( ssp.dwCurrentState == SERVICE_STOP_PENDING ) 
    {
        printf("Service stop pending...\n");

        // Do not wait longer than the wait hint. A good interval is 
        // one-tenth of the wait hint but not less than 1 second  
        // and not more than 10 seconds. 
 
        dwWaitTime = ssp.dwWaitHint / 10;

        if( dwWaitTime < 1000 )
            dwWaitTime = 1000;
        else if ( dwWaitTime > 10000 )
            dwWaitTime = 10000;

        Sleep( dwWaitTime );

        if ( !QueryServiceStatusEx( 
                 schService, 
                 SC_STATUS_PROCESS_INFO,
                 (LPBYTE)&ssp, 
                 sizeof(SERVICE_STATUS_PROCESS),
                 &dwBytesNeeded ) )
        {
            printf("QueryServiceStatusEx failed (%d)\n", GetLastError()); 
            goto stop_cleanup;
        }

        if ( ssp.dwCurrentState == SERVICE_STOPPED )
        {
            printf("Service stopped successfully.\n");
            goto stop_cleanup;
        }

        if ( GetTickCount() - dwStartTime > dwTimeout )
        {
            printf("Service stop timed out.\n");
            goto stop_cleanup;
        }
    }

    // If the service is running, dependencies must be stopped first.

    StopDependentServices();

    // Send a stop code to the service.

    if ( !ControlService( 
            schService, 
            SERVICE_CONTROL_STOP, 
            (LPSERVICE_STATUS) &ssp ) )
    {
        printf( "ControlService failed (%d)\n", GetLastError() );
        goto stop_cleanup;
    }

    // Wait for the service to stop.

    while ( ssp.dwCurrentState != SERVICE_STOPPED ) 
    {
        Sleep( ssp.dwWaitHint );
        if ( !QueryServiceStatusEx( 
                schService, 
                SC_STATUS_PROCESS_INFO,
                (LPBYTE)&ssp, 
                sizeof(SERVICE_STATUS_PROCESS),
                &dwBytesNeeded ) )
        {
            printf( "QueryServiceStatusEx failed (%d)\n", GetLastError() );
            goto stop_cleanup;
        }

        if ( ssp.dwCurrentState == SERVICE_STOPPED )
            break;

        if ( GetTickCount() - dwStartTime > dwTimeout )
        {
            printf( "Wait timed out\n" );
            goto stop_cleanup;
        }
    }
    printf("Service stopped successfully\n");

stop_cleanup:
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

BOOL __stdcall StopDependentServices()
{
    DWORD i;
    DWORD dwBytesNeeded;
    DWORD dwCount;

    LPENUM_SERVICE_STATUS   lpDependencies = NULL;
    ENUM_SERVICE_STATUS     ess;
    SC_HANDLE               hDepService;
    SERVICE_STATUS_PROCESS  ssp;

    DWORD dwStartTime = GetTickCount();
    DWORD dwTimeout = 30000; // 30-second time-out

    // Pass a zero-length buffer to get the required buffer size.
    if ( EnumDependentServices( schService, SERVICE_ACTIVE, 
         lpDependencies, 0, &dwBytesNeeded, &dwCount ) ) 
    {
         // If the Enum call succeeds, then there are no dependent
         // services, so do nothing.
         return TRUE;
    } 
    else 
    {
        if ( GetLastError() != ERROR_MORE_DATA )
            return FALSE; // Unexpected error

        // Allocate a buffer for the dependencies.
        lpDependencies = (LPENUM_SERVICE_STATUS) HeapAlloc( 
            GetProcessHeap(), HEAP_ZERO_MEMORY, dwBytesNeeded );
  
        if ( !lpDependencies )
            return FALSE;

        __try {
            // Enumerate the dependencies.
            if ( !EnumDependentServices( schService, SERVICE_ACTIVE, 
                lpDependencies, dwBytesNeeded, &dwBytesNeeded,
                &dwCount ) )
            return FALSE;

            for ( i = 0; i < dwCount; i++ ) 
            {
                ess = *(lpDependencies + i);
                // Open the service.
                hDepService = OpenService( schSCManager, 
                   ess.lpServiceName, 
                   SERVICE_STOP | SERVICE_QUERY_STATUS );

                if ( !hDepService )
                   return FALSE;

                __try {
                    // Send a stop code.
                    if ( !ControlService( hDepService, 
                            SERVICE_CONTROL_STOP,
                            (LPSERVICE_STATUS) &ssp ) )
                    return FALSE;

                    // Wait for the service to stop.
                    while ( ssp.dwCurrentState != SERVICE_STOPPED ) 
                    {
                        Sleep( ssp.dwWaitHint );
                        if ( !QueryServiceStatusEx( 
                                hDepService, 
                                SC_STATUS_PROCESS_INFO,
                                (LPBYTE)&ssp, 
                                sizeof(SERVICE_STATUS_PROCESS),
                                &dwBytesNeeded ) )
                        return FALSE;

                        if ( ssp.dwCurrentState == SERVICE_STOPPED )
                            break;

                        if ( GetTickCount() - dwStartTime > dwTimeout )
                            return FALSE;
                    }
                } 
                __finally 
                {
                    // Always release the service handle.
                    CloseServiceHandle( hDepService );
                }
            }
        } 
        __finally 
        {
            // Always free the enumeration buffer.
            HeapFree( GetProcessHeap(), 0, lpDependencies );
        }
    } 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="cce10-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="cce10-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce10-113">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="cce10-113">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
