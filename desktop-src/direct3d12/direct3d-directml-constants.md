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
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988575"
---
# <a name="directml-constants"></a><span data-ttu-id="8b433-104">DirectML 常數</span><span class="sxs-lookup"><span data-stu-id="8b433-104">DirectML constants</span></span>

<span data-ttu-id="8b433-105">下列常數是在中宣告 `DirectML.h` 。</span><span class="sxs-lookup"><span data-stu-id="8b433-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="8b433-106">常數</span><span class="sxs-lookup"><span data-stu-id="8b433-106">Constant</span></span> | <span data-ttu-id="8b433-107">值</span><span class="sxs-lookup"><span data-stu-id="8b433-107">Value</span></span> | <span data-ttu-id="8b433-108">描述</span><span class="sxs-lookup"><span data-stu-id="8b433-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="8b433-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="8b433-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="8b433-110">5</span><span class="sxs-lookup"><span data-stu-id="8b433-110">5</span></span> | <span data-ttu-id="8b433-111">針對 DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0，DirectML 張量支援最多5個維度。</span><span class="sxs-lookup"><span data-stu-id="8b433-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="8b433-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="8b433-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="8b433-113">8</span><span class="sxs-lookup"><span data-stu-id="8b433-113">8</span></span> | <span data-ttu-id="8b433-114">DirectML 張量支援最多8個 DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0 的維度。</span><span class="sxs-lookup"><span data-stu-id="8b433-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="8b433-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="8b433-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="8b433-116">256</span><span class="sxs-lookup"><span data-stu-id="8b433-116">256</span></span> | <span data-ttu-id="8b433-117">暫存和持續性緩衝區必須有對齊256個位元組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="8b433-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="8b433-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="8b433-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="8b433-119">256</span><span class="sxs-lookup"><span data-stu-id="8b433-119">256</span></span> | <span data-ttu-id="8b433-120">暫存和持續性緩衝區必須有對齊256個位元組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="8b433-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="8b433-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="8b433-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="8b433-122">16</span><span class="sxs-lookup"><span data-stu-id="8b433-122">16</span></span> | <span data-ttu-id="8b433-123">緩衝區張量的基本位址對齊需求下限為16個位元組。</span><span class="sxs-lookup"><span data-stu-id="8b433-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="8b433-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b433-124">Requirements</span></span>

| <span data-ttu-id="8b433-125">需求</span><span class="sxs-lookup"><span data-stu-id="8b433-125">Requirement</span></span> | <span data-ttu-id="8b433-126">值</span><span class="sxs-lookup"><span data-stu-id="8b433-126">Value</span></span> |
|-|-|
| <span data-ttu-id="8b433-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8b433-127">Header</span></span> | <span data-ttu-id="8b433-128">D3D12。h</span><span class="sxs-lookup"><span data-stu-id="8b433-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="8b433-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b433-129">See also</span></span>

* [<span data-ttu-id="8b433-130">DirectML 參考</span><span class="sxs-lookup"><span data-stu-id="8b433-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="8b433-131">核心參考</span><span class="sxs-lookup"><span data-stu-id="8b433-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="8b433-132">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="8b433-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
