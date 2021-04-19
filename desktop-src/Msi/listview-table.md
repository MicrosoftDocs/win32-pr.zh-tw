---
description: Listview 的行不會被視為個別控制項，但它們是做為控制項的 listview 的一部分。 ListView 資料表會定義所有 listview 的值。
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: ListView 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979097"
---
# <a name="listview-table"></a><span data-ttu-id="4e1d6-104">ListView 資料表</span><span class="sxs-lookup"><span data-stu-id="4e1d6-104">ListView Table</span></span>

<span data-ttu-id="4e1d6-105">Listview 的行不會被視為個別控制項，但它們是做為控制項的 listview 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="4e1d6-106">ListView 資料表會定義所有 listview 的值。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="4e1d6-107">ListView 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="4e1d6-108">Column</span><span class="sxs-lookup"><span data-stu-id="4e1d6-108">Column</span></span>   | <span data-ttu-id="4e1d6-109">類型</span><span class="sxs-lookup"><span data-stu-id="4e1d6-109">Type</span></span>                         | <span data-ttu-id="4e1d6-110">答案</span><span class="sxs-lookup"><span data-stu-id="4e1d6-110">Key</span></span> | <span data-ttu-id="4e1d6-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="4e1d6-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="4e1d6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4e1d6-112">Property</span></span> | [<span data-ttu-id="4e1d6-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="4e1d6-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="4e1d6-114">Y</span><span class="sxs-lookup"><span data-stu-id="4e1d6-114">Y</span></span>   | <span data-ttu-id="4e1d6-115">N</span><span class="sxs-lookup"><span data-stu-id="4e1d6-115">N</span></span>        |
| <span data-ttu-id="4e1d6-116">單</span><span class="sxs-lookup"><span data-stu-id="4e1d6-116">Order</span></span>    | [<span data-ttu-id="4e1d6-117">整數</span><span class="sxs-lookup"><span data-stu-id="4e1d6-117">Integer</span></span>](integer.md)       | <span data-ttu-id="4e1d6-118">Y</span><span class="sxs-lookup"><span data-stu-id="4e1d6-118">Y</span></span>   | <span data-ttu-id="4e1d6-119">N</span><span class="sxs-lookup"><span data-stu-id="4e1d6-119">N</span></span>        |
| <span data-ttu-id="4e1d6-120">值</span><span class="sxs-lookup"><span data-stu-id="4e1d6-120">Value</span></span>    | [<span data-ttu-id="4e1d6-121">格式 化</span><span class="sxs-lookup"><span data-stu-id="4e1d6-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="4e1d6-122">N</span><span class="sxs-lookup"><span data-stu-id="4e1d6-122">N</span></span>   | <span data-ttu-id="4e1d6-123">N</span><span class="sxs-lookup"><span data-stu-id="4e1d6-123">N</span></span>        |
| <span data-ttu-id="4e1d6-124">Text</span><span class="sxs-lookup"><span data-stu-id="4e1d6-124">Text</span></span>     | [<span data-ttu-id="4e1d6-125">格式 化</span><span class="sxs-lookup"><span data-stu-id="4e1d6-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="4e1d6-126">N</span><span class="sxs-lookup"><span data-stu-id="4e1d6-126">N</span></span>   | <span data-ttu-id="4e1d6-127">Y</span><span class="sxs-lookup"><span data-stu-id="4e1d6-127">Y</span></span>        |
| <span data-ttu-id="4e1d6-128">二 進 制\_</span><span class="sxs-lookup"><span data-stu-id="4e1d6-128">Binary\_</span></span> | [<span data-ttu-id="4e1d6-129">識別碼</span><span class="sxs-lookup"><span data-stu-id="4e1d6-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="4e1d6-130">N</span><span class="sxs-lookup"><span data-stu-id="4e1d6-130">N</span></span>   | <span data-ttu-id="4e1d6-131">Y</span><span class="sxs-lookup"><span data-stu-id="4e1d6-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4e1d6-132">資料行</span><span class="sxs-lookup"><span data-stu-id="4e1d6-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4e1d6-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="4e1d6-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="4e1d6-134">要系結至這個專案的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-134">A named property to be tied to this item.</span></span> <span data-ttu-id="4e1d6-135">所有系結至相同屬性的專案都會變成相同 listview 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="4e1d6-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>以</span><span class="sxs-lookup"><span data-stu-id="4e1d6-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="4e1d6-137">正整數，用來決定出現在單一 listview 清單中的專案順序。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="4e1d6-138">整數不需要是連續的。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="4e1d6-139">如果 listview 定義為已排序，則所有專案都應該有排序值。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="4e1d6-140">如果 listview 定義為未排序，則會忽略此資料行。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="4e1d6-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="4e1d6-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="4e1d6-142">與這個專案相關聯的值字串。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-142">The value string associated with this item.</span></span> <span data-ttu-id="4e1d6-143">選取該行會將相關聯的屬性設定為此值。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="4e1d6-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本</span><span class="sxs-lookup"><span data-stu-id="4e1d6-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="4e1d6-145">要指派給專案的可見、可當地語系化文字。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="4e1d6-146">如果遺漏此專案或整個資料行，則文字會預設為 [值] 中的對應專案。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="4e1d6-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>二 進 制\_</span><span class="sxs-lookup"><span data-stu-id="4e1d6-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="4e1d6-148">圖示的影像資料。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-148">The image data for the icon.</span></span> <span data-ttu-id="4e1d6-149">這是 [二進位資料表](binary-table.md)的外鍵。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e1d6-150">備註</span><span class="sxs-lookup"><span data-stu-id="4e1d6-150">Remarks</span></span>

<span data-ttu-id="4e1d6-151">[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式會在建立控制項時將值和文字欄位的內容格式化，因此可以包含 MsiFormatRecord 函數可以解讀的任何運算式。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="4e1d6-152">只有在建立控制項時，才會進行格式化，而且如果在控制項的存留期間修改了包含在運算式中的屬性，則不會更新。</span><span class="sxs-lookup"><span data-stu-id="4e1d6-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="4e1d6-153">驗證</span><span class="sxs-lookup"><span data-stu-id="4e1d6-153">Validation</span></span>

<dl>

[<span data-ttu-id="4e1d6-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="4e1d6-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="4e1d6-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="4e1d6-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="4e1d6-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="4e1d6-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="4e1d6-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="4e1d6-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



