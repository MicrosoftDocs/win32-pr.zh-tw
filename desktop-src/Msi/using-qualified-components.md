---
description: 限定元件是間接取值的方法，可用來將具有平行功能的元件群組成類別。
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: 使用限定元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113241"
---
# <a name="using-qualified-components"></a><span data-ttu-id="84aec-103">使用限定元件</span><span class="sxs-lookup"><span data-stu-id="84aec-103">Using Qualified Components</span></span>

<span data-ttu-id="84aec-104">限定元件是間接取值的方法，可用來將具有平行功能的元件群組成類別。</span><span class="sxs-lookup"><span data-stu-id="84aec-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="84aec-105">若要傳回完整路徑並安裝 [限定的元件](qualified-components.md)，請呼叫 [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) 或 [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)。</span><span class="sxs-lookup"><span data-stu-id="84aec-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="84aec-106">若要列舉所有限定的元件限定詞和描述性字串，請呼叫 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)。</span><span class="sxs-lookup"><span data-stu-id="84aec-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="84aec-107">**將元件群組在一起成為合格元件類別**</span><span class="sxs-lookup"><span data-stu-id="84aec-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="84aec-108">在 [元件資料表](component-table.md) 中，包含在新的限定元件類別中的每個元件都必須有一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="84aec-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="84aec-109">撰寫元件資料表中的欄位，與一般元件相同。</span><span class="sxs-lookup"><span data-stu-id="84aec-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="84aec-110">請注意，每個限定元件都必須在元件資料表的 [元件識別碼] 資料行中輸入唯一的元件識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="84aec-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="84aec-111">產生每個限定元件的辨識符號文字字串。</span><span class="sxs-lookup"><span data-stu-id="84aec-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="84aec-112">限定詞必須是唯一的文字字串，才能在搜尋限定元件時輕鬆地產生。</span><span class="sxs-lookup"><span data-stu-id="84aec-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="84aec-113">例如，如果類別中的元件是以語言限定，則 (LCID 的數值地區設定識別碼) 是合理的辨識符號字串。</span><span class="sxs-lookup"><span data-stu-id="84aec-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="84aec-114">在 [PublishComponent 資料表](publishcomponent-table.md) 中為每個限定元件新增記錄。</span><span class="sxs-lookup"><span data-stu-id="84aec-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="84aec-115">在 [元件] 資料表的 [元件] 資料行中，輸入合格元件的識別碼至 PublishComponent 資料表的 [元件] 資料 \_ 行。</span><span class="sxs-lookup"><span data-stu-id="84aec-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="84aec-116">在 [辨識符號] 資料行中，輸入每個限定元件的辨識符號字串。</span><span class="sxs-lookup"><span data-stu-id="84aec-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="84aec-117">輸入要向使用者顯示的當地語系化字串，並將限定的元件描述至選擇性的 AppData 資料行。</span><span class="sxs-lookup"><span data-stu-id="84aec-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="84aec-118">說明字串應該放在 AppData 欄位中，例如「法文字典」，而不只是數位 LCID。</span><span class="sxs-lookup"><span data-stu-id="84aec-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="84aec-119">在 [功能] 資料行中，輸入使用此元件的功能名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="84aec-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="84aec-120">此欄位中的功能識別碼也必須列在 [功能資料表](feature-table.md)的 [功能] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="84aec-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="84aec-121">為此限定元件類別產生類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="84aec-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="84aec-122">這必須是有效的 [GUID](guid.md)。</span><span class="sxs-lookup"><span data-stu-id="84aec-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="84aec-123">如果您使用 GUIDGEN 之類的公用程式來產生 GUID，請確定它只包含大寫字母。</span><span class="sxs-lookup"><span data-stu-id="84aec-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="84aec-124">針對此類別中的每個限定元件，在 [PublishComponent 資料表](publishcomponent-table.md)的 [元件] 欄位中輸入類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="84aec-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="84aec-125">下列範例說明如何將合格元件的「傳真範本」類別撰寫至元件、功能和 PublishComponent 資料表。</span><span class="sxs-lookup"><span data-stu-id="84aec-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="84aec-126">PublishComponent 資料表</span><span class="sxs-lookup"><span data-stu-id="84aec-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="84aec-127">ComponentId</span><span class="sxs-lookup"><span data-stu-id="84aec-127">ComponentId</span></span>                  | <span data-ttu-id="84aec-128">Qualifier</span><span class="sxs-lookup"><span data-stu-id="84aec-128">Qualifier</span></span> | <span data-ttu-id="84aec-129">AppData</span><span class="sxs-lookup"><span data-stu-id="84aec-129">AppData</span></span>             | <span data-ttu-id="84aec-130">功能\_</span><span class="sxs-lookup"><span data-stu-id="84aec-130">Feature\_</span></span>   | <span data-ttu-id="84aec-131">元件\_</span><span class="sxs-lookup"><span data-stu-id="84aec-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="84aec-132">{傳真範本類別 GUID}</span><span class="sxs-lookup"><span data-stu-id="84aec-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="84aec-133">1033</span><span class="sxs-lookup"><span data-stu-id="84aec-133">1033</span></span>      | <span data-ttu-id="84aec-134">美式英文範本</span><span class="sxs-lookup"><span data-stu-id="84aec-134">US English template</span></span> | <span data-ttu-id="84aec-135">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-135">FAXTemplate</span></span> | <span data-ttu-id="84aec-136">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="84aec-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="84aec-137">1041</span><span class="sxs-lookup"><span data-stu-id="84aec-137">1041</span></span>      | <span data-ttu-id="84aec-138">日文範本</span><span class="sxs-lookup"><span data-stu-id="84aec-138">Japanese template</span></span>   | <span data-ttu-id="84aec-139">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-139">FAXTemplate</span></span> | <span data-ttu-id="84aec-140">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="84aec-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="84aec-141">1054</span><span class="sxs-lookup"><span data-stu-id="84aec-141">1054</span></span>      | <span data-ttu-id="84aec-142">泰文範本</span><span class="sxs-lookup"><span data-stu-id="84aec-142">Thai template</span></span>       | <span data-ttu-id="84aec-143">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-143">FAXTemplate</span></span> | <span data-ttu-id="84aec-144">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="84aec-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="84aec-145">1031</span><span class="sxs-lookup"><span data-stu-id="84aec-145">1031</span></span>      | <span data-ttu-id="84aec-146">德文範本</span><span class="sxs-lookup"><span data-stu-id="84aec-146">German template</span></span>     | <span data-ttu-id="84aec-147">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-147">FAXTemplate</span></span> | <span data-ttu-id="84aec-148">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="84aec-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="84aec-149">[元件資料表](component-table.md) (部分資料表) </span><span class="sxs-lookup"><span data-stu-id="84aec-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="84aec-150">元件</span><span class="sxs-lookup"><span data-stu-id="84aec-150">Component</span></span>      | <span data-ttu-id="84aec-151">ComponentId</span><span class="sxs-lookup"><span data-stu-id="84aec-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="84aec-152">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="84aec-152">FAXTemplateENU</span></span> | <span data-ttu-id="84aec-153">{*FAX Template (US 英文) 元件 GUID*}</span><span class="sxs-lookup"><span data-stu-id="84aec-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="84aec-154">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="84aec-154">FAXTemplateJPN</span></span> | <span data-ttu-id="84aec-155">{*FAX Template (日文) 元件 GUID*}</span><span class="sxs-lookup"><span data-stu-id="84aec-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="84aec-156">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="84aec-156">FAXTemplateTHA</span></span> | <span data-ttu-id="84aec-157">{*FAX Template (泰文) 元件 GUID*}</span><span class="sxs-lookup"><span data-stu-id="84aec-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="84aec-158">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="84aec-158">FAXTemplateDEU</span></span> | <span data-ttu-id="84aec-159">{*FAX Template (德文) 元件 GUID*}</span><span class="sxs-lookup"><span data-stu-id="84aec-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="84aec-160">[功能表](feature-table.md) (部分資料表) </span><span class="sxs-lookup"><span data-stu-id="84aec-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="84aec-161">功能</span><span class="sxs-lookup"><span data-stu-id="84aec-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="84aec-162">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-162">FAXTemplate</span></span> |
| <span data-ttu-id="84aec-163">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-163">FAXTemplate</span></span> |
| <span data-ttu-id="84aec-164">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-164">FAXTemplate</span></span> |
| <span data-ttu-id="84aec-165">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="84aec-165">FAXTemplate</span></span> |



 

 

 



