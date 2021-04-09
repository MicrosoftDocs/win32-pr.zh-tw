---
description: 在正在進行調試的進程中發生例外狀況時，系統會將例外狀況傳遞給偵錯工具，以通知偵錯工具。 這就是所謂的第一次通知。 系統接著會暫止正在進行調試之進程中的所有線程。
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: 用於偵錯工具的例外狀況處理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846932"
---
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="5c81d-105">用於偵錯工具的例外狀況處理函式</span><span class="sxs-lookup"><span data-stu-id="5c81d-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="5c81d-106">在正在進行調試的進程中發生例外狀況時，系統會將例外狀況傳遞給偵錯工具，以通知偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="5c81d-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="5c81d-107">這就是所謂的 *第一次通知*。</span><span class="sxs-lookup"><span data-stu-id="5c81d-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="5c81d-108">系統接著會暫止正在進行調試之進程中的所有線程。</span><span class="sxs-lookup"><span data-stu-id="5c81d-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="5c81d-109">如果偵錯工具未處理例外狀況，系統會嘗試找出適當的例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="5c81d-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="5c81d-110">如果系統找不到適當的系統，系統會再次通知偵錯工具發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5c81d-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="5c81d-111">這就是所謂的 *最後機會通知*。</span><span class="sxs-lookup"><span data-stu-id="5c81d-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="5c81d-112">如果偵錯工具未在最後一次發生通知之後處理例外狀況，則系統會終止正在進行調試的進程。</span><span class="sxs-lookup"><span data-stu-id="5c81d-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="5c81d-113">如需詳細資訊，請參閱 [偵錯工具例外狀況處理](debugger-exception-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="5c81d-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



