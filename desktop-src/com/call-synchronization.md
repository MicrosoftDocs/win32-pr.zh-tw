---
title: 呼叫同步處理
description: 呼叫同步處理
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024159"
---
# <a name="call-synchronization"></a><span data-ttu-id="503b4-103">呼叫同步處理</span><span class="sxs-lookup"><span data-stu-id="503b4-103">Call Synchronization</span></span>

<span data-ttu-id="503b4-104">COM 應用程式在處理來自 COM 或作業系統的一或多個呼叫時，必須能夠正確地處理使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="503b4-104">COM applications must be able to deal correctly with user input while processing one or more calls from COM or the operating system.</span></span> <span data-ttu-id="503b4-105">COM 僅提供單一執行緒單元的呼叫同步處理。</span><span class="sxs-lookup"><span data-stu-id="503b4-105">COM provides call synchronization for single-threaded apartments only.</span></span> <span data-ttu-id="503b4-106">多執行緒單元 (包含無限制執行緒的執行緒) 不會在) 的相同執行緒上進行 (呼叫時接收呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-106">Multithreaded apartments (containing free-threaded threads) do not receive calls while making calls (on the same thread).</span></span> <span data-ttu-id="503b4-107">多執行緒單元無法進行輸入同步處理呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-107">Multithreaded apartments cannot make input synchronized calls.</span></span> <span data-ttu-id="503b4-108">非同步呼叫會轉換成多執行緒單元中的同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-108">Asynchronous calls are converted to synchronous calls in multithreaded apartments.</span></span> <span data-ttu-id="503b4-109">不會針對多執行緒單元中的任何執行緒呼叫訊息篩選器。</span><span class="sxs-lookup"><span data-stu-id="503b4-109">The message filter is not called for any thread in a multithreaded apartment.</span></span> <span data-ttu-id="503b4-110">如需執行緒問題的詳細資訊，請參閱 [進程、執行緒和單元](processes--threads--and-apartments.md)。</span><span class="sxs-lookup"><span data-stu-id="503b4-110">For more information about threading issues, see [Processes, Threads, and Apartments](processes--threads--and-apartments.md).</span></span>

<span data-ttu-id="503b4-111">進程之間的 COM 呼叫分為三個類別，如下所示：</span><span class="sxs-lookup"><span data-stu-id="503b4-111">COM calls between processes fall into three categories, as follows:</span></span>

<dl> <dt>

<span data-ttu-id="503b4-112"><span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*同步呼叫*</span><span class="sxs-lookup"><span data-stu-id="503b4-112"><span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Synchronous calls*</span></span>
</dt> <dd>

<span data-ttu-id="503b4-113">大部分在 COM 中發生的通訊都是同步的。</span><span class="sxs-lookup"><span data-stu-id="503b4-113">Most of the communication that takes place within COM is synchronous.</span></span> <span data-ttu-id="503b4-114">進行同步呼叫時，呼叫端會先等候回復，再繼續進行，並可在等候時接收傳入訊息。</span><span class="sxs-lookup"><span data-stu-id="503b4-114">When making synchronous calls, the caller waits for the reply before continuing and can receive incoming messages while waiting.</span></span> <span data-ttu-id="503b4-115">COM 進入強制回應迴圈，以控制的方式來等候回復、接收和分派其他訊息。</span><span class="sxs-lookup"><span data-stu-id="503b4-115">COM enters a modal loop to wait for the reply, receiving and dispatching other messages in a controlled manner.</span></span>

</dd> <dt>

<span data-ttu-id="503b4-116"><span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*非同步通知*</span><span class="sxs-lookup"><span data-stu-id="503b4-116"><span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Asynchronous notifications*</span></span>
</dt> <dd>

<span data-ttu-id="503b4-117">傳送非同步通知時，呼叫端不會等候回復。</span><span class="sxs-lookup"><span data-stu-id="503b4-117">When sending asynchronous notifications, the caller does not wait for the reply.</span></span> <span data-ttu-id="503b4-118">COM 會使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 或高階事件來傳送非同步通知（視平臺而定）。</span><span class="sxs-lookup"><span data-stu-id="503b4-118">COM uses [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) or high-level events to send asynchronous notifications, depending on the platform.</span></span> <span data-ttu-id="503b4-119">COM 定義五個 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)的非同步方法：</span><span class="sxs-lookup"><span data-stu-id="503b4-119">COM defines five asynchronous methods of [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):</span></span>

