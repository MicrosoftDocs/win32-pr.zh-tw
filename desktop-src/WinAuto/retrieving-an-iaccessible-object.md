---
title: 正在抓取 IAccessible 物件
description: Microsoft Active Accessibility 提供可讓用戶端取出可存取物件的 AccessibleObjectFromWindow 和 AccessibleObjectFromPoint 等功能。
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300275"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="905cf-103">正在抓取 IAccessible 物件</span><span class="sxs-lookup"><span data-stu-id="905cf-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="905cf-104">Microsoft Active Accessibility 提供可讓用戶端取出可存取物件的 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 和 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) 等功能。</span><span class="sxs-lookup"><span data-stu-id="905cf-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="905cf-105">這些函式會傳回 [**IDispatch**](idispatch-interface.md) 或 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，用戶端可以透過此指標取得可存取物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="905cf-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="905cf-106">當用戶端呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 或任何其他 \**AccessibleObjectFrom \* \* \* X* 函式以抓取物件的介面時，Microsoft Active Accessibility 會將 [**WM \_ GETOBJECT**](wm-getobject.md) 視窗訊息傳送至適當應用程式內適用的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="905cf-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="905cf-107">若要提供資訊給用戶端，伺服器必須回應 **WM \_ GETOBJECT** message。</span><span class="sxs-lookup"><span data-stu-id="905cf-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="905cf-108">若要收集有關 UI 元素的特定資訊，用戶端必須先取得元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="905cf-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="905cf-109">若要取出專案的 **IAccessible** 物件，用戶端可以使用下列其中一項功能：</span><span class="sxs-lookup"><span data-stu-id="905cf-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="905cf-110">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="905cf-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="905cf-111">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="905cf-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="905cf-112">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="905cf-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="905cf-113">**若要取出 IAccessible 介面指標**</span><span class="sxs-lookup"><span data-stu-id="905cf-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="905cf-114">用戶端會呼叫其中一個 \**AccessibleObjectFrom \* \* \* X* 函數。</span><span class="sxs-lookup"><span data-stu-id="905cf-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="905cf-115">Oleacc.dll 將 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="905cf-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="905cf-116">伺服器會決定哪個 UI 元素對應至要求。</span><span class="sxs-lookup"><span data-stu-id="905cf-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="905cf-117">伺服器會傳回零以要求 Oleacc.dll proxy。</span><span class="sxs-lookup"><span data-stu-id="905cf-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="905cf-118">Or</span><span class="sxs-lookup"><span data-stu-id="905cf-118">Or</span></span>

    <span data-ttu-id="905cf-119">傳回 (原生執行) 的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。</span><span class="sxs-lookup"><span data-stu-id="905cf-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="905cf-120">若要這樣做，它會：</span><span class="sxs-lookup"><span data-stu-id="905cf-120">To do this, it:</span></span>

    -   <span data-ttu-id="905cf-121">為元素結構 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。</span><span class="sxs-lookup"><span data-stu-id="905cf-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="905cf-122">呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 來封送處理物件的指標。</span><span class="sxs-lookup"><span data-stu-id="905cf-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="905cf-123">傳回要 Oleacc.dll 的 LRESULT。</span><span class="sxs-lookup"><span data-stu-id="905cf-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="905cf-124">Oleacc.dll 會檢查來自 [**WM \_ GETOBJECT**](wm-getobject.md)的傳回值。</span><span class="sxs-lookup"><span data-stu-id="905cf-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="905cf-125">如果為零，Oleacc.dll 會建立 proxy 物件，並將它傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="905cf-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="905cf-126">Or</span><span class="sxs-lookup"><span data-stu-id="905cf-126">Or</span></span>

    <span data-ttu-id="905cf-127">如果非零，Oleacc.dll 會呼叫 [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) 來 unmarshal 原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件指標，並將它傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="905cf-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




