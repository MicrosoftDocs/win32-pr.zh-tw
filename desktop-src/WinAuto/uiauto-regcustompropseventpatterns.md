---
title: 註冊自訂屬性、事件和控制項模式
description: 在可以使用自訂屬性、事件或控制項模式之前，提供者和用戶端都必須在執行時間註冊屬性、事件或控制項模式。
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- 消費者介面自動化，自訂屬性
- 消費者介面自動化，事件總覽
- 消費者介面自動化，控制項模式總覽
- 消費者介面自動化，註冊自訂屬性
- 消費者介面自動化，註冊事件
- 消費者介面自動化，註冊控制項模式
- 自訂屬性，註冊
- 事件，註冊
- 控制項模式，註冊
- 註冊，自訂屬性
- 註冊、事件
- 註冊、控制模式
- 控制項模式，自訂
- 控制項模式，執行自訂
- 執行自訂控制項模式
- 自訂控制項模式
- 用戶端包裝函式
- 模式處理常式
- 執行模式處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023916"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="c5d73-122">註冊自訂屬性、事件和控制項模式</span><span class="sxs-lookup"><span data-stu-id="c5d73-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="c5d73-123">在可以使用自訂屬性、事件或控制項模式之前，提供者和用戶端都必須在執行時間註冊屬性、事件或控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c5d73-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="c5d73-124">註冊在應用程式程式中是全域有效的，而且在處理常式關閉或最後一個 Microsoft 消費者介面自動化元素物件 ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 或 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) 發行至進程之前，會保持有效。</span><span class="sxs-lookup"><span data-stu-id="c5d73-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="c5d73-125">Registation 牽涉到傳遞 GUID 給消費者介面自動化，以及有關自訂屬性、事件或控制項模式的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c5d73-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="c5d73-126">第二次使用相同的資訊註冊相同的 GUID 將會成功，但嘗試以不同的資訊再次註冊相同的 GUID (例如，不同類型的自訂屬性) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c5d73-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="c5d73-127">未來，如果自訂規格已接受並整合到消費者介面自動化 core 中，消費者介面自動化將會驗證自訂的註冊資訊，並使用已註冊的程式碼，而不是「官方」架構的執行，藉此將應用程式相容性問題降至最低。</span><span class="sxs-lookup"><span data-stu-id="c5d73-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="c5d73-128">您無法移除已註冊的屬性、事件或控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c5d73-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="c5d73-129">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="c5d73-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c5d73-130">註冊自訂屬性和事件</span><span class="sxs-lookup"><span data-stu-id="c5d73-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="c5d73-131">執行自訂控制項模式</span><span class="sxs-lookup"><span data-stu-id="c5d73-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="c5d73-132">用戶端包裝函式和模式處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d73-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="c5d73-133">執行用戶端包裝函式</span><span class="sxs-lookup"><span data-stu-id="c5d73-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="c5d73-134">執行模式處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d73-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="c5d73-135">註冊自訂控制項模式</span><span class="sxs-lookup"><span data-stu-id="c5d73-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="c5d73-136">自訂控制項模式的範例執行</span><span class="sxs-lookup"><span data-stu-id="c5d73-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="c5d73-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5d73-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="c5d73-138">註冊自訂屬性和事件</span><span class="sxs-lookup"><span data-stu-id="c5d73-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="c5d73-139">註冊自訂屬性或事件，可讓提供者和用戶端取得屬性或事件的識別碼，然後將其傳遞給以識別碼做為參數的各種 API 方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="c5d73-140">若要註冊屬性或事件：</span><span class="sxs-lookup"><span data-stu-id="c5d73-140">To register a property or event:</span></span>

