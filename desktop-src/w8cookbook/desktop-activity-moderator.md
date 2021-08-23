---
title: 桌面活動仲裁者
description: 桌面活動仲裁者
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- 電池壽命
- 連線待命
- 懸 架
- 節流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b465bbb377a06fdad50d04d5fcf788cb2e687fdf5db852125e4143fd971773d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815418"
---
# <a name="desktop-activity-moderator"></a>桌面活動仲裁者

## <a name="platform"></a>平台

**用戶端**– Windows 8 


> [!Note]  
> 只有在支援連線待命的 Windows 8 用戶端電腦上才會出現此 DAM。 伺服器 Sku 上沒有該 DAM。

 

  

> [!Note]  
> Windows針對 Windows 8 所建立的商店應用程式不會受到 DAM 的影響。

 

  
</dl>

## <a name="description"></a>描述

我們的客戶轉向更輕量、更小、更多行動平臺，以滿足其運算需求。 在轉移至行動裝置的過程中，使用者已越來越在意其裝置的電池壽命。 「桌面活動仲裁者」 (「DAM) 是 Windows 8 的其中一項新功能，其設計目的是為了確保支援連線待命的裝置具有一致且長時間的電池壽命。

當裝置開啟電源，但畫面已關閉時，就會發生連線待命。 在此電源狀態中，系統在技術上一律「開啟」 (，以支援郵件、VoIP、社交網路和立即訊息，以及 Windows Store 應用程式) 的立即訊息。 它類似于當使用者按下電源按鈕時，智慧型手機所在的狀態。

因此，軟體 (包括應用程式和作業系統軟體) 在連線待命期間必須有良好的行為。 建立的 DAM 是為了隱藏桌面應用程式執行，其方式類似于 ACPI 裝置上的睡眠狀態 (S3) 。 這樣做的方法是，在連線待命專案的情況下，暫停或節流整個系統上的桌面軟體處理常式。 這可讓支援連線待命的系統提供最小化的資源使用量和長時間一致的電池壽命，同時讓 Windows Store 應用程式能夠提供其所保證的連線體驗。

## <a name="details"></a>詳細資料

如果系統支援連線待命，則是在系統開機時載入和初始化的一種核心模式驅動程式。  (這是藉由評估 CallNtPowerInformation 所傳回之系統電源功能結構中的 AOAC 欄位 \_ \_ 是否設定為 TRUE) 來決定。

當啟用了 DAM 並建立您的桌面進程時，[DAM] 會將您的進程新增至系統管理的工作物件：

-   如果進程是在會話0中建立的，則會將進程新增至受限於 **節流** 的工作物件
-   如果程式是在互動式會話中建立 (會話1或更高的) ，則 [DAM] 會將處理常式新增 **至可能** 擱置的工作物件。

> [!Note]  
> 針對 Windows 8，工作物件可以嵌套。 這表示，使用工作物件的 DAM 時，不會干擾應用程式的現有工作物件使用方式。

 

當畫面開啟時，會未佔用 DAM，且不會影響系統上的任何處理程式。 當系統處於連線待命狀態時，根據系統上的活動而定，DAM 可能會節流或暫停處理常式。

-   受擱置的進程會擱置其所有線程 (不允許在任何情況下執行) ;維護應用程式狀態 (進程記憶體) 
-   受擱置和 unsuspended 之間的節流週期所限制的進程， (很長的時間會花在暫停的狀態) 
    -   請注意，Windows 也可以偵測到重大活動發生，而且可能會在此活動期間，讓節流服務的時間變長一段時間。
    -   此外，請注意，在連線待命環境中，感應器和網路可能無法使用，因此，您應該針對大部分的程式設計節流的程式以復原網路狀況不佳的 (情況，這並不需要進行任何變更) 

當您參與或未佔用 DAM 暫止時，會觸發將 WM \_ POWERBROADCAST 訊息傳遞給那些處理常式的處理常式，而這些進程可能會透過 API 呼叫或相容性填充碼來進入訊息傳遞 (，稍後) 所述。 在幾秒鐘的延遲之後，DAM 會暫停處理常式。

當您參與或未佔用 DAM 節流時，不會有任何通知。 進程應該不需要修改;進程會繼續運作，但速度較慢。

## <a name="manifestation"></a>表現

