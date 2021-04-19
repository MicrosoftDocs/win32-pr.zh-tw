---
description: 如果設定了 CDROMVolume 控制項位，此控制項就會顯示目前安裝中的所有磁片區，再加上所有的 CD-ROM 磁片區。
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: CDROMVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996697"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="59778-103">CDROMVolume 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="59778-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="59778-104">如果設定了 CDROMVolume 控制項位，此控制項就會顯示目前安裝中的所有磁片區，再加上所有的 CD-ROM 磁片區。</span><span class="sxs-lookup"><span data-stu-id="59778-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="59778-105">如果未設定此位，控制項會顯示目前安裝中的所有磁片區。</span><span class="sxs-lookup"><span data-stu-id="59778-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="59778-106">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="59778-106">Valid Controls</span></span>

[<span data-ttu-id="59778-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="59778-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="59778-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="59778-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="59778-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="59778-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="59778-110">值</span><span class="sxs-lookup"><span data-stu-id="59778-110">Value</span></span>



| <span data-ttu-id="59778-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="59778-111">Decimal</span></span> | <span data-ttu-id="59778-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="59778-112">Hexadecimal</span></span> | <span data-ttu-id="59778-113">常數</span><span class="sxs-lookup"><span data-stu-id="59778-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="59778-114">524288</span><span class="sxs-lookup"><span data-stu-id="59778-114">524288</span></span>  | <span data-ttu-id="59778-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="59778-115">0x00080000</span></span>  | <span data-ttu-id="59778-116">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="59778-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="59778-117">備註</span><span class="sxs-lookup"><span data-stu-id="59778-117">Remarks</span></span>

<span data-ttu-id="59778-118">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 CDROMVolume 位。</span><span class="sxs-lookup"><span data-stu-id="59778-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="59778-119">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="59778-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



