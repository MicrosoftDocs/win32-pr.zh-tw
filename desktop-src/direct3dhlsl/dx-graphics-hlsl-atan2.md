---
title: 'atan2 (Corecrt \_ math .h) '
description: 傳回兩個值的反正切值 (x，y) 。
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196248"
---
# <a name="atan2"></a><span data-ttu-id="3633d-104">atan2</span><span class="sxs-lookup"><span data-stu-id="3633d-104">atan2</span></span>

<span data-ttu-id="3633d-105">傳回兩個值的反正切值 (x，y) 。</span><span class="sxs-lookup"><span data-stu-id="3633d-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="3633d-106">*ret* atan2 (*y*， *x*) </span><span class="sxs-lookup"><span data-stu-id="3633d-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="3633d-107">參數</span><span class="sxs-lookup"><span data-stu-id="3633d-107">Parameters</span></span>



| <span data-ttu-id="3633d-108">項目</span><span class="sxs-lookup"><span data-stu-id="3633d-108">Item</span></span>                                                   | <span data-ttu-id="3633d-109">描述</span><span class="sxs-lookup"><span data-stu-id="3633d-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3633d-110"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="3633d-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="3633d-111">\[\]的 y 值。</span><span class="sxs-lookup"><span data-stu-id="3633d-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="3633d-112"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="3633d-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3633d-113">\[在 \] x 值中。</span><span class="sxs-lookup"><span data-stu-id="3633d-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3633d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3633d-114">Return Value</span></span>

<span data-ttu-id="3633d-115"> (y，x) 的反正切值。</span><span class="sxs-lookup"><span data-stu-id="3633d-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="3633d-116">備註</span><span class="sxs-lookup"><span data-stu-id="3633d-116">Remarks</span></span>

<span data-ttu-id="3633d-117">*X* 和 *y* 參數的正負號用來判斷-π至π範圍內傳回值的象限。</span><span class="sxs-lookup"><span data-stu-id="3633d-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="3633d-118">**Atan2** HLSL 內建函式會針對來源以外的每個點妥善定義，即使 *y* 等於0且 *x* 不等於0也是一樣。</span><span class="sxs-lookup"><span data-stu-id="3633d-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="3633d-119">類型描述</span><span class="sxs-lookup"><span data-stu-id="3633d-119">Type Description</span></span>



| <span data-ttu-id="3633d-120">Name</span><span class="sxs-lookup"><span data-stu-id="3633d-120">Name</span></span>  | [<span data-ttu-id="3633d-121">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="3633d-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3633d-122">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="3633d-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3633d-123">大小</span><span class="sxs-lookup"><span data-stu-id="3633d-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="3633d-124">*y*</span><span class="sxs-lookup"><span data-stu-id="3633d-124">*y*</span></span>   | <span data-ttu-id="3633d-125">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="3633d-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3633d-126">**浮動**</span><span class="sxs-lookup"><span data-stu-id="3633d-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3633d-127">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="3633d-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="3633d-128">*x*</span><span class="sxs-lookup"><span data-stu-id="3633d-128">*x*</span></span>   | <span data-ttu-id="3633d-129">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="3633d-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="3633d-130">**浮動**</span><span class="sxs-lookup"><span data-stu-id="3633d-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3633d-131">任意</span><span class="sxs-lookup"><span data-stu-id="3633d-131">any</span></span>                            |
| <span data-ttu-id="3633d-132">*Ret*</span><span class="sxs-lookup"><span data-stu-id="3633d-132">*ret*</span></span> | <span data-ttu-id="3633d-133">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="3633d-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="3633d-134">**浮動**</span><span class="sxs-lookup"><span data-stu-id="3633d-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3633d-135">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="3633d-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3633d-136">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3633d-136">Minimum Shader Model</span></span>

<span data-ttu-id="3633d-137">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3633d-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3633d-138">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3633d-138">Shader Model</span></span>                                                                       | <span data-ttu-id="3633d-139">支援</span><span class="sxs-lookup"><span data-stu-id="3633d-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3633d-140">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="3633d-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3633d-141">是</span><span class="sxs-lookup"><span data-stu-id="3633d-141">yes</span></span>       |
| [<span data-ttu-id="3633d-142">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3633d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3633d-143">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3633d-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="3633d-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="3633d-144">Requirements</span></span>



| <span data-ttu-id="3633d-145">需求</span><span class="sxs-lookup"><span data-stu-id="3633d-145">Requirement</span></span> | <span data-ttu-id="3633d-146">值</span><span class="sxs-lookup"><span data-stu-id="3633d-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3633d-147">標頭</span><span class="sxs-lookup"><span data-stu-id="3633d-147">Header</span></span><br/> | <dl> <span data-ttu-id="3633d-148"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3633d-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3633d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3633d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3633d-150">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="3633d-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

