---
title: CheckAccessFullyMapped 函式
description: 判斷範例、收集或載入作業中的所有值是否已在磚資源中存取對應的磚。
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- CheckAccessFullyMapped 函式 HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682875"
---
# <a name="checkaccessfullymapped-function"></a><span data-ttu-id="96fb6-104">CheckAccessFullyMapped 函式</span><span class="sxs-lookup"><span data-stu-id="96fb6-104">CheckAccessFullyMapped function</span></span>

<span data-ttu-id="96fb6-105">判斷 **範例**、 **收集** 或 **載入** 作業中的所有值是否已在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚。</span><span class="sxs-lookup"><span data-stu-id="96fb6-105">Determines whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span>

## <a name="syntax"></a><span data-ttu-id="96fb6-106">語法</span><span class="sxs-lookup"><span data-stu-id="96fb6-106">Syntax</span></span>

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a><span data-ttu-id="96fb6-107">參數</span><span class="sxs-lookup"><span data-stu-id="96fb6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96fb6-108">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96fb6-108">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96fb6-109">類型： **\_ 僅限 uint**</span><span class="sxs-lookup"><span data-stu-id="96fb6-109">Type: **uint\_only**</span></span>

<span data-ttu-id="96fb6-110">從 **範例**、 **收集** 或 **載入** 作業傳回的狀態值。</span><span class="sxs-lookup"><span data-stu-id="96fb6-110">The status value that is returned from a **Sample**, **Gather**, or **Load** operation.</span></span> <span data-ttu-id="96fb6-111">因為您無法直接存取此狀態值，所以您必須將它傳遞給 **CheckAccessFullyMapped**。</span><span class="sxs-lookup"><span data-stu-id="96fb6-111">Because you can't access this status value directly, you need to pass it to **CheckAccessFullyMapped**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96fb6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="96fb6-112">Return value</span></span>

<span data-ttu-id="96fb6-113">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="96fb6-113">Type: **bool**</span></span>

<span data-ttu-id="96fb6-114">傳回 **布林** 值，這個值會指出 **範例**、 **收集** 或 **載入** 作業中的所有值是否都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚。</span><span class="sxs-lookup"><span data-stu-id="96fb6-114">Returns a **Boolean** value that indicates whether all values from a **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="96fb6-115">如果作業中的所有值都已存取對應的磚，則傳回 **TRUE** ;否則，如果從未對應的磚取得任何值，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="96fb6-115">Returns **TRUE** if all values from the operation accessed mapped tiles; otherwise, returns **FALSE** if any values were taken from an unmapped tile.</span></span>

## <a name="remarks"></a><span data-ttu-id="96fb6-116">備註</span><span class="sxs-lookup"><span data-stu-id="96fb6-116">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="96fb6-117">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="96fb6-117">Minimum Shader Model</span></span>

<span data-ttu-id="96fb6-118">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="96fb6-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="96fb6-119">著色器模型</span><span class="sxs-lookup"><span data-stu-id="96fb6-119">Shader Model</span></span>                                                                | <span data-ttu-id="96fb6-120">支援</span><span class="sxs-lookup"><span data-stu-id="96fb6-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="96fb6-121">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="96fb6-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="96fb6-122">是</span><span class="sxs-lookup"><span data-stu-id="96fb6-122">yes</span></span>       |



 

<span data-ttu-id="96fb6-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="96fb6-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="96fb6-124">頂點</span><span class="sxs-lookup"><span data-stu-id="96fb6-124">Vertex</span></span> | <span data-ttu-id="96fb6-125">船體</span><span class="sxs-lookup"><span data-stu-id="96fb6-125">Hull</span></span> | <span data-ttu-id="96fb6-126">網域</span><span class="sxs-lookup"><span data-stu-id="96fb6-126">Domain</span></span> | <span data-ttu-id="96fb6-127">幾何</span><span class="sxs-lookup"><span data-stu-id="96fb6-127">Geometry</span></span> | <span data-ttu-id="96fb6-128">像素</span><span class="sxs-lookup"><span data-stu-id="96fb6-128">Pixel</span></span> | <span data-ttu-id="96fb6-129">計算</span><span class="sxs-lookup"><span data-stu-id="96fb6-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="96fb6-130">x</span><span class="sxs-lookup"><span data-stu-id="96fb6-130">x</span></span>     | <span data-ttu-id="96fb6-131">x</span><span class="sxs-lookup"><span data-stu-id="96fb6-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="96fb6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96fb6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96fb6-133">內建函式</span><span class="sxs-lookup"><span data-stu-id="96fb6-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 