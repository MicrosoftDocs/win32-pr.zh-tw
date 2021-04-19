---
title: '篩選權數識別碼 (Fwpmu .h) '
description: 基礎篩選引擎 (BFE) 用來計算自動產生之篩選加權的篩選權數識別碼。
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967992"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="3cfa3-103">篩選權數識別碼</span><span class="sxs-lookup"><span data-stu-id="3cfa3-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="3cfa3-104">基礎篩選引擎 (BFE) 用來計算自動產生之篩選權數的篩選權數識別碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="3cfa3-105">如需篩選權數產生的詳細資訊，請參閱 [篩選權數指派](filter-weight-assignment.md) 。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="3cfa3-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM \_ 自動 \_ 權數 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="3cfa3-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cfa3-107"> (60) </span><span class="sxs-lookup"><span data-stu-id="3cfa3-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="3cfa3-108">用於自動產生之篩選加權的位數。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3cfa3-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM \_ 自動 \_ 加權 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="3cfa3-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cfa3-110"> (**MAXUINT64** >> 4) </span><span class="sxs-lookup"><span data-stu-id="3cfa3-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="3cfa3-111">自動產生的篩選權數上限。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3cfa3-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM \_ 權數 \_ 範圍 \_ IKE \_ 豁免**</span><span class="sxs-lookup"><span data-stu-id="3cfa3-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cfa3-113"> (0xC) </span><span class="sxs-lookup"><span data-stu-id="3cfa3-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="3cfa3-114">BFE 會將具有此範圍值的權數指派給 IKE 和 AuthIP 篩選器。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="3cfa3-115">如需 IKE/AuthIP 篩選器的詳細資訊，請參閱 [ike/Authip 豁免](ike-exemptions.md) 。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3cfa3-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM \_ 權數 \_ 範圍 \_ IPSEC**</span><span class="sxs-lookup"><span data-stu-id="3cfa3-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cfa3-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="3cfa3-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="3cfa3-118">BFE 會將具有此範圍值的權數指派給 IPsec 原則篩選器。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3cfa3-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM \_ 權數 \_ 範圍 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="3cfa3-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cfa3-120"> (**MAXUINT64** >> 60) </span><span class="sxs-lookup"><span data-stu-id="3cfa3-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="3cfa3-121">允許的篩選權數範圍值上限。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="3cfa3-122">**MAXUINT64** 代表 **UINT64** 的最大可能值。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="3cfa3-123">這個常數的值為0xFFFFFFFFFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="3cfa3-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3cfa3-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cfa3-124">Requirements</span></span>



| <span data-ttu-id="3cfa3-125">需求</span><span class="sxs-lookup"><span data-stu-id="3cfa3-125">Requirement</span></span> | <span data-ttu-id="3cfa3-126">值</span><span class="sxs-lookup"><span data-stu-id="3cfa3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfa3-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cfa3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfa3-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cfa3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3cfa3-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cfa3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfa3-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cfa3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3cfa3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3cfa3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cfa3-132"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cfa3-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





