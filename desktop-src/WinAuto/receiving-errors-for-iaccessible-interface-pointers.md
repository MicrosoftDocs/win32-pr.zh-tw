---
title: 接收 IAccessible 介面指標的錯誤
description: 本主題說明您可能會收到 IAccessible 介面指標錯誤的情況。
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840431"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="26622-103">接收 IAccessible 介面指標的錯誤</span><span class="sxs-lookup"><span data-stu-id="26622-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="26622-104">本主題說明您可能會收到 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標錯誤的情況。</span><span class="sxs-lookup"><span data-stu-id="26622-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="26622-105">當使用者關閉物件所屬的應用程式，或是使用者透過使用者介面關閉控制項時， **IAccessible** 函式可能會傳回 **IAccessible** 介面指標的錯誤。</span><span class="sxs-lookup"><span data-stu-id="26622-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="26622-106">使用者關閉應用程式</span><span class="sxs-lookup"><span data-stu-id="26622-106">User Closes an Application</span></span>

<span data-ttu-id="26622-107">如果使用者關閉包含 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標指向之物件的應用程式，則未來對該物件的所有呼叫都會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="26622-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="26622-108">錯誤（如 **共同 \_ 電子 \_ OBJNOTCONNECTED**）將會指出物件不再存在。</span><span class="sxs-lookup"><span data-stu-id="26622-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="26622-109">這適用于所有 **IAccessible** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="26622-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="26622-110">使用者關閉控制項</span><span class="sxs-lookup"><span data-stu-id="26622-110">User Dismisses a Control</span></span>

<span data-ttu-id="26622-111">如果使用者關閉控制項 (例如，按下按下按鈕) ，用戶端仍然可以在此物件上呼叫 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性，因為物件尚未釋放。</span><span class="sxs-lookup"><span data-stu-id="26622-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="26622-112">不過，未來的呼叫將會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="26622-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="26622-113">這種情況適用于下列函數和方法：</span><span class="sxs-lookup"><span data-stu-id="26622-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="26622-114">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="26622-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="26622-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="26622-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="26622-116">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="26622-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="26622-117">**IAccessible：： accHitTest**</span><span class="sxs-lookup"><span data-stu-id="26622-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="26622-118">**IAccessible：： accNavigate**</span><span class="sxs-lookup"><span data-stu-id="26622-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="26622-119">**IAccessible：： get \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="26622-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="26622-120">**IAccessible：： get \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="26622-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




