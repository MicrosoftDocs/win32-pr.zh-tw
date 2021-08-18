---
description: 當發送器執行緒呼叫處理函式時，它會處理在 Opcode 參數中傳遞的控制項程式碼，然後呼叫 ReportSvcStatus 函數來更新服務狀態。
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: 撰寫控制項處理常式函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bf8ab32edb73fdf11f3f0370a512b17b143b8af219a2bd539e59bdf062a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888059"
---
# <a name="writing-a-control-handler-function"></a>撰寫控制項處理常式函數

當發送器執行緒呼叫處理函式時，它會處理在 *Opcode* 參數中傳遞的控制項 [**程式**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)代碼，然後呼叫 ReportSvcStatus 函數來更新服務狀態。 當處理函式收到控制項 [**程式**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 代碼時，只有在處理控制項程式碼導致服務狀態變更時，才應該報表服務狀態。 如果服務未在控制項上採取動作，它就不應該將狀態報表給服務控制管理員。 如需 ReportSvcStatus 的原始程式碼，請參閱 [撰寫 ServiceMain 函數](writing-a-servicemain-function.md)。

在下列範例中，SvcCtrlHandler 函數是 [**處理**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 函式的範例。 請注意，ghSvcStopEvent 變數是應該初始化和使用的全域變數，如 [撰寫 ServiceMain](writing-a-servicemain-function.md)函式中所示。


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[服務控制處理函式](service-control-handler-function.md)
</dt> <dt>

[完整的服務範例](the-complete-service-sample.md)
</dt> </dl>

 

 



