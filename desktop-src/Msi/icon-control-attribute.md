---
description: 如果設定此位，則會將文字取代為圖示影像，而控制資料表中的文字資料行則是二進位資料表中的外鍵。
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Icon 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993014"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="3277c-103">Icon 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="3277c-103">Icon Control Attribute</span></span>

<span data-ttu-id="3277c-104">如果設定此位，則會將文字取代為圖示影像，而 [控制資料表](control-table.md) 中的文字資料行則是 [二進位資料表](binary-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="3277c-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="3277c-105">如果未設定此位，則會在 [控制資料表](control-table.md)的文字資料行中指定控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="3277c-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="3277c-106">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="3277c-106">Valid Controls</span></span>

[<span data-ttu-id="3277c-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="3277c-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="3277c-108">按鈕</span><span class="sxs-lookup"><span data-stu-id="3277c-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="3277c-109">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="3277c-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="3277c-110">值</span><span class="sxs-lookup"><span data-stu-id="3277c-110">Value</span></span>



| <span data-ttu-id="3277c-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="3277c-111">Decimal</span></span> | <span data-ttu-id="3277c-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="3277c-112">Hexadecimal</span></span> | <span data-ttu-id="3277c-113">常數</span><span class="sxs-lookup"><span data-stu-id="3277c-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="3277c-114">5242288</span><span class="sxs-lookup"><span data-stu-id="3277c-114">5242288</span></span> | <span data-ttu-id="3277c-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3277c-115">0x00080000</span></span>  | <span data-ttu-id="3277c-116">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="3277c-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3277c-117">備註</span><span class="sxs-lookup"><span data-stu-id="3277c-117">Remarks</span></span>

<span data-ttu-id="3277c-118">若要在控制項上設定此屬性，請在控制 [資料表](control-table.md)中，于控制項記錄的 [屬性] 資料行中包含圖示位。</span><span class="sxs-lookup"><span data-stu-id="3277c-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="3277c-119">控制資料表中的文字資料行是用來當做 [二進位資料表](binary-table.md)的外鍵，因此控制項不能同時包含圖示影像和文字。</span><span class="sxs-lookup"><span data-stu-id="3277c-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="3277c-120">請勿同時設定圖示和 [點陣圖](bitmap-control-attribute.md) 位。</span><span class="sxs-lookup"><span data-stu-id="3277c-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="3277c-121">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="3277c-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