處理常式通常會在連線的待命狀態期間暫停或節流。 在大部分的已暫止的應用程式中，這應該與 S3 暫停/繼續或 S4 休眠/繼續轉換非常類似。 表徵可能包含但不限於執行時間/執行時間與時鐘時間的不一致、計時器行為不一致，或在暫停完成之前和之後的作業系統狀態大幅變更。

暫止和節流會以一個單位的形式進行， (所有可暫停的進程都已暫止並 unsuspended，而且所有可進行節流處理的處理常式會在一致的) 中進行節流和調節，因此兩個已暫止進程或兩個節流程式之間的通訊不會造成問題

依賴跨進程通訊的軟體可能需要特別考慮：

-   **會話0中處理常式之間的通訊 (節流) 和會話 1 + (暫止)** –範例包括代表目前服務狀態的紙匣圖示或 UI 元件
-   **使用者模式中元件之間的通訊 (會話0或 1) 和驅動程式 (但兩者都不會受到節流或暫停)** –範例包括代表驅動程式運作的服務

在這些情況下，如果未正確處理跨進程通訊，則應用程式可能會顯示為無回應或沒有回應 (雖然使用者可能不會直接看到這種影響，因為在連線待命) 中，畫面將會關閉。 不過，在大部分情況下，應該已經開發服務和驅動程式，以針對跨進程通訊問題進行穩固的處理。

建立或相依于網站之軟體的廠商，應該考慮程式暫止如何影響連接存留期和交握。 此外，因為在連線待命模式時可能無法使用網路連線能力，所以在會話0中建立之進程的開發人員應該特別注意間歇性網路連接對進程有何影響。

## <a name="solution"></a>解決方案

WindowsMicrosoft Store 應用程式不會受到 DAM 的影響。 如果您的桌面應用程式受到了 DAM 的影響，您可以在暫停進行之前要求通知 (例如，使用下列其中一種方法來儲存狀態或關閉網路連接) ：

-   如果您的應用程式有 (HWND) 的視窗，而您想要透過視窗程式處理這些通知，請呼叫 [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) 來註冊這些訊息 (或 [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) 以取消註冊) 。 您可以使用 \_ \_ \_ 旗標參數中的裝置通知視窗控制碼，並將視窗的 HWND 以收件者參數的形式傳遞。 收到的訊息是 WM \_ POWERBROADCAST 訊息。
-   如果您的應用程式沒有 (HWND) 的視窗，或您想要直接回呼，請呼叫 [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) 來註冊這些訊息 (或 [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) 以取消註冊) 。 您必須 \_ \_ 在旗標參數中使用裝置通知回呼，並 \_ \_ \_ 在收件者參數中傳遞類型 PDEVICE 通知訂閱參數的值。
-   如果無法重新編譯您的應用程式，您可以 \_ 使用 PromoteDAM 填充碼) ，選擇透過 [AppCompat 工具](../win7appqual/application-compatibility-toolkit--act-.md) 組 (接收這些 WM 的 POWERBROADCAST 訊息。

暫止訊息是 \_ 使用 wParam = PBT APMSUSPEND 的 WM POWERBROADCAST \_ ; 此訊息會同時廣播到系統上所有已選擇的進程。 您的應用程式必須快速且有效率地在暫止路徑上執行任何工作。 廣播通知是全域的，而不是每個進程，因此，如果此路徑中所需的工作很廣泛，則您的進程可能會爭用系統資源。

Resume 訊息是 \_ 具有 wParam = PBT APMRESUME 的 WM POWERBROADCAST \_ ; 此訊息會在繼續進行時，同時廣播到所有選擇的進程。 不保證從連線待命傳遞到系統結束的相對時間。

針對相機相關的應用程式，當發生電源狀態轉換時，應用程式必須釋放所有對相機的參考 (所有的 capture 管線物件都必須關閉並處置) 。  若要避免可能的電池耗盡，在 Windows 10 RS3 + 系統上 Windows 相機框架伺服器服務會在應用程式未正確處理擱置通知時關閉所有的捕獲會話。  這是因為當系統離開待命或 S3/S4 狀態時，應用程式的「捕捉管線」將不再處於「作用中」狀態。

## <a name="tests"></a>測試

在連線的待命轉換之間測試您的軟體。

## <a name="resources"></a>資源

-   [Windows 7 的行動電池壽命解決方案](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [系統 \_ 電源 \_ 功能](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [CallNtPowerInformation 函式](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [工作物件](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [AppCompat 工具組](../win7appqual/application-compatibility-toolkit--act-.md)

 

 