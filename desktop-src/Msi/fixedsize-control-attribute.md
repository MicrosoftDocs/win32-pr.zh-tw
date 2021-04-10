---
description: 如果設定了 FixedSize 控制項位，則圖片會在控制項中裁剪或置中，而不會變更其形狀或大小。
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: FixedSize 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690248"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="6434a-103">FixedSize 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="6434a-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="6434a-104">如果設定了 FixedSize 控制項位，則圖片會在控制項中裁剪或置中，而不會變更其形狀或大小。</span><span class="sxs-lookup"><span data-stu-id="6434a-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="6434a-105">如果未設定此位，則會將圖片伸展以符合控制項。</span><span class="sxs-lookup"><span data-stu-id="6434a-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6434a-106">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="6434a-106">Valid Controls</span></span>

[<span data-ttu-id="6434a-107">點陣圖</span><span class="sxs-lookup"><span data-stu-id="6434a-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="6434a-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="6434a-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="6434a-109">圖示</span><span class="sxs-lookup"><span data-stu-id="6434a-109">Icon</span></span>](icon-control.md)

[<span data-ttu-id="6434a-110">按鈕</span><span class="sxs-lookup"><span data-stu-id="6434a-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="6434a-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="6434a-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="6434a-112">值</span><span class="sxs-lookup"><span data-stu-id="6434a-112">Value</span></span>



| <span data-ttu-id="6434a-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="6434a-113">Decimal</span></span> | <span data-ttu-id="6434a-114">十六進位</span><span class="sxs-lookup"><span data-stu-id="6434a-114">Hexadecimal</span></span> | <span data-ttu-id="6434a-115">常數</span><span class="sxs-lookup"><span data-stu-id="6434a-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="6434a-116">1048576</span><span class="sxs-lookup"><span data-stu-id="6434a-116">1048576</span></span> | <span data-ttu-id="6434a-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="6434a-117">0x00100000</span></span>  | <span data-ttu-id="6434a-118">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="6434a-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6434a-119">備註</span><span class="sxs-lookup"><span data-stu-id="6434a-119">Remarks</span></span>

<span data-ttu-id="6434a-120">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FixedSize 位。</span><span class="sxs-lookup"><span data-stu-id="6434a-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="6434a-121">如果沒有設定[點陣圖](bitmap-control-attribute.md)或[圖示](icon-control-attribute.md)，則設定 FixedSize 位不會影響[核取方塊](checkbox-control.md)、[按鈕](pushbutton-control.md)或[RadioButtonGroup](radiobuttongroup-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="6434a-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="6434a-122">如果未設定 [IconSize](iconsize-control-attribute.md) 位，則設定 FixedSize 位不會影響圖示控制項或與圖示相關聯的按鍵。</span><span class="sxs-lookup"><span data-stu-id="6434a-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="6434a-123">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="6434a-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