-   [<span data-ttu-id="503b4-120">**OnDataChange**</span><span class="sxs-lookup"><span data-stu-id="503b4-120">**OnDataChange**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [<span data-ttu-id="503b4-121">**OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="503b4-121">**OnViewChange**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [<span data-ttu-id="503b4-122">**OnRename**</span><span class="sxs-lookup"><span data-stu-id="503b4-122">**OnRename**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [<span data-ttu-id="503b4-123">**OnSave**</span><span class="sxs-lookup"><span data-stu-id="503b4-123">**OnSave**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [<span data-ttu-id="503b4-124">**OnClose**</span><span class="sxs-lookup"><span data-stu-id="503b4-124">**OnClose**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> <span data-ttu-id="503b4-125">當 COM 正在處理非同步呼叫時，無法進行同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-125">While COM is processing an asynchronous call, synchronous calls cannot be made.</span></span> <span data-ttu-id="503b4-126">例如，容器應用程式的 [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) 執行不能包含 [**IPersistStorage：： Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-126">For example, a container application's implementation of [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) cannot contain a call to [**IPersistStorage::Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save).</span></span> <span data-ttu-id="503b4-127">這些呼叫是 COM 唯一支援的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-127">These calls are the only asynchronous calls supported by COM.</span></span> <span data-ttu-id="503b4-128">目前沒有任何方法可建立非同步自訂介面。</span><span class="sxs-lookup"><span data-stu-id="503b4-128">There is no way to create a custom interface that is asynchronous at this time.</span></span>

 

</dd> <dt>

<span data-ttu-id="503b4-129"><span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*輸入同步呼叫*</span><span class="sxs-lookup"><span data-stu-id="503b4-129"><span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Input-synchronized calls*</span></span>
</dt> <dd>

<span data-ttu-id="503b4-130">進行輸入同步處理呼叫時，呼叫的物件必須先完成呼叫，才能產生控制權。</span><span class="sxs-lookup"><span data-stu-id="503b4-130">When making input-synchronized calls, the object called must complete the call before yielding control.</span></span> <span data-ttu-id="503b4-131">這有助於確保焦點管理能正常運作，而且會適當地處理使用者輸入的資料。</span><span class="sxs-lookup"><span data-stu-id="503b4-131">This helps ensure that focus management works correctly and that data entered by the user is processed appropriately.</span></span> <span data-ttu-id="503b4-132">這些呼叫是由 COM 透過 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式來進行，而不需要進入強制回應迴圈。</span><span class="sxs-lookup"><span data-stu-id="503b4-132">These calls are made by COM through the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function, without entering a modal loop.</span></span> <span data-ttu-id="503b4-133">處理輸入同步處理的呼叫時，呼叫的物件不能呼叫任何函數或方法 (包括可能會產生控制權) 的同步方法。</span><span class="sxs-lookup"><span data-stu-id="503b4-133">While processing an input-synchronized call, the object called must not call any function or method (including synchronous methods) that might yield control.</span></span> <span data-ttu-id="503b4-134">下列是輸入同步處理的方法</span><span class="sxs-lookup"><span data-stu-id="503b4-134">The following methods are input synchronized</span></span>

-   [<span data-ttu-id="503b4-135">**IOleWindow：： GetWindow**</span><span class="sxs-lookup"><span data-stu-id="503b4-135">**IOleWindow::GetWindow**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [<span data-ttu-id="503b4-136">**IOleInPlaceActiveObject：： OnFrameWindowActivate**</span><span class="sxs-lookup"><span data-stu-id="503b4-136">**IOleInPlaceActiveObject::OnFrameWindowActivate**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [<span data-ttu-id="503b4-137">**IOleInPlaceActiveObject：： OnDocWindowActivate**</span><span class="sxs-lookup"><span data-stu-id="503b4-137">**IOleInPlaceActiveObject::OnDocWindowActivate**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [<span data-ttu-id="503b4-138">**IOleInPlaceActiveObject：： ResizeBorder**</span><span class="sxs-lookup"><span data-stu-id="503b4-138">**IOleInPlaceActiveObject::ResizeBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [<span data-ttu-id="503b4-139">**IOleInPlaceUIWindow::GetBorder**</span><span class="sxs-lookup"><span data-stu-id="503b4-139">**IOleInPlaceUIWindow::GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [<span data-ttu-id="503b4-140">**IOleInPlaceUIWindow::RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="503b4-140">**IOleInPlaceUIWindow::RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [<span data-ttu-id="503b4-141">**IOleInPlaceUIWindow::SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="503b4-141">**IOleInPlaceUIWindow::SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [<span data-ttu-id="503b4-142">**IOleInPlaceFrame：： SetMenu**</span><span class="sxs-lookup"><span data-stu-id="503b4-142">**IOleInPlaceFrame::SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [<span data-ttu-id="503b4-143">**IOleInPlaceFrame：： SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="503b4-143">**IOleInPlaceFrame::SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [<span data-ttu-id="503b4-144">**IOleInPlaceObject::SetObjectRects**</span><span class="sxs-lookup"><span data-stu-id="503b4-144">**IOleInPlaceObject::SetObjectRects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

<span data-ttu-id="503b4-145">為了將非同步訊息處理可能產生的問題降至最低，大部分的 COM 方法呼叫都是同步的。</span><span class="sxs-lookup"><span data-stu-id="503b4-145">To minimize problems that can arise from asynchronous message processing, the majority of COM method calls are synchronous.</span></span> <span data-ttu-id="503b4-146">透過同步通訊，不需要特殊的程式碼來分派和處理傳入的訊息。</span><span class="sxs-lookup"><span data-stu-id="503b4-146">With synchronous communication, there is no need for special code to dispatch and handle incoming messages.</span></span> <span data-ttu-id="503b4-147">當應用程式進行同步方法呼叫時，COM 會進入強制回應的等候迴圈，以處理所需的回復，並將傳入訊息分派到能夠處理這些訊息的應用程式。</span><span class="sxs-lookup"><span data-stu-id="503b4-147">When an application makes a synchronous method call, COM enters a modal wait loop that handles the required replies and dispatches incoming messages to applications capable of processing them.</span></span>

<span data-ttu-id="503b4-148">COM 會藉由指派稱為 *邏輯執行緒* 識別碼的識別碼來管理方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="503b4-148">COM manages method calls by assigning an identifier called a *logical thread ID*.</span></span> <span data-ttu-id="503b4-149">當使用者選取功能表命令或應用程式起始新的 COM 作業時，就會指派新的。</span><span class="sxs-lookup"><span data-stu-id="503b4-149">A new one is assigned when a user selects a menu command or when the application initiates a new COM operation.</span></span> <span data-ttu-id="503b4-150">後續與初始 COM 呼叫相關的呼叫會被指派與初始呼叫相同的邏輯執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="503b4-150">Subsequent calls that relate to the initial COM call are assigned the same logical thread ID as the initial call.</span></span>

 

 