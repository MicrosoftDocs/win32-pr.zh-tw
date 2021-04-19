---
description: 疑難排解秘訣
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: 疑難排解秘訣
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993192"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="d80b9-103">疑難排解秘訣</span><span class="sxs-lookup"><span data-stu-id="d80b9-103">Troubleshooting Tips</span></span>

<span data-ttu-id="d80b9-104">下列秘訣可協助您避免在您的 DirectShow 應用程式中發生鎖死或損毀。</span><span class="sxs-lookup"><span data-stu-id="d80b9-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="d80b9-105">**全域物件**</span><span class="sxs-lookup"><span data-stu-id="d80b9-105">**Global Objects**</span></span>

<span data-ttu-id="d80b9-106">全域 c + + 物件不應該在其函式方法中建立 DirectShow 物件，或在其函式方法中釋放它們。</span><span class="sxs-lookup"><span data-stu-id="d80b9-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="d80b9-107">這樣做可能會導致應用程式無限期地封鎖，原因如下：</span><span class="sxs-lookup"><span data-stu-id="d80b9-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="d80b9-108">執行緒無法在 DLL 的進入點函數內結束。</span><span class="sxs-lookup"><span data-stu-id="d80b9-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="d80b9-109">核心32會在進入點函式期間保存全域程式鎖定，而且鎖定會防止執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="d80b9-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="d80b9-110">因為某些 DirectShow 物件擁有線程，所以如果是從 DLL 進入點函式內釋出，就可以封鎖它們。</span><span class="sxs-lookup"><span data-stu-id="d80b9-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="d80b9-111">如果應用程式有全域 c + + 物件，則在卸載 DLL 時，C 執行時間 DLL 會呼叫物件的「函式」。</span><span class="sxs-lookup"><span data-stu-id="d80b9-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="d80b9-112">如果函式會釋出 DirectShow 物件，它可以封鎖結果。</span><span class="sxs-lookup"><span data-stu-id="d80b9-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="d80b9-113">基於類似的原因，DLL 不應該在其進入點常式中建立或釋放 DirectShow 物件。</span><span class="sxs-lookup"><span data-stu-id="d80b9-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="d80b9-114">**釋放介面**</span><span class="sxs-lookup"><span data-stu-id="d80b9-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="d80b9-115">當您的應用程式仍在處理訊息時，您應該釋放所有的 DirectShow 介面指標，然後才結束訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="d80b9-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="d80b9-116">否則，您可能會看到各種判斷提示，因為某些 DirectShow 物件會在其清除常式期間傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="d80b9-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="d80b9-117"> (為必然結果，如果您使用 ATL **CWindowImpl** 類別，請勿等候 **OnFinalMessage** 釋放介面。</span><span class="sxs-lookup"><span data-stu-id="d80b9-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="d80b9-118">相反地，當您處理 WM 關閉訊息時，請釋放這些專案 \_ 。 ) </span><span class="sxs-lookup"><span data-stu-id="d80b9-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="d80b9-119">**參考計數**</span><span class="sxs-lookup"><span data-stu-id="d80b9-119">**Reference Counts**</span></span>

<span data-ttu-id="d80b9-120">當 Quartz.dll 卸載的偵錯工具時，它會檢查是否有任何 DirectShow 物件具有未釋放的參考計數。</span><span class="sxs-lookup"><span data-stu-id="d80b9-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="d80b9-121">如果是，則會擲回判斷提示：</span><span class="sxs-lookup"><span data-stu-id="d80b9-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="d80b9-122">當此判斷提示失敗時，表示您的應用程式已洩漏參考計數。</span><span class="sxs-lookup"><span data-stu-id="d80b9-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="d80b9-123">請檢查您的程式碼，並確定您已釋放所有介面指標。</span><span class="sxs-lookup"><span data-stu-id="d80b9-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d80b9-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="d80b9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d80b9-125">在 DirectShow 中進行調試</span><span class="sxs-lookup"><span data-stu-id="d80b9-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



