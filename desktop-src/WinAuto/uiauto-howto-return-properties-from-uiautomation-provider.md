---
title: 如何從消費者介面自動化提供者傳回屬性
description: 本主題包含範例程式碼，示範 Microsoft 消費者介面自動化提供者如何將 UI 元素的屬性傳回給用戶端應用程式。
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1284e2969d726006b4f8a8b0b6b3e63a7e421a14fb688dae5cbf8b8aa53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859457"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>如何從消費者介面自動化提供者傳回屬性

本主題包含範例程式碼，示範 Microsoft 消費者介面自動化提供者如何將 UI 元素的屬性傳回給用戶端應用程式。

為了從提供者抓取屬性值，消費者介面自動化會呼叫提供者的 [**IRawElementProviderSimple：： GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) 方法，並傳遞要取得之屬性的識別碼，以及 [**變數**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構的指標。 如果提供者支援指定的屬性，則會將屬性的資料類型和值複製到 **VARIANT** 結構。 如果不支援此屬性，提供者會將 **VARIANT** 結構的 **vt** 成員設定為 vt \_ 空白。


```C++
IFACEMETHODIMP Provider::GetPropertyValue(PROPERTYID propertyId, VARIANT* pRetVal)
{
    // The Name property is typically the same as the Caption property of the 
    // control window, if it has one. Here, the Name is overridden for the 
    // sake of illustration. 
    if (propertyId == UIA_NamePropertyId) 
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"Custom button");
    }
    
    else if (propertyId == UIA_ControlTypePropertyId) 
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UIA_ButtonControlTypeId; 
    }

    else if (propertyId == UIA_IsContentElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    else if (propertyId == UIA_IsControlElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    //
    // Return other properties as appropriate for the control type. 
    //

    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the  
        // provider for window that hosts the control.
    }
    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[消費者介面自動化提供者的使用說明主題](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 