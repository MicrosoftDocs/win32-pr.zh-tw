---
title: WinEvents 和 Active Accessibility 總覽
description: Microsoft Active Accessibility 伺服器會引發 WinEvents，以便在可存取的物件變更時通知用戶端。
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b351b1ce7b6337c4ca0ac0827daff2978c6611af
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103932883"
---
# <a name="winevents-and-active-accessibility"></a><span data-ttu-id="b08d4-103">WinEvents 和 Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="b08d4-103">WinEvents and Active Accessibility</span></span>

<span data-ttu-id="b08d4-104">Microsoft Active Accessibility 伺服器會引發 *WinEvents* ，以便在可存取的物件變更時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="b08d4-104">Microsoft Active Accessibility servers raise *WinEvents* to notify clients when an accessible object changes.</span></span> <span data-ttu-id="b08d4-105">在許多情況中，伺服器會通知用戶端有變更。</span><span class="sxs-lookup"><span data-stu-id="b08d4-105">There are numerous conditions in which a server notifies a client of a change.</span></span> <span data-ttu-id="b08d4-106">Microsoft Active Accessibility 所定義的每個 [事件常數](event-constants.md) 都會描述用戶端收到通知的條件。</span><span class="sxs-lookup"><span data-stu-id="b08d4-106">Each [event constant](event-constants.md) defined by Microsoft Active Accessibility describes a condition about which a client is notified.</span></span> <span data-ttu-id="b08d4-107">例如，WinEvents 可能會發出信號：</span><span class="sxs-lookup"><span data-stu-id="b08d4-107">For example, WinEvents can signal:</span></span>

- <span data-ttu-id="b08d4-108">建立或終結物件時。</span><span class="sxs-lookup"><span data-stu-id="b08d4-108">When an object is created or destroyed.</span></span>
- <span data-ttu-id="b08d4-109">當物件接收或失去焦點時。</span><span class="sxs-lookup"><span data-stu-id="b08d4-109">When an object receives or loses focus.</span></span>
- <span data-ttu-id="b08d4-110">當物件的狀態或位置變更時。</span><span class="sxs-lookup"><span data-stu-id="b08d4-110">When the state or location of an object changes.</span></span>
- <span data-ttu-id="b08d4-111">當物件的任何屬性變更時。</span><span class="sxs-lookup"><span data-stu-id="b08d4-111">When any property of an object changes.</span></span>

<span data-ttu-id="b08d4-112">用戶端應用程式不會自動接收事件通知;他們必須藉由呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) 函式來指定想要接收的事件。</span><span class="sxs-lookup"><span data-stu-id="b08d4-112">Client applications do not receive event notifications automatically; they must specify which events they want to receive by calling the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) function.</span></span> <span data-ttu-id="b08d4-113">使用 **SetWinEventHook** 時，用戶端會註冊以接收一或多個事件，並設定攔截函式來處理指定的事件。</span><span class="sxs-lookup"><span data-stu-id="b08d4-113">With **SetWinEventHook**, a client registers to receive one or more events and sets a hook function to handle the specified events.</span></span> <span data-ttu-id="b08d4-114">用戶端可以使用相同的攔截函式來處理多種類型的事件，也可以使用 multipe 攔截函式。</span><span class="sxs-lookup"><span data-stu-id="b08d4-114">Clients can use the same hook function to handle multiple types of events, or it can use multipe hook functions.</span></span> <span data-ttu-id="b08d4-115">用戶端會針對每個需要註冊的攔截函式呼叫 **SetWinEventHook** 一次。</span><span class="sxs-lookup"><span data-stu-id="b08d4-115">Clients call the **SetWinEventHook** once for each hook function it needs to register.</span></span>

