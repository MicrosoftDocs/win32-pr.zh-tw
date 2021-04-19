---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: 重要的屬性實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982159"
---
# <a name="important-property-instances"></a><span data-ttu-id="c1063-104">重要的屬性實例</span><span class="sxs-lookup"><span data-stu-id="c1063-104">Important Property Instances</span></span>

<span data-ttu-id="c1063-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c1063-105">This topic is not current.</span></span> <span data-ttu-id="c1063-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c1063-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1063-107">為了讓 PrintCapabilities 用戶端能夠建立合理的 PrintTicket，PrintCapabilities 檔必須提供功能實例的某些屬性，以及功能中的選項實例。</span><span class="sxs-lookup"><span data-stu-id="c1063-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="c1063-108">一般使用者介面 (UI) 模組需要這類資訊來建立 UI。</span><span class="sxs-lookup"><span data-stu-id="c1063-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="c1063-109">這接著需要 Print Schema 關鍵字定義一些屬性實例，這些實例會顯示為功能和 Option 元素的子系。</span><span class="sxs-lookup"><span data-stu-id="c1063-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="c1063-110">功能元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c1063-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="c1063-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c1063-111">Property</span></span>                  | <span data-ttu-id="c1063-112">值</span><span class="sxs-lookup"><span data-stu-id="c1063-112">Values</span></span>                                 | <span data-ttu-id="c1063-113">目的</span><span class="sxs-lookup"><span data-stu-id="c1063-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1063-114">SelectionType</span><span class="sxs-lookup"><span data-stu-id="c1063-114">SelectionType</span></span> <br/> | <span data-ttu-id="c1063-115">PickOne</span><span class="sxs-lookup"><span data-stu-id="c1063-115">PickOne</span></span><br/> <span data-ttu-id="c1063-116">PickMany</span><span class="sxs-lookup"><span data-stu-id="c1063-116">PickMany</span></span><br/> | <span data-ttu-id="c1063-117">指定可在指定時間（一個 (PickOne) 或一個以上的 (PickMany) ）選取這項功能的選項數目。</span><span class="sxs-lookup"><span data-stu-id="c1063-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="c1063-118">用戶端可以使用此資訊來建立 PrintTicket。</span><span class="sxs-lookup"><span data-stu-id="c1063-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="c1063-119">這項資訊會影響 UI 行為，以及提供者的 PrintTicket 驗證。</span><span class="sxs-lookup"><span data-stu-id="c1063-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="c1063-120">選項元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c1063-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="c1063-121">屬性</span><span class="sxs-lookup"><span data-stu-id="c1063-121">Property</span></span>                   | <span data-ttu-id="c1063-122">值</span><span class="sxs-lookup"><span data-stu-id="c1063-122">Values</span></span>                           | <span data-ttu-id="c1063-123">目的</span><span class="sxs-lookup"><span data-stu-id="c1063-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1063-124">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="c1063-124">IdentityOption</span></span> <br/> | <span data-ttu-id="c1063-125">是</span><span class="sxs-lookup"><span data-stu-id="c1063-125">True</span></span><br/> <span data-ttu-id="c1063-126">否</span><span class="sxs-lookup"><span data-stu-id="c1063-126">False</span></span><br/> | <span data-ttu-id="c1063-127">選取 [IdentityOption] 屬性工作表示「停用此功能」。</span><span class="sxs-lookup"><span data-stu-id="c1063-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="c1063-128">包含 SelectionType 屬性（其值為 PickMany）的功能也必須包含具有 IdentityOption 屬性的選項。</span><span class="sxs-lookup"><span data-stu-id="c1063-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="c1063-129">如果選取了 IdentityOption 屬性，則在建立 PrintTicket) 的 UI 程式碼 (或用戶端必須取消選取任何其他選項。</span><span class="sxs-lookup"><span data-stu-id="c1063-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="c1063-130">Feature、Option 和 ParameterDef 元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c1063-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="c1063-131">屬性</span><span class="sxs-lookup"><span data-stu-id="c1063-131">Property</span></span>              | <span data-ttu-id="c1063-132">值</span><span class="sxs-lookup"><span data-stu-id="c1063-132">Values</span></span>                          | <span data-ttu-id="c1063-133">目的</span><span class="sxs-lookup"><span data-stu-id="c1063-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1063-134">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="c1063-134">DisplayUI</span></span> <br/> | <span data-ttu-id="c1063-135">顯示</span><span class="sxs-lookup"><span data-stu-id="c1063-135">Show</span></span><br/> <span data-ttu-id="c1063-136">隱藏</span><span class="sxs-lookup"><span data-stu-id="c1063-136">Hide</span></span><br/> | <span data-ttu-id="c1063-137">指定父元素是否應顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="c1063-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="c1063-138">顯示指出元素應顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="c1063-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="c1063-139">隱藏表示元素不應顯示在 UI 中。</span><span class="sxs-lookup"><span data-stu-id="c1063-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="c1063-140">如果未定義專案的這個屬性，則會顯示預設轉譯，表示會顯示元素。</span><span class="sxs-lookup"><span data-stu-id="c1063-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="c1063-141">Feature、Option 和 ParameterDef 元素可以包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c1063-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="c1063-142">屬性</span><span class="sxs-lookup"><span data-stu-id="c1063-142">Property</span></span>                | <span data-ttu-id="c1063-143">值</span><span class="sxs-lookup"><span data-stu-id="c1063-143">Value</span></span>             | <span data-ttu-id="c1063-144">目的</span><span class="sxs-lookup"><span data-stu-id="c1063-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1063-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c1063-145">DisplayName</span></span> <br/> | <span data-ttu-id="c1063-146">String</span><span class="sxs-lookup"><span data-stu-id="c1063-146">String</span></span><br/> | <span data-ttu-id="c1063-147">指定父元素的顯示字串，覆寫預設的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c1063-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="c1063-148">可供 PrintCapabilities 提供者用來呈現當地語系化和使用者易記顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c1063-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="c1063-149">預設顯示名稱值是父元素的名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="c1063-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="c1063-150">在 Option 元素的情況下，如果未提供 name 屬性，則 DisplayName 屬性必須存在。</span><span class="sxs-lookup"><span data-stu-id="c1063-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c1063-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1063-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1063-152">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c1063-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




