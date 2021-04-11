---
description: 如果設定此位，則會以指定的順序顯示控制項中所列的專案。 如果未設定位，專案會依字母順序顯示。
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: 排序的控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026100"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="64bb9-104">排序的控制項屬性</span><span class="sxs-lookup"><span data-stu-id="64bb9-104">Sorted Control Attribute</span></span>

<span data-ttu-id="64bb9-105">如果設定此位，則會以指定的順序顯示控制項中所列的專案。</span><span class="sxs-lookup"><span data-stu-id="64bb9-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="64bb9-106">如果未設定位，專案會依字母順序顯示。</span><span class="sxs-lookup"><span data-stu-id="64bb9-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="64bb9-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="64bb9-107">Valid Controls</span></span>

[<span data-ttu-id="64bb9-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="64bb9-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="64bb9-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="64bb9-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="64bb9-110">ListView 控制項</span><span class="sxs-lookup"><span data-stu-id="64bb9-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="64bb9-111">值</span><span class="sxs-lookup"><span data-stu-id="64bb9-111">Value</span></span>



| <span data-ttu-id="64bb9-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="64bb9-112">Decimal</span></span> | <span data-ttu-id="64bb9-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="64bb9-113">Hexadecimal</span></span> | <span data-ttu-id="64bb9-114">常數</span><span class="sxs-lookup"><span data-stu-id="64bb9-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="64bb9-115">65536</span><span class="sxs-lookup"><span data-stu-id="64bb9-115">65536</span></span>   | <span data-ttu-id="64bb9-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="64bb9-116">0x00010000</span></span>  | <span data-ttu-id="64bb9-117">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="64bb9-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="64bb9-118">備註</span><span class="sxs-lookup"><span data-stu-id="64bb9-118">Remarks</span></span>

<span data-ttu-id="64bb9-119">若要排序下拉式 [方塊中的專案，請](combobox-control.md)在 [控制資料表](control-table.md) 的 [屬性] 資料行中包含已排序的位，並在 [ComboBox 資料表](combobox-table.md)的 [順序] 資料行中指定專案順序。</span><span class="sxs-lookup"><span data-stu-id="64bb9-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="64bb9-120">若要排序 [ListBox](listbox-control.md)中的專案，請在 [控制資料表](control-table.md) 的 [屬性] 資料行中包含已排序的位，並在 [ComboBox 資料表](combobox-table.md)的 [順序] 資料行中指定專案順序。</span><span class="sxs-lookup"><span data-stu-id="64bb9-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="64bb9-121">若要排序 [ListView](listview-control.md)中的專案，請在 [控制資料表](control-table.md) 的 [屬性] 資料行中包含已排序的位，並在 [ComboBox 資料表](combobox-table.md)中指定專案的順序。</span><span class="sxs-lookup"><span data-stu-id="64bb9-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="64bb9-122">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="64bb9-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