<span data-ttu-id="b08d4-116">攔截函式位於用戶端的程式碼主體內、對應至用戶端進程的 DLL 中，或對應至伺服器進程的 DLL 中。</span><span class="sxs-lookup"><span data-stu-id="b08d4-116">Hook functions are located within the client's code body, in a DLL mapped into the client's process, or in a DLL mapped into the server's process.</span></span> <span data-ttu-id="b08d4-117">這兩種方法都有其優點和缺點。</span><span class="sxs-lookup"><span data-stu-id="b08d4-117">Each of these methods has advantages and disadvantages.</span></span> <span data-ttu-id="b08d4-118">如需詳細資訊，請參閱內部 [內容和跨內容](in-context-and-out-of-context-hook-functions.md)攔截函式。</span><span class="sxs-lookup"><span data-stu-id="b08d4-118">For more information, see [In-Context and Out-of-Context Hook Functions](in-context-and-out-of-context-hook-functions.md).</span></span>

<span data-ttu-id="b08d4-119">若要通知用戶端發生事件，伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)。</span><span class="sxs-lookup"><span data-stu-id="b08d4-119">To notify clients of an event occurrence, servers call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).</span></span> <span data-ttu-id="b08d4-120">系統會檢查是否有任何用戶端應用程式已設定事件的攔截函式，並視需要呼叫適當的攔截函式。</span><span class="sxs-lookup"><span data-stu-id="b08d4-120">The system checks whether any client applications have set hook functions for the event and calls the appropriate hook functions as necessary.</span></span>

<span data-ttu-id="b08d4-121">呼叫用戶端的攔截函式時，它會接收許多描述事件的參數，以及產生事件的物件。</span><span class="sxs-lookup"><span data-stu-id="b08d4-121">When the client's hook function is called, it receives a number of parameters that describe the event and the object that generated the event.</span></span> <span data-ttu-id="b08d4-122">為了取得產生事件之物件的存取權，用戶端攔截函式會呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。</span><span class="sxs-lookup"><span data-stu-id="b08d4-122">To gain access to the object that generated the event, the client hook function calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

> [!NOTE]
> <span data-ttu-id="b08d4-123">如果沒有任何用戶端註冊接收 WinEvents，則對伺服器呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 的效能影響可說是微不足道。</span><span class="sxs-lookup"><span data-stu-id="b08d4-123">If no clients have registered to receive WinEvents, the performance impact on a server for calling [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) is negligible.</span></span>
>
> <span data-ttu-id="b08d4-124">伺服器只會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ，以便在自己的可存取物件中進行變更;它們不會針對系統提供的使用者介面元素中的變更呼叫 **NotifyWinEvent** 。</span><span class="sxs-lookup"><span data-stu-id="b08d4-124">Servers call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) for changes only in their own accessible objects; they do not call **NotifyWinEvent** for changes in system-provided user interface elements.</span></span>

## <a name="event-driven-communication"></a><span data-ttu-id="b08d4-125">Event-Driven 通訊</span><span class="sxs-lookup"><span data-stu-id="b08d4-125">Event-Driven Communication</span></span>

<span data-ttu-id="b08d4-126">用戶端必須先註冊 New-winevent 勾點，才能接收 New-winevent 通知。</span><span class="sxs-lookup"><span data-stu-id="b08d4-126">Clients must register a WinEvent hook before they can receive WinEvent notifications.</span></span> <span data-ttu-id="b08d4-127">為了避免不必要的回呼並提高效能，建議用戶端只註冊所需接收的事件。</span><span class="sxs-lookup"><span data-stu-id="b08d4-127">To avoid unnecessary callbacks and improve performance, clients are advised to register only for the events they need to receive.</span></span>

<span data-ttu-id="b08d4-128">在攔截程式中，用戶端可以呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ，以針對套用事件的元素抓取 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。</span><span class="sxs-lookup"><span data-stu-id="b08d4-128">Inside the hook procedure, the client can call [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element to which the event applies.</span></span> <span data-ttu-id="b08d4-129">使用這個物件，用戶端就可以開始呼叫 **IAccessible** 方法，以抓取資訊或與 UI 元素互動。</span><span class="sxs-lookup"><span data-stu-id="b08d4-129">With this object, the client can begin calling **IAccessible** methods to retrieve information or interact with the UI element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b08d4-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="b08d4-130">Related topics</span></span>

[<span data-ttu-id="b08d4-131">WinEvents</span><span class="sxs-lookup"><span data-stu-id="b08d4-131">WinEvents</span></span>](winevents-infrastructure.md)
