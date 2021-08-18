---
description: 瞭解如何避免 Windows 7 和 Windows Server 2008 R2 平臺 Windows 的應用程式停止回應。
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: 防止 Windows 的應用程式停止回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5509b8733e45b105694a8bfdadddae0d67096b92c390ed98b3dd937817823b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994814"
---
# <a name="preventing-hangs-in-windows-applications"></a>防止 Windows 的應用程式停止回應

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器**-Windows Server 2008 R2  









## <a name="description"></a>描述

**停止回應-使用者的觀點**

像是回應式應用程式的使用者。 當他們按下功能表時，他們想要讓應用程式立即回應，即使它目前正在列印工作也一樣。 當他們將冗長的檔儲存在最愛的字處理器時，他們想要在磁片仍在旋轉時繼續輸入。 當應用程式不會及時回應其輸入時，使用者會取得不耐，而不是快速回應。

程式設計師可能會辨識出應用程式不會立即回應使用者輸入的許多合法原因。 應用程式可能忙於重新計算一些資料，或只是等候其磁片 i/o 完成。 不過，從使用者研究中，我們知道使用者只需要幾秒鐘的時間無回應，就能感到苦惱並感到挫折。 在5秒後，他們會嘗試終止無回應的應用程式。 在損毀的情況下，應用程式停止回應是使用 Win32 應用程式時最常見的使用者中斷來源。

應用程式停止回應有許多不同的根本原因，而且並非所有的根本原因都在沒有回應的 UI 中。 不過，沒有回應的 UI 是最常見的停止回應體驗之一，而此案例目前會獲得偵測和復原的大部分作業系統支援。 Windows 會自動偵測、收集偵錯工具資訊，並選擇性地終止或重新開機無回應的應用程式。 否則，使用者可能必須重新開機電腦，才能復原無回應的應用程式。

**停止回應-作業系統透視圖**

當應用程式 (或更精確時，執行緒) 會在桌面上建立視窗，並使用桌面視窗管理員 (DWM) 進入隱含合約，以及時處理視窗訊息。 DWM 會將訊息張貼 (鍵盤/滑鼠輸入和其他視窗中的訊息，也) 到執行緒特定的訊息佇列中。 執行緒會透過它的訊息佇列來抓取和分派這些訊息。 如果執行緒未藉由呼叫 GetMessage () 來服務佇列，則不會處理訊息，而且視窗會停止回應：它無法重繪，也無法接受使用者的輸入。 作業系統會藉由將計時器附加到訊息佇列中的擱置中訊息來偵測此狀態。 如果訊息未在5秒內被抓取，DWM 會將視窗宣告為無反應。 您可以透過 IsHungAppWindow () API 查詢這個特定的視窗狀態。

偵測只是第一個步驟。 此時，使用者仍然無法終止應用程式-按一下 [X (關閉]) 按鈕會導致 WM \_ 關閉訊息，而這會在訊息佇列中停滯，就像任何其他訊息一樣。 桌面視窗管理員可透過以「准刪除」複本來顯示原始視窗先前工作 (區的點陣圖，並將「沒有回應」新增至標題列) ，以協助您順利隱藏和取代無反應視窗。 只要原始視窗的執行緒不會取得訊息，DWM 就會同時管理這兩個視窗，但只允許使用者與准刪除複製進行互動。 使用此准刪除視窗，使用者只能移動、最小化和-最重要的是關閉沒有回應的應用程式，但不會變更其內部狀態。

整個 ghost 體驗看起來像這樣：

![顯示 [記事本沒有回應] 對話方塊的螢幕擷取畫面。](images/preventinghangs-ghostwindow.gif)

桌面視窗管理員會進行最後一件事;它會與 Windows 錯誤報告整合，讓使用者不僅能關閉並選擇性地重新開機應用程式，還可以將寶貴的調試資料傳送回 Microsoft。 您可以在 Winqual 網站上註冊，為自己的應用程式取得這項停止回應資料。

Windows 7 在此體驗中新增了一項新功能。 作業系統會分析無回應的應用程式，而且在某些情況下，會提供使用者取消封鎖作業的選項，並讓應用程式再次回應。 目前的實值支援取消封鎖通訊端呼叫;未來的版本將會有更多的作業可供使用者取消。

若要整合您的應用程式與無回應復原體驗，並充分利用可用的資料，請遵循下列步驟：

-   確定您的應用程式已註冊重新開機和復原，讓您可以放心地將其停止回應給使用者。 已正確註冊的應用程式可能會自動重新開機，而不會有大部分未儲存的資料。 這適用于應用程式停止回應和當機。
-   取得頻率資訊，以及針對您的無回應和當機的應用程式，從 Winqual 網站進行資料的偵錯工具。 即使在測試期間也可以使用此資訊來改善您的程式碼。 如需簡短的總覽，請參閱「簡介 Windows 錯誤報告」。
-   您可以透過呼叫 DisableProcessWindowsGhosting () ，在您的應用程式中停用重設功能。 不過，這可防止一般使用者關閉和重新開機無回應的應用程式，而且通常會在重新開機時結束。

