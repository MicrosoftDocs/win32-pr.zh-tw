---
description: 偵錯工具可以用來建立基本的事件驅動偵錯工具。
ms.assetid: 3c9e186b-6844-4126-b035-a3541880e109
title: 關於基本的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa3e2889d860d747978f2e8866094b0f866910c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847142"
---
# <a name="about-basic-debugging"></a><span data-ttu-id="9e533-103">關於基本的調試</span><span class="sxs-lookup"><span data-stu-id="9e533-103">About Basic Debugging</span></span>

<span data-ttu-id="9e533-104">[調試](debugging-functions.md)程式可以用來建立基本的事件驅動偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9e533-104">The [debugging functions](debugging-functions.md) can be used to create a basic, event-driven debugger.</span></span> <span data-ttu-id="9e533-105">*事件驅動* 表示每次在所要進行的進程中發生特定事件時，就會通知偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9e533-105">*Event-driven* means that the debugger is notified every time certain events occur in the process being debugged.</span></span> <span data-ttu-id="9e533-106">通知可讓偵錯工具採取適當的動作來回應事件。</span><span class="sxs-lookup"><span data-stu-id="9e533-106">Notification enables the debugger to take appropriate action in response to the events.</span></span>

<span data-ttu-id="9e533-107">如需偵錯工具詞彙的總覽，請參閱 [偵錯工具術語](debugging-terminology.md)。</span><span class="sxs-lookup"><span data-stu-id="9e533-107">For an overview of debugging terms, see [Debugging Terminology](debugging-terminology.md).</span></span>

<span data-ttu-id="9e533-108">[進程、執行緒和例外](debug-support-from-process-thread-and-exception-functions.md) 狀況函式的 Debug 支援描述特定進程、執行緒和例外狀況處理函式的偵錯工具特定功能。</span><span class="sxs-lookup"><span data-stu-id="9e533-108">[Debug Support from Process, Thread, and Exception Functions](debug-support-from-process-thread-and-exception-functions.md) describes the debugging-specific features of certain process, thread, and exception-handling functions.</span></span>

<span data-ttu-id="9e533-109">[建立基本的偵錯工具](creating-a-basic-debugger.md) 描述如何使用基本的偵錯工具來建立簡單的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9e533-109">[Creating a Basic Debugger](creating-a-basic-debugger.md) describes using the basic debugging functions to create a simple debugger.</span></span> <span data-ttu-id="9e533-110">這些函式可讓應用程式等候偵測事件、引發中斷點例外狀況、將執行控制傳送到偵錯工具等等。</span><span class="sxs-lookup"><span data-stu-id="9e533-110">These functions enable an application to wait for debugging events, cause breakpoint exceptions, transfer execution control to the debugger, and so on.</span></span>

<span data-ttu-id="9e533-111">[調試事件](debugging-events.md) 會描述 debug 事件機制。</span><span class="sxs-lookup"><span data-stu-id="9e533-111">[Debugging Events](debugging-events.md) describes the debug event mechanism.</span></span> <span data-ttu-id="9e533-112">偵錯工具事件會導致系統通知偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9e533-112">Debugging events cause the system to notify the debugger.</span></span>

 

 



