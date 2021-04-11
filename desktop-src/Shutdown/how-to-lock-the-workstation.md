---
description: 下列範例會使用 >lockworkstation 函數來鎖定工作站。 系統會顯示 [鎖定工作站] 對話方塊。 對話方塊的文字指出工作站正在使用中，且已由使用者鎖定。
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: 如何鎖定工作站
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849596"
---
# <a name="how-to-lock-the-workstation"></a>如何鎖定工作站

下列範例會使用 [**>lockworkstation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) 函數來鎖定工作站。 系統會顯示 [ **鎖定工作站** ] 對話方塊。 對話方塊的文字指出工作站正在使用中，且已由使用者鎖定。


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



若要判斷工作站是否已鎖定，請測試您的視窗是否可見。

工作站可以由使用者或系統管理員解除鎖定。 若要解除鎖定系統，請按 Ctrl + Alt + Del 並登入。 若要在使用者登入時收到通知，請使用 [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) 函數進行註冊，以接收 [**WM \_ WTSSESSION \_ 變更**](../termserv/wm-wtssession-change.md) 訊息。 收到此訊息時，請檢查 *wParam* 參數是否等於 WTS \_ 會話 \_ 鎖定。

 

 