**停止回應-開發人員觀點**

作業系統會將應用程式停止回應為至少有5秒未處理訊息的 UI 執行緒。 明顯的錯誤會導致一些停止回應，例如，等候從未收到信號的事件的執行緒，以及兩個執行緒，每個執行緒都持有鎖定並嘗試取得其他執行緒。 您可以修正這些 bug，而不需要太多精力。 但是，許多停止回應並不是那麼明顯。 是，UI 執行緒不會抓取訊息，但它同樣忙於執行其他「重要」工作，且最終會回到處理訊息。

但是，使用者會將此視為錯誤。 設計應該符合使用者的期望。 如果應用程式的設計會導致沒有回應的應用程式，則設計將必須變更。 最後，這是很重要的，無回應不能像程式碼錯誤一樣修正;它需要在設計階段進行提前工作。 嘗試改建應用程式的現有程式碼基底，讓 UI 更具回應性，通常太昂貴。 下列設計指導方針可能有所説明。

-   讓 UI 回應性成為最上層需求;使用者應隨時掌控您的應用程式
-   確定使用者可以取消花費超過一秒的作業完成，並（或）該作業可以在背景中完成;視需要提供適當的進度 UI

![顯示 [正在複製專案] 對話方塊的螢幕擷取畫面。](images/preventinghangs-progressbar.gif)

-   將長時間執行或封鎖作業排入佇列，以做為背景工作 (這需要經過妥善考慮的訊息機制，在工作完成時通知 UI 執行緒) 
-   讓 UI 執行緒的程式碼保持簡單;盡可能移除最多封鎖的 API 呼叫
-   只有在已就緒且可完全運作時，才會顯示視窗和對話方塊。 如果對話方塊需要顯示太過資源而無法計算的資訊，請先顯示一些一般資訊，並且在有更多資料可供使用時，即時更新它。 Windows 檔案總管的 [資料夾屬性] 對話方塊就是一個很好的例子。 它必須顯示資料夾的總大小，也就是檔案系統中未提供的資訊。 對話方塊會立即顯示，而 [大小] 欄位則會從背景工作執行緒更新：

![顯示 [一般] 頁面的螢幕擷取畫面，其中顯示 [大小]、[磁片大小] 和 [包含] 文字的 Windows 屬性。](images/preventinghangs-updatingdialog.gif)

可惜的是，沒有簡單的方法可以設計及撰寫回應式應用程式。 Windows 不提供簡單的非同步架構，可讓您輕鬆地排程封鎖或長時間執行的作業。 下列各節介紹一些預防停止回應的最佳作法，並強調一些常見的陷阱。

## <a name="best-practices"></a>最佳做法

**讓 UI 執行緒保持簡單**

UI 執行緒的主要責任是取得和分派訊息。 任何其他類型的工作都有可能會造成這個執行緒所擁有的 windows 中止。

**任務**

-   移動耗用大量資源或未系結的演算法，以產生長時間執行的背景工作執行緒作業
-   盡可能找出多個封鎖函式呼叫，並嘗試將它們移至背景工作執行緒;任何呼叫另一個 DLL 的函式都應該是可疑的
-   進行額外的工作，以從您的背景工作執行緒移除所有檔案 i/o 和網路 API 呼叫。 如果不是幾分鐘的時間，這些函式可能會封鎖數秒鐘。 如果您需要在 UI 執行緒中進行任何類型的 i/o，請考慮使用非同步 i/o
-   請注意，您的 UI 執行緒也會提供處理常式所裝載之所有單一執行緒的單元 (STA) COM 伺服器;如果您進行封鎖通話，則在您再次服務訊息佇列之前，這些 COM 伺服器將會沒有回應

**請勿：**

-   等候任何核心物件 (例如事件或 Mutex) 超過一段非常短的時間;如果您必須等待，請考慮使用 MsgWaitForMultipleObjects () ，這會在新訊息抵達時解除封鎖
-   使用 AttachThreadInput () 函式，與另一個執行緒共用執行緒的視窗訊息佇列。 正確地同步處理佇列的存取並不容易，也可以防止 Windows 作業系統正確地偵測到無回應視窗
-   在任何背景工作執行緒上使用 TerminateThread () 。 以這種方式終止執行緒將不會允許它釋放鎖定或發出訊號事件，並可輕鬆地產生孤立的同步處理物件。
-   從 UI 執行緒呼叫任何「未知的」程式碼。 如果您的應用程式具有擴充性模型，則更是如此。不保證協力廠商程式碼遵循您的回應性指導方針
-   進行任何種類的封鎖廣播通話;SendMessage (HWND \_ 廣播) 可讓您 mercy 目前執行的每個未撰寫錯誤的應用程式

