---
title: 'fma (Corecrt \_ math .h) '
description: 傳回 \ b + c 的雙精確度融合乘積。
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- fma HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384609"
---
# <a name="fma"></a><span data-ttu-id="2b429-104">fma</span><span class="sxs-lookup"><span data-stu-id="2b429-104">fma</span></span>

<span data-ttu-id="2b429-105">傳回 b + c 的雙精確度融合乘積 \* 。</span><span class="sxs-lookup"><span data-stu-id="2b429-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="2b429-106">*ret* fma (雙 *a*、 *b*、 *c*) ;</span><span class="sxs-lookup"><span data-stu-id="2b429-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2b429-107">參數</span><span class="sxs-lookup"><span data-stu-id="2b429-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b429-108"><span id="a"></span><span id="A"></span>*的*</span><span class="sxs-lookup"><span data-stu-id="2b429-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="2b429-109">\[在 \] 融合的乘法-加法中的第一個值。</span><span class="sxs-lookup"><span data-stu-id="2b429-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="2b429-110"><span id="b"></span><span id="B"></span>*B*</span><span class="sxs-lookup"><span data-stu-id="2b429-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="2b429-111">\[在 \] 融合的乘法-加法中的第二個值。</span><span class="sxs-lookup"><span data-stu-id="2b429-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="2b429-112"><span id="c"></span><span id="C"></span>*C*</span><span class="sxs-lookup"><span data-stu-id="2b429-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="2b429-113">\[在 \] 融合乘積的第三個值中。</span><span class="sxs-lookup"><span data-stu-id="2b429-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b429-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b429-114">Return Value</span></span>

<span data-ttu-id="2b429-115">雙精確度融合的數位加上 \* *b*  +  *c* 的參數。</span><span class="sxs-lookup"><span data-stu-id="2b429-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="2b429-116">傳回的值必須精確為0.5 的精確度 (ULP) 的最小有效位數。</span><span class="sxs-lookup"><span data-stu-id="2b429-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b429-117">備註</span><span class="sxs-lookup"><span data-stu-id="2b429-117">Remarks</span></span>

<span data-ttu-id="2b429-118">**Fma** 內建函式必須支援 Nan、Inf 和 Denorms。</span><span class="sxs-lookup"><span data-stu-id="2b429-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="2b429-119">若要在您的著色器程式碼中使用 **fma** 內建，請使用 [**D3D11 \_ 功能 \_ D3D11 \_ 選項**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature)來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)方法，以確認 Direct3D 裝置支援 [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)功能選項。</span><span class="sxs-lookup"><span data-stu-id="2b429-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="2b429-120">**Fma** 內建需要 WDDM 1.2 顯示驅動程式，而所有 WDDM 1.2 顯示器驅動程式都必須支援 **fma**。</span><span class="sxs-lookup"><span data-stu-id="2b429-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="2b429-121">如果您的應用程式使用 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 或11.1 建立轉譯裝置，而且編譯目標為著色器模型5或更新版本，則 HLSL 原始程式碼可以使用 **fma** 內建。</span><span class="sxs-lookup"><span data-stu-id="2b429-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="2b429-122">類型描述</span><span class="sxs-lookup"><span data-stu-id="2b429-122">Type Description</span></span>



| <span data-ttu-id="2b429-123">Name</span><span class="sxs-lookup"><span data-stu-id="2b429-123">Name</span></span>  | [<span data-ttu-id="2b429-124">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="2b429-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="2b429-125">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="2b429-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="2b429-126">大小</span><span class="sxs-lookup"><span data-stu-id="2b429-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="2b429-127">*的*</span><span class="sxs-lookup"><span data-stu-id="2b429-127">*a*</span></span>   | <span data-ttu-id="2b429-128">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="2b429-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="2b429-129">**double**</span><span class="sxs-lookup"><span data-stu-id="2b429-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="2b429-130">任意</span><span class="sxs-lookup"><span data-stu-id="2b429-130">any</span></span>                          |
| <span data-ttu-id="2b429-131">*b*</span><span class="sxs-lookup"><span data-stu-id="2b429-131">*b*</span></span>   | <span data-ttu-id="2b429-132">與輸入 *a* 相同</span><span class="sxs-lookup"><span data-stu-id="2b429-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="2b429-133">**double**</span><span class="sxs-lookup"><span data-stu-id="2b429-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="2b429-134">與輸入 a 相同 *的* 維度</span><span class="sxs-lookup"><span data-stu-id="2b429-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="2b429-135">*c*</span><span class="sxs-lookup"><span data-stu-id="2b429-135">*c*</span></span>   | <span data-ttu-id="2b429-136">與輸入 *a* 相同</span><span class="sxs-lookup"><span data-stu-id="2b429-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="2b429-137">**double**</span><span class="sxs-lookup"><span data-stu-id="2b429-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="2b429-138">與輸入 a 相同 *的* 維度</span><span class="sxs-lookup"><span data-stu-id="2b429-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="2b429-139">*Ret*</span><span class="sxs-lookup"><span data-stu-id="2b429-139">*ret*</span></span> | <span data-ttu-id="2b429-140">與輸入 *a* 相同</span><span class="sxs-lookup"><span data-stu-id="2b429-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="2b429-141">**double**</span><span class="sxs-lookup"><span data-stu-id="2b429-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="2b429-142">與輸入 a 相同 *的* 維度</span><span class="sxs-lookup"><span data-stu-id="2b429-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="2b429-143">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2b429-143">Minimum Shader Model</span></span>

<span data-ttu-id="2b429-144">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2b429-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2b429-145">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2b429-145">Shader Model</span></span>                                                | <span data-ttu-id="2b429-146">支援</span><span class="sxs-lookup"><span data-stu-id="2b429-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="2b429-147">著色器模型5或更新版本</span><span class="sxs-lookup"><span data-stu-id="2b429-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="2b429-148">是</span><span class="sxs-lookup"><span data-stu-id="2b429-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="2b429-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b429-149">Requirements</span></span>



| <span data-ttu-id="2b429-150">需求</span><span class="sxs-lookup"><span data-stu-id="2b429-150">Requirement</span></span> | <span data-ttu-id="2b429-151">值</span><span class="sxs-lookup"><span data-stu-id="2b429-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b429-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b429-152">Minimum supported client</span></span><br/> | <span data-ttu-id="2b429-153">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b429-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="2b429-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b429-154">Minimum supported server</span></span><br/> | <span data-ttu-id="2b429-155">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b429-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="2b429-156">標頭</span><span class="sxs-lookup"><span data-stu-id="2b429-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b429-157"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b429-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b429-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b429-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b429-159">內建函式</span><span class="sxs-lookup"><span data-stu-id="2b429-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

