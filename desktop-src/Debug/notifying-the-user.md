---
description: 為了通知使用者發生某種類型的錯誤，許多應用程式只會使用 MessageBeep 函式來產生音效，或使用 FlashWindow 或 FlashWindowEx 函數來閃爍視窗。
ms.assetid: 35b6e93c-323a-4592-9394-a2e9dd79d9e6
title: 通知使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01a4e68b0c5dffcc5dcae5f2fe3b0c84288f59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187614"
---
# <a name="notifying-the-user"></a><span data-ttu-id="e030b-103">通知使用者</span><span class="sxs-lookup"><span data-stu-id="e030b-103">Notifying the User</span></span>

<span data-ttu-id="e030b-104">為了通知使用者發生某種類型的錯誤，許多應用程式只會使用 [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep) 函式來產生音效，或使用 [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow) 或 [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex) 函數來閃爍視窗。</span><span class="sxs-lookup"><span data-stu-id="e030b-104">To notify the user that some kind of error has occurred, many applications simply produce a sound by using the [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep) function or flash the window by using either the [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow) or [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex) function.</span></span> <span data-ttu-id="e030b-105">應用程式也可以使用這些函式來注意錯誤，然後顯示包含錯誤詳細資料的訊息方塊或錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e030b-105">An application can also use these functions to call attention to an error and then display a message box or an error message containing details about the error.</span></span>

 

 



