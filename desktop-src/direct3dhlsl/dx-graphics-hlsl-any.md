---
title: 任意
description: 判斷指定值的任何元件是否為非零。
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- 任何 HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971796"
---
# <a name="any"></a><span data-ttu-id="54338-104">任意</span><span class="sxs-lookup"><span data-stu-id="54338-104">any</span></span>

<span data-ttu-id="54338-105">判斷指定值的任何元件是否為非零。</span><span class="sxs-lookup"><span data-stu-id="54338-105">Determines if any components of the specified value are non-zero.</span></span>



| <span data-ttu-id="54338-106">*ret* 任何 (*x*) </span><span class="sxs-lookup"><span data-stu-id="54338-106">*ret* any(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="54338-107">參數</span><span class="sxs-lookup"><span data-stu-id="54338-107">Parameters</span></span>



| <span data-ttu-id="54338-108">項目</span><span class="sxs-lookup"><span data-stu-id="54338-108">Item</span></span>                                                   | <span data-ttu-id="54338-109">描述</span><span class="sxs-lookup"><span data-stu-id="54338-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="54338-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="54338-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="54338-111">\[在 \] 指定的值中。</span><span class="sxs-lookup"><span data-stu-id="54338-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="54338-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="54338-112">Return Value</span></span>

<span data-ttu-id="54338-113">如果 *x* 參數的任何元件為非零，則 **為 True** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="54338-113">**True** if any components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="54338-114">備註</span><span class="sxs-lookup"><span data-stu-id="54338-114">Remarks</span></span>

<span data-ttu-id="54338-115">此函數類似于 [**all**](dx-graphics-hlsl-all.md) HLSL 內建函式。</span><span class="sxs-lookup"><span data-stu-id="54338-115">This function is similar to the [**all**](dx-graphics-hlsl-all.md) HLSL intrinsic function.</span></span> <span data-ttu-id="54338-116">**Any** 函式會判斷指定值的任何元件是否為非零，而 **all** 函數會判斷指定值的所有元件是否為非零。</span><span class="sxs-lookup"><span data-stu-id="54338-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="54338-117">類型描述</span><span class="sxs-lookup"><span data-stu-id="54338-117">Type Description</span></span>



| <span data-ttu-id="54338-118">Name</span><span class="sxs-lookup"><span data-stu-id="54338-118">Name</span></span>  | [<span data-ttu-id="54338-119">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="54338-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="54338-120">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="54338-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="54338-121">大小</span><span class="sxs-lookup"><span data-stu-id="54338-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="54338-122">*x*</span><span class="sxs-lookup"><span data-stu-id="54338-122">*x*</span></span>   | <span data-ttu-id="54338-123">純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣**</span><span class="sxs-lookup"><span data-stu-id="54338-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="54338-124">[**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54338-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="54338-125">任意</span><span class="sxs-lookup"><span data-stu-id="54338-125">any</span></span>  |
| <span data-ttu-id="54338-126">*Ret*</span><span class="sxs-lookup"><span data-stu-id="54338-126">*ret*</span></span> | [<span data-ttu-id="54338-127">**純量 (scalar)**</span><span class="sxs-lookup"><span data-stu-id="54338-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="54338-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="54338-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="54338-129">1</span><span class="sxs-lookup"><span data-stu-id="54338-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54338-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="54338-130">Minimum Shader Model</span></span>

<span data-ttu-id="54338-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="54338-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="54338-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="54338-132">Shader Model</span></span>                                                                       | <span data-ttu-id="54338-133">支援</span><span class="sxs-lookup"><span data-stu-id="54338-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="54338-134">[著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="54338-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="54338-135">是</span><span class="sxs-lookup"><span data-stu-id="54338-135">yes</span></span>                   |
| [<span data-ttu-id="54338-136">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="54338-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="54338-137">vs \_ 1 \_ 1 和 ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="54338-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="54338-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54338-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54338-139">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="54338-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

