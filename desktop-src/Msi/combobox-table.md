---
description: 下拉式方塊的行不會被視為個別控制項;它們是做為控制項的單一下拉式方塊的一部分。 下表列出每個下拉式方塊的值。
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: ComboBox 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979945"
---
# <a name="combobox-table"></a><span data-ttu-id="e682f-104">ComboBox 資料表</span><span class="sxs-lookup"><span data-stu-id="e682f-104">ComboBox Table</span></span>

<span data-ttu-id="e682f-105">下拉式方塊的行不會被視為個別控制項;它們是做為控制項的單一下拉式方塊的一部分。</span><span class="sxs-lookup"><span data-stu-id="e682f-105">The lines of a combo box are not treated as individual controls; they are part of a single combo box that functions as a control.</span></span> <span data-ttu-id="e682f-106">下表列出每個下拉式方塊的值。</span><span class="sxs-lookup"><span data-stu-id="e682f-106">This table lists the values for each combo box.</span></span>

<span data-ttu-id="e682f-107">ComboBox 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="e682f-107">The ComboBox table has the following columns.</span></span>



| <span data-ttu-id="e682f-108">Column</span><span class="sxs-lookup"><span data-stu-id="e682f-108">Column</span></span>   | <span data-ttu-id="e682f-109">類型</span><span class="sxs-lookup"><span data-stu-id="e682f-109">Type</span></span>                         | <span data-ttu-id="e682f-110">答案</span><span class="sxs-lookup"><span data-stu-id="e682f-110">Key</span></span> | <span data-ttu-id="e682f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="e682f-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="e682f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e682f-112">Property</span></span> | [<span data-ttu-id="e682f-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="e682f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="e682f-114">Y</span><span class="sxs-lookup"><span data-stu-id="e682f-114">Y</span></span>   | <span data-ttu-id="e682f-115">N</span><span class="sxs-lookup"><span data-stu-id="e682f-115">N</span></span>        |
| <span data-ttu-id="e682f-116">單</span><span class="sxs-lookup"><span data-stu-id="e682f-116">Order</span></span>    | [<span data-ttu-id="e682f-117">整數</span><span class="sxs-lookup"><span data-stu-id="e682f-117">Integer</span></span>](integer.md)       | <span data-ttu-id="e682f-118">Y</span><span class="sxs-lookup"><span data-stu-id="e682f-118">Y</span></span>   | <span data-ttu-id="e682f-119">N</span><span class="sxs-lookup"><span data-stu-id="e682f-119">N</span></span>        |
| <span data-ttu-id="e682f-120">值</span><span class="sxs-lookup"><span data-stu-id="e682f-120">Value</span></span>    | [<span data-ttu-id="e682f-121">格式 化</span><span class="sxs-lookup"><span data-stu-id="e682f-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="e682f-122">N</span><span class="sxs-lookup"><span data-stu-id="e682f-122">N</span></span>   | <span data-ttu-id="e682f-123">N</span><span class="sxs-lookup"><span data-stu-id="e682f-123">N</span></span>        |
| <span data-ttu-id="e682f-124">Text</span><span class="sxs-lookup"><span data-stu-id="e682f-124">Text</span></span>     | [<span data-ttu-id="e682f-125">Text</span><span class="sxs-lookup"><span data-stu-id="e682f-125">Text</span></span>](text.md)             | <span data-ttu-id="e682f-126">N</span><span class="sxs-lookup"><span data-stu-id="e682f-126">N</span></span>   | <span data-ttu-id="e682f-127">Y</span><span class="sxs-lookup"><span data-stu-id="e682f-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e682f-128">資料行</span><span class="sxs-lookup"><span data-stu-id="e682f-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e682f-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="e682f-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="e682f-130">要系結至這個專案的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="e682f-130">A named property to be tied to this item.</span></span> <span data-ttu-id="e682f-131">系結至相同屬性的所有專案都會變成相同下拉式方塊的一部分。</span><span class="sxs-lookup"><span data-stu-id="e682f-131">All the items tied to the same property become part of the same combo box.</span></span>

</dd> <dt>

<span data-ttu-id="e682f-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>以</span><span class="sxs-lookup"><span data-stu-id="e682f-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="e682f-133">正整數，用來決定出現在單一下拉式方塊清單中的專案順序。</span><span class="sxs-lookup"><span data-stu-id="e682f-133">A positive integer used to determine the ordering of the items that appear in a single combo box list.</span></span> <span data-ttu-id="e682f-134">整數不需要是連續的。</span><span class="sxs-lookup"><span data-stu-id="e682f-134">The integers do not have to be consecutive.</span></span> <span data-ttu-id="e682f-135">如果下拉式方塊定義為已排序，則所有專案都應該有 Order 值。</span><span class="sxs-lookup"><span data-stu-id="e682f-135">If a combo box is defined as ordered, then all the items should have an Order value.</span></span> <span data-ttu-id="e682f-136">如果下拉式列示方塊定義為未排序，則會忽略此資料行。</span><span class="sxs-lookup"><span data-stu-id="e682f-136">If the combo box is defined as unordered, then this column is ignored.</span></span>

<span data-ttu-id="e682f-137">僅限正數。</span><span class="sxs-lookup"><span data-stu-id="e682f-137">Positive numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="e682f-138"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="e682f-138"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="e682f-139">與這個專案相關聯的值字串。</span><span class="sxs-lookup"><span data-stu-id="e682f-139">The value string associated with this item.</span></span> <span data-ttu-id="e682f-140">選取此下拉式方塊行，就會將屬性) 中指定的相關屬性 (設定為此值。</span><span class="sxs-lookup"><span data-stu-id="e682f-140">Selecting this line of the combo box sets the associated property (specified in Property) to this value.</span></span>

</dd> <dt>

<span data-ttu-id="e682f-141"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本</span><span class="sxs-lookup"><span data-stu-id="e682f-141"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="e682f-142">要指派給專案的可見、可當地語系化文字。</span><span class="sxs-lookup"><span data-stu-id="e682f-142">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="e682f-143">如果遺漏此專案或整個資料行，則文字會預設為 [值] 中的專案。</span><span class="sxs-lookup"><span data-stu-id="e682f-143">If this entry or the entire column is missing, then the text defaults to the entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e682f-144">備註</span><span class="sxs-lookup"><span data-stu-id="e682f-144">Remarks</span></span>

<span data-ttu-id="e682f-145">[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 **MsiFormatRecord** 函數可以解讀的任何運算式。</span><span class="sxs-lookup"><span data-stu-id="e682f-145">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="e682f-146">只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期內修改了包含在運算式中的屬性，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="e682f-146">The formatting occurs only when the control is created and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="e682f-147">驗證</span><span class="sxs-lookup"><span data-stu-id="e682f-147">Validation</span></span>

<dl>

[<span data-ttu-id="e682f-148">ICE03</span><span class="sxs-lookup"><span data-stu-id="e682f-148">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e682f-149">ICE06</span><span class="sxs-lookup"><span data-stu-id="e682f-149">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e682f-150">ICE17</span><span class="sxs-lookup"><span data-stu-id="e682f-150">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="e682f-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="e682f-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



