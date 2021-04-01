---
title: 'isinf (Corecrt \_ math .h) '
description: 判斷指定的值是否為無限。
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- isinf HLSL
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4df738438d62d5a66dd3b08ad769d475df562d5f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196326"
---
# <a name="isinf"></a><span data-ttu-id="6a433-104">isinf</span><span class="sxs-lookup"><span data-stu-id="6a433-104">isinf</span></span>

<span data-ttu-id="6a433-105">判斷指定的值是否為無限。</span><span class="sxs-lookup"><span data-stu-id="6a433-105">Determines if the specified value is infinite.</span></span>



| <span data-ttu-id="6a433-106">*ret* isinf (*x*) </span><span class="sxs-lookup"><span data-stu-id="6a433-106">*ret* isinf(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="6a433-107">參數</span><span class="sxs-lookup"><span data-stu-id="6a433-107">Parameters</span></span>



| <span data-ttu-id="6a433-108">項目</span><span class="sxs-lookup"><span data-stu-id="6a433-108">Item</span></span>                                                   | <span data-ttu-id="6a433-109">描述</span><span class="sxs-lookup"><span data-stu-id="6a433-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="6a433-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="6a433-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6a433-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="6a433-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6a433-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a433-112">Return Value</span></span>

<span data-ttu-id="6a433-113">傳回與輸入相同大小的值，如果 *x* 參數是 + INF 或-inf，則值設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="6a433-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is +INF or -INF.</span></span> <span data-ttu-id="6a433-114">否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="6a433-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="6a433-115">類型描述</span><span class="sxs-lookup"><span data-stu-id="6a433-115">Type Description</span></span>



| <span data-ttu-id="6a433-116">Name</span><span class="sxs-lookup"><span data-stu-id="6a433-116">Name</span></span>  | [<span data-ttu-id="6a433-117">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="6a433-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="6a433-118">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="6a433-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6a433-119">大小</span><span class="sxs-lookup"><span data-stu-id="6a433-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="6a433-120">*x*</span><span class="sxs-lookup"><span data-stu-id="6a433-120">*x*</span></span>   | <span data-ttu-id="6a433-121">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="6a433-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6a433-122">**浮動**</span><span class="sxs-lookup"><span data-stu-id="6a433-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a433-123">任意</span><span class="sxs-lookup"><span data-stu-id="6a433-123">any</span></span>      |
| <span data-ttu-id="6a433-124">*Ret*</span><span class="sxs-lookup"><span data-stu-id="6a433-124">*ret*</span></span> | <span data-ttu-id="6a433-125">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="6a433-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6a433-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="6a433-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="6a433-127">作為輸入</span><span class="sxs-lookup"><span data-stu-id="6a433-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a433-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a433-128">Minimum Shader Model</span></span>

<span data-ttu-id="6a433-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="6a433-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a433-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a433-130">Shader Model</span></span>                                                                       | <span data-ttu-id="6a433-131">支援</span><span class="sxs-lookup"><span data-stu-id="6a433-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="6a433-132">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="6a433-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6a433-133">是</span><span class="sxs-lookup"><span data-stu-id="6a433-133">yes</span></span>                 |
| [<span data-ttu-id="6a433-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="6a433-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6a433-135">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="6a433-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6a433-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a433-136">Requirements</span></span>



| <span data-ttu-id="6a433-137">需求</span><span class="sxs-lookup"><span data-stu-id="6a433-137">Requirement</span></span> | <span data-ttu-id="6a433-138">值</span><span class="sxs-lookup"><span data-stu-id="6a433-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a433-139">標頭</span><span class="sxs-lookup"><span data-stu-id="6a433-139">Header</span></span><br/> | <dl> <span data-ttu-id="6a433-140"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a433-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a433-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a433-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a433-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="6a433-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

