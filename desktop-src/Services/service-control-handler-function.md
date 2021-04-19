---
description: 每個服務都有控制項處理常式，也就是處理函式，會在服務進程從服務控制程式接收控制項要求時由控制項發送器叫用。
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: 服務控制處理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1303bff45421ee7206d02be9ee30066324648823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972619"
---
# <a name="service-control-handler-function"></a>服務控制處理函式

每個服務都有控制項處理常式，也就是 [**處理**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) 函式，會在服務進程從服務控制程式接收控制項要求時由控制項發送器叫用。 因此，此函式會在控制項發送器的內容中執行。 如需範例，請參閱 [撰寫控制項處理常式函數](writing-a-control-handler-function.md)。

服務會呼叫 [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) 或 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) 函式來註冊其服務控制處理常式函式。

當叫用服務控制處理常式時，服務必須呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 函式，只有在處理控制項程式碼導致服務狀態變更時，才會將其狀態報表給 SCM。 如果處理控制項程式碼不會導致服務狀態變更，則不需要呼叫 **>setservicestatus**。

服務控制程式可以使用 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來傳送控制要求。 所有服務都必須接受並處理 **服務 \_ 控制 \_** 的查閱控制項程式碼。 您可以藉由呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)來啟用或停用其他控制項代碼的接受。 若要接收 **服務 \_ 控制 \_ DEVICEEVENT** 控制項程式碼，您必須呼叫 [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) 函數。 服務也可以處理其他使用者定義的控制項碼。

如果服務接受 **服務 \_ 控制 \_ 停止** 控制程式代碼，它必須在收到時停止，並進入 **服務 \_ 停止 \_ 暫** 止或 **服務 \_ 已停止** 狀態。 SCM 傳送此控制項程式碼之後，就不會傳送其他控制碼。

**WINDOWS XP：** 如果服務未傳回 **\_ 錯誤** 並繼續執行，它會繼續接收控制碼。 此行為自 Windows Server 2003 和 Windows XP Service Pack 2 (SP2) 起變更。

控制處理常式必須在30秒內傳回，否則 SCM 會傳回錯誤。 如果服務在執行控制處理常式時必須執行冗長的處理，它應該會建立次要執行緒來執行冗長的處理，然後從控制項處理常式返回。 這可防止服務與控制項發送器系結。 例如，處理需要很長時間之服務的停止要求時，請建立另一個執行緒來處理停止進程。 控制項處理常式應該只呼叫具有 **服務 \_ 停止 \_ 暫** 止訊息的 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) ，然後再返回。

當使用者關閉系統時，所有已呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 與服務的控制項處理常式都會 **\_ 接受 \_ PRESHUTDOWN** 控制項程式碼，以接收 **服務 \_ 控制項 \_ PRESHUTDOWN** 控制項程式碼。 服務控制管理員會等到服務停止或指定的 preshutdown 超時值過期 (此值可以使用 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函數) 來設定。 只有在特殊情況下，才應該使用這個控制項程式碼，因為處理此通知的服務會封鎖系統關閉，直到服務停止或 preshutdown 逾時間隔到期為止。

Preshutdown 通知完成之後，所有已呼叫 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 與 **服務 \_ 接受 \_ 關機** 控制程式代碼的控制項處理常式都會收到 **服務 \_ 控制 \_ 關閉** 控制程式代碼。 系統會以它們出現在已安裝服務的資料庫中的順序來通知。 根據預設，服務大約需要20秒的時間，才能在系統關機之前執行清除工作。 在這段時間到期後，不論服務關機是否已完成，系統關機都會繼續進行。 請注意，如果系統處於關機狀態 (未重新開機或關閉) ，則服務會繼續執行。

如果服務需要更多時間來清除，它會傳送 **停止 \_ 擱置** 狀態訊息，以及等待提示，因此服務控制器知道在向系統回報服務關機完成之前，要等待多久的時間。 不過，為了避免服務停止關機，服務控制器等候的時間會有所限制。 如果要透過服務嵌入式管理單元關閉服務，限制為125秒或125000毫秒。 如果作業系統正在重新開機，則會在 **WaitToKillServiceTimeout** 值中指定時間限制， (以毫秒為單位) 下列登錄機碼：

**HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**

> [!IMPORTANT]
> 服務不應嘗試藉由修改此值來增加時間限制。 如果您需要手動設定 **WaitToKillServiceTimeout** ，此值應以毫秒為單位。

客戶需要快速關閉作業系統。 例如，如果在 ups 電源上執行的電腦無法在 UPS 耗盡電源之前完成關機，資料可能會遺失。 因此，服務應該儘快完成其清除工作。 藉由定期儲存資料、追蹤儲存至磁片的資料，並只在關機時儲存未儲存的資料，是很好的做法。 由於電腦正在關機，因此請勿花時間釋出已配置的記憶體或其他系統資源。 如果您需要通知伺服器正在結束，請將等待回復所花費的時間降到最低，因為網路問題可能會延遲服務的關機。

請注意，在服務關閉期間，SCM 預設不會考慮相依性。 SCM 會列舉正在執行的服務清單，並傳送 **服務 \_ 控制 \_ 關閉** 命令。 因此，服務可能會失敗，因為它所依存的另一個服務已停止。

若要手動設定服務的關機順序，請建立 multistring 登錄值，其中包含服務名稱（依應關閉的順序），並將其指派給控制項索引鍵的 **PreshutdownOrder** 值，如下所示：

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ PreshutdownOrder = "Shutdown Order"**

若要從您的應用程式設定相依服務的關機順序，請使用 [**SetProcessShutdownParameters**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) 函數。 SCM 會使用此函式來提供其處理常式0x1E0 優先權。 SCM 會在呼叫其控制處理常式時傳送 **服務 \_ 控制 \_ 關閉** 通知，並等候服務結束，然後再從其控制處理常式傳回。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫控制項處理常式函數](writing-a-control-handler-function.md)
</dt> </dl>

 

 
