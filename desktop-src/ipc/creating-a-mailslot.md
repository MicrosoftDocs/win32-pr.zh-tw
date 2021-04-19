---
description: 如何建立 mailslots。 Mailslots 由三個特殊功能支援： CreateMailslot、GetMailslotInfo 和 SetMailslotInfo。 這些函式是由郵筒伺服器使用。
ms.assetid: 7f5a3b36-9583-43fc-a977-321c00a48edb
title: 建立信箱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4cfbcf990162347d1e45da01c815002f39299e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987369"
---
# <a name="creating-a-mailslot"></a><span data-ttu-id="2f981-105">建立信箱</span><span class="sxs-lookup"><span data-stu-id="2f981-105">Creating a Mailslot</span></span>

<span data-ttu-id="2f981-106">Mailslots 由三個特殊功能支援： [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)、 [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo)和 [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo)。</span><span class="sxs-lookup"><span data-stu-id="2f981-106">Mailslots are supported by three specialized functions: [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota), [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo), and [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo).</span></span> <span data-ttu-id="2f981-107">這些函式是由郵筒伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="2f981-107">These functions are used by the mailslot server.</span></span>

<span data-ttu-id="2f981-108">下列程式碼範例會使用 [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) 函式，將控制碼抓取到名為「範例 mailslot」的信箱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2f981-108">The following code sample uses the [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota) function to retrieve the handle to a mailslot named "sample\_mailslot".</span></span> <span data-ttu-id="2f981-109">[寫入郵筒](writing-to-a-mailslot.md)的程式碼範例會顯示用戶端應用程式如何寫入此信箱。</span><span class="sxs-lookup"><span data-stu-id="2f981-109">The code sample in [Writing to a Mailslot](writing-to-a-mailslot.md) shows how client application can write to this mailslot.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

HANDLE hSlot;
LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WINAPI MakeSlot(LPCTSTR lpszSlotName) 
{ 
    hSlot = CreateMailslot(lpszSlotName, 
        0,                             // no maximum message size 
        MAILSLOT_WAIT_FOREVER,         // no time-out for operations 
        (LPSECURITY_ATTRIBUTES) NULL); // default security
 
    if (hSlot == INVALID_HANDLE_VALUE) 
    { 
        printf("CreateMailslot failed with %d\n", GetLastError());
        return FALSE; 
    } 
    else printf("Mailslot created successfully.\n"); 
    return TRUE; 
}

void main()
{ 
   MakeSlot(SlotName);
}
```



<span data-ttu-id="2f981-110">若要建立可由子進程繼承的郵筒，應用程式應變更作為 [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)最後一個參數傳遞的 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85))結構。</span><span class="sxs-lookup"><span data-stu-id="2f981-110">To create a mailslot that can be inherited by child processes, an application should change the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure passed as the last parameter of [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota).</span></span> <span data-ttu-id="2f981-111">若要這樣做，應用程式會將此結構的 **bInheritHandle** 成員設定為 **TRUE** (預設設定為 **FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="2f981-111">To do this, the application sets the **bInheritHandle** member of this structure to **TRUE** (the default setting is **FALSE**).</span></span>

 

 
