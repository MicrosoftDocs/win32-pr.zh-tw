---
description: 圖示檔可保存相同圖示影像的數種不同大小。
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: IconSize 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026633"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="7f9d5-103">IconSize 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="7f9d5-103">IconSize Control Attribute</span></span>

<span data-ttu-id="7f9d5-104">圖示檔可保存相同圖示影像的數種不同大小。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="7f9d5-105">這些位指定要載入之圖示影像的大小。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="7f9d5-106">如果未設定任何位，則會載入第一個映射。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="7f9d5-107">如果只設定 **msidbControlAttributesIconSize16** ，則會載入第一個16x16 映射。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="7f9d5-108">如果只設定 **msidbControlAttributesIconSize32** ，則會載入第一個32x32 映射。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="7f9d5-109">如果設定了 **msidbControlAttributesIconSize48** ，則會載入第一個48x48 映射。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="7f9d5-110">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="7f9d5-110">Valid Controls</span></span>

[<span data-ttu-id="7f9d5-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="7f9d5-111">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="7f9d5-112">圖示</span><span class="sxs-lookup"><span data-stu-id="7f9d5-112">Icon</span></span>](icon-control.md)

[<span data-ttu-id="7f9d5-113">按鈕</span><span class="sxs-lookup"><span data-stu-id="7f9d5-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="7f9d5-114">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="7f9d5-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="7f9d5-115">值</span><span class="sxs-lookup"><span data-stu-id="7f9d5-115">Value</span></span>



| <span data-ttu-id="7f9d5-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="7f9d5-116">Decimal</span></span> | <span data-ttu-id="7f9d5-117">十六進位</span><span class="sxs-lookup"><span data-stu-id="7f9d5-117">Hexadecimal</span></span> | <span data-ttu-id="7f9d5-118">Description</span><span class="sxs-lookup"><span data-stu-id="7f9d5-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="7f9d5-119">2097152</span><span class="sxs-lookup"><span data-stu-id="7f9d5-119">2097152</span></span> | <span data-ttu-id="7f9d5-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="7f9d5-120">0x00200000</span></span>  | <span data-ttu-id="7f9d5-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="7f9d5-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="7f9d5-122">4194304</span><span class="sxs-lookup"><span data-stu-id="7f9d5-122">4194304</span></span> | <span data-ttu-id="7f9d5-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="7f9d5-123">0x00400000</span></span>  | <span data-ttu-id="7f9d5-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="7f9d5-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="7f9d5-125">6291456</span><span class="sxs-lookup"><span data-stu-id="7f9d5-125">6291456</span></span> | <span data-ttu-id="7f9d5-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="7f9d5-126">0x00600000</span></span>  | <span data-ttu-id="7f9d5-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="7f9d5-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f9d5-128">備註</span><span class="sxs-lookup"><span data-stu-id="7f9d5-128">Remarks</span></span>

<span data-ttu-id="7f9d5-129">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 IconSize 位。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="7f9d5-130">如果未設定 [FixedSize](fixedsize-control-attribute.md) 位，則會壓縮或延展載入的影像以符合圖示控制項。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="7f9d5-131">如果已設定 [FixedSize](fixedsize-control-attribute.md) 位，且載入的影像小於圖示控制項，則圖片會以中央顯示在控制項內。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="7f9d5-132">如果已設定 [FixedSize](fixedsize-control-attribute.md) 位，且載入的影像大於圖示控制項，則圖片會縮小以符合控制項。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="7f9d5-133">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="7f9d5-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



