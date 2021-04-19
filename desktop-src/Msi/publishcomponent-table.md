---
description: PublishComponent 資料表會將元件資料表中所列的元件與限定詞文字字串和分類識別碼 GUID 建立關聯。
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: PublishComponent 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989392"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="41e46-103">PublishComponent 資料表</span><span class="sxs-lookup"><span data-stu-id="41e46-103">PublishComponent Table</span></span>

<span data-ttu-id="41e46-104">PublishComponent 資料表會將 [元件資料表](component-table.md) 中所列的元件與限定詞文字字串和分類識別碼 GUID 建立關聯。</span><span class="sxs-lookup"><span data-stu-id="41e46-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="41e46-105">具有以這種方式群組在一起之平行功能的元件，稱為合格元件。</span><span class="sxs-lookup"><span data-stu-id="41e46-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="41e46-106">請參閱 [合格元件](qualified-components.md)。</span><span class="sxs-lookup"><span data-stu-id="41e46-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="41e46-107">這會在參考元件時，為安裝程式提供單一層級間接取值的方法。</span><span class="sxs-lookup"><span data-stu-id="41e46-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="41e46-108">請參閱 [使用限定的元件](using-qualified-components.md)。</span><span class="sxs-lookup"><span data-stu-id="41e46-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="41e46-109">PublishComponent 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="41e46-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="41e46-110">Column</span><span class="sxs-lookup"><span data-stu-id="41e46-110">Column</span></span>      | <span data-ttu-id="41e46-111">類型</span><span class="sxs-lookup"><span data-stu-id="41e46-111">Type</span></span>                         | <span data-ttu-id="41e46-112">答案</span><span class="sxs-lookup"><span data-stu-id="41e46-112">Key</span></span> | <span data-ttu-id="41e46-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="41e46-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="41e46-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="41e46-114">ComponentId</span></span> | [<span data-ttu-id="41e46-115">GUID</span><span class="sxs-lookup"><span data-stu-id="41e46-115">GUID</span></span>](guid.md)             | <span data-ttu-id="41e46-116">Y</span><span class="sxs-lookup"><span data-stu-id="41e46-116">Y</span></span>   | <span data-ttu-id="41e46-117">N</span><span class="sxs-lookup"><span data-stu-id="41e46-117">N</span></span>        |
| <span data-ttu-id="41e46-118">Qualifier</span><span class="sxs-lookup"><span data-stu-id="41e46-118">Qualifier</span></span>   | [<span data-ttu-id="41e46-119">Text</span><span class="sxs-lookup"><span data-stu-id="41e46-119">Text</span></span>](text.md)             | <span data-ttu-id="41e46-120">Y</span><span class="sxs-lookup"><span data-stu-id="41e46-120">Y</span></span>   | <span data-ttu-id="41e46-121">N</span><span class="sxs-lookup"><span data-stu-id="41e46-121">N</span></span>        |
| <span data-ttu-id="41e46-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="41e46-122">Component\_</span></span> | [<span data-ttu-id="41e46-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="41e46-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="41e46-124">Y</span><span class="sxs-lookup"><span data-stu-id="41e46-124">Y</span></span>   | <span data-ttu-id="41e46-125">N</span><span class="sxs-lookup"><span data-stu-id="41e46-125">N</span></span>        |
| <span data-ttu-id="41e46-126">AppData</span><span class="sxs-lookup"><span data-stu-id="41e46-126">AppData</span></span>     | [<span data-ttu-id="41e46-127">Text</span><span class="sxs-lookup"><span data-stu-id="41e46-127">Text</span></span>](text.md)             | <span data-ttu-id="41e46-128">N</span><span class="sxs-lookup"><span data-stu-id="41e46-128">N</span></span>   | <span data-ttu-id="41e46-129">Y</span><span class="sxs-lookup"><span data-stu-id="41e46-129">Y</span></span>        |
| <span data-ttu-id="41e46-130">功能\_</span><span class="sxs-lookup"><span data-stu-id="41e46-130">Feature\_</span></span>   | [<span data-ttu-id="41e46-131">識別碼</span><span class="sxs-lookup"><span data-stu-id="41e46-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="41e46-132">N</span><span class="sxs-lookup"><span data-stu-id="41e46-132">N</span></span>   | <span data-ttu-id="41e46-133">N</span><span class="sxs-lookup"><span data-stu-id="41e46-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="41e46-134">資料行</span><span class="sxs-lookup"><span data-stu-id="41e46-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="41e46-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="41e46-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="41e46-136">字串 [GUID](guid.md) ，表示正在群組在一起的元件類別。</span><span class="sxs-lookup"><span data-stu-id="41e46-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="41e46-137">請注意，這個資料行的標題會誤導。</span><span class="sxs-lookup"><span data-stu-id="41e46-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="41e46-138">這是限定元件類別的 GUID，而且與 [元件資料表](component-table.md)的 [元件] 資料行中顯示的 guid 不同。</span><span class="sxs-lookup"><span data-stu-id="41e46-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="41e46-139">這裡是指提供元件功能給外部用戶端的伺服器，而不是元件本身。</span><span class="sxs-lookup"><span data-stu-id="41e46-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="41e46-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>限定 符</span><span class="sxs-lookup"><span data-stu-id="41e46-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="41e46-141">符合 [元件] 資料行中之值的文字字串。</span><span class="sxs-lookup"><span data-stu-id="41e46-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="41e46-142">辨識符號是用來區別相同元件的多個表單，例如以多種語言所執行的元件。</span><span class="sxs-lookup"><span data-stu-id="41e46-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="41e46-143">這些是 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)所傳回的辨識符號文字字串。</span><span class="sxs-lookup"><span data-stu-id="41e46-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="41e46-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="41e46-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="41e46-145">在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="41e46-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="41e46-146">此識別碼會參考元件資料表中的限定元件記錄。</span><span class="sxs-lookup"><span data-stu-id="41e46-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="41e46-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span><span class="sxs-lookup"><span data-stu-id="41e46-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="41e46-148">描述此記錄之限定元件的選擇性可當地語系化文字。</span><span class="sxs-lookup"><span data-stu-id="41e46-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="41e46-149">此字串通常是由應用程式進行剖析，並且可以向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="41e46-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="41e46-150">它應該描述限定的元件。</span><span class="sxs-lookup"><span data-stu-id="41e46-150">It should describe the qualified component.</span></span> <span data-ttu-id="41e46-151">您可以使用 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)來取出。</span><span class="sxs-lookup"><span data-stu-id="41e46-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="41e46-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="41e46-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="41e46-153">在 [功能資料表](feature-table.md)的第一個資料行中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="41e46-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="41e46-154">這是使用此合格元件的功能。</span><span class="sxs-lookup"><span data-stu-id="41e46-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41e46-155">備註</span><span class="sxs-lookup"><span data-stu-id="41e46-155">Remarks</span></span>

<span data-ttu-id="41e46-156">當執行 [PublishComponents 動作](publishcomponents-action.md) 或 [UnpublishComponents 動作](unpublishcomponents-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="41e46-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="41e46-157">請注意，此資料表的名稱會誤導。</span><span class="sxs-lookup"><span data-stu-id="41e46-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="41e46-158">撰寫公告不需要此資料表。</span><span class="sxs-lookup"><span data-stu-id="41e46-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="41e46-159">請參閱 [元件資料表](component-table.md) 和 [功能表](feature-table.md) 的屬性資料行，以取得如何設定要公告的元件安裝狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="41e46-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="41e46-160">驗證</span><span class="sxs-lookup"><span data-stu-id="41e46-160">Validation</span></span>

<dl>

[<span data-ttu-id="41e46-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="41e46-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="41e46-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="41e46-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="41e46-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="41e46-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="41e46-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="41e46-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="41e46-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="41e46-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



