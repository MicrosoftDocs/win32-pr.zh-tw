---
description: 如果設定點陣圖控制項位，則會以點陣圖影像取代控制項中的文字。 控制資料表中的文字資料行是二進位資料表中的外鍵。
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Bitmap 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848950"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="de84f-104">Bitmap 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="de84f-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="de84f-105">如果設定點陣圖控制項位，則會以點陣圖影像取代控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="de84f-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="de84f-106">[控制資料表](control-table.md)中的文字資料行是[二進位資料表](binary-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="de84f-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="de84f-107">如果未設定此位，則會在 [控制資料表](control-table.md)的文字資料行中指定控制項中的文字。</span><span class="sxs-lookup"><span data-stu-id="de84f-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="de84f-108">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="de84f-108">Valid Controls</span></span>

[<span data-ttu-id="de84f-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="de84f-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="de84f-110">按鈕</span><span class="sxs-lookup"><span data-stu-id="de84f-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="de84f-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="de84f-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="de84f-112">值</span><span class="sxs-lookup"><span data-stu-id="de84f-112">Value</span></span>



| <span data-ttu-id="de84f-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="de84f-113">Decimal</span></span> | <span data-ttu-id="de84f-114">十六進位</span><span class="sxs-lookup"><span data-stu-id="de84f-114">Hexadecimal</span></span> | <span data-ttu-id="de84f-115">常數</span><span class="sxs-lookup"><span data-stu-id="de84f-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="de84f-116">262144</span><span class="sxs-lookup"><span data-stu-id="de84f-116">262144</span></span>  | <span data-ttu-id="de84f-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="de84f-117">0x00040000</span></span>  | <span data-ttu-id="de84f-118">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="de84f-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="de84f-119">備註</span><span class="sxs-lookup"><span data-stu-id="de84f-119">Remarks</span></span>

<span data-ttu-id="de84f-120">若要在控制項上設定此屬性，請在控制 [資料表](control-table.md)中，于控制項記錄的 [屬性] 資料行中包含點陣圖位。</span><span class="sxs-lookup"><span data-stu-id="de84f-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="de84f-121">控制資料表中的文字資料行是用來當做 [二進位資料表](binary-table.md)的外鍵，因此控制項不能同時包含圖示影像和文字。</span><span class="sxs-lookup"><span data-stu-id="de84f-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="de84f-122">請勿同時設定 [圖示](icon-control-attribute.md) 和點陣圖位。</span><span class="sxs-lookup"><span data-stu-id="de84f-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="de84f-123">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="de84f-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



