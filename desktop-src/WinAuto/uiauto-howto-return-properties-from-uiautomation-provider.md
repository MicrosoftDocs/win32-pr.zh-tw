---
title: 如何從消費者介面自動化提供者傳回屬性
description: 本主題包含範例程式碼，示範 Microsoft 消費者介面自動化提供者如何將 UI 元素的屬性傳回給用戶端應用程式。
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4133a53df3c59e6d5c93b1c9cd8e6aa942b4bd56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375429"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a><span data-ttu-id="8aadb-103">如何從消費者介面自動化提供者傳回屬性</span><span class="sxs-lookup"><span data-stu-id="8aadb-103">How to Return Properties from a UI Automation Provider</span></span>

<span data-ttu-id="8aadb-104">本主題包含範例程式碼，示範 Microsoft 消費者介面自動化提供者如何將 UI 元素的屬性傳回給用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="8aadb-104">This topic contains example code that shows how a Microsoft UI Automation provider returns properties of a UI element to client applications.</span></span>

<span data-ttu-id="8aadb-105">為了從提供者抓取屬性值，消費者介面自動化會呼叫提供者的 [**IRawElementProviderSimple：： GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) 方法，並傳遞要取得之屬性的識別碼，以及 [**變數**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8aadb-105">To retrieve a property value from the provider, UI Automation calls a provider's implementation of the [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) method, passing the ID of the property to retrieve, and a pointer to a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure.</span></span> <span data-ttu-id="8aadb-106">如果提供者支援指定的屬性，則會將屬性的資料類型和值複製到 **VARIANT** 結構。</span><span class="sxs-lookup"><span data-stu-id="8aadb-106">If the provider supports the specified property, it copies the data type and value of the property into the **VARIANT** structure.</span></span> <span data-ttu-id="8aadb-107">如果不支援此屬性，提供者會將 **VARIANT** 結構的 **vt** 成員設定為 vt \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="8aadb-107">If the property is not supported, the provider sets the **vt** member of the **VARIANT** structure to VT\_EMPTY.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8aadb-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="8aadb-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8aadb-109">**概念**</span><span class="sxs-lookup"><span data-stu-id="8aadb-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8aadb-110">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="8aadb-110">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="8aadb-111">消費者介面自動化提供者的使用說明主題</span><span class="sxs-lookup"><span data-stu-id="8aadb-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 