---
description: 當發送器執行緒呼叫處理函式時，它會處理在 Opcode 參數中傳遞的控制項程式碼，然後呼叫 ReportSvcStatus 函數來更新服務狀態。
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: 撰寫控制項處理常式函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973247"
---
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="9b3db-103">撰寫控制項處理常式函數</span><span class="sxs-lookup"><span data-stu-id="9b3db-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="9b3db-104">當發送器執行緒呼叫處理函式時，它會處理在 *Opcode* 參數中傳遞的控制項 [**程式**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)代碼，然後呼叫 ReportSvcStatus 函數來更新服務狀態。</span><span class="sxs-lookup"><span data-stu-id="9b3db-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="9b3db-105">當處理函式收到控制項 [**程式**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 代碼時，只有在處理控制項程式碼導致服務狀態變更時，才應該報表服務狀態。</span><span class="sxs-lookup"><span data-stu-id="9b3db-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="9b3db-106">如果服務未在控制項上採取動作，它就不應該將狀態報表給服務控制管理員。</span><span class="sxs-lookup"><span data-stu-id="9b3db-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="9b3db-107">如需 ReportSvcStatus 的原始程式碼，請參閱 [撰寫 ServiceMain 函數](writing-a-servicemain-function.md)。</span><span class="sxs-lookup"><span data-stu-id="9b3db-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="9b3db-108">在下列範例中，SvcCtrlHandler 函數是 [**處理**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 函式的範例。</span><span class="sxs-lookup"><span data-stu-id="9b3db-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="9b3db-109">請注意，ghSvcStopEvent 變數是應該初始化和使用的全域變數，如 [撰寫 ServiceMain](writing-a-servicemain-function.md)函式中所示。</span><span class="sxs-lookup"><span data-stu-id="9b3db-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9b3db-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b3db-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b3db-111">服務控制處理函式</span><span class="sxs-lookup"><span data-stu-id="9b3db-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="9b3db-112">完整的服務範例</span><span class="sxs-lookup"><span data-stu-id="9b3db-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



