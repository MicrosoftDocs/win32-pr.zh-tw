---
title: WM_GETOBJECT 的運作方式
description: '\_當用戶端呼叫其中一個 AccessibleObjectFromX 函數時，Microsoft Active Accessibility 會將 WM GETOBJECT 訊息傳送至適當的伺服器應用程式。'
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe287bca68c925cb7be95ff52d2dac547ed097
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315283"
---
# <a name="how-wm_getobject-works"></a><span data-ttu-id="5a0aa-103">WM \_ GETOBJECT 的運作方式</span><span class="sxs-lookup"><span data-stu-id="5a0aa-103">How WM\_GETOBJECT Works</span></span>

<span data-ttu-id="5a0aa-104">當用戶端呼叫其中一個 \**AccessibleObjectFrom \* \* \* X* 函式時，Microsoft Active Accessibility 會將 [**WM \_ GETOBJECT**](wm-getobject.md)訊息傳送至適當的伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-104">Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) message to the appropriate server application when a client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span> <span data-ttu-id="5a0aa-105">下列清單說明發生的各種案例：</span><span class="sxs-lookup"><span data-stu-id="5a0aa-105">The following list describes the various scenarios that occur:</span></span>

-   <span data-ttu-id="5a0aa-106">如果接收 [**WM \_ GETOBJECT**](wm-getobject.md)的視窗或控制項執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，則視窗會傳回使用 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)的 **IAccessible** 介面參考。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-106">If the window or control that receives [**WM\_GETOBJECT**](wm-getobject.md) implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window returns a reference to the **IAccessible** interface using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="5a0aa-107">Microsoft Active Accessibility，結合元件物件模型 (COM) 程式庫時，會執行適當的封送處理，並將介面指標從伺服器傳遞回用戶端。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-107">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>
-   <span data-ttu-id="5a0aa-108">如果接收訊息的視窗沒有執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-108">If the window that receives the message does not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), it should return zero.</span></span>
-   <span data-ttu-id="5a0aa-109">如果視窗未處理 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息， [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-109">If the window does not handle the [**WM\_GETOBJECT**](wm-getobject.md) message, the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

<span data-ttu-id="5a0aa-110">即使伺服器傳回零，Microsoft Active Accessibility 仍會為用戶端提供物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-110">Even if the server returns zero, Microsoft Active Accessibility still provides the client with information about the object.</span></span> <span data-ttu-id="5a0aa-111">針對大部分系統提供的物件（例如清單方塊和按鈕），Microsoft Active Accessibility 提供完整的資訊。對於其他物件，則會限制資訊。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-111">For most system-provided objects such as list boxes and buttons, Microsoft Active Accessibility provides complete information; for other objects, the information is limited.</span></span> <span data-ttu-id="5a0aa-112">例如，Microsoft Active Accessibility 不會提供沒有視窗控制碼之控制項的資訊。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-112">For example, Microsoft Active Accessibility does not provide information for controls that do not have a window handle.</span></span> <span data-ttu-id="5a0aa-113">Microsoft Active Accessibility 會傳回 proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，用戶端會使用此指標來取得物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-113">Microsoft Active Accessibility returns a proxied [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer that the client uses to get information about the object.</span></span>

<span data-ttu-id="5a0aa-114">如需詳細資訊，請參閱 [WM \_ GETOBJECT Message](the-wm-getobject-message.md)。</span><span class="sxs-lookup"><span data-stu-id="5a0aa-114">For more information, see [The WM\_GETOBJECT Message](the-wm-getobject-message.md).</span></span>

 

 