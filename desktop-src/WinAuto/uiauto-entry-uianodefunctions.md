---
title: 已淘汰的節點函式
description: 已淘汰的節點函式
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103933684"
---
# <a name="deprecated-node-functions"></a><span data-ttu-id="fedbc-103">已淘汰的節點函式</span><span class="sxs-lookup"><span data-stu-id="fedbc-103">Deprecated Node Functions</span></span>

> [!Note]  
> <span data-ttu-id="fedbc-104">本節所述的控制項模式函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="fedbc-105">用戶端應用程式應該使用元件物件模型 (COM) 介面，如下列各節所述：</span><span class="sxs-lookup"><span data-stu-id="fedbc-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="fedbc-106">用戶端的消費者介面自動化元素介面</span><span class="sxs-lookup"><span data-stu-id="fedbc-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="fedbc-107">用戶端的屬性條件介面</span><span class="sxs-lookup"><span data-stu-id="fedbc-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="fedbc-108">用戶端的控制項模式介面</span><span class="sxs-lookup"><span data-stu-id="fedbc-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="fedbc-109">用戶端的事件處理介面</span><span class="sxs-lookup"><span data-stu-id="fedbc-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="fedbc-110">用戶端的 Proxy Factory 介面</span><span class="sxs-lookup"><span data-stu-id="fedbc-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="fedbc-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="fedbc-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fedbc-112">函式</span><span class="sxs-lookup"><span data-stu-id="fedbc-112">Function</span></span></th>
<th><span data-ttu-id="fedbc-113">描述</span><span class="sxs-lookup"><span data-stu-id="fedbc-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fedbc-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-115">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-115">This function is deprecated.</span></span> <span data-ttu-id="fedbc-116">用戶端應用程式應該改用 Microsoft 消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-117">在消費者介面自動化樹狀結構中的節點上加入事件的接聽程式。</span><span class="sxs-lookup"><span data-stu-id="fedbc-117">Adds a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-119">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-119">This function is deprecated.</span></span> <span data-ttu-id="fedbc-120">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-121">將視窗加入至事件接聽程式。</span><span class="sxs-lookup"><span data-stu-id="fedbc-121">Adds a window to the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-123">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-123">This function is deprecated.</span></span> <span data-ttu-id="fedbc-124">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-125">用戶端所執行的函式，當用戶端已訂閱的事件引發時，消費者介面自動化會呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="fedbc-125">A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-127">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-127">This function is deprecated.</span></span> <span data-ttu-id="fedbc-128">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-129">從事件接聽程式中移除視窗。</span><span class="sxs-lookup"><span data-stu-id="fedbc-129">Removes a window from the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-131">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-131">This function is deprecated.</span></span> <span data-ttu-id="fedbc-132">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-133">抓取符合搜尋準則的一或多個消費者介面自動化節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-133">Retrieves one or more UI Automation nodes that match the search criteria.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-135">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-135">This function is deprecated.</span></span> <span data-ttu-id="fedbc-136">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-137">取得可傳遞給用戶端的錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="fedbc-137">Gets an error string so that it can be passed to the client.</span></span> <span data-ttu-id="fedbc-138">用戶端不直接使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fedbc-138">This method is not used directly by clients.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-140">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-140">This function is deprecated.</span></span> <span data-ttu-id="fedbc-141">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-141">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-142">抓取 <em>控制項模式</em>。</span><span class="sxs-lookup"><span data-stu-id="fedbc-142">Retrieves a <em>control pattern</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-144">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-144">This function is deprecated.</span></span> <span data-ttu-id="fedbc-145">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-145">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-146">抓取消費者介面自動化屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fedbc-146">Retrieves the value of a UI Automation property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-148">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-148">This function is deprecated.</span></span> <span data-ttu-id="fedbc-149">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-149">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-150">抓取根消費者介面自動化節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-150">Retrieves the root UI Automation node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-152">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-152">This function is deprecated.</span></span> <span data-ttu-id="fedbc-153">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-153">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-154">抓取消費者介面自動化節點的執行時間識別碼。</span><span class="sxs-lookup"><span data-stu-id="fedbc-154">Retrieves the runtime identifier of a UI Automation node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-156">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-156">This function is deprecated.</span></span> <span data-ttu-id="fedbc-157">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-157">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-158">更新屬性值和控制項模式的快取。</span><span class="sxs-lookup"><span data-stu-id="fedbc-158">Updates the cache of property values and control patterns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-160">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-160">This function is deprecated.</span></span> <span data-ttu-id="fedbc-161">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-161">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-162">從 <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> 型別取得控制項模式物件。</span><span class="sxs-lookup"><span data-stu-id="fedbc-162">Gets a control pattern object from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-164">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-164">This function is deprecated.</span></span> <span data-ttu-id="fedbc-165">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-165">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-166">從 <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> 類型取得文字範圍。</span><span class="sxs-lookup"><span data-stu-id="fedbc-166">Gets a text range from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-168">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-168">This function is deprecated.</span></span> <span data-ttu-id="fedbc-169">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-169">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-170">從 <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> 型別取得 HUIANODE。</span><span class="sxs-lookup"><span data-stu-id="fedbc-170">Gets an HUIANODE from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-172">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-172">This function is deprecated.</span></span> <span data-ttu-id="fedbc-173">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-173">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-174">取得可用於需要 PROPERTYID、PATTERNID、CONTROLTYPEID、TEXTATTRIBUTEID 或 EVENTID 之方法中的整數識別碼。</span><span class="sxs-lookup"><span data-stu-id="fedbc-174">Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-176">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-176">This function is deprecated.</span></span> <span data-ttu-id="fedbc-177">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-177">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-178">在消費者介面自動化樹狀結構中流覽，選擇性地取出快取的資訊。</span><span class="sxs-lookup"><span data-stu-id="fedbc-178">Navigates in the UI Automation tree, optionally retrieving cached information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-180">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-180">This function is deprecated.</span></span> <span data-ttu-id="fedbc-181">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-181">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-182">針對目前具有輸入焦點的 UI 元素，抓取消費者介面自動化節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-182">Retrieves the UI Automation node for the UI element that currently has input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-184">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-184">This function is deprecated.</span></span> <span data-ttu-id="fedbc-185">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-185">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-186">抓取與視窗相關聯的消費者介面自動化節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-186">Retrieves the UI Automation node associated with a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-188">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-188">This function is deprecated.</span></span> <span data-ttu-id="fedbc-189">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-189">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-190">針對位於指定點的專案，抓取消費者介面自動化節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-190">Retrieves the UI Automation node for the element at the specified point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-192">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-192">This function is deprecated.</span></span> <span data-ttu-id="fedbc-193">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-193">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-194">抓取原始元素提供者的消費者介面自動化節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-194">Retrieves the UI Automation node for a raw element provider.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-196">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-196">This function is deprecated.</span></span> <span data-ttu-id="fedbc-197">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-197">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-198">從記憶體中刪除節點。</span><span class="sxs-lookup"><span data-stu-id="fedbc-198">Deletes a node from memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-200">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-200">This function is deprecated.</span></span> <span data-ttu-id="fedbc-201">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-201">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-202">從記憶體刪除配置的模式物件。</span><span class="sxs-lookup"><span data-stu-id="fedbc-202">Deletes an allocated pattern object from memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-204">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-204">This function is deprecated.</span></span> <span data-ttu-id="fedbc-205">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-205">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-206">由消費者介面自動化呼叫的應用程式定義函式，可取得專案的用戶端提供者。</span><span class="sxs-lookup"><span data-stu-id="fedbc-206">An application-defined function that is called by UI Automation to obtain a client-side provider for an element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-208">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-208">This function is deprecated.</span></span> <span data-ttu-id="fedbc-209">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-209">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-210">取得布林值，這個值會指定矩形是否將其所有座標設定為0。</span><span class="sxs-lookup"><span data-stu-id="fedbc-210">Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-212">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-212">This function is deprecated.</span></span> <span data-ttu-id="fedbc-213">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-213">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-214">將 <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> 結構的元素設定為0。</span><span class="sxs-lookup"><span data-stu-id="fedbc-214">Sets the elements of a <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> structure to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-216">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-216">This function is deprecated.</span></span> <span data-ttu-id="fedbc-217">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-218">註冊由消費者介面自動化呼叫的應用程式定義方法，以取得元素的提供者。</span><span class="sxs-lookup"><span data-stu-id="fedbc-218">Registers the application-defined method that is called by UI Automation to obtain a provider for an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-220">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-220">This function is deprecated.</span></span> <span data-ttu-id="fedbc-221">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-222">移除消費者介面自動化樹狀結構中節點上的事件接聽程式。</span><span class="sxs-lookup"><span data-stu-id="fedbc-222">Removes a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fedbc-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-224">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-224">This function is deprecated.</span></span> <span data-ttu-id="fedbc-225">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-226">將輸入焦點設定為 UI 中的指定元素。</span><span class="sxs-lookup"><span data-stu-id="fedbc-226">Sets the input focus to the specified element in the UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fedbc-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="fedbc-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="fedbc-228">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="fedbc-228">This function is deprecated.</span></span> <span data-ttu-id="fedbc-229">用戶端應用程式應該改用消費者介面自動化 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="fedbc-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="fedbc-230">從記憶體中刪除配置的文字範圍物件。</span><span class="sxs-lookup"><span data-stu-id="fedbc-230">Deletes an allocated text range object from memory.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fedbc-231">相關主題</span><span class="sxs-lookup"><span data-stu-id="fedbc-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fedbc-232">消費者介面自動化用戶端</span><span class="sxs-lookup"><span data-stu-id="fedbc-232">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

