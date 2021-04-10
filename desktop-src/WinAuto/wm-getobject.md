---
title: 'WM_GETOBJECT 訊息 (Winuser .h) '
description: 由 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化傳送，可取得伺服器應用程式中所包含之可存取物件的相關資訊。
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT message Windows 協助工具
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106464"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="8bf91-104">WM \_ GETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="8bf91-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="8bf91-105">由 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化傳送，可取得伺服器應用程式中所包含之可存取物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8bf91-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="8bf91-106">應用程式永遠不會直接傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8bf91-106">Applications never send this message directly.</span></span> <span data-ttu-id="8bf91-107">Microsoft Active Accessibility 傳送此訊息以回應 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)、 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8bf91-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="8bf91-108">不過，伺服器應用程式會處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="8bf91-108">However, server applications handle this message.</span></span> <span data-ttu-id="8bf91-109">消費者介面自動化傳送此訊息以回應 [**IUIAutomation：： ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)、 [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)和 [**system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)的呼叫，以及處理用戶端已註冊的事件時。</span><span class="sxs-lookup"><span data-stu-id="8bf91-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8bf91-110">參數</span><span class="sxs-lookup"><span data-stu-id="8bf91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf91-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8bf91-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf91-112">提供訊息的其他相關資訊，而且僅供系統使用。</span><span class="sxs-lookup"><span data-stu-id="8bf91-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="8bf91-113">伺服器會在處理訊息時，將 *dwFlags* 傳遞為 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)呼叫中的 *wParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="8bf91-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="8bf91-114">*dwObjId*</span><span class="sxs-lookup"><span data-stu-id="8bf91-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf91-115">物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bf91-115">Object identifier.</span></span> <span data-ttu-id="8bf91-116">此值是其中一個 [物件識別碼](object-identifiers.md) 常數或自訂物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bf91-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="8bf91-117">伺服器應用程式必須檢查此值，以識別所要求的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="8bf91-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="8bf91-118">在比較此值與 OBJID \_ 值之前，伺服器必須將它轉換成 **DWORD**; 否則，在64位的 Windows 上， *lParam* 的正負號延伸可能會干擾比較。</span><span class="sxs-lookup"><span data-stu-id="8bf91-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="8bf91-119">如果 *dwObjId* 是其中一個 OBJID \_ 值（例如 [**OBJID \_ 用戶端**](object-identifiers.md)），則要求是針對可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的 Microsoft Active Accessibility 物件。</span><span class="sxs-lookup"><span data-stu-id="8bf91-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="8bf91-120">如果 *dwObjId* 等於 **UiaRootObjectId**，則要求是針對消費者介面自動化提供者。</span><span class="sxs-lookup"><span data-stu-id="8bf91-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="8bf91-121">如果伺服器正在執行消費者介面自動化，則應該使用 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函式傳回提供者。</span><span class="sxs-lookup"><span data-stu-id="8bf91-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="8bf91-122">如果 *dwObjId* 是 [**OBJID \_ NATIVEOM**](object-identifiers.md)，則要求是針對控制項的基礎物件模型。</span><span class="sxs-lookup"><span data-stu-id="8bf91-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="8bf91-123">如果控制項支援此要求，則會呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式來傳回適當的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="8bf91-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="8bf91-124">如果 *dwObjId* 是 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md)，則要求會讓控制項將本身識別為標準的 Windows 控制項，或是通用控制項程式庫 (ComCtrl.dll) 所執行的通用控制項。</span><span class="sxs-lookup"><span data-stu-id="8bf91-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf91-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bf91-125">Return value</span></span>

<span data-ttu-id="8bf91-126">如果視窗或控制項不需要回應這則訊息，則應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式;否則，視窗或控制項應傳回對應至 *dwObjId* 所指定之要求的值：</span><span class="sxs-lookup"><span data-stu-id="8bf91-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="8bf91-127">如果視窗或控制項執行消費者介面自動化，則視窗或控制項應該會傳回呼叫 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函式所取得的值。</span><span class="sxs-lookup"><span data-stu-id="8bf91-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="8bf91-128">如果 *dwObjId* 是 [**OBJID \_ NATIVEOM**](object-identifiers.md) ，且視窗公開原生物件模型，則 Windows 應該會傳回呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函數所取得的值。</span><span class="sxs-lookup"><span data-stu-id="8bf91-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="8bf91-129">如果 *dwObjId* 是 [**OBJID \_ 用戶端**](object-identifiers.md) 且視窗會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，則視窗應該會傳回 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 函式的呼叫所取得的值。</span><span class="sxs-lookup"><span data-stu-id="8bf91-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf91-130">備註</span><span class="sxs-lookup"><span data-stu-id="8bf91-130">Remarks</span></span>

