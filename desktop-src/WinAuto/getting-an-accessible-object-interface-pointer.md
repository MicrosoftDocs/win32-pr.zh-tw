---
title: 取得可存取的物件介面指標
description: Microsoft Active Accessibility 用戶端應用程式使用下列其中一個函式，抓取可存取物件的介面指標。
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4006bf073075f2aa47a9911565213050e3d11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106978584"
---
# <a name="getting-an-accessible-object-interface-pointer"></a><span data-ttu-id="24833-103">取得可存取的物件介面指標</span><span class="sxs-lookup"><span data-stu-id="24833-103">Getting an Accessible Object Interface Pointer</span></span>

<span data-ttu-id="24833-104">Microsoft Active Accessibility 用戶端應用程式使用下列其中一個函式，抓取可存取物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="24833-104">Microsoft Active Accessibility client applications retrieve interface pointers to accessible objects by using one of the following functions.</span></span>

<span data-ttu-id="24833-105">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="24833-105">**AccessibleObjectFromEvent**</span></span>

<span data-ttu-id="24833-106">許多用戶端會查閱產生事件之特定可存取物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24833-106">Many clients look up information about specific accessible objects that generate events.</span></span> <span data-ttu-id="24833-107">由於 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面是可存取物件的「閘道」，因此用戶端必須有簡單的方法，將 [WinEvents](winevents-overview.md) 與產生事件之物件的 **IAccessible** 介面產生關聯。</span><span class="sxs-lookup"><span data-stu-id="24833-107">Because the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is the "gateway" to accessible objects, clients must have an easy way to associate [WinEvents](winevents-overview.md) with the **IAccessible** interface of the object generating the events.</span></span> <span data-ttu-id="24833-108">Microsoft Active Accessibility 針對此用途特別提供 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 函數。</span><span class="sxs-lookup"><span data-stu-id="24833-108">Microsoft Active Accessibility provides the [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) function specifically for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="24833-109">具有內容攔截函式的用戶端必須先呼叫 [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow)函 [式](in-context-hook-functions.md)，才能呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。</span><span class="sxs-lookup"><span data-stu-id="24833-109">Clients with [in-context hook functions](in-context-hook-functions.md) must call the [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) function before calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

<span data-ttu-id="24833-110">[**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)函式會接受用戶端攔截函式 [*所接收的*](/windows/desktop/api/Winuser/nc-winuser-wineventproc)許多相同資訊。</span><span class="sxs-lookup"><span data-stu-id="24833-110">The [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) function accepts much of the same information that a client's [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) receives.</span></span> <span data-ttu-id="24833-111">當用戶端攔截函式收到事件通知時，它會將適當的參數從事件傳遞至 **AccessibleObjectFromEvent**。</span><span class="sxs-lookup"><span data-stu-id="24833-111">When a client hook function receives an event notification, it passes the appropriate parameters from events to **AccessibleObjectFromEvent**.</span></span>

<span data-ttu-id="24833-112">此函式會抓取產生事件之使用者介面專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，或元素父物件的介面。</span><span class="sxs-lookup"><span data-stu-id="24833-112">The function retrieves either the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface of the user interface element that generated the event or the interface of the element's parent object.</span></span> <span data-ttu-id="24833-113">如果傳回父物件的介面指標，用戶端會呼叫父系的屬性和方法，以取得產生事件之子項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24833-113">If the parent object's interface pointer is returned, the client calls the parent's properties and methods to obtain information about the child element that generated the event.</span></span>

<span data-ttu-id="24833-114">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="24833-114">**AccessibleObjectFromPoint**</span></span>

<span data-ttu-id="24833-115">若要在螢幕上的指定點取出物件 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的位址，用戶端會使用 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) 函數。</span><span class="sxs-lookup"><span data-stu-id="24833-115">To retrieve the address of an object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface at a specified point on the screen, clients use the [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) function.</span></span>

<span data-ttu-id="24833-116">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="24833-116">**AccessibleObjectFromWindow**</span></span>

<span data-ttu-id="24833-117">為了從視窗控制碼取出物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，用戶端會使用 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函數。</span><span class="sxs-lookup"><span data-stu-id="24833-117">To retrieve an object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface from a window handle, clients use the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function.</span></span>

<span data-ttu-id="24833-118">每次呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函數時，伺服器都可以針對相同的使用者介面專案傳回相異的介面指標。</span><span class="sxs-lookup"><span data-stu-id="24833-118">It is possible that servers return distinct interface pointers for the same user interface element each time the [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function is called.</span></span> <span data-ttu-id="24833-119">若要判斷兩個指標是否參考相同的使用者介面元素，用戶端開發人員必須比較物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性，而非指標。</span><span class="sxs-lookup"><span data-stu-id="24833-119">To determine if two pointers refer to the same user interface element, client developers must compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object, not pointers.</span></span>

 

 