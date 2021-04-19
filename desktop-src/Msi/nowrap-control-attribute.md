---
description: 如果設定此位，則控制項中的文字會顯示在同一行上。 如果文字延伸超過控制項的邊界，則會被截斷，而且省略號 (&\# 0034; ... &\# 0034; ) 插入結尾以表示截斷。 如果未設定此位，則文字會換行。
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979198"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="3c63b-105">NoWrap 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="3c63b-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="3c63b-106">如果設定此位，則控制項中的文字會顯示在同一行上。</span><span class="sxs-lookup"><span data-stu-id="3c63b-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="3c63b-107">如果文字延伸超過控制項的邊界，則會截斷，並在結尾插入省略號 ( "... ) "，以表示截斷。</span><span class="sxs-lookup"><span data-stu-id="3c63b-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="3c63b-108">如果未設定此位，則文字會換行。</span><span class="sxs-lookup"><span data-stu-id="3c63b-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="3c63b-109">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="3c63b-109">Valid Controls</span></span>

[<span data-ttu-id="3c63b-110">Text</span><span class="sxs-lookup"><span data-stu-id="3c63b-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="3c63b-111">值</span><span class="sxs-lookup"><span data-stu-id="3c63b-111">Value</span></span>



| <span data-ttu-id="3c63b-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="3c63b-112">Decimal</span></span> | <span data-ttu-id="3c63b-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="3c63b-113">Hexadecimal</span></span> | <span data-ttu-id="3c63b-114">常數</span><span class="sxs-lookup"><span data-stu-id="3c63b-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="3c63b-115">262144</span><span class="sxs-lookup"><span data-stu-id="3c63b-115">262144</span></span>  | <span data-ttu-id="3c63b-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="3c63b-116">0x00040000</span></span>  | <span data-ttu-id="3c63b-117">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="3c63b-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3c63b-118">備註</span><span class="sxs-lookup"><span data-stu-id="3c63b-118">Remarks</span></span>

<span data-ttu-id="3c63b-119">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 NoWrap 位。</span><span class="sxs-lookup"><span data-stu-id="3c63b-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="3c63b-120">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="3c63b-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



