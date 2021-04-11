---
title: 使用非同步呼叫的事件
description: 使用非同步呼叫的事件
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK，使用非同步呼叫的事件
- Windows Media Format SDK，非同步呼叫事件
- 事件，非同步呼叫
- 非同步呼叫事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372516"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="afff2-107">使用非同步呼叫的事件</span><span class="sxs-lookup"><span data-stu-id="afff2-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="afff2-108">通常，使用以非同步方式呼叫的方法時，您會想要停止進一步處理應用程式，直到方法完成處理為止。</span><span class="sxs-lookup"><span data-stu-id="afff2-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="afff2-109">您可以實行任何您想要的技術來處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="afff2-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="afff2-110">本節說明如何使用事件來等候呼叫執行緒中的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="afff2-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="afff2-111">這項技術經常搭配 Windows Media Format SDK 使用，並會在一些範例應用程式中示範。</span><span class="sxs-lookup"><span data-stu-id="afff2-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="afff2-112">下列清單摘要說明如何使用事件來等候非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="afff2-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="afff2-113">藉由呼叫 Platform SDK 的 **CreateEvent** 函式，建立與您的應用程式搭配使用的事件。</span><span class="sxs-lookup"><span data-stu-id="afff2-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="afff2-114">為您的應用程式執行適當的回呼時，請將需要等候的訊息設為陷阱。</span><span class="sxs-lookup"><span data-stu-id="afff2-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="afff2-115">在所需訊息的訊息處理邏輯中，藉由呼叫 Platform SDK 的 **SetEvent** 函式來發出事件的信號。</span><span class="sxs-lookup"><span data-stu-id="afff2-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="afff2-116">在您的應用程式中進行非同步事件的呼叫之後，請透過呼叫 Platform SDK 的 **WaitForSingleObject** 函式，等候事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="afff2-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="afff2-117">如果您要設計 Windows 應用程式，您應該建立一個迴圈來檢查 Windows 訊息，並在短暫的等候時間內包含對迴圈的 **WaitForSingleObject** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="afff2-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afff2-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="afff2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afff2-119">**使用回呼方法**</span><span class="sxs-lookup"><span data-stu-id="afff2-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




