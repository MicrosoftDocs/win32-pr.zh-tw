---
description: 如果設定了 FixedVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有固定的內部硬碟。
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: FixedVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848507"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="f6720-103">FixedVolume 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="f6720-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="f6720-104">如果設定了 FixedVolume 控制項位，此控制項就會顯示與目前安裝相關的所有磁片區，再加上所有固定的內部硬碟。</span><span class="sxs-lookup"><span data-stu-id="f6720-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="f6720-105">如果未設定此位，控制項會列出目前安裝中的磁片區。</span><span class="sxs-lookup"><span data-stu-id="f6720-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f6720-106">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="f6720-106">Valid Controls</span></span>

[<span data-ttu-id="f6720-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="f6720-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="f6720-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="f6720-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="f6720-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="f6720-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="f6720-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="f6720-110">Decimal</span></span> | <span data-ttu-id="f6720-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="f6720-111">Hexadecimal</span></span> | <span data-ttu-id="f6720-112">常數</span><span class="sxs-lookup"><span data-stu-id="f6720-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="f6720-113">131072</span><span class="sxs-lookup"><span data-stu-id="f6720-113">131072</span></span>  | <span data-ttu-id="f6720-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="f6720-114">0x00020000</span></span>  | <span data-ttu-id="f6720-115">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="f6720-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f6720-116">備註</span><span class="sxs-lookup"><span data-stu-id="f6720-116">Remarks</span></span>

<span data-ttu-id="f6720-117">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FixedVolume 位。</span><span class="sxs-lookup"><span data-stu-id="f6720-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="f6720-118">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="f6720-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



