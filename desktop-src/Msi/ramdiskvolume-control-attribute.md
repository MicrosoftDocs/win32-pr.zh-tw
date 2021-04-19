---
description: 如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有 RAM 磁碟區。 如果未設定此位，控制項會列出目前安裝中的磁片區。
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: RAMDiskVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980835"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="87b5a-104">RAMDiskVolume 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="87b5a-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="87b5a-105">如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有 RAM 磁碟區。</span><span class="sxs-lookup"><span data-stu-id="87b5a-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="87b5a-106">如果未設定此位，控制項會列出目前安裝中的磁片區。</span><span class="sxs-lookup"><span data-stu-id="87b5a-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="87b5a-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="87b5a-107">Valid Controls</span></span>

[<span data-ttu-id="87b5a-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="87b5a-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="87b5a-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="87b5a-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="87b5a-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="87b5a-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="87b5a-111">值</span><span class="sxs-lookup"><span data-stu-id="87b5a-111">Value</span></span>



| <span data-ttu-id="87b5a-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="87b5a-112">Decimal</span></span> | <span data-ttu-id="87b5a-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="87b5a-113">Hexadecimal</span></span> | <span data-ttu-id="87b5a-114">常數</span><span class="sxs-lookup"><span data-stu-id="87b5a-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="87b5a-115">1048567</span><span class="sxs-lookup"><span data-stu-id="87b5a-115">1048567</span></span> | <span data-ttu-id="87b5a-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="87b5a-116">0x00100000</span></span>  | <span data-ttu-id="87b5a-117">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="87b5a-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="87b5a-118">備註</span><span class="sxs-lookup"><span data-stu-id="87b5a-118">Remarks</span></span>

<span data-ttu-id="87b5a-119">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 RAMDiskVolume 位。</span><span class="sxs-lookup"><span data-stu-id="87b5a-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="87b5a-120">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="87b5a-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



