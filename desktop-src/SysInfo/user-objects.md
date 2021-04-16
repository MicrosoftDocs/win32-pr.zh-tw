---
description: 使用者介面物件只支援每個物件一個控制碼。 進程無法繼承或重複使用者物件的控制碼。 某個會話中的進程無法參考另一個會話中的使用者控制碼。
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: 使用者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ed8afcf0f1d0e4c232cf503bc2c7ba86dca42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553179"
---
# <a name="user-objects"></a>使用者物件

使用者介面物件只支援每個物件一個控制碼。 進程無法繼承或重複使用者物件的控制碼。 某個會話中的進程無法參考另一個會話中的使用者控制碼。

每個會話都有65536個使用者控制碼的理論限制。 不過，每個會話可以開啟的最大使用者控制碼數目通常較低，因為它會受到可用記憶體的影響。 另外還有使用者控制碼的預設每一進程限制。 若要變更此限制，請設定下列登錄值：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

這個值可以設定為介於200到18000之間的數位。

## <a name="handles-to-user-objects"></a>使用者物件的控制碼

使用者物件的控制碼對所有進程都是公用的。 也就是說，只要進程具有物件的安全性存取權，任何程式都可以使用使用者物件控制碼。

在下圖中，應用程式會建立視窗物件。 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)函數會建立視窗物件，並傳回物件控制碼。

![建立視窗物件的應用程式](images/cshob-01.png)

建立視窗物件之後，應用程式可以使用視窗控制碼來顯示或變更視窗。 控制碼會維持有效，直到視窗物件終結為止。

在下一個圖中，應用程式會終結 window 物件。 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)函式會從記憶體中移除視窗物件，使視窗控制碼失效。

![終結視窗物件](images/cshob-02.png)

## <a name="managing-user-objects"></a>管理使用者物件

下表列出使用者物件，以及每個物件的建立者和 destroyer 函數。 建立者函式會建立物件和物件控制碼，或只傳回現有的物件控制碼。 Destroyer 函式會從記憶體中移除物件，這樣會使物件控制碼失效。



| 使用者物件       | Creator 函數                                                                                                                                                                                                                                                              | Destroyer 函式                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 快速鍵對應表 | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| 插入點             | [**CreateCaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| 資料指標            | [**CreateCursor**](/windows/win32/api/winuser/nf-winuser-createcursor)、 [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)、 [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| DDE 交談  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect)、 [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect)、 [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| 鉤              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| 圖示              | [**CreateIconIndirect**](/windows/win32/api/winuser/nf-winuser-createiconindirect)、 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)、 [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| 功能表              | [**CreateMenu**](/windows/win32/api/winuser/nf-winuser-createmenu)、 [**CreatePopupMenu**](/windows/win32/api/winuser/nf-winuser-createpopupmenu)、 [**LoadMenu**](/windows/win32/api/winuser/nf-winuser-loadmenua)、 [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| 時間範圍            | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)、 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)、 [**CreateDialogParam**](/windows/win32/api/winuser/nf-winuser-createdialogparama)、 [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)、 [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| 視窗位置   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
