---
title: 'RestartStrip (DirectX HLSL Stream-Output 物件) '
description: 結束目前的基本區域並啟動新的帶。 如果目前的帶狀沒有發出足夠的頂點來填滿基本拓撲，則會捨棄結尾不完整的基本。
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120193"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="3a970-104">RestartStrip (DirectX HLSL Stream-Output 物件) </span><span class="sxs-lookup"><span data-stu-id="3a970-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="3a970-105">結束目前的基本區域並啟動新的帶。</span><span class="sxs-lookup"><span data-stu-id="3a970-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="3a970-106">如果目前的帶狀沒有發出足夠的頂點來填滿基本拓撲，則會捨棄結尾不完整的基本。</span><span class="sxs-lookup"><span data-stu-id="3a970-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>

<span data-ttu-id="3a970-107">RestartStrip () ;</span><span class="sxs-lookup"><span data-stu-id="3a970-107">RestartStrip();</span></span>



 

## <a name="parameters"></a><span data-ttu-id="3a970-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a970-108">Parameters</span></span>



| <span data-ttu-id="3a970-109">項目</span><span class="sxs-lookup"><span data-stu-id="3a970-109">Item</span></span>                                                                                     | <span data-ttu-id="3a970-110">描述</span><span class="sxs-lookup"><span data-stu-id="3a970-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="3a970-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**沒有**</span><span class="sxs-lookup"><span data-stu-id="3a970-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="3a970-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a970-112">Return Value</span></span>

<span data-ttu-id="3a970-113">無</span><span class="sxs-lookup"><span data-stu-id="3a970-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="3a970-114">備註</span><span class="sxs-lookup"><span data-stu-id="3a970-114">Remarks</span></span>

<span data-ttu-id="3a970-115">區域剪下會導致目前的帶狀結束，並啟動新的帶。</span><span class="sxs-lookup"><span data-stu-id="3a970-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="3a970-116">您可以藉由明確地呼叫這個方法，或藉由轉譯最大的索引值 ( 1 來完成帶剪，也就是在) 的16位索引中，以0xffffffff 表示32位的索引或0xffff。</span><span class="sxs-lookup"><span data-stu-id="3a970-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="3a970-117">索引實例繪製的每個實例都會自動剪下剪下。</span><span class="sxs-lookup"><span data-stu-id="3a970-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="3a970-118">即使拓撲不是三角形帶，也是如此。</span><span class="sxs-lookup"><span data-stu-id="3a970-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="3a970-119">只有在 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 或更高的裝置上，才可支援重新開機和1個「魔術值」。</span><span class="sxs-lookup"><span data-stu-id="3a970-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="3a970-120">輸出一律會假設為三角形帶。</span><span class="sxs-lookup"><span data-stu-id="3a970-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="3a970-121">若要讓輸出成為三角形清單，您必須在每個三角形之間呼叫 RestartStrip。</span><span class="sxs-lookup"><span data-stu-id="3a970-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="3a970-122">不支援三角形風扇。</span><span class="sxs-lookup"><span data-stu-id="3a970-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3a970-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3a970-123">Minimum Shader Model</span></span>

<span data-ttu-id="3a970-124">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3a970-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a970-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3a970-125">Shader Model</span></span>                                              | <span data-ttu-id="3a970-126">支援</span><span class="sxs-lookup"><span data-stu-id="3a970-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a970-127">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="3a970-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a970-128">是</span><span class="sxs-lookup"><span data-stu-id="3a970-128">yes</span></span>       |
| [<span data-ttu-id="3a970-129">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a970-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a970-130">否</span><span class="sxs-lookup"><span data-stu-id="3a970-130">no</span></span>        |
| [<span data-ttu-id="3a970-131">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a970-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a970-132">否</span><span class="sxs-lookup"><span data-stu-id="3a970-132">no</span></span>        |
| [<span data-ttu-id="3a970-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3a970-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a970-134">否</span><span class="sxs-lookup"><span data-stu-id="3a970-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a970-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a970-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a970-136">資料流程輸出物件</span><span class="sxs-lookup"><span data-stu-id="3a970-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

