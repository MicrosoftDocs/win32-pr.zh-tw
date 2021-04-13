---
title: 根據系統控制項公開控制項
description: 根據系統控制項公開控制項
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376240"
---
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="7b7a8-103">根據系統控制項公開控制項</span><span class="sxs-lookup"><span data-stu-id="7b7a8-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="7b7a8-104">在嘗試本節所述的技術之前，您應該考慮使用某種形式的動態注釋（直接、值對應或伺服器）。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="7b7a8-105">如需詳細資訊，請參閱 [動態批註 API](dynamic-annotation-api.md)。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="7b7a8-106">在大部分的情況下，Microsoft Active Accessibility 會公開 superclass 或子類別化控制項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="7b7a8-107">Superclassing 和子類別化可讓應用程式開發人員使用系統控制項的基本功能來建立自訂控制項，並包含應用程式所提供的增強功能。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="7b7a8-108">Superclass 控制項的視窗類別名稱不同于它所依據的系統控制項。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="7b7a8-109">子類別化控制項具有相同的視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="7b7a8-110">如需有關 superclassing 和子類別化的詳細資訊，請參閱 Windows 軟體開發套件 (SDK) 檔。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="7b7a8-111">因為 Microsoft Active Accessibility 會公開系統提供之控制項的相關資訊，所以 Microsoft Active Accessibility 會公開修改過的控制項，除非 superclass 或子類別化控制項與基底控制項截然不同。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="7b7a8-112">為了判斷修改過的控制項是否可供存取，應用程式開發人員應該使用 [檢查](inspect-objects.md) 和 [可存取的事件](accessible-event-watcher.md) 監看員之類的公用程式，來比較修改過的控制項與基底控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="7b7a8-113">如果您在使用這些公用程式之後判斷出修改過的控制項無法存取，您就必須將控制項視為任何其他自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="7b7a8-114">控制項必須觸發事件，而應用程式的視窗程式必須提供 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面，讓用戶端應用程式用來取得控制項的相關資訊，以回應 [**WM \_ GETOBJECT**](wm-getobject.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="7b7a8-115">CreateStdAccessibleProxy 和 CreateStdAccessibleObject</span><span class="sxs-lookup"><span data-stu-id="7b7a8-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="7b7a8-116">如果已修改控制項的所有或大部分 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性與基底控制項相同，請使用 [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) 或 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) 來簡化控制項 **IAccessible** 介面的執行。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="7b7a8-117">Superclassing 或子類別化可存取的控制項時，請注意 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) 函式所抓取的物件可能只會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="7b7a8-118">它可能包含其他介面，例如 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="7b7a8-119">您可能需要包裝這些額外的介面，以保留控制項原始實作所提供的協助工具支援。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="7b7a8-120">[**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)和 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)函式會為指定的系統控制項取出 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="7b7a8-121">這些函式的差異在於， **CreateStdAccessibleObject** 會使用從 *hwnd* 參數取得的視窗類別名稱，而 **CreateStdAccessibleProxy** 則會使用其 *szClassName* 參數中所指定的視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="7b7a8-122">因此，如果您決定使用這些函式，請使用 **CreateStdAccessibleProxy** 來公開 superclass 控制項的相關資訊，並使用子類別化控制項來執行這兩項功能。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="7b7a8-123">取得系統控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標之後，請在 **IAccessible** 介面的執行中，針對修改過的控制項使用指標。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="7b7a8-124">如果已修改控制項的屬性或方法與基底控制項相同，請使用 **IAccessible** 指標傳回基底控制項所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="7b7a8-125">如果已修改控制項的屬性與基底控制項不同，請覆寫基底控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="7b7a8-126">在下列範例中， **CAccCustomButton** 是衍生自 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的應用程式定義類別。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="7b7a8-127">成員變數 **m \_ PAccDefaultButton** 是 **IAccessible** 介面的指標，該介面是在控制項的初始化程式期間從 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) 取得的。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="7b7a8-128">在此範例中，自訂控制項的 **role** 屬性與系統控制項的 **role** 屬性相同，因此會傳回基底控制項的 **role** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="7b7a8-129">不過， **Description** 屬性與基底控制項的不同，因此會覆寫這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



<span data-ttu-id="7b7a8-130">如需有關系統控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的詳細資訊，請參閱 [附錄 A：支援的消費者介面元素參考](appendix-a--supported-user-interface-elements-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="7b7a8-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 