---
description: 如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有遠端磁片區。 如果未設定此位，控制項會列出目前安裝中的磁片區。
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: RemoteVolume 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970979"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="3d18f-104">RemoteVolume 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="3d18f-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="3d18f-105">如果設定此位，此控制項會顯示與目前安裝相關的所有磁片區，再加上所有遠端磁片區。</span><span class="sxs-lookup"><span data-stu-id="3d18f-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="3d18f-106">如果未設定此位，控制項會列出目前安裝中的磁片區。</span><span class="sxs-lookup"><span data-stu-id="3d18f-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="3d18f-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="3d18f-107">Valid Controls</span></span>

[<span data-ttu-id="3d18f-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="3d18f-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="3d18f-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="3d18f-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="3d18f-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="3d18f-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="3d18f-111">值</span><span class="sxs-lookup"><span data-stu-id="3d18f-111">Value</span></span>



| <span data-ttu-id="3d18f-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="3d18f-112">Decimal</span></span> | <span data-ttu-id="3d18f-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="3d18f-113">Hexadecimal</span></span> | <span data-ttu-id="3d18f-114">常數</span><span class="sxs-lookup"><span data-stu-id="3d18f-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="3d18f-115">262144</span><span class="sxs-lookup"><span data-stu-id="3d18f-115">262144</span></span>  | <span data-ttu-id="3d18f-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="3d18f-116">0x00040000</span></span>  | <span data-ttu-id="3d18f-117">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="3d18f-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3d18f-118">備註</span><span class="sxs-lookup"><span data-stu-id="3d18f-118">Remarks</span></span>

<span data-ttu-id="3d18f-119">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 RemoteVolume 位。</span><span class="sxs-lookup"><span data-stu-id="3d18f-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="3d18f-120">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="3d18f-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



