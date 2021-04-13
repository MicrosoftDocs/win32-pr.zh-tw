---
title: 什麼是視窗
description: .
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fcbba817e3e4c9059340d0a67c7170f4583270c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375093"
---
# <a name="what-is-a-window"></a>什麼是視窗？

## <a name="what-is-a-window"></a>什麼是視窗？

很明顯地，windows 是 Windows 的核心。 他們很重要的是，它們會在作業系統之後命名。 但什麼是視窗？ 當您想像一下某個視窗時，您可能會想一下像這樣的內容：

![應用程式視窗的螢幕擷取畫面](images/window01.png)

這種視窗稱為 *應用程式視窗* 或 *主視窗*。 它通常會有一個具有標題列的框架、 **最小化** 和 **最大化** 按鈕，以及其他標準 UI 元素。 框架稱為視窗的 *非工作區* ，因此呼叫的原因是作業系統會管理視窗的該部分。 框架內的區域是工作 *區*。 這是您的程式所管理視窗的一部分。

以下是另一種視窗：

![控制項視窗的螢幕擷取畫面](images/window02.png)

如果您不熟悉 Windows 程式設計，您可能會驚訝 UI 控制項（例如按鈕和編輯方塊）本身就是 windows。 UI 控制項與應用程式視窗之間的主要差異在於控制項本身不存在。 相反地，控制項相對於應用程式視窗的位置。 當您拖曳應用程式視窗時，控制項會依照您的預期來移動它。 此外，控制項和應用程式視窗也可以彼此通訊。  (例如，應用程式視窗會從按鈕接收按一下通知。 ) 

因此，當您考慮到 *視窗* 時，請不要只考慮 *應用程式視窗*。 相反地，請將視窗視為程式設計結構，如下所示：

-   佔用畫面的特定部分。
-   在指定的時刻，可能或可能不會顯示。
-   知道如何自行繪製。
-   回應來自使用者或作業系統的事件。

## <a name="parent-windows-and-owner-windows"></a>父視窗和擁有者視窗

在 UI 控制項的案例中，控制項視窗稱為應用程式視窗的 *子* 系。 應用程式視窗是控制項視窗的 *父系* 。 父視窗提供用來放置子視窗的座標系統。 擁有父視窗會影響視窗外觀的各個層面;例如，會裁剪子視窗，讓子視窗的任何部分不能出現在其父視窗的框線之外。

另一個關聯性是應用程式視窗和強制回應對話方塊視窗之間的關聯性。 當應用程式顯示模式對話方塊時，應用程式視窗會是擁有 *者視窗，* 而對話方塊則是 *擁有* 的視窗。 擁有的視窗一律會出現在其擁有者視窗前方。 當擁有者最小化時，它會被隱藏，而且會與擁有者同時終結。

下圖顯示的應用程式會顯示具有兩個按鈕的對話方塊：

![具有對話方塊的應用程式螢幕擷取畫面](images/window03.png)

應用程式視窗擁有對話方塊視窗，而對話方塊視窗則是這兩個按鈕視窗的父視窗。 下圖顯示這些關係：

![顯示父/子系和擁有者/擁有關系的圖例](images/window04.png)

## <a name="window-handles"></a>視窗控制碼

Windows 是物件—它們都有程式碼和資料，但它們不是 c + + 類別。 相反地，程式會使用稱為 *控制碼* 的值來參考視窗。 控制碼是不透明的型別。 基本上，它只是作業系統用來識別物件的數位。 您可以將視窗畫為具有所有已建立視窗的大型表格。 它會使用此資料表，依據其控點來查閱視窗。  (它在內部的運作方式並不重要。 ) 視窗控制碼的資料型別是 **HWND**，通常是「aitch-風」。 建立 windows： [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) 和 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的函式會傳回視窗控制碼。

若要在視窗上執行作業，您通常會呼叫一些接受 **HWND** 值作為參數的函式。 例如，若要在螢幕上重新調整視窗的位置，請呼叫 [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) 函式：


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



第一個參數是您想要移動的視窗控制碼。 其他參數則指定視窗的新位置，以及是否應該重新繪製視窗。

請記住，控制碼不是指標。 如果 *hwnd* 是包含控制碼的變數，嘗試透過寫入來將控制碼取值 `*hwnd` 是錯誤。

## <a name="screen-and-window-coordinates"></a>螢幕和視窗座標

座標是以與裝置無關的圖元來測量。 當我們討論圖形時，我們將更瞭解與裝置無關的 *圖元* 相關的 *裝置* 部分。

視您的工作而定，您可能會測量相對於畫面的座標（相對於視窗 (，包括畫面格) 或相對於視窗的工作區）。 例如，您會使用螢幕座標將視窗放置在螢幕上，但您會在使用用戶端座標的視窗內繪製。 在每個案例中，原點 (0，0) 一律是區域的左上角。

![顯示幕幕、視窗和工作區座標的圖例](images/coordinates01.png)

## <a name="next"></a>下一個

[WinMain：應用程式進入點](winmain--the-application-entry-point.md)

 

 