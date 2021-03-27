---
title: 行列 式
description: 傳回指定之浮點數、正方形矩陣的行列式。
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- 行列式 HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971729"
---
# <a name="determinant"></a><span data-ttu-id="d0ed0-104">行列 式</span><span class="sxs-lookup"><span data-stu-id="d0ed0-104">determinant</span></span>

<span data-ttu-id="d0ed0-105">傳回指定之浮點數、正方形矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="d0ed0-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="d0ed0-106">*ret* 行列式 (*m*) </span><span class="sxs-lookup"><span data-stu-id="d0ed0-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d0ed0-107">參數</span><span class="sxs-lookup"><span data-stu-id="d0ed0-107">Parameters</span></span>



| <span data-ttu-id="d0ed0-108">項目</span><span class="sxs-lookup"><span data-stu-id="d0ed0-108">Item</span></span>                                                   | <span data-ttu-id="d0ed0-109">描述</span><span class="sxs-lookup"><span data-stu-id="d0ed0-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d0ed0-110"><span id="m"></span><span id="M"></span>*m*</span><span class="sxs-lookup"><span data-stu-id="d0ed0-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="d0ed0-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="d0ed0-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d0ed0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0ed0-112">Return Value</span></span>

<span data-ttu-id="d0ed0-113">浮點數的純量值，表示 *m* 參數的行列式。</span><span class="sxs-lookup"><span data-stu-id="d0ed0-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d0ed0-114">類型描述</span><span class="sxs-lookup"><span data-stu-id="d0ed0-114">Type Description</span></span>



| <span data-ttu-id="d0ed0-115">Name</span><span class="sxs-lookup"><span data-stu-id="d0ed0-115">Name</span></span>  | [<span data-ttu-id="d0ed0-116">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d0ed0-117">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d0ed0-118">大小</span><span class="sxs-lookup"><span data-stu-id="d0ed0-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="d0ed0-119">*m*</span><span class="sxs-lookup"><span data-stu-id="d0ed0-119">*m*</span></span>   | [<span data-ttu-id="d0ed0-120">**矩陣**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0ed0-121">**浮動**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0ed0-122">任何 (的資料列數目 = 資料行數目) </span><span class="sxs-lookup"><span data-stu-id="d0ed0-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="d0ed0-123">*Ret*</span><span class="sxs-lookup"><span data-stu-id="d0ed0-123">*ret*</span></span> | [<span data-ttu-id="d0ed0-124">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d0ed0-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d0ed0-126">1</span><span class="sxs-lookup"><span data-stu-id="d0ed0-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d0ed0-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d0ed0-127">Minimum Shader Model</span></span>

<span data-ttu-id="d0ed0-128">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d0ed0-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d0ed0-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d0ed0-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d0ed0-130">支援</span><span class="sxs-lookup"><span data-stu-id="d0ed0-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="d0ed0-131">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="d0ed0-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d0ed0-132">是</span><span class="sxs-lookup"><span data-stu-id="d0ed0-132">yes</span></span>                   |
| [<span data-ttu-id="d0ed0-133">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d0ed0-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d0ed0-134">vs \_ 1 \_ 1 和 ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d0ed0-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d0ed0-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0ed0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ed0-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="d0ed0-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

