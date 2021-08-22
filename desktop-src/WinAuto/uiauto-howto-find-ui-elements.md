---
title: 如何尋找 UI 元素
description: 本主題包含範例程式碼，示範如何在消費者介面自動化樹狀結構中尋找 UI 元素。
ms.assetid: b613eb18-e14d-468e-833d-072bad29ba06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52998ad92fe1912a5159443642d95bbc14a28da595ddd2b2a255ebecaed8c74d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505268"
---
# <a name="how-to-find-ui-elements"></a>如何尋找 UI 元素

本主題包含範例程式碼，示範如何在消費者介面自動化樹狀結構中尋找 UI 元素。

-   [依名稱尋找元素](#finding-an-element-by-name)
-   [尋找相關元素](#finding-related-elements)
-   [相關主題](#related-topics)

## <a name="finding-an-element-by-name"></a>依名稱尋找元素

下列範例會尋找具有指定名稱的 Microsoft 消費者介面自動化元素，而且是桌面視窗的子系。


```C++
IUIAutomationElement* GetTopLevelWindowByName(LPWSTR windowName)
{
    if (windowName == NULL)
    {
        return NULL;
    }

    VARIANT varProp;
    varProp.vt = VT_BSTR;
    varProp.bstrVal = SysAllocString(windowName);
    if (varProp.bstrVal == NULL)
    {
        return NULL;
    }

    IUIAutomationElement* pRoot = NULL;
    IUIAutomationElement* pFound = NULL;

    // Get the desktop element. 
    HRESULT hr = g_pAutomation->GetRootElement(&pRoot);
    if (FAILED(hr) || pRoot == NULL)
        goto cleanup;

    // Get a top-level element by name, such as "Program Manager"
    IUIAutomationCondition* pCondition;
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varProp, &pCondition);
    if (FAILED(hr))
        goto cleanup;

    pRoot->FindFirst(TreeScope_Children, pCondition, &pFound);

cleanup:
    if (pRoot != NULL)
        pRoot->Release();

    if (pCondition != NULL)
        pCondition->Release();

    VariantClear(&varProp);
    return pFound;
}
```



## <a name="finding-related-elements"></a>尋找相關元素

下列範例函式會傳回所有啟用之按鈕的集合，這些按鈕是指定專案的子系。


```C++
IUIAutomationElementArray* GetEnabledButtons(IUIAutomationElement* pParent)
{
    if (pParent == NULL)
    {
        return NULL;
    }
    IUIAutomationCondition* pButtonCondition = NULL;
    IUIAutomationCondition* pEnabledCondition = NULL;
    IUIAutomationCondition* pCombinedCondition = NULL;
    IUIAutomationElementArray* pFound = NULL;

    // Create a property condition for the button control type.
    VARIANT varProp;
    varProp.vt = VT_I4;
    varProp.lVal = UIA_ButtonControlTypeId;
    g_pAutomation->CreatePropertyCondition(UIA_ControlTypePropertyId, varProp, &pButtonCondition);
    if (pButtonCondition == NULL)
        goto cleanup;

    // Create a property condition for the enabled property.
    varProp.vt = VT_BOOL;
    varProp.boolVal = VARIANT_TRUE;
    g_pAutomation->CreatePropertyCondition(UIA_IsEnabledPropertyId, varProp, &pEnabledCondition);
    if (pEnabledCondition == NULL)
        goto cleanup;

    // Combine the conditions.
    g_pAutomation->CreateAndCondition(pButtonCondition, pEnabledCondition, &pCombinedCondition);
    if (pCombinedCondition == NULL)
        goto cleanup;

    // Find the matching elements. Note that if the scope is changed to TreeScope_Descendants, 
    // system buttons on the caption bar will be found as well.
    pParent->FindAll(TreeScope_Children, pCombinedCondition, &pFound);

cleanup:
    if (pButtonCondition != NULL)
        pButtonCondition->Release();

    if (pEnabledCondition != NULL) 
        pEnabledCondition->Release();
    
    if (pCombinedCondition != NULL)
        pCombinedCondition->Release();

    return pFound;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[取得 UI 自動化項目](uiauto-obtainingelements.md)
</dt> <dt>

[消費者介面自動化用戶端的使用說明主題](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




