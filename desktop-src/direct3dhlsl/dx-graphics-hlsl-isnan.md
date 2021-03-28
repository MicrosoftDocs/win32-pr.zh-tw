---
title: 'isnan (Corecrt \_ math .h) '
description: 判斷指定的值是否為 NAN 或 QNAN。
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- isnan HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9f4549b6a142f5bf6011cdfb144de92efde64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035424"
---
# <a name="isnan"></a><span data-ttu-id="f2ab6-104">isnan</span><span class="sxs-lookup"><span data-stu-id="f2ab6-104">isnan</span></span>

<span data-ttu-id="f2ab6-105">判斷指定的值是否為 NAN 或 QNAN。</span><span class="sxs-lookup"><span data-stu-id="f2ab6-105">Determines if the specified value is NAN or QNAN.</span></span>



| <span data-ttu-id="f2ab6-106">*ret* isnan (*x*) </span><span class="sxs-lookup"><span data-stu-id="f2ab6-106">*ret* isnan(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="f2ab6-107">參數</span><span class="sxs-lookup"><span data-stu-id="f2ab6-107">Parameters</span></span>



| <span data-ttu-id="f2ab6-108">項目</span><span class="sxs-lookup"><span data-stu-id="f2ab6-108">Item</span></span>                                                   | <span data-ttu-id="f2ab6-109">描述</span><span class="sxs-lookup"><span data-stu-id="f2ab6-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f2ab6-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="f2ab6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f2ab6-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="f2ab6-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f2ab6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2ab6-112">Return Value</span></span>

<span data-ttu-id="f2ab6-113">傳回與輸入相同大小的值，如果 *x* 參數是 NAN 或 QNAN，則值設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="f2ab6-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN.</span></span> <span data-ttu-id="f2ab6-114">否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="f2ab6-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="f2ab6-115">類型描述</span><span class="sxs-lookup"><span data-stu-id="f2ab6-115">Type Description</span></span>



| <span data-ttu-id="f2ab6-116">Name</span><span class="sxs-lookup"><span data-stu-id="f2ab6-116">Name</span></span>  | [<span data-ttu-id="f2ab6-117">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f2ab6-118">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f2ab6-119">大小</span><span class="sxs-lookup"><span data-stu-id="f2ab6-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="f2ab6-120">*x*</span><span class="sxs-lookup"><span data-stu-id="f2ab6-120">*x*</span></span>   | <span data-ttu-id="f2ab6-121">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f2ab6-122">**浮動**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f2ab6-123">任意</span><span class="sxs-lookup"><span data-stu-id="f2ab6-123">any</span></span>      |
| <span data-ttu-id="f2ab6-124">*Ret*</span><span class="sxs-lookup"><span data-stu-id="f2ab6-124">*ret*</span></span> | <span data-ttu-id="f2ab6-125">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f2ab6-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="f2ab6-127">作為輸入</span><span class="sxs-lookup"><span data-stu-id="f2ab6-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f2ab6-128">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2ab6-128">Minimum Shader Model</span></span>

<span data-ttu-id="f2ab6-129">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="f2ab6-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f2ab6-130">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2ab6-130">Shader Model</span></span>                                                                       | <span data-ttu-id="f2ab6-131">支援</span><span class="sxs-lookup"><span data-stu-id="f2ab6-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f2ab6-132">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="f2ab6-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f2ab6-133">是</span><span class="sxs-lookup"><span data-stu-id="f2ab6-133">yes</span></span>                 |
| [<span data-ttu-id="f2ab6-134">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="f2ab6-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f2ab6-135">是 (\_ \_ 只有) 的 vs 1</span><span class="sxs-lookup"><span data-stu-id="f2ab6-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f2ab6-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2ab6-136">Requirements</span></span>



| <span data-ttu-id="f2ab6-137">需求</span><span class="sxs-lookup"><span data-stu-id="f2ab6-137">Requirement</span></span> | <span data-ttu-id="f2ab6-138">值</span><span class="sxs-lookup"><span data-stu-id="f2ab6-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ab6-139">標頭</span><span class="sxs-lookup"><span data-stu-id="f2ab6-139">Header</span></span><br/> | <dl> <span data-ttu-id="f2ab6-140"><dt>Corecrt \_ math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ab6-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ab6-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2ab6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ab6-142">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="f2ab6-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

