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
# <a name="how-to-lock-the-workstation"></a><span data-ttu-id="afb83-105">如何鎖定工作站</span><span class="sxs-lookup"><span data-stu-id="afb83-105">How to Lock the Workstation</span></span>

<span data-ttu-id="afb83-106">下列範例會使用 [**>lockworkstation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) 函數來鎖定工作站。</span><span class="sxs-lookup"><span data-stu-id="afb83-106">The following example locks the workstation using the [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) function.</span></span> <span data-ttu-id="afb83-107">系統會顯示 [ **鎖定工作站** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="afb83-107">The system displays the **Lock Workstation** dialog box.</span></span> <span data-ttu-id="afb83-108">對話方塊的文字指出工作站正在使用中，且已由使用者鎖定。</span><span class="sxs-lookup"><span data-stu-id="afb83-108">The dialog box text says that the workstation is in use and has been locked by the user.</span></span>


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



<span data-ttu-id="afb83-109">若要判斷工作站是否已鎖定，請測試您的視窗是否可見。</span><span class="sxs-lookup"><span data-stu-id="afb83-109">To determine whether the workstation is locked, test whether your window is visible.</span></span>

<span data-ttu-id="afb83-110">工作站可以由使用者或系統管理員解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="afb83-110">The workstation can be unlocked by the user or an administrator.</span></span> <span data-ttu-id="afb83-111">若要解除鎖定系統，請按 Ctrl + Alt + Del 並登入。</span><span class="sxs-lookup"><span data-stu-id="afb83-111">To unlock the system, press Ctrl+Alt+Del and log in.</span></span> <span data-ttu-id="afb83-112">若要在使用者登入時收到通知，請使用 [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) 函數進行註冊，以接收 [**WM \_ WTSSESSION \_ 變更**](../termserv/wm-wtssession-change.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="afb83-112">To receive notification when the user logs in, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function to register to receive [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) messages.</span></span> <span data-ttu-id="afb83-113">收到此訊息時，請檢查 *wParam* 參數是否等於 WTS \_ 會話 \_ 鎖定。</span><span class="sxs-lookup"><span data-stu-id="afb83-113">When this message is received, check whether the *wParam* parameter is equal to WTS\_SESSION\_LOCK.</span></span>

 

 
