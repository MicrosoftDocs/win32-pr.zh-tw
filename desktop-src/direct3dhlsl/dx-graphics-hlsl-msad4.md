---
title: msad4
description: 比較4位元組的參考值和8位元組的來源值，並累積4加總的向量。 每個總和都會對應至參考值與來源值之間不同位元組對齊的絕對差異的遮罩總和。
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104971856"
---
# <a name="msad4"></a><span data-ttu-id="2b47d-105">msad4</span><span class="sxs-lookup"><span data-stu-id="2b47d-105">msad4</span></span>

<span data-ttu-id="2b47d-106">比較4位元組的參考值和8位元組的來源值，並累積4加總的向量。</span><span class="sxs-lookup"><span data-stu-id="2b47d-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="2b47d-107">每個總和都會對應至參考值與來源值之間不同位元組對齊的絕對差異的遮罩總和。</span><span class="sxs-lookup"><span data-stu-id="2b47d-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="2b47d-108">uint4 result = msad4 (uint reference、uint2 source、uint4 accum) ;</span><span class="sxs-lookup"><span data-stu-id="2b47d-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2b47d-109">參數</span><span class="sxs-lookup"><span data-stu-id="2b47d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b47d-110"><span id="reference"></span><span id="REFERENCE"></span>*參考*</span><span class="sxs-lookup"><span data-stu-id="2b47d-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="2b47d-111">\[在 \] 一個 **uint** 值中4個位元組的參考陣列中。</span><span class="sxs-lookup"><span data-stu-id="2b47d-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="2b47d-112"><span id="source"></span><span id="SOURCE"></span>*源*</span><span class="sxs-lookup"><span data-stu-id="2b47d-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="2b47d-113">\[在 \] 8 個位元組的來源陣列中，兩個 **uint2** 值。</span><span class="sxs-lookup"><span data-stu-id="2b47d-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="2b47d-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span><span class="sxs-lookup"><span data-stu-id="2b47d-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="2b47d-115">\[在 \] 4 個值的向量中。</span><span class="sxs-lookup"><span data-stu-id="2b47d-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="2b47d-116">**msad4** 會將這個向量新增至參考值與來源值之間不同位元組對齊的遮罩加總。</span><span class="sxs-lookup"><span data-stu-id="2b47d-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b47d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b47d-117">Return Value</span></span>

<span data-ttu-id="2b47d-118">4加總的向量。</span><span class="sxs-lookup"><span data-stu-id="2b47d-118">A vector of 4 sums.</span></span> <span data-ttu-id="2b47d-119">每個總和都對應于參考值與來源值之間不同位元組對齊的遮罩加總。</span><span class="sxs-lookup"><span data-stu-id="2b47d-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="2b47d-120">如果 msad4 的差異是遮罩的，則不會包含總和的差異 (也就是說，參考位元組為 0) 。</span><span class="sxs-lookup"><span data-stu-id="2b47d-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b47d-121">備註</span><span class="sxs-lookup"><span data-stu-id="2b47d-121">Remarks</span></span>

<span data-ttu-id="2b47d-122">若要在您的著色器程式碼中使用 **msad4** 內建，請使用 [**D3D11 \_ FEATURE \_ D3D11 \_ 選項**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature)來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)方法，以確認 Direct3D 裝置支援 [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)功能選項。</span><span class="sxs-lookup"><span data-stu-id="2b47d-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="2b47d-123">**Msad4** 內建需要 WDDM 1.2 顯示驅動程式，且所有 WDDM 1.2 顯示器驅動程式都必須支援 **msad4**。</span><span class="sxs-lookup"><span data-stu-id="2b47d-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="2b47d-124">如果您的應用程式使用 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 或11.1 建立轉譯裝置，而且編譯目標為著色器模型5或更新版本，則 HLSL 原始程式碼可以使用 **msad4** 內建。</span><span class="sxs-lookup"><span data-stu-id="2b47d-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="2b47d-125">傳回值的精確度最高為65535。</span><span class="sxs-lookup"><span data-stu-id="2b47d-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="2b47d-126">如果您使用可能導致傳回值大於65535的輸入來呼叫 **msad4** 內建， **msad4** 會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="2b47d-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2b47d-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2b47d-127">Minimum Shader Model</span></span>

<span data-ttu-id="2b47d-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2b47d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2b47d-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2b47d-129">Shader Model</span></span>                                                | <span data-ttu-id="2b47d-130">支援</span><span class="sxs-lookup"><span data-stu-id="2b47d-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="2b47d-131">著色器模型5或更新版本</span><span class="sxs-lookup"><span data-stu-id="2b47d-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="2b47d-132">是</span><span class="sxs-lookup"><span data-stu-id="2b47d-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="2b47d-133">範例</span><span class="sxs-lookup"><span data-stu-id="2b47d-133">Examples</span></span>

<span data-ttu-id="2b47d-134">以下是 **msad4** 的範例結果計算：</span><span class="sxs-lookup"><span data-stu-id="2b47d-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="2b47d-135">以下範例示範如何使用 **msad4** 來搜尋緩衝區內的參考模式：</span><span class="sxs-lookup"><span data-stu-id="2b47d-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="2b47d-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b47d-136">Requirements</span></span>



| <span data-ttu-id="2b47d-137">需求</span><span class="sxs-lookup"><span data-stu-id="2b47d-137">Requirement</span></span> | <span data-ttu-id="2b47d-138">值</span><span class="sxs-lookup"><span data-stu-id="2b47d-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2b47d-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b47d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2b47d-140">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b47d-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="2b47d-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b47d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2b47d-142">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b47d-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b47d-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b47d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b47d-144">內建函式</span><span class="sxs-lookup"><span data-stu-id="2b47d-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