**執行非同步模式**

從 UI 執行緒中移除長時間執行或封鎖的作業需要執行可將這些作業卸載至背景工作執行緒的非同步架構。

**任務**

-   在 UI 執行緒中使用非同步視窗訊息 Api，特別是將 SendMessage 取代為其中一個非封鎖對等： PostMessage、SendNotifyMessage 或 SendMessageCallback
-   使用背景執行緒來執行長時間執行或封鎖的工作。 使用新的執行緒集區 API 來執行您的背景工作執行緒
-   針對長時間執行的背景工作提供取消支援。 若為封鎖 i/o 作業，請使用 i/o 取消，但僅做為最後的手段;取消 ' right ' 作業並不容易
-   使用 IAsyncResult 模式或使用事件來執行 managed 程式碼的非同步設計

**明智地使用鎖定**

您的應用程式或 DLL 需要鎖定，以同步處理其內部資料結構的存取。 使用多個鎖定可增加平行處理，並讓您的應用程式更具回應性。 不過，使用多個鎖定也會增加以不同順序取得這些鎖定，並導致您的執行緒鎖死的機會。 如果兩個執行緒各自持有鎖定，然後嘗試取得其他執行緒的鎖定，其作業會形成迴圈等候，以封鎖這些執行緒的任何轉寄進度。 您只能藉由確保應用程式中的所有線程一律取得相同順序的所有鎖定，來避免此鎖死。 不過，以「右方」順序取得鎖定並不容易。 您可以撰寫軟體元件，但不能進行鎖定。 如果您的程式碼呼叫其他元件，則該元件的鎖定現在會變成隱含鎖定順序的一部分，即使您沒有這些鎖定的可見度。

因為鎖定作業所包含的功能遠超過重要區段、Mutex 和其他傳統鎖定的一般功能，所以會變得更困難。 跨越執行緒界限的任何封鎖呼叫都有可能導致鎖死的同步處理屬性。 呼叫執行緒會執行具有「取得」語義的作業，而且無法解除封鎖，直到呼叫的目標執行緒「釋放」為止。 有很多的 User32 函式 (例如 SendMessage) ，而且許多封鎖的 COM 呼叫都屬於此類別。

更糟的是，作業系統有自己的內部進程特定鎖定，有時在您的程式碼執行時仍會保留。 當 Dll 載入至進程時，就會取得此鎖定，因此稱為「載入器鎖定」。 DllMain 函式一律會在載入器鎖定下執行;如果您在 DllMain (中取得任何鎖定，而且不應該) ，您必須讓載入器鎖定鎖定順序的一部分。 呼叫特定的 Win32 Api 也可能會對您的函式（例如 LoadLibraryEx、GetModuleHandle，特別是 CoCreateInstance）取得載入器鎖定。

若要結合上述所有程式碼，請參閱下列範例程式碼。 此函式會取得多個同步處理物件，並隱含地定義鎖定順序，在粗略檢查時不一定很明顯。 在函式專案中，程式碼會取得重要區段，而不會在函式結束之前釋出它，藉此使其成為鎖定階層中的最上層節點。 然後，此程式碼會呼叫 Win32 函式 LoadIcon () ，其中的背後可能會呼叫作業系統載入器來載入此二進位檔。 這項作業會取得載入器鎖定，現在也會成為這個鎖定階層的一部分 (請確定 DllMain 函式未取得 g \_ cs 鎖定) 。 接下來，程式碼會呼叫 SendMessage () ，這是封鎖的跨執行緒操作，除非 UI 執行緒回應，否則不會傳回。 同樣地，請確定 UI 執行緒永遠不會取得 g \_ cs。

```
bool foo::bar (char* buffer)  
{  
      EnterCriticalSection(&g_cs);  
      // Get 'new data' icon  
      this.m_Icon = LoadIcon(hInst, MAKEINTRESOURCE(5));  
      // Let UI thread know to update icon SendMessage(hWnd,WM_COMMAND,IDM_ICON,NULL);  
      this.m_Params = GetParams(buffer);  
      LeaveCriticalSection(&g_cs);
      return true;  
}  
```

查看這段程式碼看起來似乎是因為我們 \_ 只想要同步存取類別成員變數，所以我們會在鎖定階層中隱含地將 g cs 設為最上層鎖定。

**任務**

