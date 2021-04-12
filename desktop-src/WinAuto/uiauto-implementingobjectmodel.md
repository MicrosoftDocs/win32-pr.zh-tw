---
title: System.collections.objectmodel.observablecollection 控制項模式
description: 描述執行 IObjectModelProvider 的方針和慣例，包括方法的相關資訊。 System.collections.objectmodel.observablecollection 控制項模式是用來公開檔基礎物件模型的指標。
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- 消費者介面自動化，執行 System.collections.objectmodel.observablecollection 控制項模式
- 消費者介面自動化，System.collections.objectmodel.observablecollection 控制項模式
- 消費者介面自動化、IObjectModelProvider
- IObjectModelProvider
- 執行消費者介面自動化 System.collections.objectmodel.observablecollection 控制項模式
- System.collections.objectmodel.observablecollection 控制項模式
- 控制項模式，IObjectModelProvider
- 控制模式，消費者介面自動化執行 System.collections.objectmodel.observablecollection
- 控制項模式，System.collections.objectmodel.observablecollection
- 介面，IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315781"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="79feb-114">System.collections.objectmodel.observablecollection 控制項模式</span><span class="sxs-lookup"><span data-stu-id="79feb-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="79feb-115">描述執行 [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)的方針和慣例，包括方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79feb-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="79feb-116">**System.collections.objectmodel.observablecollection** 控制項模式是用來公開檔基礎物件模型的指標。</span><span class="sxs-lookup"><span data-stu-id="79feb-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="79feb-117">許多應用程式會執行豐富的物件模型，以增加 Microsoft 消費者介面自動化所提供的價值。</span><span class="sxs-lookup"><span data-stu-id="79feb-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="79feb-118">此控制項模式可讓用戶端從消費者介面自動化元素流覽至基礎物件模型。</span><span class="sxs-lookup"><span data-stu-id="79feb-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="79feb-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="79feb-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="79feb-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="79feb-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="79feb-121">**IObjectModelProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="79feb-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="79feb-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="79feb-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="79feb-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="79feb-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="79feb-124">在執行 **system.collections.objectmodel.observablecollection** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="79feb-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="79feb-125">[**IObjectModelProvider：： GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel)方法應該將指標傳回至盡可能接近來源 UI 元素的物件。</span><span class="sxs-lookup"><span data-stu-id="79feb-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="79feb-126">例如，在網頁瀏覽器中，單一元素的消費者介面自動化提供者應該會傳回專案的物件模型指標。</span><span class="sxs-lookup"><span data-stu-id="79feb-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="79feb-127">傳回檔根目錄的物件模型指標並不太實用。</span><span class="sxs-lookup"><span data-stu-id="79feb-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="79feb-128">**System.collections.objectmodel.observablecollection** 控制項模式的用戶端預期會有其所要搜尋之介面的 IID，這就是它足以傳回簡單 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)指標的原因。</span><span class="sxs-lookup"><span data-stu-id="79feb-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="79feb-129">因為消費者介面自動化會將指標封送處理至用戶端進程，所以提供者應該預期用戶端必須使用標準元件物件模型來存取物件模型 (COM) 實務。</span><span class="sxs-lookup"><span data-stu-id="79feb-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="79feb-130">**IObjectModelProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="79feb-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="79feb-131">以下是執行 [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) 介面的必要方法。</span><span class="sxs-lookup"><span data-stu-id="79feb-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="79feb-132">必要成員</span><span class="sxs-lookup"><span data-stu-id="79feb-132">Required members</span></span>                                                                             | <span data-ttu-id="79feb-133">成員類型</span><span class="sxs-lookup"><span data-stu-id="79feb-133">Member type</span></span> | <span data-ttu-id="79feb-134">備註</span><span class="sxs-lookup"><span data-stu-id="79feb-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79feb-135">**GetUnderlyingObjectModel**</span><span class="sxs-lookup"><span data-stu-id="79feb-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="79feb-136">方法</span><span class="sxs-lookup"><span data-stu-id="79feb-136">Method</span></span>      | <span data-ttu-id="79feb-137">傳回基礎物件模型的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="79feb-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="79feb-138">用戶端必須呼叫 [**IUnknown：： QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法，以取得特定的物件模型指標。</span><span class="sxs-lookup"><span data-stu-id="79feb-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="79feb-139">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="79feb-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79feb-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="79feb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79feb-141">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="79feb-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="79feb-142">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="79feb-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="79feb-143">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="79feb-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 