---
title: 規範
description: 根據 x/length (x) 標準化指定的浮點向量。
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- 標準化 HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933581"
---
# <a name="normalize"></a><span data-ttu-id="54672-104">規範</span><span class="sxs-lookup"><span data-stu-id="54672-104">normalize</span></span>

<span data-ttu-id="54672-105">根據 x/length (x) 標準化指定的浮點向量。</span><span class="sxs-lookup"><span data-stu-id="54672-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="54672-106">*ret* 標準化 (*x*) </span><span class="sxs-lookup"><span data-stu-id="54672-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="54672-107">參數</span><span class="sxs-lookup"><span data-stu-id="54672-107">Parameters</span></span>



| <span data-ttu-id="54672-108">項目</span><span class="sxs-lookup"><span data-stu-id="54672-108">Item</span></span>                                                   | <span data-ttu-id="54672-109">描述</span><span class="sxs-lookup"><span data-stu-id="54672-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="54672-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="54672-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="54672-111">\[在 \] 指定的浮點向量中。</span><span class="sxs-lookup"><span data-stu-id="54672-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="54672-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="54672-112">Return Value</span></span>

<span data-ttu-id="54672-113">正規化 *x* 參數。</span><span class="sxs-lookup"><span data-stu-id="54672-113">The normalized *x* parameter.</span></span> <span data-ttu-id="54672-114">如果 *x* 參數的長度為0，則結果為不定。</span><span class="sxs-lookup"><span data-stu-id="54672-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="54672-115">備註</span><span class="sxs-lookup"><span data-stu-id="54672-115">Remarks</span></span>

<span data-ttu-id="54672-116">正規化 **HLSL 內部** 函數會使用下列公式： *x*  /  [**長度**](dx-graphics-hlsl-length.md) (*x*) 。</span><span class="sxs-lookup"><span data-stu-id="54672-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="54672-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="54672-117">Type Description</span></span>



| <span data-ttu-id="54672-118">Name</span><span class="sxs-lookup"><span data-stu-id="54672-118">Name</span></span>  | [<span data-ttu-id="54672-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="54672-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="54672-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="54672-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="54672-121">大小</span><span class="sxs-lookup"><span data-stu-id="54672-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="54672-122">*x*</span><span class="sxs-lookup"><span data-stu-id="54672-122">*x*</span></span>   | [<span data-ttu-id="54672-123">**向量**</span><span class="sxs-lookup"><span data-stu-id="54672-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="54672-124">**浮動**</span><span class="sxs-lookup"><span data-stu-id="54672-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="54672-125">任意</span><span class="sxs-lookup"><span data-stu-id="54672-125">any</span></span>                            |
| <span data-ttu-id="54672-126">*Ret*</span><span class="sxs-lookup"><span data-stu-id="54672-126">*ret*</span></span> | <span data-ttu-id="54672-127">與輸入 *x* 相同</span><span class="sxs-lookup"><span data-stu-id="54672-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="54672-128">**浮動**</span><span class="sxs-lookup"><span data-stu-id="54672-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="54672-129">) 為輸入 *x* 的相同維度 (s</span><span class="sxs-lookup"><span data-stu-id="54672-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54672-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="54672-130">Minimum Shader Model</span></span>

<span data-ttu-id="54672-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="54672-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="54672-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="54672-132">Shader Model</span></span>                                                                       | <span data-ttu-id="54672-133">支援</span><span class="sxs-lookup"><span data-stu-id="54672-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="54672-134">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="54672-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="54672-135">是</span><span class="sxs-lookup"><span data-stu-id="54672-135">yes</span></span>                 |
| [<span data-ttu-id="54672-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="54672-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="54672-137">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="54672-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="54672-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54672-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54672-139">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="54672-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

