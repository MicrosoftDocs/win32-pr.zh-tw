---
title: 關於 IP 位址控制項
description: 網際網路通訊協定 (IP) 位址控制可讓使用者以容易理解的格式輸入 IP 位址。
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933644"
---
# <a name="about-ip-address-controls"></a>關於 IP 位址控制項

網際網路通訊協定 (IP) 位址控制可讓使用者以容易理解的格式輸入 IP 位址。 此控制項也可讓應用程式以數值格式（而不是文字格式）取得位址。

-   [關於 IP 位址控制項](#about-ip-address-controls)
-   [建立 IP 位址控制項](#creating-an-ip-address-control)
-   [IP 位址是否可以控制編輯控制項？](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>關於 IP 位址控制項

Windows Internet Explorer 4.0 版引進了 IP 位址控制項，這是一個新的控制項，類似于編輯控制項，可讓使用者輸入網際網路通訊協定中的數位位址， (IP) 格式。 此格式包含 4 3 位數的欄位。 每個欄位都會個別處理;欄位號碼是以零為基底，並從左至右繼續，如下圖所示。

![顯示 ip 位址控制項四個欄位中各項值的圖表](images/ipa-scrn.png)

控制項只允許在每個欄位中輸入數位文字。 一旦在指定的欄位中輸入三個數字，鍵盤焦點就會自動移至下一個欄位。 如果應用程式不需要填滿整個欄位，使用者可以輸入少於三位數。 例如，如果欄位只應包含第二十個數字，輸入 "21" 並按下按鍵，就會將使用者帶到下一個欄位。

每個欄位的預設範圍是0到255，但應用程式可以將範圍設定為這些限制與 [**IPM \_ SETRANGE**](ipm-setrange.md) 訊息之間的任何值。

> [!Note]  
> IP 位址控制是在 Comctl32.dll 4.71 版和更新版本中執行。

 

## <a name="creating-an-ip-address-control"></a>建立 IP 位址控制項

建立 IP 位址控制項之前，請使用 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **dwICC** 成員中設定的「 **ICC \_ 網際網路 \_ 類別**」旗標來呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 。

使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立 IP 位址控制項。 控制項的類別名稱是 [**WC \_ IPADDRESS**](common-control-window-classes.md)，定義于 Commctrl 中。 沒有任何 IP 位址控制特定樣式存在;不過，因為這是子控制項，所以請至少使用 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 系樣式。

## <a name="is-an-ip-address-control-an-edit-control"></a>IP 位址是否可以控制編輯控制項？

IP 位址控制項不是編輯控制項，也不會回應 EM \_ 訊息。 不過，它會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，將下列編輯控制項通知傳送給擁有者視窗。 請注意，IP 位址控制也會 \_ 透過 [**WM \_ 通知**](wm-notify.md) 訊息傳送私用 IPN 通知。



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **通知**                  | **通知的原因**                                                                                                                                                                             |
| [EN \_ SETFOCUS](en-setfocus.md)   | 在 IP 位址控制取得鍵盤焦點時傳送。                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | 在 IP 位址控制項失去鍵盤焦點時傳送。                                                                                                                                              |
| [EN \_ 變更](en-change.md)       | 在 IP 位址控制項中的任何欄位變更時傳送。 就像來自標準編輯控制項的 [EN \_ 變更](en-change.md) 通知一樣，此通知會在螢幕更新之後收到。 |



 

 

 