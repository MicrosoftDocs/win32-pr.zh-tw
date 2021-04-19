---
title: 什麼是 WinEvents
description: 當系統或使用者介面發生變更時，伺服器應用程式和作業系統會使用 WinEvents 來通知用戶端。
ms.assetid: 43723706-a173-4ddc-b135-824a7a8e8b40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97864f2b1464718680d781ad843345f1e46fce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968057"
---
# <a name="what-are-winevents"></a><span data-ttu-id="5d264-103">什麼是 WinEvents？</span><span class="sxs-lookup"><span data-stu-id="5d264-103">What Are WinEvents?</span></span>

<span data-ttu-id="5d264-104">當系統或使用者介面發生變更時，伺服器應用程式和作業系統會使用 WinEvents 來通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="5d264-104">Server applications and the operating system use WinEvents to notify clients when a change occurs in the system or in the user interface.</span></span>

<span data-ttu-id="5d264-105">New-winevent 支援是 Windows 作業系統的一項功能，可提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="5d264-105">WinEvent support is a feature of the Windows operating system that provides:</span></span>

-   <span data-ttu-id="5d264-106">用戶端用來註冊事件通知的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="5d264-106">A simple way for clients to register for event notifications.</span></span>
-   <span data-ttu-id="5d264-107">將用戶端程式代碼插入伺服器的機制。</span><span class="sxs-lookup"><span data-stu-id="5d264-107">A mechanism for injecting client code into servers.</span></span>
-   <span data-ttu-id="5d264-108">將事件從伺服器路由傳送到感興趣的用戶端。</span><span class="sxs-lookup"><span data-stu-id="5d264-108">Routing of events from servers to interested clients.</span></span>
-   <span data-ttu-id="5d264-109">針對大部分的 **HWND** 型控制項自動產生事件。</span><span class="sxs-lookup"><span data-stu-id="5d264-109">Automatic event generation for most **HWND**-based controls.</span></span>

<span data-ttu-id="5d264-110">**HWND** 型控制項的事件產生對伺服器開發人員來說特別重要。</span><span class="sxs-lookup"><span data-stu-id="5d264-110">Event generation for **HWND**-based controls is especially important for server developers.</span></span> <span data-ttu-id="5d264-111">Microsoft Active Accessibility 執行時間提供所有標準 UI 元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proxy。</span><span class="sxs-lookup"><span data-stu-id="5d264-111">The Microsoft Active Accessibility run-time provides [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proxies for all standard UI elements.</span></span> <span data-ttu-id="5d264-112">同樣地，系統會在每次建立、終結、移動、調整大小或對 **HWND** 型控制項執行任何其他動作時，自動產生適當的 WinEvents。</span><span class="sxs-lookup"><span data-stu-id="5d264-112">Similarly, the system automatically generates the appropriate WinEvents whenever it creates, destroys, moves, resizes, or performs any other action on an **HWND**-based control.</span></span>

<span data-ttu-id="5d264-113">系統會自動支援某些 WinEvents （包括一般 **HWND** 事件）。</span><span class="sxs-lookup"><span data-stu-id="5d264-113">Some WinEvents, including general **HWND** events, are automatically supported by the system.</span></span> <span data-ttu-id="5d264-114">Microsoft Active Accessibility 的伺服器支援其他類型的 WinEvents，例如特定控制項特定的狀態變更或選取事件。</span><span class="sxs-lookup"><span data-stu-id="5d264-114">Other types of WinEvents, such as state changes or selection events specific to a particular control, are supported by Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="5d264-115">當發生影響 UI 的事件時，伺服器可以藉由呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函式，將事件通知廣播給所有感興趣的用戶端。</span><span class="sxs-lookup"><span data-stu-id="5d264-115">When an event occurs that affects the UI, servers can broadcast an event notification to all interested clients by calling the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function.</span></span> <span data-ttu-id="5d264-116">函式呼叫包含的資訊可識別發生的事件種類，以及套用事件的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="5d264-116">The function call includes information that identifies the type of event that occurred, and the UI element to which the event applies.</span></span> <span data-ttu-id="5d264-117">用戶端可以使用此資訊來取得 UI 專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件，並收集詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5d264-117">Clients can use this information to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the UI element and collect more information.</span></span>

<span data-ttu-id="5d264-118">例如，若要通知用戶端控制項的名稱已變更，伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 並傳遞事件參數中的 [**事件 \_ 物件 \_ NAMECHANGE**](event-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d264-118">For example, to notify clients that a control's name has changed, a server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) and passes [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) in the event parameter.</span></span> <span data-ttu-id="5d264-119">系統會藉由判斷哪些用戶端已註冊要接收該特定事件並呼叫其已註冊的回呼函式來回應。</span><span class="sxs-lookup"><span data-stu-id="5d264-119">The system responds by determining which clients have registered to receive that particular event and calls their registered callback function.</span></span> <span data-ttu-id="5d264-120">如果沒有為事件註冊的用戶端，則伺服器對 **NotifyWinEvent** 的呼叫會相當於「無作業」，且效能影響可忽略。</span><span class="sxs-lookup"><span data-stu-id="5d264-120">If no clients have registered for the event, the server's call to **NotifyWinEvent** is comparable to a "no operation" and the performance impact is negligible.</span></span>

<span data-ttu-id="5d264-121">伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ，在事件發生之後向系統公告事件。</span><span class="sxs-lookup"><span data-stu-id="5d264-121">Servers call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to announce the event to the system after the event has occurred.</span></span> <span data-ttu-id="5d264-122">在事件發生之前，它們絕對不能通知系統事件。</span><span class="sxs-lookup"><span data-stu-id="5d264-122">They must never notify the system of an event before the event occurs.</span></span>

<span data-ttu-id="5d264-123">用戶端會使用 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)來註冊回呼攔截函式，以通知事件。</span><span class="sxs-lookup"><span data-stu-id="5d264-123">To be notified of events, clients register callback hook functions by using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="5d264-124">用戶端會針對所有可能的事件設定單一攔截函式，或針對不同的事件範圍設定多個攔截函式。</span><span class="sxs-lookup"><span data-stu-id="5d264-124">Clients set a single hook function for all possible events or multiple hook functions for discrete ranges of events.</span></span> <span data-ttu-id="5d264-125">如需詳細資訊，請參閱 [註冊](registering-a-hook-function.md)攔截函式。</span><span class="sxs-lookup"><span data-stu-id="5d264-125">For more information, see [Registering a Hook Function](registering-a-hook-function.md).</span></span>

<span data-ttu-id="5d264-126">當 Microsoft Active Accessibility 收到事件的通知時，它會呼叫任何針對該事件註冊的攔截函式，並從 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)傳遞參數。</span><span class="sxs-lookup"><span data-stu-id="5d264-126">When Microsoft Active Accessibility is notified of an event, it calls any hook functions that were registered for that event, passing along the parameters from [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent).</span></span>

 

 