-   設計鎖定階層，並遵循它。 新增所有必要的鎖定。 比起 Mutex 和 CriticalSections，有更多的同步處理原始物件;這些都必須包含在內。 如果您在 DllMain 中採用任何鎖定，請在階層中包含載入器鎖定 () 
-   同意您的相依性鎖定通訊協定。 您的應用程式所呼叫或可能呼叫應用程式的任何程式碼都必須共用相同的鎖定階層
-   鎖定資料結構不是函數。 從函式進入點移離鎖定，並只防護鎖定的資料存取。 如果較少的程式碼在鎖定下運作，可能會有鎖死的機率
-   分析您的錯誤處理常式代碼中的鎖定取得和釋放。 如果嘗試從錯誤狀況中復原時，通常會忽略鎖定階層
-   將嵌套鎖定取代為參考計數器-它們不能鎖死。 清單和資料表中個別鎖定的元素是理想的候選項目
-   從 DLL 等候執行緒控制碼時，請務必小心。 一律假設您的程式碼可能會在載入器鎖定下呼叫。 最好參考計數您的資源，讓背景工作執行緒自行進行清除 (然後使用 FreeLibraryAndExitThread 來完全終止) 
-   如果您想要診斷自己的鎖死，請使用 Wait Chain 遍歷 API

**請勿：**

-   在您的 DllMain () 函式中執行非常簡單的初始化工作。 如需詳細資訊，請參閱 DllMain 回呼函數。 尤其不要呼叫 LoadLibraryEx 或 CoCreateInstance
-   撰寫您自己的鎖定基本專案。 自訂同步處理常式代碼可以輕鬆地在程式碼基底中引進微妙的錯誤。 改為使用豐富的作業系統同步處理物件選項
-   針對全域變數在函式和析構函式中執行任何工作，這些都是在載入器鎖定下執行

**注意例外狀況**

例外狀況允許分隔一般程式流程和錯誤處理。 由於這種分隔，在例外狀況發生之前，可能很難知道程式的精確狀態，而且例外狀況處理常式可能會錯過還原有效狀態的重要步驟。 這特別適用于需要在處理常式中釋出的鎖定，以避免未來的鎖死。

下列範例程式碼說明此問題。 「緩衝區」變數的無限制存取有時候會導致 (AV) 發生存取違規。 原生例外狀況處理常式會攔截此 AV，但它並沒有簡單的方法可以判斷是否已在例外狀況發生時取得重要區段， (AV 甚至可能在 EnterCriticalSection 程式碼) 的某處發生。

```
 BOOL bar (char* buffer)  
{  
   BOOL rc = FALSE;  
   __try {  
      EnterCriticalSection(&cs);  
      while (*buffer++ != '&') ;  
      rc = GetParams(buffer);  
      LeaveCriticalSection(&cs);  
   } __except (EXCEPTION_EXECUTE_HANDLER)  
   {  
      return FALSE;  
   } 
   return rc;  
}  
```

**任務**

-   \_ \_ 請盡可能移除 try/ \_ \_ Except; 請勿使用 SetUnhandledExceptionFilter
-   如果您使用 c + + 例外狀況，請將鎖定包裝在自訂的自動 \_ ptr 範本中。 鎖定應該在函式中釋放。 若為原生例外狀況，請釋放 \_ \_ finally 語句中的鎖定
-   請小心使用在原生例外狀況處理常式中執行的程式碼;例外狀況可能已洩漏許多鎖定，因此您的處理常式不應該取得任何

**請勿：**

-   如果 Win32 Api 不需要或不需要，請處理原生例外狀況。 如果您在發生嚴重錯誤後，使用原生例外狀況處理常式進行報告或資料復原，請考慮改為使用預設的作業系統機制 Windows 錯誤報告
-   使用 c + + 例外狀況搭配任何類型的 UI (user32) 程式碼;回呼中擲回的例外狀況將會流經作業系統所提供的 C 程式碼層。 該程式碼不知道 c + + 展開語義

## <a name="links-to-resources"></a>資源的連結

-   [Windows 錯誤報告](../wer/windows-error-reporting.md)
-   [非同步設計](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [非同步 i/o](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**AttachThreadInput 函式**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**自動 \_ Ptr 類別**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**DisableProcessWindowsGhosting 函式**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**DllMain 回呼函數**](../dlls/dllmain.md)
-   [事件](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**GetMessage 函式**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [I/o 取消](../fileio/canceling-pending-i-o-operations.md)
-   [**IsHungAppWindow 函式**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [訊息佇列](../winmsg/using-messages-and-message-queues.md)
-   [**MsgWaitForMultipleObjects 函式**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [新的執行緒集區 API](../procthread/thread-pool-api.md)
-   [**PostMessage 函式**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [重新開機和復原](../recovery/registering-for-application-restart.md)
-   [**SendMessageCallback 函式**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**SendNotifyMessage 函式**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [同步處理物件](../sync/about-synchronization.md)
-   [**TerminateThread 函式**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Windows 錯誤報告](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