<span data-ttu-id="8bf91-131">當用戶端呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 或任何其他 **AccessibleObjectFrom**_X_ 函式，以抓取物件的介面時，Microsoft Active Accessibility 會將 **WM \_ GETOBJECT** 訊息傳送至適當的伺服器應用程式中適當的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="8bf91-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="8bf91-132">處理 **WM \_ GETOBJECT** 時，伺服器應用程式會呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ，並使用此函數的傳回值做為訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="8bf91-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="8bf91-133">Microsoft Active Accessibility 與 COM 程式庫搭配使用，會執行適當的封送處理，並將介面指標從伺服器傳遞回用戶端。</span><span class="sxs-lookup"><span data-stu-id="8bf91-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="8bf91-134">在物件完全初始化或開始關閉之前，伺服器不會回應 **WM \_ GETOBJECT** 。</span><span class="sxs-lookup"><span data-stu-id="8bf91-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="8bf91-135">當應用程式建立新的視窗時，系統會傳送 [**事件 \_ 物件 \_ 建立**](event-constants.md) 來通知用戶端，然後再將 [WM \_ 建立](../winmsg/wm-create.md) 訊息傳送至應用程式的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="8bf91-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="8bf91-136">因為許多應用程式都使用 WM \_ create 來啟動其初始化程式，所以在完成處理 **wm \_ 建立** 訊息之前，伺服器不會回應 **wm \_ GETOBJECT** 訊息。</span><span class="sxs-lookup"><span data-stu-id="8bf91-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="8bf91-137">伺服器會使用 **WM \_ GETOBJECT** 來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="8bf91-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="8bf91-138">建立新的可存取物件</span><span class="sxs-lookup"><span data-stu-id="8bf91-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="8bf91-139">重複使用物件的現有指標</span><span class="sxs-lookup"><span data-stu-id="8bf91-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="8bf91-140">建立相同物件的新介面</span><span class="sxs-lookup"><span data-stu-id="8bf91-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="8bf91-141">針對用戶端，這表示它們可能會接收相同使用者介面元素的相異介面指標，視伺服器的動作而定。</span><span class="sxs-lookup"><span data-stu-id="8bf91-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="8bf91-142">為了判斷兩個介面指標是否指向相同的使用者介面元素，用戶端會比較物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性。</span><span class="sxs-lookup"><span data-stu-id="8bf91-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="8bf91-143">比較指標無法運作。</span><span class="sxs-lookup"><span data-stu-id="8bf91-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf91-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bf91-144">Requirements</span></span>



| <span data-ttu-id="8bf91-145">需求</span><span class="sxs-lookup"><span data-stu-id="8bf91-145">Requirement</span></span> | <span data-ttu-id="8bf91-146">值</span><span class="sxs-lookup"><span data-stu-id="8bf91-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf91-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bf91-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf91-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bf91-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8bf91-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bf91-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf91-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bf91-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8bf91-151">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8bf91-151">Redistributable</span></span><br/>          | <span data-ttu-id="8bf91-152">使用 SP6 和更新版本和 Windows 95 在 Windows NT 4.0 上 Active Accessibility 1.3 的 RDK</span><span class="sxs-lookup"><span data-stu-id="8bf91-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="8bf91-153">標頭</span><span class="sxs-lookup"><span data-stu-id="8bf91-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf91-154"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8bf91-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf91-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bf91-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf91-156">如何處理 WM \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="8bf91-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="8bf91-157">WM \_ GETOBJECT 的運作方式</span><span class="sxs-lookup"><span data-stu-id="8bf91-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="8bf91-158">**LresultFromObject**</span><span class="sxs-lookup"><span data-stu-id="8bf91-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

