---
description: 任何執行緒都可以建立視窗。
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: 線上程中建立視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985449"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="2e7b4-103">線上程中建立視窗</span><span class="sxs-lookup"><span data-stu-id="2e7b4-103">Creating Windows in Threads</span></span>

<span data-ttu-id="2e7b4-104">任何執行緒都可以建立視窗。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-104">Any thread can create a window.</span></span> <span data-ttu-id="2e7b4-105">建立視窗的執行緒擁有視窗和其相關聯的訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="2e7b4-106">因此，執行緒必須提供訊息迴圈，以處理其訊息佇列中的訊息。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="2e7b4-107">此外，您必須在該執行緒中使用 [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) 或 [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) ，而不是在其他 [等候](/windows/desktop/Sync/wait-functions)函式中使用，讓它可以處理訊息。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="2e7b4-108">否則，當執行緒在等候時傳送訊息時，系統可能會變成鎖死。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="2e7b4-109">[**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)函數可以用來允許一組執行緒共用相同的輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="2e7b4-110">藉由共用輸入狀態，執行緒就會共用使用中視窗的概念。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="2e7b4-111">如此一來，一個執行緒就可以永遠啟動另一個執行緒的視窗。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="2e7b4-112">這項功能也適用于在共用輸入狀態的不同執行緒所建立的視窗之間，共用焦點狀態、滑鼠捕捉狀態、鍵盤狀態和視窗迭置順序狀態。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="2e7b4-113">如需建立 windows 的詳細資訊，請參閱 [Windows 類別](../winmsg/window-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="2e7b4-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
