---
title: 'GetSamplePosition (DirectX HLSL 材質物件) '
description: 取得指定之範例的位置。
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118583"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="58b57-103">GetSamplePosition (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="58b57-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="58b57-104">取得指定之範例的位置。</span><span class="sxs-lookup"><span data-stu-id="58b57-104">Gets the position of the specified sample.</span></span>

<span data-ttu-id="58b57-105">ret 物件. GetSamplePosition ( int s ) ;</span><span class="sxs-lookup"><span data-stu-id="58b57-105">ret Object.GetSamplePosition( int s );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="58b57-106">參數</span><span class="sxs-lookup"><span data-stu-id="58b57-106">Parameters</span></span>



| <span data-ttu-id="58b57-107">項目</span><span class="sxs-lookup"><span data-stu-id="58b57-107">Item</span></span>                                                                                           | <span data-ttu-id="58b57-108">描述</span><span class="sxs-lookup"><span data-stu-id="58b57-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b57-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*</span><span class="sxs-lookup"><span data-stu-id="58b57-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="58b57-110">Texture2DMS 或 Texture2DMSArray [材質物件](dx-graphics-hlsl-to-type.md) 類型。</span><span class="sxs-lookup"><span data-stu-id="58b57-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="58b57-111"><span id="s"></span><span id="S"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="58b57-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="58b57-112">\[以 \] 零為基底的範例索引。</span><span class="sxs-lookup"><span data-stu-id="58b57-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="58b57-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="58b57-113">Return Value</span></span>

<span data-ttu-id="58b57-114">傳回 (x，y) 樣本位置，這是兩個元件的浮點數向量。</span><span class="sxs-lookup"><span data-stu-id="58b57-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="58b57-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="58b57-115">Minimum Shader Model</span></span>

<span data-ttu-id="58b57-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="58b57-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="58b57-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58b57-117">vs\_4\_0</span></span> | <span data-ttu-id="58b57-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="58b57-118">vs\_4\_1</span></span>  | <span data-ttu-id="58b57-119">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58b57-119">ps\_4\_0</span></span> | <span data-ttu-id="58b57-120">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="58b57-120">ps\_4\_1</span></span>  | <span data-ttu-id="58b57-121">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58b57-121">gs\_4\_0</span></span> | <span data-ttu-id="58b57-122">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="58b57-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="58b57-123">x</span><span class="sxs-lookup"><span data-stu-id="58b57-123">x</span></span>         |          | <span data-ttu-id="58b57-124">x</span><span class="sxs-lookup"><span data-stu-id="58b57-124">x</span></span>         |          | <span data-ttu-id="58b57-125">x</span><span class="sxs-lookup"><span data-stu-id="58b57-125">x</span></span>         |



 

-   <span data-ttu-id="58b57-126">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="58b57-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b57-127">備註</span><span class="sxs-lookup"><span data-stu-id="58b57-127">Remarks</span></span>

<span data-ttu-id="58b57-128">圖元著色器可依取樣頻率進行評估 (針對每個樣本) 或圖元頻率執行圖元著色器， (每圖元) 執行一次圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="58b57-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="58b57-129">將 SV \_ SampleIndex 語義附加至圖元著色器輸入，以取樣頻率叫用圖元著色器，然後輸入值會在取樣轉譯目標時當做樣本索引。</span><span class="sxs-lookup"><span data-stu-id="58b57-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="58b57-130">您可以透過數種方式來插入圖元著色器輸入。</span><span class="sxs-lookup"><span data-stu-id="58b57-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="58b57-131">若要插入：</span><span class="sxs-lookup"><span data-stu-id="58b57-131">To interpolate at:</span></span>

-   <span data-ttu-id="58b57-132">圖元中心，請勿使用任何語義。</span><span class="sxs-lookup"><span data-stu-id="58b57-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="58b57-133">範例，請使用 SV \_ SampleIndex 語義。</span><span class="sxs-lookup"><span data-stu-id="58b57-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="58b57-134">距心位置，請使用[ \_ 距心](dx-graphics-hlsl-struct.md)修飾詞。</span><span class="sxs-lookup"><span data-stu-id="58b57-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58b57-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="58b57-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58b57-136">材質物件</span><span class="sxs-lookup"><span data-stu-id="58b57-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





