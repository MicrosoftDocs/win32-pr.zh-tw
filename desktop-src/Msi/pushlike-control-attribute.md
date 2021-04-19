---
description: 如果已在核取方塊或選項按鈕群組上設定此位，則會使用 [按下] 按鈕的外觀來繪製按鈕，但其邏輯會維持不變。 如果未設定位，則會以其一般樣式來繪製控制項。
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: PushLike 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974441"
---
# <a name="pushlike-control-attribute"></a><span data-ttu-id="e2a55-104">PushLike 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="e2a55-104">PushLike Control Attribute</span></span>

<span data-ttu-id="e2a55-105">如果已在核取方塊或選項按鈕群組上設定此位，則會使用 [按下] 按鈕的外觀來繪製按鈕，但其邏輯會維持不變。</span><span class="sxs-lookup"><span data-stu-id="e2a55-105">If this bit is set on a check box or a radio button group, the button is drawn with the appearance of a push button, but its logic stays the same.</span></span> <span data-ttu-id="e2a55-106">如果未設定位，則會以其一般樣式來繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="e2a55-106">If the bit is not set, the controls are drawn in their usual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="e2a55-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="e2a55-107">Valid Controls</span></span>

<span data-ttu-id="e2a55-108">[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)</span><span class="sxs-lookup"><span data-stu-id="e2a55-108">[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)</span></span>

## <a name="value"></a><span data-ttu-id="e2a55-109">值</span><span class="sxs-lookup"><span data-stu-id="e2a55-109">Value</span></span>



| <span data-ttu-id="e2a55-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="e2a55-110">Decimal</span></span> | <span data-ttu-id="e2a55-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="e2a55-111">Hexadecimal</span></span> | <span data-ttu-id="e2a55-112">常數</span><span class="sxs-lookup"><span data-stu-id="e2a55-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="e2a55-113">131072</span><span class="sxs-lookup"><span data-stu-id="e2a55-113">131072</span></span>  | <span data-ttu-id="e2a55-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="e2a55-114">0x00020000</span></span>  | <span data-ttu-id="e2a55-115">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="e2a55-115">**msidbControlAttributesPushLike**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e2a55-116">備註</span><span class="sxs-lookup"><span data-stu-id="e2a55-116">Remarks</span></span>

<span data-ttu-id="e2a55-117">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 PushLike 位。</span><span class="sxs-lookup"><span data-stu-id="e2a55-117">To set this attribute on a control, include the PushLike bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="e2a55-118">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="e2a55-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