1.  <span data-ttu-id="c5d73-141">定義自訂屬性或事件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c5d73-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="c5d73-142">以屬性或事件的相關資訊填入 [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) 或 [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) 結構，包括 GUID 和包含自訂屬性或事件名稱的 nonlocalizable 字串。</span><span class="sxs-lookup"><span data-stu-id="c5d73-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="c5d73-143">自訂屬性也需要指定屬性的資料類型，例如屬性是否保留整數或字串。</span><span class="sxs-lookup"><span data-stu-id="c5d73-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="c5d73-144">資料類型必須是 [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) 列舉所指定的下列其中一種類型。</span><span class="sxs-lookup"><span data-stu-id="c5d73-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="c5d73-145">自訂屬性不支援其他資料類型。</span><span class="sxs-lookup"><span data-stu-id="c5d73-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="c5d73-146">**UIAutomationType \_ Bool**</span><span class="sxs-lookup"><span data-stu-id="c5d73-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="c5d73-147">**UIAutomationType \_ Double**</span><span class="sxs-lookup"><span data-stu-id="c5d73-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="c5d73-148">**UIAutomationType \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="c5d73-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="c5d73-149">**UIAutomationType \_ Int**</span><span class="sxs-lookup"><span data-stu-id="c5d73-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="c5d73-150">**UIAutomationType \_ 點**</span><span class="sxs-lookup"><span data-stu-id="c5d73-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="c5d73-151">**UIAutomationType \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="c5d73-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="c5d73-152">使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立 [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) 物件的實例，並取得物件之 [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c5d73-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="c5d73-153">呼叫 [**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) 或 [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) 方法，並傳遞 [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) 結構或 [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="c5d73-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="c5d73-154">[**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty)或 [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent)方法會傳回屬性識別碼或事件識別碼，應用程式可以傳遞給採用這類識別碼做為參數的任何消費者介面自動化方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="c5d73-155">例如，您可以將已註冊的屬性識別碼傳遞給 [**IUIAutomationElement：： GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) 方法或 [**IUIAutomation：： CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="c5d73-156">下列範例示範如何註冊自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="c5d73-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="c5d73-157">[**IUIAutomationRegistrar：： RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty)和 [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent)方法所抓取的屬性和事件識別碼，只在取得它們的應用程式內容中有效，而且只會在應用程式存留期間內有效。</span><span class="sxs-lookup"><span data-stu-id="c5d73-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="c5d73-158">當在相同的應用程式的不同執行時間實例上呼叫時，註冊方法可以針對相同的 GUID 傳回不同的整數值。</span><span class="sxs-lookup"><span data-stu-id="c5d73-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="c5d73-159">沒有任何方法可取消註冊自訂屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="c5d73-160">相反地，它們會在最後一個消費者介面自動化物件釋放時隱含地取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c5d73-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5d73-161">如果您的程式碼是 Microsoft Active Accessibility (MSAA) 用戶端，則當您變更自訂屬性的值時，必須呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 函數。</span><span class="sxs-lookup"><span data-stu-id="c5d73-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="c5d73-162">執行自訂控制項模式</span><span class="sxs-lookup"><span data-stu-id="c5d73-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="c5d73-163">自訂控制項模式不包含在消費者介面自動化 API 中，但會在執行時間由協力廠商提供。</span><span class="sxs-lookup"><span data-stu-id="c5d73-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="c5d73-164">用戶端和提供者應用程式的開發人員必須一起合作來定義自訂控制項模式，包括控制項模式將支援的方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="c5d73-165">定義控制項模式之後，用戶端和提供者都必須將支援元件物件模型 (COM) 物件，以及在執行時間註冊控制項模式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c5d73-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="c5d73-166">自訂控制項模式需要執行兩個 COM 物件：用戶端包裝函式和模式處理常式。</span><span class="sxs-lookup"><span data-stu-id="c5d73-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="c5d73-167">下列主題中的範例將說明如何執行自訂控制項模式，以複製現有 [值](uiauto-implementingvalue.md) 控制項模式的功能。</span><span class="sxs-lookup"><span data-stu-id="c5d73-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="c5d73-168">這些範例僅供教學之用。</span><span class="sxs-lookup"><span data-stu-id="c5d73-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="c5d73-169">實際的自訂控制項模式應該提供標準消費者介面自動化控制項模式無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="c5d73-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="c5d73-170">用戶端包裝函式和模式處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d73-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="c5d73-171">用戶端包裝函式會執行 API，用戶端會使用此 API 來取得屬性，並呼叫自訂控制項模式所公開的方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="c5d73-172">API 會實作為 COM 介面，此介面會將所有屬性要求和方法呼叫傳遞給消費者介面自動化 core，然後將要求和呼叫封送處理給提供者。</span><span class="sxs-lookup"><span data-stu-id="c5d73-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="c5d73-173">註冊自訂控制項模式的程式碼必須提供消費者介面自動化可以用來建立用戶端包裝函式物件實例的 class factory。</span><span class="sxs-lookup"><span data-stu-id="c5d73-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="c5d73-174">當自訂控制項模式成功註冊之後，消費者介面自動化會傳回 [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) 介面指標，用戶端會使用此指標將屬性要求和方法呼叫轉送至消費者介面自動化核心。</span><span class="sxs-lookup"><span data-stu-id="c5d73-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="c5d73-175">在提供者端，消費者介面自動化 core 會接受來自用戶端的屬性要求和方法呼叫，並將它們傳遞給模式處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="c5d73-176">然後，模式處理常式會針對自訂控制項模式，在提供者介面上呼叫適當的方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="c5d73-177">註冊自訂控制項模式的程式碼會建立模式處理常式物件，而且當註冊控制項模式時，會提供具有物件 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面指標的消費者介面自動化。</span><span class="sxs-lookup"><span data-stu-id="c5d73-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="c5d73-178">下圖顯示用戶端屬性要求或方法呼叫如何從用戶端包裝函式、透過消費者介面自動化核心元件流向模式處理常式，然後再到提供者介面。</span><span class="sxs-lookup"><span data-stu-id="c5d73-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![顯示從用戶端包裝函式流向模式處理常式和提供者之流程的圖表](images/custompatternsupport.jpg)

<span data-ttu-id="c5d73-180">執行用戶端包裝函式和模式處理常式介面的物件必須是無限制執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5d73-180">The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id="c5d73-181">此外，消費者介面自動化 core 必須能夠直接呼叫物件，而不需要任何中繼封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="c5d73-181">Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name="implementing-the-client-wrapper"></a><span data-ttu-id="c5d73-182">執行用戶端包裝函式</span><span class="sxs-lookup"><span data-stu-id="c5d73-182">Implementing the Client Wrapper</span></span>

<span data-ttu-id="c5d73-183">用戶端包裝函式是一個物件，此物件會公開用戶端用來要求屬性和呼叫自訂控制項模式所支援之方法的 IXxxPattern 介面。</span><span class="sxs-lookup"><span data-stu-id="c5d73-183">The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id="c5d73-184">介面是由每個支援的屬性所組成的一對 "getter" 方法 (get \_ CurrentXxx 和 get \_ CachedXxx 方法) ，以及每個支援的方法都有一個 "呼叫端" 方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="c5d73-185">當物件具現化時，物件的函式會收到 [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) 介面的指標，該介面是由消費者介面自動化 core 所執行。</span><span class="sxs-lookup"><span data-stu-id="c5d73-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="c5d73-186">IXxxPattern 介面的方法會使用 [**IUIAutomationPatternInstance：： GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) 和 [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) 方法，將屬性要求和方法呼叫轉送至消費者介面自動化核心。</span><span class="sxs-lookup"><span data-stu-id="c5d73-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="c5d73-187">下列範例顯示如何針對支援單一屬性的簡單自訂控制項模式，執行用戶端包裝函式物件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="c5d73-188">如需更複雜的範例，請參閱 [自訂控制項模式的範例執行](#example-implementation-of-a-custom-control-pattern)。</span><span class="sxs-lookup"><span data-stu-id="c5d73-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="c5d73-189">執行模式處理常式</span><span class="sxs-lookup"><span data-stu-id="c5d73-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="c5d73-190">模式處理常式是實 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="c5d73-191">這個介面有兩種方法： [**IUIAutomationPatternHandler：： CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) 和 [**分派**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch)。</span><span class="sxs-lookup"><span data-stu-id="c5d73-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="c5d73-192">消費者介面自動化 core 會呼叫 **CreateClientWrapper** 方法，並接收 [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c5d73-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="c5d73-193">**CreateClientWrapper** 會透過具現化用戶端包裝函式物件，並將 **IUIAutomationPatternInstance** 介面指標傳遞至用戶端包裝函式，來回應。</span><span class="sxs-lookup"><span data-stu-id="c5d73-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="c5d73-194">消費者介面自動化 core 會使用 [**分派**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) 方法，將屬性要求和方法呼叫傳遞給自訂控制項模式的提供者介面。</span><span class="sxs-lookup"><span data-stu-id="c5d73-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="c5d73-195">參數包含提供者介面的指標、要呼叫之屬性 getter 或方法的以零為基底的索引，以及包含要傳遞給提供者之參數的 [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="c5d73-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="c5d73-196">模式處理常式會藉由檢查索引參數來判斷要呼叫的提供者方法來回應，然後呼叫該提供者介面，並傳遞包含在 **UIAutomationParameter** 結構中的參數。</span><span class="sxs-lookup"><span data-stu-id="c5d73-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="c5d73-197">在註冊控制項模式之前，會以註冊自訂控制項模式的相同程式碼來具現化模式處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="c5d73-198">在註冊時，程式碼必須將模式處理常式物件的 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面指標傳遞至消費者介面自動化 core。</span><span class="sxs-lookup"><span data-stu-id="c5d73-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="c5d73-199">下列範例示範如何針對支援單一屬性的簡單自訂控制項模式，執行模式處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="c5d73-200">如需更複雜的範例，請參閱 [自訂控制項模式的範例執行](#example-implementation-of-a-custom-control-pattern)。</span><span class="sxs-lookup"><span data-stu-id="c5d73-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="c5d73-201">註冊自訂控制項模式</span><span class="sxs-lookup"><span data-stu-id="c5d73-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="c5d73-202">在可以使用之前，自訂控制項模式必須由提供者和用戶端註冊。</span><span class="sxs-lookup"><span data-stu-id="c5d73-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="c5d73-203">註冊會提供消費者介面自動化核心與控制項模式的詳細資訊，並提供具有控制項模式識別碼的提供者或用戶端，以及控制項模式所支援之屬性和事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5d73-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="c5d73-204">在提供者端，必須先註冊自訂控制項模式，關聯的控制項才能處理 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，或同時處理。</span><span class="sxs-lookup"><span data-stu-id="c5d73-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="c5d73-205">註冊自訂控制項模式時，提供者或用戶端會提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="c5d73-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="c5d73-206">自訂控制項模式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c5d73-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="c5d73-207">Nonlocalizable 字串，其中包含自訂控制項模式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5d73-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="c5d73-208">支援自訂控制項模式之提供者介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c5d73-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="c5d73-209">支援自訂控制項模式之用戶端介面的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c5d73-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="c5d73-210">[**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)結構的陣列，描述自訂控制項模式所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="c5d73-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="c5d73-211">您必須為每個屬性指定 GUID、屬性名稱和資料類型。</span><span class="sxs-lookup"><span data-stu-id="c5d73-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="c5d73-212">[**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)結構的陣列，描述自訂控制項模式所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="c5d73-213">針對每個方法，結構會包含下列資訊：方法名稱、參數的計數、參數資料類型的清單，以及參數名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="c5d73-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="c5d73-214">[**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)結構的陣列，描述自訂控制項模式所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="c5d73-215">針對每個事件，必須指定 GUID 和事件名稱。</span><span class="sxs-lookup"><span data-stu-id="c5d73-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="c5d73-216">將自訂控制項模式提供給用戶端的模式處理常式物件之 [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) 介面的位址。</span><span class="sxs-lookup"><span data-stu-id="c5d73-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="c5d73-217">若要註冊自訂控制項模式，提供者或用戶端程式代碼必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c5d73-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="c5d73-218">使用上述資訊填入 [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="c5d73-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="c5d73-219">使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來建立 [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) 物件的實例，並取得物件之 [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c5d73-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="c5d73-220">呼叫 [**IUIAutomationRegistrar：： RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) 方法，並傳遞 [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="c5d73-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="c5d73-221">[**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern)方法會傳回控制項模式識別碼，以及屬性識別碼和事件識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="c5d73-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="c5d73-222">應用程式可以將這些識別碼傳遞給採用這類識別碼做為參數的任何消費者介面自動化方法。</span><span class="sxs-lookup"><span data-stu-id="c5d73-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="c5d73-223">例如，您可以將已註冊的模式識別碼傳遞至 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) 方法，以取得控制項模式的提供者介面指標。</span><span class="sxs-lookup"><span data-stu-id="c5d73-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="c5d73-224">沒有任何方法可取消註冊自訂控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c5d73-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="c5d73-225">相反地，在釋放最後一個消費者介面自動化物件時，它會隱含地取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c5d73-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="c5d73-226">如需示範如何註冊自訂控制項模式的範例，請參閱下一節。</span><span class="sxs-lookup"><span data-stu-id="c5d73-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="c5d73-227">自訂控制項模式的範例執行</span><span class="sxs-lookup"><span data-stu-id="c5d73-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="c5d73-228">本章節包含範例程式碼，示範如何針對自訂控制項模式執行用戶端包裝函式和模式處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="c5d73-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="c5d73-229">此範例會根據 [值](uiauto-implementingvalue.md) 控制項模式來執行自訂控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c5d73-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c5d73-230">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5d73-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c5d73-231">**概念**</span><span class="sxs-lookup"><span data-stu-id="c5d73-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5d73-232">設計自訂屬性、事件和控制項模式</span><span class="sxs-lookup"><span data-stu-id="c5d73-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="c5d73-233">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="c5d73-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="c5d73-234">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="c5d73-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="c5d73-235">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="c5d73-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 