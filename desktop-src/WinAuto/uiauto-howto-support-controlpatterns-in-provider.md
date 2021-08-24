---
title: 支援 UI 自動化提供者的控制項模式
description: 本主題說明 Microsoft 消費者介面自動化提供者如何實行控制項的控制項模式。 控制項模式可讓用戶端應用程式操作控制項並取得其相關資訊。
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649f9419c5e3003c0185f435cba4d38f4a25c3d7adc1bdc7cf9c53cd06b32a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759228"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>支援 UI 自動化提供者的控制項模式

本主題說明 Microsoft 消費者介面自動化提供者如何實行控制項的控制項模式。 控制項模式可讓用戶端應用程式操作控制項並取得其相關資訊。

提供者會依照下列主要步驟來執行控制項模式：

1.  執行支援控制項模式的提供者介面。 例如，若要支援 [選取](uiauto-implementingselection.md) 控制項模式，自訂清單控制項的提供者會執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 介面。
2.  當消費者介面自動化呼叫提供者的 [**IRawElementProviderSimple：： GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) 方法時，傳回包含控制項模式提供者介面的物件。

下列範例顯示自訂單一選取清單控制項的 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 介面執行。 此實作為 IsSelectionRequired 和 CanSelectMultiple 屬性的屬性抓取方法，以及用來為選取的清單專案取得提供者的方法。


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



下列範例示範 [**IRawElementProviderSimple：： GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) 的執行，其會傳回可執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)的物件。 大部分的清單控制項也會支援其他模式，但此範例會傳回所有其他控制項模式識別碼的 null 參考。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[消費者介面自動化提供者的使用說明主題](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




