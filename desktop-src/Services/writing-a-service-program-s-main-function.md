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
# <a name="writing-a-service-programs-main-function"></a>撰寫服務程式的 main 函數

[服務程式](service-programs.md)的 **main** 函式會呼叫 [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)函式，以連接至 [服務控制管理員](service-control-manager.md) (SCM) 並啟動控制發送器執行緒。 發送器執行緒會迴圈，等候分派資料表中指定之服務的傳入控制項要求。 當發生錯誤或進程中的所有服務都已結束時，這個執行緒就會傳回。 當進程中的所有服務都已結束時，SCM 會將控制項要求傳送給發送器執行緒，告知其結束。 此執行緒接著會從 **StartServiceCtrlDispatcher** 呼叫傳回，而且進程可以終止。

此範例中使用下列全域定義。


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



下列範例可用來作為支援單一服務之服務程式的進入點。 如果您的服務程式支援多個服務，請將其他服務的名稱新增至分派資料表，以便發送器執行緒監視這些服務的名稱。

Tmain 函式 \_ 是進入點。 SvcReportEvent 函數會將參考用訊息和錯誤寫入事件記錄檔。 如需撰寫 SvcMain 函式的詳細資訊，請參閱 [撰寫 ServiceMain 函數](writing-a-servicemain-function.md)。 如需 SvcInstall 函數的詳細資訊，請參閱 [安裝服務](installing-a-service.md)。 如需撰寫 SvcCtrlHandler 函式的詳細資訊，請參閱 [撰寫控制項處理常式函數](writing-a-control-handler-function.md)。 如需完整的範例服務，包括 SvcReportEvent 函數的來源，請參閱 [.svc](svc-cpp.md)。


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



以下是訊息編譯器所產生的範例 .h 範例。 如需詳細資訊，請參閱 [Sample.mc](sample-mc.md)。

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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[服務進入點](service-entry-point.md)
</dt> <dt>

[完整的服務範例](the-complete-service-sample.md)
</dt> </dl>

 

 



