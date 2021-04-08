---
description: 當服務控制程式要求新的服務執行時，服務控制管理員 (SCM) 啟動服務並將啟動要求傳送至控制發送器。
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: 服務 ServiceMain 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed50f0f378f348415e56827a09fcf17eea7fc330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945127"
---
# <a name="service-servicemain-function"></a>服務 ServiceMain 函式

當服務控制程式要求新的服務執行時，服務控制管理員 (SCM) 啟動服務並將啟動要求傳送至控制發送器。 控制項發送器會建立新的執行緒，以執行服務的 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) 函式。 如需範例，請參閱 [撰寫 ServiceMain](writing-a-servicemain-function.md)函式。

[**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)函式應該會執行下列工作：

1.  將所有全域變數初始化。
2.  立即呼叫 [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) 函式來註冊 [**處理常式**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 函式，以處理服務的控制項要求。 **RegisterServiceCtrlHandler** 的傳回值是 *服務狀態控制碼*，會在呼叫中用來通知 SCM 的服務狀態。
3.  執行初始化。 如果初始化程式碼的執行時間預期會很短 (小於一秒) ，就可以直接在 [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)中執行初始化。

    如果初始化時間預期的時間超過一秒，服務應該使用下列其中一種初始化技術：

    -   呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 函數來執行報表服務， \_ 但在初始化完成之前不接受任何控制項。 服務會藉由呼叫 **>setservicestatus** ，並將 **dwCurrentState** 設定為執行中的服務 \_ ，並在 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)結構中將 **dwControlsAccepted** 設定為0。 這可確保 SCM 不會在服務就緒之前將任何控制權要求傳送至服務，並釋放 SCM 來管理其他服務。 針對效能，建議使用這種初始化方法，尤其是自動啟動服務。
    -   報表服務 \_ 開始 \_ 暫止、不接受任何控制項，並指定等候提示。 如果您服務的初始化程式碼所執行的工作所需的時間比初始等候提示值還長，則您的程式碼必須定期呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 函式 (可能會有修改過的等候提示) 指出正在進行的進度。 請務必只在初始化進行中時呼叫 **>setservicestatus** 。 否則，SCM 可以等候服務進入服務執行 \_ 狀態，假設您的服務正在進行，並封鎖其他服務啟動。 除非您確定執行初始化的執行緒確實正在進行，否則請勿從個別的執行緒呼叫 **>setservicestatus** 。

        使用這種方法的服務也可以指定檢查點值，並在冗長的初始化期間，定期遞增值。 啟動服務的程式可以呼叫 [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) 或 [**QUERYSERVICESTATUSEX**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) ，從 SCM 取得最新的檢查點值，並使用此值向使用者報告增量進度。

4.  初始化完成時，呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 以將服務狀態設定為執行中的服務 \_ ，並指定服務已準備好接受的控制項。 如需控制項的清單，請參閱 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) 結構。
5.  執行服務工作，或者，如果沒有暫止的工作，請將控制權傳回給呼叫者。 服務狀態的任何變更都需要呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 來報告新的狀態資訊。
6.  如果服務正在初始化或執行時發生錯誤，服務應該呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) ，以將服務狀態設定為服務 \_ 停止暫止（ \_ 如果清除會很長）。 清除完成之後，請呼叫 **>setservicestatus** ，將 \_ 最後一個執行緒停止的服務狀態設定為 [服務]。 請務必設定 [**服務 \_ 狀態**](/windows/desktop/api/Winsvc/ns-winsvc-service_status)結構的 **dwServiceSpecificExitCode** 和 **dwWin32ExitCode** 成員，以找出錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 ServiceMain 函式](writing-a-servicemain-function.md)
</dt> </dl>

 

 
