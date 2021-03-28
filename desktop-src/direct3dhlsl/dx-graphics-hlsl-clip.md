---
title: clip
description: 如果指定的值小於零，則會捨棄目前的圖元。
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- 剪輯 HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971732"
---
# <a name="clip"></a><span data-ttu-id="50e42-104">clip</span><span class="sxs-lookup"><span data-stu-id="50e42-104">clip</span></span>

<span data-ttu-id="50e42-105">如果指定的值小於零，則會捨棄目前的圖元。</span><span class="sxs-lookup"><span data-stu-id="50e42-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="50e42-106">剪輯 (*x*) </span><span class="sxs-lookup"><span data-stu-id="50e42-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="50e42-107">參數</span><span class="sxs-lookup"><span data-stu-id="50e42-107">Parameters</span></span>



| <span data-ttu-id="50e42-108">項目</span><span class="sxs-lookup"><span data-stu-id="50e42-108">Item</span></span>                                                   | <span data-ttu-id="50e42-109">描述</span><span class="sxs-lookup"><span data-stu-id="50e42-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="50e42-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="50e42-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="50e42-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="50e42-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="50e42-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="50e42-112">Return Value</span></span>

<span data-ttu-id="50e42-113">無。</span><span class="sxs-lookup"><span data-stu-id="50e42-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e42-114">備註</span><span class="sxs-lookup"><span data-stu-id="50e42-114">Remarks</span></span>

<span data-ttu-id="50e42-115">如果 *x* 參數的每個元件都代表與平面之間的距離，請使用 **clip** HLSL 內建函式來模擬裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="50e42-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="50e42-116">此外，使用 **剪輯** 函式來測試 Alpha 行為，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="50e42-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="50e42-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="50e42-117">Type Description</span></span>



| <span data-ttu-id="50e42-118">Name</span><span class="sxs-lookup"><span data-stu-id="50e42-118">Name</span></span> | [<span data-ttu-id="50e42-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="50e42-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="50e42-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="50e42-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="50e42-121">大小</span><span class="sxs-lookup"><span data-stu-id="50e42-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="50e42-122">*x*</span><span class="sxs-lookup"><span data-stu-id="50e42-122">*x*</span></span>  | <span data-ttu-id="50e42-123">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="50e42-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="50e42-124">**浮動**</span><span class="sxs-lookup"><span data-stu-id="50e42-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="50e42-125">任意</span><span class="sxs-lookup"><span data-stu-id="50e42-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="50e42-126">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="50e42-126">Minimum Shader Model</span></span>

<span data-ttu-id="50e42-127">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="50e42-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="50e42-128">著色器模型</span><span class="sxs-lookup"><span data-stu-id="50e42-128">Shader Model</span></span>                                              | <span data-ttu-id="50e42-129">支援</span><span class="sxs-lookup"><span data-stu-id="50e42-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="50e42-130">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="50e42-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="50e42-131">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="50e42-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="50e42-132">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50e42-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="50e42-133">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="50e42-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="50e42-134">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50e42-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="50e42-135">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="50e42-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="50e42-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="50e42-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="50e42-137">是 (只) 圖元著色器</span><span class="sxs-lookup"><span data-stu-id="50e42-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="50e42-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50e42-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e42-139">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="50e42-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

