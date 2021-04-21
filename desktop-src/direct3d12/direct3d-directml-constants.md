---
title: DirectML 常數
description: 下列常數是在中宣告 `DirectML.h` 。
keywords:
- 常數
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803407"
---
# <a name="directml-constants"></a><span data-ttu-id="1d8fe-104">DirectML 常數</span><span class="sxs-lookup"><span data-stu-id="1d8fe-104">DirectML constants</span></span>

<span data-ttu-id="1d8fe-105">下列常數是在中宣告 `DirectML.h` 。</span><span class="sxs-lookup"><span data-stu-id="1d8fe-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="1d8fe-106">常數</span><span class="sxs-lookup"><span data-stu-id="1d8fe-106">Constant</span></span> | <span data-ttu-id="1d8fe-107">值</span><span class="sxs-lookup"><span data-stu-id="1d8fe-107">Value</span></span> | <span data-ttu-id="1d8fe-108">描述</span><span class="sxs-lookup"><span data-stu-id="1d8fe-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="1d8fe-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="1d8fe-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="1d8fe-110">5</span><span class="sxs-lookup"><span data-stu-id="1d8fe-110">5</span></span> | <span data-ttu-id="1d8fe-111">針對 DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0，DirectML 張量支援最多5個維度。</span><span class="sxs-lookup"><span data-stu-id="1d8fe-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="1d8fe-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="1d8fe-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="1d8fe-113">8</span><span class="sxs-lookup"><span data-stu-id="1d8fe-113">8</span></span> | <span data-ttu-id="1d8fe-114">DirectML 張量支援最多8個 DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0 的維度。</span><span class="sxs-lookup"><span data-stu-id="1d8fe-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="1d8fe-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="1d8fe-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="1d8fe-116">256</span><span class="sxs-lookup"><span data-stu-id="1d8fe-116">256</span></span> | <span data-ttu-id="1d8fe-117">暫存和持續性緩衝區必須有對齊256個位元組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="1d8fe-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="1d8fe-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="1d8fe-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="1d8fe-119">256</span><span class="sxs-lookup"><span data-stu-id="1d8fe-119">256</span></span> | <span data-ttu-id="1d8fe-120">暫存和持續性緩衝區必須有對齊256個位元組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="1d8fe-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="1d8fe-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="1d8fe-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="1d8fe-122">16</span><span class="sxs-lookup"><span data-stu-id="1d8fe-122">16</span></span> | <span data-ttu-id="1d8fe-123">緩衝區張量的基本位址對齊需求下限為16個位元組。</span><span class="sxs-lookup"><span data-stu-id="1d8fe-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="1d8fe-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d8fe-124">Requirements</span></span>

| <span data-ttu-id="1d8fe-125">需求</span><span class="sxs-lookup"><span data-stu-id="1d8fe-125">Requirement</span></span> | <span data-ttu-id="1d8fe-126">值</span><span class="sxs-lookup"><span data-stu-id="1d8fe-126">Value</span></span> |
|-|-|
| <span data-ttu-id="1d8fe-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1d8fe-127">Header</span></span> | <span data-ttu-id="1d8fe-128">DirectML。h</span><span class="sxs-lookup"><span data-stu-id="1d8fe-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="1d8fe-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d8fe-129">See also</span></span>

* [<span data-ttu-id="1d8fe-130">DirectML 參考</span><span class="sxs-lookup"><span data-stu-id="1d8fe-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="1d8fe-131">核心參考</span><span class="sxs-lookup"><span data-stu-id="1d8fe-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="1d8fe-132">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="1d8fe-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
