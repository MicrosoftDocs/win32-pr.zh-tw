---
title: 使用 WER
description: 從 Windows Vista 開始，Windows 預設會提供損毀、非回應和核心錯誤報表，而不需要變更您的應用程式。
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- 使用 < Windows 錯誤報告 Windows 錯誤報告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dfa8bc2235f43770cd177ad3e5d9a7d1aacde36034152b88cb06af3879e8c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442237"
---
# <a name="using-wer"></a>使用 WER

從 Windows Vista 開始，Windows 預設會提供損毀、非回應和核心錯誤報表，而不需要變更您的應用程式。 如有需要，報表將包含小型傾印和堆積傾印資訊。 應用程式改為使用 WER API 將應用程式特定的問題報告傳送給 Microsoft。

因為 Windows 會自動報告未處理的例外狀況，所以應用程式不應該處理嚴重的例外狀況。 如果發生錯誤或無回應的程式是互動式的，則 WER 會顯示通知使用者問題的使用者介面。 如果應用程式未在使用者嘗試與應用程式互動時，回應五秒的 Windows 訊息，則會被視為沒有回應。

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>損毀、非回應和核心錯誤的 Windows 錯誤報告流程

下圖顯示應用程式損毀、非回應或核心錯誤所發生的步驟。

1.  發生問題事件。
2.  作業系統會叫用 WER。
3.  如果需要) ，WER 會收集資料、建立報表，並提示使用者同意 (。
4.  如果使用者同意，則 WER 會將報告傳送至 Microsoft (Watson Server) 。
5.  如果 Watson 伺服器要求額外的資料，則 WER 會收集資料，並視需要) 要求使用者同意 (。
6.  如果應用程式已註冊復原並重新啟動，則當資料壓縮並傳送至 Microsoft (（如果使用者同意) ），則 WER 會執行已註冊的回呼函式。
7.  如果 Microsoft 提供問題的回應，就會通知使用者。

應用程式可以使用下列函數來自訂傳送給 Microsoft 之報表的內容。 註冊函式會告知 WER 將特定檔案和記憶體區塊包含在它所建立的錯誤報表中。

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>一般附隨報告的 Windows 錯誤報告流程

下列步驟顯示應用程式如何取得非嚴重錯誤狀況的錯誤報表。

1.  發生非嚴重問題事件。
2.  應用程式會辨識該事件，並使用下列函式呼叫順序來產生報表。
    1.  呼叫 [**WerReportCreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) 函數來建立報表。
    2.  呼叫 [**WerReportSetParameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) 函數來設定報表參數。
    3.  呼叫 [**WerReportAddFile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) 函數，以將檔案加入至報表。
    4.  如有) 需要，請呼叫 [**WerReportAddDump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) 函數，以將小型傾印新增至報表 (。
    5.  呼叫 [**WerReportSubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) 函數來傳送報表。
    6.  呼叫 [**WerReportCloseHandle**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) 以釋放資源。
3.  根據在步驟2中呼叫函數時所使用的特定選項，WER 將完成錯誤報表。 WER 可確保報告是根據使用者設定的原則來完成。 例如，WER 會將報表傳送給 Microsoft、將報表排入佇列，並向使用者顯示適當的使用者介面。

## <a name="excluding-an-application-from-windows-error-reporting"></a>從 Windows 錯誤報告排除應用程式

若要將您的應用程式排除 Windows 錯誤報告，請使用 [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)函數。 若要還原應用程式的錯誤報表，請使用 [**WerRemoveExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication) 函數。

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>自動復原資料並重新啟動錯誤的應用程式

應用程式可以使用應用程式復原並重新啟動，以在應用程式因為未處理的例外狀況或應用程式停止回應的情況結束之前儲存資料和狀態資訊。 如果要求，也會重新開機應用程式。 如需詳細資訊，請參閱 [應用程式修復和重新開機](/windows/desktop/Recovery/application-recovery-and-restart-portal)。

## <a name="legacy-api"></a>舊版 API

應用程式可以藉由呼叫 [**ReportFault**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) 函數來報告錯誤。 不過，您不應該使用 **ReportFault** 函式，除非您有非常特定的需求，亦即作業系統的預設錯誤報表行為無法完成。

如果已啟用 [錯誤報表]，系統就會向使用者顯示一個對話方塊，指出應用程式發生問題，並將關閉。 如果已在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AeDebug** 金鑰中設定偵錯工具，則會提供使用者啟動偵錯工具的選項。 使用者也可以選擇將報表傳送給 Microsoft。 如果使用者傳送報表，系統會顯示另一個對話方塊來感謝報表的使用者，並提供詳細資訊的連結。

錯誤報表系統支援下列作業模式。



| 作業模式          | Description                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 共用記憶體報告 | 如果應用程式的安全性內容與已登入之使用者的安全性內容相同，則錯誤報表系統會使用共用記憶體區塊進行通訊。 此模式無法與資訊清單報告模式搭配使用。<br/>                                                                                               |
| 資訊清單報告      | 如果應用程式的安全性內容與已登入之使用者的安全性內容不同，則錯誤報表系統會使用檔案進行通訊。 此模式也用於報告沒有回應的應用程式和核心錯誤。 此模式不能與共享記憶體報告模式搭配使用。<br/>                      |
| 網際網路報告      | 錯誤報表系統會透過網際網路將所有資料傳送給 Microsoft。 這是預設作業模式。 它無法與公司報表模式搭配使用。 當系統管理員未指定任何公司上傳路徑時，就會使用此模式。<br/>                                                                     |
| 公司報告     | 錯誤報表系統會將所有資料傳送至檔案共用，而不是直接上傳至 Microsoft。 這可讓企業 IT 管理員在資料傳送給 Microsoft 之前，先審核資料。 當系統管理員指定了公司上傳路徑時，就會使用此模式。 它無法與網際網路報表模式搭配使用。<br/> |
| 無周邊報告      | 錯誤報表系統將不會對使用者顯示任何對話方塊。 這可讓企業 IT 管理員隨時收集員工的錯誤報表。 當系統管理員啟用報告時，會使用此模式，但會停用通知。 它只能與公司報表模式搭配使用。<br/>        |



 

若要將您的應用程式從錯誤報表中排除，請使用 [**AddERExcludedApplication**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa) 函數。

 

