---
description: 在一個以上的監視器上的視窗或功能表會導致檢視器出現視覺中斷。 為了將這個問題降至最低，系統會在一個監視器上顯示功能表和新的和最大化的視窗。 下表說明如何選擇監視器。
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: 將物件放置在多個顯示監視器上
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6581fbed64b6a8ac83e29410e9758c6dea7b2d145958c57fa187abf34985c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602728"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>將物件放置在多個顯示監視器上

在一個以上的監視器上的視窗或功能表會導致檢視器出現視覺中斷。 為了將這個問題降至最低，系統會在一個監視器上顯示功能表和新的和最大化的視窗。 下表說明如何選擇監視器。



| Object         | 位置                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 時間範圍         | [ [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) (例如) 在監視器上顯示一個視窗，其中包含視窗的最大部分。最大化包含視窗最大部分的監視器，直到最小化為止。<br/> ALT 鍵的按鍵組合會在具有目前使用中視窗的監視器上顯示一個視窗。<br/>                                                                                                                                          |
| 擁有的視窗   | 在與擁有者相同的監視器上。                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 子        | 出現在包含對應功能表項目最大部分的監視器上。                                                                                                                                                                                                                                                                                                                                                                                                          |
| 內容功能表   | 出現在按一下滑鼠右鍵的監視器上。                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 下拉式清單 | 出現在包含下拉式方塊矩形的監視器上。                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 對話方塊     | 會顯示在擁有它之視窗的監視器上。如果定義了 DS \_ CENTERMOUSE 樣式，它就會顯示在具有滑鼠的監視器上。<br/> 如果沒有擁有者，且使用中視窗和對話方塊都在相同的應用程式中，對話方塊會出現在目前使用中視窗的監視器上。<br/> 如果對話方塊沒有擁有者，且使用中視窗與對話方塊不在相同的應用程式中，則會在主要監視器上顯示此對話方塊。<br/> |
| 訊息方塊    | 會顯示在擁有它之視窗的監視器上。                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

如果視窗跨越兩個監視器，而其中一個監視器已重新置放，系統會將視窗放置於包含原始視窗最大部分的監視器上。

應用程式通常也需要放置物件。 例如，可能需要在與另一個視窗相同的監視器上建立一個視窗。

**將物件放置在多個監視系統上**

1.  判斷適當的監視。
2.  取得監視器的座標。
3.  使用座標來放置物件。

一般而言，您會將物件放在主要監視器上，或是在其上已有物件的監視器上。 若要識別指定點、矩形或視窗的監視器，請使用 [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)、 [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)和 [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)。

若要取得監視器的座標，請使用 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)，以提供工作區域和整個監視器矩形。 請注意，SM \_ CXSCREEN 和 sm \_ CYSCREEN 一律會參考主要監視器，而不一定是顯示您應用程式的監視器。 此外，請避免 \_ 使用 SM xxVIRTUALSCREEN，因為這會將您的視窗置於虛擬螢幕上，而不是監視器。

若要在視窗的工作區中將對話方塊置中，請使用 DS \_ 中心樣式。 若要將對話方塊置中至應用程式視窗，請使用 [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect)。 Windows 會自動將功能表和對話方塊限制為監視器。 不過，自訂功能表、自訂下拉式方塊、自訂工具調板和儲存的應用程式位置可能會有問題。

如需如何正確放置物件的範例，請參閱 [在多個顯示器設定上放置物件](positioning-objects-on-a-multiple-display-setup.md)。

使用 SM \_ CXSCREEN 和 sm \_ CYSCREEN 判斷應用程式桌面工具列的位置 (也稱為 *appbar*) 將 appbar 限制為主要監視器。 若要允許 appbar 在任何監視的任何邊緣，請使用適當的系統計量來計算監視器的邊緣。 此外，使用 **get \_ X \_ LPARAM** 並 **取得 \_ Y \_ LPARAM** 宏來將座標解壓縮，否則座標的正負號可能會錯誤。 這些宏包含在 Windowsx 中。

全螢幕視窗的大小需要在不同解析度的監視器之間移動時變更。 若要這樣做，應用程式必須使用 [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) 或 [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) 檢查它所在的視窗，然後使用 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) 來取得監視器的大小。 或者，您可以從 DirectX **DirectDrawEnumerateEx** 功能使用 **HMONITOR** 。 然後使用 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 來定位並調整視窗的大小，以涵蓋監視器。

最大化的視窗不會涵蓋具有 [永遠開啟] 屬性的工作列。 但是，全螢幕視窗涵蓋工作列，例如，Microsoft PowerPoint 投影片放映和遊戲中。

若要在應用程式結束時儲存（以及稍後還原）視窗的位置，請使用 [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) 和 [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) 函數。 不過，請先檢查位置是否仍然有效，再使用它，因為可能已從系統中移動或移除此監視器。 如果視窗的 **HMONITOR** 無效，應用程式會在主要監視器上顯示視窗。

系統會嘗試在包含其快捷方式的監視器上啟動應用程式。 因此，將應用程式定位的其中一種方式是在所需的監視器上具有其快捷方式。

如果您使用 [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) ，請提供 *hWnd* ，讓系統在與呼叫應用程式相同的監視器上開啟任何新視窗。

請注意，具有多個監視器的系統會稍微改變 [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) 結構的值。

 

 
