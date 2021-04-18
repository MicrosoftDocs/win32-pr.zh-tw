---
title: 關於動畫控制項
description: 動畫控制項是顯示 Audio-Video 交錯 (AVI) 剪輯的視窗。 AVI 剪輯是一系列的點陣圖框架，例如電影。 動畫控制項只能顯示不包含音訊的 AVI 剪輯。
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625828e5f4febce7314da365c9db93ce3a07136
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965870"
---
# <a name="about-animation-controls"></a>關於動畫控制項

*動畫控制項* 是顯示 Audio-Video 交錯 (AVI) 剪輯的視窗。 AVI 剪輯是一系列的點陣圖框架，例如電影。 動畫控制項只能顯示不包含音訊的 AVI 剪輯。

動畫控制項的常見用途之一，是在冗長的作業期間表示系統活動。 這是可能的，因為操作執行緒會在顯示 AVI 剪輯時繼續執行。 例如，Windows 檔案總管的 [尋找] 對話方塊會在系統搜尋檔案時顯示移動放大鏡。

> [!Note]  
> 如果您使用 ComCtl32.dll 版本6，則不支援此執行緒;請確定您的應用程式不會封鎖 UI，否則不會發生動畫。

 

動畫控制項可以顯示源自未壓縮 AVI 檔案的 AVI 剪輯，或從使用執行時間長度 (BI RLE8) 編碼所壓縮的 AVI 檔案 \_ 。 您可以將 AVI 剪輯以 AVI 資源的形式新增至您的應用程式，也可以將您的應用程式隨附于不同的 AVI 檔。

> [!Note]  
> AVI 檔案或資源不能有音效通道。 動畫控制項的功能非常有限，而且可能會變更。 如果您需要控制項來提供應用程式的多媒體播放和記錄功能，您可以使用 MCIWnd 控制項。 如需詳細資訊，請參閱 [MCIWnd 視窗類別](/windows/desktop/Multimedia/mciwnd-window-class)。

 

本節將討論下列主題。

-   [建立動畫控制項](#animation-control-creation)
-   [關於動畫控制項訊息](#about-animation-control-messages)
-   [預設訊息處理](#default-message-processing)

## <a name="animation-control-creation"></a>建立動畫控制項

動畫控制項屬於 [**動畫 \_ 類別**](common-control-window-classes.md) 視窗類別。 您可以使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式或建立動畫宏 [**\_ 建立**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 動畫控制項。 宏會將動畫控制項放在父視窗的左上角，如果未指定 [**ACS \_ CENTER**](animation-control-styles.md) 樣式，則會根據 AVI 剪輯中的框架維度來設定控制項的寬度和高度。 如果指定了 **ACS \_ 中心** ， **\_ 建立動畫** 會將控制項的寬度和高度設定為零。 您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式來設定控制項的位置和大小。

如果您在對話方塊或對話方塊資源內建立動畫控制項，當使用者關閉對話方塊時，控制項會自動終結控制項。 如果您在視窗內建立動畫控制項，則必須明確地終結控制項。

## <a name="about-animation-control-messages"></a>關於動畫控制項訊息

應用程式會將訊息傳送至動畫控制項，以開啟、播放、停止及關閉對應的 AVI 剪輯。 每個訊息都有一或多個宏可供您使用，而不是明確地傳送訊息。

建立動畫控制項之後，應用程式會傳送未配置的 [**\_ 開啟**](acm-open.md) 訊息來開啟 AVI 剪輯，並將其載入記憶體中。 這則訊息會指定 AVI 檔案的路徑或 AVI 資源的名稱。 系統會從建立動畫控制項的模組載入 AVI 資源。

如果動畫控制項具有 [**ACS \_ 自動播放**](animation-control-styles.md) 樣式，則在開啟 AVI 檔案或 avi 資源之後，控制項會立即開始播放 avi 剪輯。 否則，應用程式可以使用「執行中的」 [**\_ 播放**](acm-play.md) 訊息來啟動 AVI 剪輯。 應用程式可以藉由傳送未產生的 [**\_ 停止**](acm-stop.md) 訊息，隨時停止剪輯。 當控制項完成播放 AVI 剪輯或傳送 **「完成」 \_ 時，會** 顯示最後播放的畫面格。

動畫控制項可以將兩個通知代碼傳送至其父視窗： [ACN \_ START](acn-start.md) 和 [ACN \_ STOP](acn-stop.md)。 大部分的應用程式都不會處理任一種通知。

若要關閉 AVI 檔案或 AVI 資源，並將它從記憶體中移除，應用程式可以使用「[**動畫 \_ 關閉**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)」宏，此宏會將檔案名或資源名稱設定為 **Null** 的 [**\_ 開啟狀態**](acm-open.md)傳送給。

## <a name="default-message-processing"></a>預設訊息處理

本章節描述由 [**動畫 \_ 類別**](common-control-window-classes.md) 視窗類別的視窗程式所處理的視窗訊息。



| 訊息                                    | 處理已執行                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close)           | 釋出與動畫控制項相關聯的 AVI 檔案或 AVI 資源。                                                                                                                                                                                                                   |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)       | 釋放 AVI 檔案或 AVI 資源、釋放內部資料結構，然後呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。                                                                                                                                                |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd) | 使用靜態控制項目前的背景色彩來清除視窗背景。                                                                                                                                                                                                        |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)     | 配置並初始化內部資料結構，然後呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。                                                                                                                                                                              |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) | 傳回 HTTRANSPARENT 點擊測試值。                                                                                                                                                                                                                                                   |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)              | 在動畫控制項中繪製 AVI 框架。                                                                                                                                                                                                                                                |
| [**WM \_ 大小**](/windows/desktop/winmsg/wm-size)             | 檢查控制項是否具有 [**ACS \_ 中心**](animation-control-styles.md) 樣式。 如果控制項不存在，就會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。 否則，它會將動畫放在控制項中，使控制項失效，然後呼叫 **DefWindowProc**。 |



 

 

 