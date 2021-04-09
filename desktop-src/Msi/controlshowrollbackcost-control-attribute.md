---
description: 這個屬性會指定是否要將回復備份檔案包含在 VolumeCostList 控制項所顯示的成本中。
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: ControlShowRollbackCost 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851180"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="67d8d-103">ControlShowRollbackCost 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="67d8d-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="67d8d-104">這個屬性會指定是否要將回復備份檔案包含在 [VolumeCostList 控制項](volumecostlist-control.md)所顯示的成本中。</span><span class="sxs-lookup"><span data-stu-id="67d8d-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="67d8d-105">如果設定此位，且 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) 屬性 = P，則會將回復備份檔案包含在 [VolumeCostList 控制項](volumecostlist-control.md)所顯示的成本中。</span><span class="sxs-lookup"><span data-stu-id="67d8d-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="67d8d-106">如果未設定此位且 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) 屬性 = P，則不會在 [VolumeCostList 控制項](volumecostlist-control.md)所顯示的成本中包含復原備份檔案。</span><span class="sxs-lookup"><span data-stu-id="67d8d-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="67d8d-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="67d8d-107">Valid Controls</span></span>

[<span data-ttu-id="67d8d-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="67d8d-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="67d8d-109">值</span><span class="sxs-lookup"><span data-stu-id="67d8d-109">Value</span></span>



| <span data-ttu-id="67d8d-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="67d8d-110">Decimal</span></span> | <span data-ttu-id="67d8d-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="67d8d-111">Hexadecimal</span></span> | <span data-ttu-id="67d8d-112">常數</span><span class="sxs-lookup"><span data-stu-id="67d8d-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="67d8d-113">4194304</span><span class="sxs-lookup"><span data-stu-id="67d8d-113">4194304</span></span> | <span data-ttu-id="67d8d-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="67d8d-114">0x00400000</span></span>  | <span data-ttu-id="67d8d-115">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="67d8d-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="67d8d-116">備註</span><span class="sxs-lookup"><span data-stu-id="67d8d-116">Remarks</span></span>

<span data-ttu-id="67d8d-117">如果 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D 或 F，則會忽略這個控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="67d8d-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="67d8d-118">如果 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F，則會包含復原的成本、備份檔案。</span><span class="sxs-lookup"><span data-stu-id="67d8d-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="67d8d-119">如果 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D 或 [**DISABLEROLLBACK**](-disablerollback.md) 屬性 = 1，就不會包含復原的成本。</span><span class="sxs-lookup"><span data-stu-id="67d8d-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



