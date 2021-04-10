---
description: 清單方塊的行不會被視為個別控制項，但它們是作為控制項的清單方塊的一部分。 ListBox 資料表會定義所有清單方塊的值。
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: ListBox 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944532"
---
# <a name="listbox-table"></a><span data-ttu-id="a4c9c-104">ListBox 資料表</span><span class="sxs-lookup"><span data-stu-id="a4c9c-104">ListBox Table</span></span>

<span data-ttu-id="a4c9c-105">清單方塊的行不會被視為個別控制項，但它們是作為控制項的清單方塊的一部分。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="a4c9c-106">ListBox 資料表會定義所有清單方塊的值。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="a4c9c-107">ListBox 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="a4c9c-108">Column</span><span class="sxs-lookup"><span data-stu-id="a4c9c-108">Column</span></span>   | <span data-ttu-id="a4c9c-109">類型</span><span class="sxs-lookup"><span data-stu-id="a4c9c-109">Type</span></span>                         | <span data-ttu-id="a4c9c-110">答案</span><span class="sxs-lookup"><span data-stu-id="a4c9c-110">Key</span></span> | <span data-ttu-id="a4c9c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a4c9c-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="a4c9c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a4c9c-112">Property</span></span> | [<span data-ttu-id="a4c9c-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="a4c9c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a4c9c-114">Y</span><span class="sxs-lookup"><span data-stu-id="a4c9c-114">Y</span></span>   | <span data-ttu-id="a4c9c-115">N</span><span class="sxs-lookup"><span data-stu-id="a4c9c-115">N</span></span>        |
| <span data-ttu-id="a4c9c-116">單</span><span class="sxs-lookup"><span data-stu-id="a4c9c-116">Order</span></span>    | [<span data-ttu-id="a4c9c-117">整數</span><span class="sxs-lookup"><span data-stu-id="a4c9c-117">Integer</span></span>](integer.md)       | <span data-ttu-id="a4c9c-118">Y</span><span class="sxs-lookup"><span data-stu-id="a4c9c-118">Y</span></span>   | <span data-ttu-id="a4c9c-119">N</span><span class="sxs-lookup"><span data-stu-id="a4c9c-119">N</span></span>        |
| <span data-ttu-id="a4c9c-120">值</span><span class="sxs-lookup"><span data-stu-id="a4c9c-120">Value</span></span>    | [<span data-ttu-id="a4c9c-121">格式 化</span><span class="sxs-lookup"><span data-stu-id="a4c9c-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a4c9c-122">N</span><span class="sxs-lookup"><span data-stu-id="a4c9c-122">N</span></span>   | <span data-ttu-id="a4c9c-123">N</span><span class="sxs-lookup"><span data-stu-id="a4c9c-123">N</span></span>        |
| <span data-ttu-id="a4c9c-124">Text</span><span class="sxs-lookup"><span data-stu-id="a4c9c-124">Text</span></span>     | [<span data-ttu-id="a4c9c-125">格式 化</span><span class="sxs-lookup"><span data-stu-id="a4c9c-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a4c9c-126">N</span><span class="sxs-lookup"><span data-stu-id="a4c9c-126">N</span></span>   | <span data-ttu-id="a4c9c-127">Y</span><span class="sxs-lookup"><span data-stu-id="a4c9c-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a4c9c-128">資料行</span><span class="sxs-lookup"><span data-stu-id="a4c9c-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a4c9c-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="a4c9c-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="a4c9c-130">要系結至這個專案的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-130">A named property to be tied to this item.</span></span> <span data-ttu-id="a4c9c-131">所有系結至相同屬性的專案都會變成相同清單方塊的一部分。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="a4c9c-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>以</span><span class="sxs-lookup"><span data-stu-id="a4c9c-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="a4c9c-133">正整數，用來決定出現在單一清單方塊中的專案順序。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="a4c9c-134">如果清單方塊定義為已排序，則所有專案都應該有 Order 值。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="a4c9c-135">整數不需要是連續的。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="a4c9c-136">如果清單方塊定義為未排序，則會忽略此資料行。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a4c9c-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="a4c9c-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a4c9c-138">與這個專案相關聯的值字串。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-138">The value string associated with this item.</span></span> <span data-ttu-id="a4c9c-139">選取該行會將相關聯的屬性設定為此值。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="a4c9c-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本</span><span class="sxs-lookup"><span data-stu-id="a4c9c-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="a4c9c-141">要指派給專案的可當地語系化、可見文字。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="a4c9c-142">如果遺漏此專案或整個資料行，則文字會預設為 [值] 中的對應專案。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4c9c-143">備註</span><span class="sxs-lookup"><span data-stu-id="a4c9c-143">Remarks</span></span>

<span data-ttu-id="a4c9c-144">[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 **MsiFormatRecord** 函數可以解讀的任何運算式。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="a4c9c-145">只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期間修改了包含在運算式中的屬性，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="a4c9c-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="a4c9c-146">驗證</span><span class="sxs-lookup"><span data-stu-id="a4c9c-146">Validation</span></span>

<dl>

[<span data-ttu-id="a4c9c-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="a4c9c-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a4c9c-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="a4c9c-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a4c9c-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="a4c9c-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="a4c9c-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="a4c9c-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="a4c9c-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="a4c9c-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



