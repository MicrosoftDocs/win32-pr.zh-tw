---
title: 用戶端/伺服器通訊
description: WinEvents 機制提供一種方式，讓伺服器能夠輕鬆與 Microsoft Active Accessibility 用戶端進行通訊。
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "106966436"
---
# <a name="clientserver-communication"></a><span data-ttu-id="3eee3-103">用戶端/伺服器通訊</span><span class="sxs-lookup"><span data-stu-id="3eee3-103">Client/Server Communication</span></span>

<span data-ttu-id="3eee3-104">[WinEvents](winevents-overview.md)機制提供一種方式，讓伺服器能夠輕鬆與 Microsoft Active Accessibility 用戶端進行通訊。</span><span class="sxs-lookup"><span data-stu-id="3eee3-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="3eee3-105">用戶端通常會藉由回應 WinEvents (來收集資訊，例如，遵循焦點) ，但是隨時都可自由地從伺服器要求資訊。</span><span class="sxs-lookup"><span data-stu-id="3eee3-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="3eee3-106">若要要求產生 New-winevent 之可存取物件的資訊，用戶端必須處理事件，並使用相關的可存取物件建立連接。</span><span class="sxs-lookup"><span data-stu-id="3eee3-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="3eee3-107">若要這樣做，用戶端會執行下列六個步驟：</span><span class="sxs-lookup"><span data-stu-id="3eee3-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="3eee3-108">伺服器會呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) ，以針對其使用者介面元素的每個變更產生 new-winevent 通知。</span><span class="sxs-lookup"><span data-stu-id="3eee3-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="3eee3-109">使用者中的 New-winevent 管理程式碼會判斷是否有任何用戶端應用程式使用 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) [*註冊 new-winevent 攔截*](/windows/desktop/api/Winuser/nc-winuser-wineventproc)函式，並呼叫已註冊的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="3eee3-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="3eee3-110">在其回呼函式中，用戶端會藉由呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 或其他可存取的物件抓取函式，要求存取產生事件的物件。</span><span class="sxs-lookup"><span data-stu-id="3eee3-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="3eee3-111">如需詳細資訊，請參閱 [取出 IAccessible 物件](retrieving-an-iaccessible-object.md)。</span><span class="sxs-lookup"><span data-stu-id="3eee3-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="3eee3-112">此 Microsoft Active Accessibility API 會將一個 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送給伺服器應用程式，以抓取可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="3eee3-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="3eee3-113">為了回應 [**WM \_ GETOBJECT**](wm-getobject.md)，伺服器應用程式會傳回零或傳回值，作為產生事件之物件的一次性參考。</span><span class="sxs-lookup"><span data-stu-id="3eee3-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="3eee3-114">如果伺服器傳回零，Microsoft Active Accessibility 會建立 proxy 物件，並將其位址提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="3eee3-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="3eee3-115">否則，Microsoft Active Accessibility 會使用這個參考來取出物件介面（例如 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 或 [**IDispatch**](idispatch-interface.md)）的位址，並將該位址提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="3eee3-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="3eee3-116">一旦用戶端有介面位址之後，就可以呼叫可存取物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法，以取得資訊。</span><span class="sxs-lookup"><span data-stu-id="3eee3-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3eee3-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="3eee3-117">In this section</span></span>

-   [<span data-ttu-id="3eee3-118">WinEvents 和 Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="3eee3-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="3eee3-119">WM \_ GETOBJECT 的運作方式</span><span class="sxs-lookup"><span data-stu-id="3eee3-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="3eee3-120">正在抓取 IAccessible 物件</span><span class="sxs-lookup"><span data-stu-id="3eee3-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




