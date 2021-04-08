---
title: 將消費者介面自動化功能新增至 Active Accessibility 伺服器
description: 沒有 Microsoft 消費者介面自動化提供者，但可執行 IAccessible 的控制項，可以透過執行 IAccessibleEx 介面，輕鬆地升級以提供某些消費者介面自動化功能。
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- 消費者介面自動化，Active Accessibility 伺服器
- 消費者介面自動化，Microsoft Active Accessibility 伺服器
- 消費者介面自動化、IAccessible
- 消費者介面自動化、IAccessibleEx
- 消費者介面自動化，公開 IAccessibleEx
- 消費者介面自動化，執行 IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- 公開 IAccessibleEx
- 執行 IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933295"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a>將消費者介面自動化功能新增至 Active Accessibility 伺服器

沒有 Microsoft 消費者介面自動化提供者，但可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 的控制項，可以透過執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，輕鬆地升級以提供某些消費者介面自動化功能。 這個介面可讓控制項公開消費者介面自動化屬性和控制項模式，而不需要完整地執行消費者介面自動化提供者介面（例如 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)）。 若要執行 **IAccessibleEx**，基準 Microsoft Active Accessibility 物件階層必須不包含任何錯誤或不一致的 (例如，父物件的父物件不會將它列為子) ，且不能與消費者介面自動化規格衝突。 如果 Microsoft Active Accessibility 的物件階層符合這些需求，則這是使用 **IAccessibleEx** 來新增功能的絕佳候選。否則，您必須單獨或 Microsoft Active Accessibility 執行來執行消費者介面自動化。

採用具有範圍值的自訂控制項案例。 控制項的 Microsoft Active Accessibility 伺服器會定義其角色，而且能夠傳回其目前值，但缺少傳回控制項最小值和最大值的方法，因為這些屬性未在 Microsoft Active Accessibility 中定義。 消費者介面自動化的用戶端能夠取得控制項的角色、目前的值和其他 Microsoft Active Accessibility 屬性，因為消費者介面自動化 core 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)取得這些屬性。 但是，若沒有物件的 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) 介面存取權，消費者介面自動化也無法取得最大值和最小值。

控制項開發人員可以為控制項提供完整的消費者介面自動化提供者，但這表示複製了許多現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行功能：例如，導覽和通用屬性。 相反地，開發人員可以繼續依賴 **IAccessible** 來提供此功能，同時透過 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)新增對控制項特定屬性的支援。

更新自訂控制項需要下列主要步驟：

-   在可存取的物件上執行 [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) ，以便在這個或個別的物件上找到 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面。
-   在可存取的物件上執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。
-   針對任何 Microsoft Active Accessibility 子專案建立相異的可存取物件，Microsoft Active Accessibility 可能已在父物件上以 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面表示 (例如，) 清單專案。 在這些物件上執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。
-   在所有可存取的物件上執行 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 。
-   在可存取的物件上，執行適當的控制項模式介面。

本主題包含下列各節。

-   [公開 IAccessibleEx](#exposing-iaccessibleex)
-   [執行 IAccessibleEx](#implementing-iaccessibleex)
-   [相關主題](#related-topics)

## <a name="exposing-iaccessibleex"></a>公開 IAccessibleEx

由於控制項的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 執行可能位於不同的物件中，因此用戶端應用程式無法依賴 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得這個介面。 相反地，用戶端應該呼叫 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))。 在這個方法的下列範例中，假設 **IAccessibleEx** 不是在另一個物件上執行;因此，此方法只會對 **QueryInterface** 呼叫。


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a>執行 IAccessibleEx

最感興趣的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 方法為 [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)。 此方法可讓 Microsoft Active Accessibility 伺服器有機會建立可存取的物件， (一個公開的子專案 **IAccessibleEx**) 。 在 Microsoft Active Accessibility 中，子專案通常不會表示為可存取的物件，而是可存取物件的子系。 不過，因為消費者介面自動化要求每個專案都以個別的可存取物件來表示，所以 **GetObjectForChild** 必須為每個子系視需要建立個別的物件。

下列範例執行會傳回自訂清單視圖中專案的可存取物件。


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



如需完整的範例執行，請參閱 [讓自訂控制項可供存取，第5部分：使用 IAccessibleEx 將消費者介面自動化支援新增至 MSDN 上的自訂控制項](/previous-versions/msdn10/cc307850(v=msdn.10)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化提供者程式設計人員指南](uiauto-providerportal.md)
</dt> </dl>

 

 