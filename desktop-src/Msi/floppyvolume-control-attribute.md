---
description: 如果設定了 FloppyVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有的磁片區。
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: FloppyVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512784"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="532a1-103">FloppyVolume 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="532a1-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="532a1-104">如果設定了 FloppyVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有的磁片區。</span><span class="sxs-lookup"><span data-stu-id="532a1-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="532a1-105">如果未設定此位，控制項會列出目前安裝中的磁片區。</span><span class="sxs-lookup"><span data-stu-id="532a1-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="532a1-106">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="532a1-106">Valid Controls</span></span>

[<span data-ttu-id="532a1-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="532a1-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="532a1-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="532a1-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="532a1-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="532a1-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="532a1-110">值</span><span class="sxs-lookup"><span data-stu-id="532a1-110">Value</span></span>



| <span data-ttu-id="532a1-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="532a1-111">Decimal</span></span> | <span data-ttu-id="532a1-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="532a1-112">Hexadecimal</span></span> | <span data-ttu-id="532a1-113">常數</span><span class="sxs-lookup"><span data-stu-id="532a1-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="532a1-114">2097152</span><span class="sxs-lookup"><span data-stu-id="532a1-114">2097152</span></span> | <span data-ttu-id="532a1-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="532a1-115">0x00200000</span></span>  | <span data-ttu-id="532a1-116">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="532a1-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="532a1-117">備註</span><span class="sxs-lookup"><span data-stu-id="532a1-117">Remarks</span></span>

<span data-ttu-id="532a1-118">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FloppyVolume 位。</span><span class="sxs-lookup"><span data-stu-id="532a1-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="532a1-119">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="532a1-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



