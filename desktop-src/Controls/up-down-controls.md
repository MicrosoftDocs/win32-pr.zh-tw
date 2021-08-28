---
title: 關於 Up-Down 控制項
description: 由上而下的控制項是一組箭號按鈕，使用者可以按一下來遞增或遞減值，例如在附屬控制項中顯示的捲軸位置或數位， (稱為「合作者視窗) 。
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749014a4b9959b8afd6e769919a0dc9df19e99ce4edeabca774e535f26f4cf8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132151"
---
# <a name="about-up-down-controls"></a>關於 Up-Down 控制項

由上而下的控制項是一組箭號按鈕，使用者可以按一下來遞增或遞減值，例如在附屬控制項中顯示的捲軸位置或數位， (稱為「合作者視窗) 。

對使用者而言，上下控制項和其合作者視窗通常看起來像單一控制項。 您可以指定由上而下的控制項自動定位於其協同視窗的旁邊，而且它會自動將好友視窗的標題設定為目前的位置。 例如，您可以使用上下按鈕控制項搭配編輯控制項，以提示使用者輸入數位。 下圖顯示以編輯控制項作為其協同視窗的上下按鈕控制項，此控制項有時也稱為微調控制項。

![螢幕擷取畫面，顯示在右邊緣有向上和向下箭號的簡短矩形控制項](images/updown.jpg)

本節將討論下列主題。

-   [上下控制項樣式](#up-down-control-styles)
-   [定位與加速](#position-and-acceleration)
-   [預設 Up-Down 控制訊息處理](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Up-Down 控制項樣式

您可以使用視窗樣式來操作最新控制項的特性，例如，它在其協同視窗中的相對位置、是否設定其協同視窗的文字，以及是否要處理向上箭號和向下鍵。

具有 ud [**\_ ALIGNLEFT**](up-down-control-styles.md) 或 ud [**\_ ALIGNRIGHT**](up-down-control-styles.md) 樣式的上下按鈕會對齊其好友視窗的左邊緣或右邊緣。 好友視窗的寬度會減少以容納上下按鈕控制項的寬度。

具有 ud [**\_ SETBUDDYINT**](up-down-control-styles.md) 樣式的上下按鈕控制項，會在目前的位置變更時，設定其好友視窗的標題。 除非指定了 ud [**\_ NOTHOUSANDS**](up-down-control-styles.md) 樣式，否則控制項會在十進位字串的每三位數之間插入千位分隔符號。 如果 [合作者] 視窗是清單方塊，則會將其目前的選取範圍（而不是其標題）設定為由上而下的控制項。

您可以指定 ud [**\_ ARROWKEYS**](up-down-control-styles.md) 樣式，以提供最新控制項的鍵盤介面。 如果指定此樣式，控制項會處理向上和向下鍵。 控制項也會將好友視窗子類別化，讓它可以在好友視窗具有焦點時處理這些按鍵。

如果您使用上下按鈕控制項來進行水準滾動，則可以指定 ud [**\_ HORZ**](up-down-control-styles.md) 樣式。 此樣式會讓下一個控制項的箭號向左和向右指向，而不是向上和向下。

根據預設，如果使用者嘗試遞增或遞減超過最大值或最小值，則目前的位置不會變更。 您可以使用 ud [**\_ 換行**](up-down-control-styles.md) 樣式來變更此行為，讓位置「換行」至相反的極端。 例如，以超過上限的遞增會將位置包裝回下限值。

## <a name="position-and-acceleration"></a>定位與加速

建立上下按鈕控制項之後，您可以藉由傳送訊息來變更控制項的目前位置、最小位置和最大位置。 您也可以變更用來顯示好友視窗中目前位置的基本基底，以及按一下向上或向下箭號時，目前位置變更的速率。

若要取出上下按鈕控制項的目前位置，請使用 [**UDM \_ GETPOS**](udm-getpos.md) 訊息。 針對具有合作者視窗的上下按鈕控制項，目前的位置是在好友視窗標題中的數位。 由於標題可能已變更 (例如，使用者可能已編輯編輯控制項的文字) ，由上而下的控制項則會取得目前的標題，並據以更新其目前的位置。

好友視窗的標題可以是十進位或十六進位字串，取決於基底基底 (也就是由上而下控制項10或 16) 。 您可以使用 [**udm \_ SETBASE**](udm-setbase.md) 訊息來設定基本基底，並使用 [**udm \_ GETBASE**](udm-getbase.md) 訊息來取得基數基底。

[**UDM \_ SETPOS**](udm-setpos.md)訊息會設定合作者視窗的目前位置。 請注意，和捲軸不同的是，當按下向上鍵和向下箭號時，上下按鈕會自動變更其目前的位置。 因此，應用程式在處理 [**WM \_ VSCROLL**](wm-vscroll.md) 或 [**WM \_ HSCROLL**](wm-hscroll.md) 訊息時，不需要設定目前的位置。

您可以使用 [**UDM \_ SETRANGE**](udm-setrange.md) 訊息來變更上下按鈕控制項的最小和最大位置。 最大位置可能小於最小值，而在此情況下，按一下向上箭號按鈕會減少目前的位置。 若要以另一種方式進行，向上指的是移到最大的位置。 若要取得上下按鈕控制項的最小和最大位置，請使用 [**UDM \_ GETRANGE**](udm-getrange.md) 訊息。

您可以設定上下按鈕控制項的加速，以控制當使用者按住箭號按鈕時，位置變更的速率。 加速是由 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) 結構的陣列所定義。 每個結構會指定時間間隔，以及該間隔結束時要遞增或遞減的單位數。 若要設定加速，請使用 [**UDM \_ SETACCEL**](udm-setaccel.md) 訊息。 若要取得加速資訊，請使用 [**UDM \_ GETACCEL**](udm-getaccel.md) 訊息。

## <a name="default-up-down-controls-message-processing"></a>預設 Up-Down 控制訊息處理

本節說明由上而下控制項所處理的標準 Windows 訊息。



| 訊息                                        | 處理已執行                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)             | 配置並初始化私用資料結構，並將其位址儲存為視窗資料。                                                                                                                     |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)           | 釋放在 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 處理期間配置的資料。                                                                                                                                   |
| [**\_啟用 WM**](/windows/desktop/winmsg/wm-enable)             | 使視窗失效。                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | 變更向上箭號或向下鍵時的目前位置。                                                                                                                                   |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | 完成位置變更。                                                                                                                                                                               |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | 捕捉滑鼠。 如果 [合作者] 視窗是 [編輯控制項] 或 [清單] 方塊，則會將焦點設定為 [好友] 視窗。 如果滑鼠移至向上或向下按鈕，就會開始變更位置並設定計時器。 |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | 完成位置的變更，並在上下按鈕控制項已捕捉到滑鼠時放開滑鼠捕捉。 如果 [合作者] 視窗是編輯控制項，則會選取 [編輯] 控制項中的所有文字。             |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                  | 繪製上下按鈕控制項。 如果 *wParam* 參數不是 Null，則控制項會假設值為 **HDC** ，並且使用該裝置內容繪製。                                                    |
| [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer)               | 變更目前的位置，如果滑鼠停留在按鈕上，而且已經過足夠的間隔時間。                                                                                            |



 

 

 