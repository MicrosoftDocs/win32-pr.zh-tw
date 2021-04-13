---
title: 支援 UI 自動化提供者的控制項模式
description: 本主題說明 Microsoft 消費者介面自動化提供者如何實行控制項的控制項模式。 控制項模式可讓用戶端應用程式操作控制項並取得其相關資訊。
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313580"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a><span data-ttu-id="e1363-104">支援 UI 自動化提供者的控制項模式</span><span class="sxs-lookup"><span data-stu-id="e1363-104">Support Control Patterns in a UI Automation Provider</span></span>

<span data-ttu-id="e1363-105">本主題說明 Microsoft 消費者介面自動化提供者如何實行控制項的控制項模式。</span><span class="sxs-lookup"><span data-stu-id="e1363-105">This topic shows how a Microsoft UI Automation provider implements control patterns for a control.</span></span> <span data-ttu-id="e1363-106">控制項模式可讓用戶端應用程式操作控制項並取得其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1363-106">Control patterns enable client applications to manipulate the control and get information about it.</span></span>

<span data-ttu-id="e1363-107">提供者會依照下列主要步驟來執行控制項模式：</span><span class="sxs-lookup"><span data-stu-id="e1363-107">A provider implements a control pattern by following these main steps:</span></span>

1.  <span data-ttu-id="e1363-108">執行支援控制項模式的提供者介面。</span><span class="sxs-lookup"><span data-stu-id="e1363-108">Implement the provider interface that supports the control pattern.</span></span> <span data-ttu-id="e1363-109">例如，若要支援 [選取](uiauto-implementingselection.md) 控制項模式，自訂清單控制項的提供者會執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="e1363-109">For example, to support the [Selection](uiauto-implementingselection.md) control pattern, a provider for a custom list control would implement the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>
2.  <span data-ttu-id="e1363-110">當消費者介面自動化呼叫提供者的 [**IRawElementProviderSimple：： GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) 方法時，傳回包含控制項模式提供者介面的物件。</span><span class="sxs-lookup"><span data-stu-id="e1363-110">Return an object that contains the control pattern provider interface when UI Automation calls the provider's [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) method.</span></span>

<span data-ttu-id="e1363-111">下列範例顯示自訂單一選取清單控制項的 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 介面執行。</span><span class="sxs-lookup"><span data-stu-id="e1363-111">The following example shows the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface implementation for a custom, single-selection list control.</span></span> <span data-ttu-id="e1363-112">此實作為 IsSelectionRequired 和 CanSelectMultiple 屬性的屬性抓取方法，以及用來為選取的清單專案取得提供者的方法。</span><span class="sxs-lookup"><span data-stu-id="e1363-112">The implementation includes property-retrieval methods for the IsSelectionRequired and CanSelectMultiple properties, and a method for retrieving the provider for the selected list item.</span></span>


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



<span data-ttu-id="e1363-113">下列範例示範 [**IRawElementProviderSimple：： GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) 的執行，其會傳回可執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)的物件。</span><span class="sxs-lookup"><span data-stu-id="e1363-113">The following example shows an implementation of [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) that returns an object that implements [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span> <span data-ttu-id="e1363-114">大部分的清單控制項也會支援其他模式，但此範例會傳回所有其他控制項模式識別碼的 null 參考。</span><span class="sxs-lookup"><span data-stu-id="e1363-114">Most list controls would support other patterns as well, but this example returns a null reference for all other control pattern identifiers.</span></span>


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="e1363-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1363-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e1363-116">**概念**</span><span class="sxs-lookup"><span data-stu-id="e1363-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1363-117">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="e1363-117">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="e1363-118">消費者介面自動化提供者的使用說明主題</span><span class="sxs-lookup"><span data-stu-id="e1363-118">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




