---
title: 使用 Win32 和 c + +) 開始的視窗訊息 (
description: 使用 Win32 和 c + +) 開始的視窗訊息 (
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00da564396e0f95947e33fb7d8db8b217ac5cdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103836"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>使用 Win32 和 c + +) 開始的視窗訊息 (

GUI 應用程式必須回應來自使用者和作業系統的事件。

- **來自使用者的事件** 包括所有人都可以與您的程式互動的方式：按一下滑鼠、按鍵筆劃、觸控畫面手勢等等。
- **作業系統中的事件** 包含程式的任何「外部」，可能會影響程式的運作方式。 例如，使用者可能會插入新的硬體裝置，或 Windows 可能會進入較低電源狀態 (睡眠或休眠) 。

這些事件可能會在程式執行時的任何時間，以幾乎任何順序發生。 您如何建立程式，使其執行流程無法事先預測？

為了解決這個問題，Windows 使用訊息傳遞模型。 作業系統會將訊息傳遞給應用程式視窗，以與您的應用程式視窗進行通訊。 訊息只是指定特定事件的數值代碼。 例如，如果使用者按下滑鼠左鍵，則視窗會收到具有下列訊息碼的訊息。

```C++
#define WM_LBUTTONDOWN    0x0201
```

有些訊息有與其相關聯的資料。 例如， [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息包含滑鼠游標的 x 座標和 y 座標。

為了將訊息傳遞至視窗，作業系統會呼叫為該視窗註冊的視窗程式。  (，現在您知道視窗程式的用途。 ) 

## <a name="the-message-loop"></a>訊息迴圈

應用程式會在執行時接收數以千計的訊息。  (考慮每個按鍵和滑鼠按鍵的點擊都會產生一則訊息。此外，) 此外，應用程式也可以有數個視窗，每個視窗都有自己的視窗程式。 程式如何接收所有這些訊息，並將它們傳遞至正確的視窗程式？ 應用程式需要迴圈來取出訊息，並將它們分派至正確的視窗。

針對每個建立視窗的執行緒，作業系統會建立視窗訊息的佇列。 此佇列會保留在該執行緒上建立之所有視窗的訊息。 佇列本身在您的程式中是隱藏的。 您無法直接操作佇列。 不過，您可以藉由呼叫 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 函數，從佇列提取訊息。

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

此函式會從佇列的標頭中移除第一則訊息。 如果佇列是空的，則函式會封鎖，直到另一個訊息排入佇列為止。 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)組塊的事實不會讓您的程式沒有回應。 如果沒有任何訊息，程式就不需要執行任何動作。 如果您必須執行背景處理，則可以建立其他執行緒，在 **GetMessage** 等候其他訊息時繼續執行。  (請參閱 [避免視窗程式中的瓶頸](writing-the-window-procedure.md)。 ) 

[**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)的第一個參數是 [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)結構的位址。 如果函式成功，它會將訊息的相關資訊填入 **訊息結構中** 。 這包括目標視窗和訊息碼。 另外三個參數可讓您篩選從佇列取得的訊息。 在幾乎所有情況下，您都會將這些參數設定為零。

雖然 [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) 結構包含訊息的相關資訊，但您幾乎不會直接檢查此結構。 相反地，您會將它直接傳遞給其他兩個函數。

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數與鍵盤輸入相關。 它會將按鍵 (鍵向下轉譯按鍵，並將按鍵) 為字元。 您實際上不需要知道此函式的運作方式。請記得在 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)之前呼叫它。 如果您有好奇，MSDN 檔的連結將會提供更多資訊。

[**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)函式會告知作業系統呼叫訊息目標視窗的視窗程式。 換句話說，作業系統會在其視窗的表格中查閱視窗控制碼、尋找與視窗相關聯的函式指標，以及叫用函數。

例如，假設使用者按下滑鼠左鍵。 這會造成一連串的事件：

1. 作業系統會將 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息放在訊息佇列上。
2. 您的程式會呼叫 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 函數。
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)會從佇列提取 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)訊息，並填滿訊息 [**結構。**](/windows/win32/api/winuser/ns-winuser-msg)
4. 您的程式會呼叫 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 和 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) 函數。
5. 在 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)內，作業系統會呼叫您的視窗程式。
6. 您的視窗程式可以回應或忽略該訊息。

當視窗程式傳回時，它會返回 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)。 這會回到下一個訊息的訊息迴圈。 只要您的程式正在執行，訊息就會繼續抵達佇列。 因此，您必須有迴圈，以持續從佇列提取訊息並分派訊息。 您可以將迴圈視為進行下列動作：

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

當然，這個迴圈永遠不會結束。 這是 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 函數的傳回值。 一般來說， **GetMessage** 會傳回非零值。 當您想要結束應用程式並中斷訊息迴圈時，請呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) 函數。

```C++
        PostQuitMessage(0);
```

[**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)函式會在訊息佇列上放置 [**WM \_ 結束**](/windows/desktop/winmsg/wm-quit)訊息。 **WM \_QUIT** 是特殊訊息：它會使 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 傳回零，並在訊息迴圈結束時發出信號。 以下是修改過的訊息迴圈。

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

只要 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 傳回非零值， **while** 迴圈中的運算式就會評估為 true。 在您呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)之後，運算式會變成 false，而且程式會中斷迴圈。 這種行為 (一個有趣的結果，就是您的視窗程式永遠不會收到 [**WM \_**](/windows/desktop/winmsg/wm-quit) 結束訊息。 因此，您在視窗程式中不需要有此訊息的 case 語句。 ) 

下一個明顯的問題是呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)的時機。 我們會在 [關閉視窗](closing-the-window.md)的主題中返回這個問題，但是首先我們必須撰寫視窗程式。

## <a name="posted-messages-versus-sent-messages"></a>張貼的訊息與傳送的訊息

上一節討論到佇列中的訊息。 有時候，作業系統會直接呼叫視窗程式，略過佇列。

這種差異的術語可能會造成混淆：

-   *張貼* 訊息表示訊息會進入訊息佇列，並透過訊息迴圈 ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 和 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)) 來分派。
-   傳送訊息表示訊息會略過佇列，而作業系統則會直接呼叫視窗程式。

目前的差異並不重要。 視窗程式會處理所有訊息。 但是，有些訊息會略過佇列，並直接移至您的視窗程式。 但是，如果您的應用程式在 windows 之間進行通訊，它可能會有差異。 您可以在 [有關訊息和訊息佇列](/windows/desktop/winmsg/about-messages-and-message-queues)的主題中找到此問題的更詳盡討論。

## <a name="next"></a>下一個

[撰寫視窗程式](writing-the-window-procedure.md)
