---
title: 使用安全陣列的最佳作法
description: Microsoft 消費者介面自動化的許多介面方法 \ 32;API 會將 SAFEARRAY 資料類型的引數稱為安全陣列。 本主題說明在消費者介面自動化應用程式中使用安全陣列的最佳作法。
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- 消費者介面自動化、安全陣列
- 消費者介面自動化，提供者
- 消費者介面自動化，用戶端
- 消費者介面自動化，在資料類型之間轉換
- 用戶端、安全陣列
- 提供者，消費者介面自動化
- 安全陣列
- 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969114"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="784d7-112">使用安全陣列的最佳作法</span><span class="sxs-lookup"><span data-stu-id="784d7-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="784d7-113">Microsoft 消費者介面自動化 API 的許多介面方法都採用 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 資料類型的引數（稱為安全陣列）。</span><span class="sxs-lookup"><span data-stu-id="784d7-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="784d7-114">本主題說明在消費者介面自動化應用程式中使用安全陣列的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="784d7-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="784d7-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="784d7-115">Clients</span></span>

<span data-ttu-id="784d7-116">搭配消費者介面自動化用戶端 API 方法使用的所有安全陣列都是以零為基礎的一維陣列。</span><span class="sxs-lookup"><span data-stu-id="784d7-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="784d7-117">若要建立消費者介面自動化用戶端方法的安全陣列，請使用 [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) 函式，以及讀取和寫入安全陣列，使用 [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) 和 [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) 函數。</span><span class="sxs-lookup"><span data-stu-id="784d7-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="784d7-118">當您使用安全陣列完成時，請一律使用 [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) 函式來終結它，無論您建立的是安全陣列，還是從消費者介面自動化用戶端方法收到它。</span><span class="sxs-lookup"><span data-stu-id="784d7-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="784d7-119">數個消費者介面自動化的方法，包括屬性抓取方法（例如 [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)），可取得可以包含 [**POINT**](/previous-versions//dd162805(v=vs.85))或 [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)結構的 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)。</span><span class="sxs-lookup"><span data-stu-id="784d7-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="784d7-120">**點** 會封裝成 **VARIANT** 形式的安全陣列， (VT \_ R8) 與位於索引0的 **x** 成員，以及位於索引1的 **y** 成員。</span><span class="sxs-lookup"><span data-stu-id="784d7-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="784d7-121">同樣地， **UiaRect** 會封裝成 **VARIANT** 形式的安全陣列，其具有 **左方**、 **頂端**、 **寬度** 和 **高度** 成員（索引0到3）。</span><span class="sxs-lookup"><span data-stu-id="784d7-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="784d7-122">針對 **UiaRect** 結構的陣列，安全陣列針對每個 **UiaRect** 包含四個雙精度浮點數的連續陣列。</span><span class="sxs-lookup"><span data-stu-id="784d7-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="784d7-123">第一個 **UiaRect** 的 **左邊**、 **top**、 **width** 和 **height** 成員占索引0到3，第二個矩形的成員佔用索引4到7，依此類推。</span><span class="sxs-lookup"><span data-stu-id="784d7-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="784d7-124">[**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)介面包含下列方法，可在 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)和各種其他資料類型之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="784d7-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="784d7-125">方法</span><span class="sxs-lookup"><span data-stu-id="784d7-125">Method</span></span>                                                                                               | <span data-ttu-id="784d7-126">描述</span><span class="sxs-lookup"><span data-stu-id="784d7-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="784d7-127">**IUIAutomation::IntNativeArrayToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="784d7-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="784d7-128">將整數陣列轉換為 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)。</span><span class="sxs-lookup"><span data-stu-id="784d7-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="784d7-129">**IUIAutomation::IntSafeArrayToNativeArray**</span><span class="sxs-lookup"><span data-stu-id="784d7-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="784d7-130">將整數的 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 轉換成陣列。</span><span class="sxs-lookup"><span data-stu-id="784d7-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="784d7-131">**IUIAutomation::SafeArrayToRectNativeArray**</span><span class="sxs-lookup"><span data-stu-id="784d7-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="784d7-132">將包含矩形座標的 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 轉換成 **RECT** 類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="784d7-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="784d7-133">提供者</span><span class="sxs-lookup"><span data-stu-id="784d7-133">Providers</span></span>

<span data-ttu-id="784d7-134">提供者必須執行一些介面方法，這些方法消費者介面自動化呼叫來從提供者取得資訊。</span><span class="sxs-lookup"><span data-stu-id="784d7-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="784d7-135">許多時候，這項資訊是由值陣列所組成。</span><span class="sxs-lookup"><span data-stu-id="784d7-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="784d7-136">若要將陣列傳回消費者介面自動化，提供者必須將陣列封裝成 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) 結構。</span><span class="sxs-lookup"><span data-stu-id="784d7-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="784d7-137">陣列元素必須是預期的資料類型，而且必須以預期的順序顯示。</span><span class="sxs-lookup"><span data-stu-id="784d7-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="784d7-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="784d7-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="784d7-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="784d7-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="784d7-140">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="784d7-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="784d7-141">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="784d7-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 