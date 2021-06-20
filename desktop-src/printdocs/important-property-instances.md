---
description: 若要讓用戶端建立 PrintTicket，PrintCapabilities 檔必須提供功能實例的屬性和功能中的選項實例。
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: 重要的屬性實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409121"
---
# <a name="important-property-instances"></a><span data-ttu-id="9934d-103">重要的屬性實例</span><span class="sxs-lookup"><span data-stu-id="9934d-103">Important Property Instances</span></span>

<span data-ttu-id="9934d-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9934d-104">This topic is not current.</span></span> <span data-ttu-id="9934d-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9934d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9934d-106">為了讓 PrintCapabilities 用戶端能夠建立合理的 PrintTicket，PrintCapabilities 檔必須提供功能實例的某些屬性，以及功能中的選項實例。</span><span class="sxs-lookup"><span data-stu-id="9934d-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="9934d-107">一般使用者介面 (UI) 模組需要這類資訊來建立 UI。</span><span class="sxs-lookup"><span data-stu-id="9934d-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="9934d-108">這接著需要 Print Schema 關鍵字定義一些屬性實例，這些實例會顯示為功能和 Option 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="9934d-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="9934d-109">功能元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9934d-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="9934d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9934d-110">Property</span></span>                  | <span data-ttu-id="9934d-111">值</span><span class="sxs-lookup"><span data-stu-id="9934d-111">Values</span></span>                                 | <span data-ttu-id="9934d-112">目的</span><span class="sxs-lookup"><span data-stu-id="9934d-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9934d-113">SelectionType</span><span class="sxs-lookup"><span data-stu-id="9934d-113">SelectionType</span></span> <br/> | <span data-ttu-id="9934d-114">PickOne</span><span class="sxs-lookup"><span data-stu-id="9934d-114">PickOne</span></span><br/> <span data-ttu-id="9934d-115">PickMany</span><span class="sxs-lookup"><span data-stu-id="9934d-115">PickMany</span></span><br/> | <span data-ttu-id="9934d-116">指定可在指定時間（一個 (PickOne) 或一個以上的 (PickMany) ）選取這項功能的選項數目。</span><span class="sxs-lookup"><span data-stu-id="9934d-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="9934d-117">用戶端可以使用此資訊來建立 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="9934d-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="9934d-118">這項資訊會影響 UI 行為，以及提供者的 PrintTicket 驗證。</span><span class="sxs-lookup"><span data-stu-id="9934d-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="9934d-119">選項元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9934d-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="9934d-120">屬性</span><span class="sxs-lookup"><span data-stu-id="9934d-120">Property</span></span>                   | <span data-ttu-id="9934d-121">值</span><span class="sxs-lookup"><span data-stu-id="9934d-121">Values</span></span>                           | <span data-ttu-id="9934d-122">目的</span><span class="sxs-lookup"><span data-stu-id="9934d-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9934d-123">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="9934d-123">IdentityOption</span></span> <br/> | <span data-ttu-id="9934d-124">True</span><span class="sxs-lookup"><span data-stu-id="9934d-124">True</span></span><br/> <span data-ttu-id="9934d-125">False</span><span class="sxs-lookup"><span data-stu-id="9934d-125">False</span></span><br/> | <span data-ttu-id="9934d-126">選取 [IdentityOption] 屬性工作表示「停用此功能」。</span><span class="sxs-lookup"><span data-stu-id="9934d-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="9934d-127">包含 SelectionType 屬性（其值為 PickMany）的功能也必須包含具有 IdentityOption 屬性的選項。</span><span class="sxs-lookup"><span data-stu-id="9934d-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="9934d-128">如果選取了 IdentityOption 屬性，則在建立 PrintTicket) 的 UI 程式碼 (或用戶端必須取消選取任何其他選項。</span><span class="sxs-lookup"><span data-stu-id="9934d-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="9934d-129">Feature、Option 和 ParameterDef 元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9934d-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="9934d-130">屬性</span><span class="sxs-lookup"><span data-stu-id="9934d-130">Property</span></span>              | <span data-ttu-id="9934d-131">值</span><span class="sxs-lookup"><span data-stu-id="9934d-131">Values</span></span>                          | <span data-ttu-id="9934d-132">目的</span><span class="sxs-lookup"><span data-stu-id="9934d-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9934d-133">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="9934d-133">DisplayUI</span></span> <br/> | <span data-ttu-id="9934d-134">顯示</span><span class="sxs-lookup"><span data-stu-id="9934d-134">Show</span></span><br/> <span data-ttu-id="9934d-135">隱藏</span><span class="sxs-lookup"><span data-stu-id="9934d-135">Hide</span></span><br/> | <span data-ttu-id="9934d-136">指定父元素是否應顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="9934d-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="9934d-137">顯示指出元素應顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="9934d-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="9934d-138">隱藏表示元素不應顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="9934d-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="9934d-139">如果未定義專案的這個屬性，則會顯示預設轉譯，表示會顯示元素。</span><span class="sxs-lookup"><span data-stu-id="9934d-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="9934d-140">Feature、Option 和 ParameterDef 元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9934d-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="9934d-141">屬性</span><span class="sxs-lookup"><span data-stu-id="9934d-141">Property</span></span>                | <span data-ttu-id="9934d-142">值</span><span class="sxs-lookup"><span data-stu-id="9934d-142">Value</span></span>             | <span data-ttu-id="9934d-143">目的</span><span class="sxs-lookup"><span data-stu-id="9934d-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9934d-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="9934d-144">DisplayName</span></span> <br/> | <span data-ttu-id="9934d-145">String</span><span class="sxs-lookup"><span data-stu-id="9934d-145">String</span></span><br/> | <span data-ttu-id="9934d-146">指定父元素的顯示字串，覆寫預設的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9934d-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="9934d-147">可供 PrintCapabilities 提供者用來呈現當地語系化和使用者易記顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9934d-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="9934d-148">預設顯示名稱值是父元素的名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="9934d-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="9934d-149">在 Option 元素的情況下，如果未提供 name 屬性，則 DisplayName 屬性必須存在。</span><span class="sxs-lookup"><span data-stu-id="9934d-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9934d-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="9934d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9934d-151">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9934d-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




