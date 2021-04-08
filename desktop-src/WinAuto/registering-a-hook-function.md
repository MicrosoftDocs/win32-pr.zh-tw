---
title: 註冊攔截函式
description: 用戶端應用程式會在 WinEventProc 回呼函數中接收 WinEvents。 回呼函式所執行的動作是由應用程式定義，但語法必須如原型中所指定。
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839663"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="d796b-104">註冊攔截函式</span><span class="sxs-lookup"><span data-stu-id="d796b-104">Registering a Hook Function</span></span>

<span data-ttu-id="d796b-105">用戶端應用程式會在 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函數中接收 WinEvents。</span><span class="sxs-lookup"><span data-stu-id="d796b-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="d796b-106">回呼函式所執行的動作是由應用程式定義，但語法必須如原型中所指定。</span><span class="sxs-lookup"><span data-stu-id="d796b-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="d796b-107">函式必須先透過呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)來註冊，才能接收事件。</span><span class="sxs-lookup"><span data-stu-id="d796b-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="d796b-108">用戶端可以多次呼叫 **SetWinEventHook** 來註冊不同的攔截函式，或為先前註冊的攔截函式設定其他事件。</span><span class="sxs-lookup"><span data-stu-id="d796b-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="d796b-109">呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) 時，用戶端會指定要接收的事件以及接收它們的方式。</span><span class="sxs-lookup"><span data-stu-id="d796b-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="d796b-110">用戶端可以選擇：</span><span class="sxs-lookup"><span data-stu-id="d796b-110">The client can choose to:</span></span>

-   <span data-ttu-id="d796b-111">接收所有事件或一組特定的事件。</span><span class="sxs-lookup"><span data-stu-id="d796b-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="d796b-112">從所有線程或從特定執行緒接收事件。</span><span class="sxs-lookup"><span data-stu-id="d796b-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="d796b-113">從所有進程或特定進程接收事件。</span><span class="sxs-lookup"><span data-stu-id="d796b-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="d796b-114">處理進程中或進程外的事件。</span><span class="sxs-lookup"><span data-stu-id="d796b-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="d796b-115">當產生的事件符合指定的準則時，系統會呼叫用戶端的 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函數 (或「攔截程式」 ) 。</span><span class="sxs-lookup"><span data-stu-id="d796b-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="d796b-116">攔截函式接收的參數會告訴用戶端有關視窗、物件，以及產生事件的可能子項目。</span><span class="sxs-lookup"><span data-stu-id="d796b-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="d796b-117">用戶端會在物件抓取呼叫中使用這些參數，例如 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。</span><span class="sxs-lookup"><span data-stu-id="d796b-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




