---
title: 變為
description: 調換指定的輸入矩陣。
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- 換位 HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375536"
---
# <a name="transpose"></a><span data-ttu-id="c93dc-104">變為</span><span class="sxs-lookup"><span data-stu-id="c93dc-104">transpose</span></span>

<span data-ttu-id="c93dc-105">調換指定的輸入矩陣。</span><span class="sxs-lookup"><span data-stu-id="c93dc-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="c93dc-106">ret 變換 (*x*) </span><span class="sxs-lookup"><span data-stu-id="c93dc-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="c93dc-107">參數</span><span class="sxs-lookup"><span data-stu-id="c93dc-107">Parameters</span></span>



| <span data-ttu-id="c93dc-108">項目</span><span class="sxs-lookup"><span data-stu-id="c93dc-108">Item</span></span>                                                   | <span data-ttu-id="c93dc-109">描述</span><span class="sxs-lookup"><span data-stu-id="c93dc-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="c93dc-110"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="c93dc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c93dc-111">\[在 \] 指定的矩陣中。</span><span class="sxs-lookup"><span data-stu-id="c93dc-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c93dc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c93dc-112">Return Value</span></span>

<span data-ttu-id="c93dc-113">*X* 參數的已轉換值。</span><span class="sxs-lookup"><span data-stu-id="c93dc-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93dc-114">備註</span><span class="sxs-lookup"><span data-stu-id="c93dc-114">Remarks</span></span>

<span data-ttu-id="c93dc-115">如果來源矩陣的維度是 rows 資料 *行，則* 產生的矩陣會是資料 *行* 資料 *列*。</span><span class="sxs-lookup"><span data-stu-id="c93dc-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="c93dc-116">類型描述</span><span class="sxs-lookup"><span data-stu-id="c93dc-116">Type Description</span></span>



| <span data-ttu-id="c93dc-117">名稱</span><span class="sxs-lookup"><span data-stu-id="c93dc-117">Name</span></span> | [<span data-ttu-id="c93dc-118">**範本類型**</span><span class="sxs-lookup"><span data-stu-id="c93dc-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="c93dc-119">**元件類型**</span><span class="sxs-lookup"><span data-stu-id="c93dc-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="c93dc-120">大小</span><span class="sxs-lookup"><span data-stu-id="c93dc-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c93dc-121">*x*</span><span class="sxs-lookup"><span data-stu-id="c93dc-121">*x*</span></span>  | [<span data-ttu-id="c93dc-122">**矩陣**</span><span class="sxs-lookup"><span data-stu-id="c93dc-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c93dc-123">[**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c93dc-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c93dc-124">任意</span><span class="sxs-lookup"><span data-stu-id="c93dc-124">any</span></span>                                                                                    |
| <span data-ttu-id="c93dc-125">Ret</span><span class="sxs-lookup"><span data-stu-id="c93dc-125">ret</span></span>  | [<span data-ttu-id="c93dc-126">**矩陣**</span><span class="sxs-lookup"><span data-stu-id="c93dc-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c93dc-127">[**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c93dc-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="c93dc-128">rows = 與輸入 *x* 相同數目的資料行，資料行 = 與輸入 *x* 相同的資料列數目</span><span class="sxs-lookup"><span data-stu-id="c93dc-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c93dc-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c93dc-129">Minimum Shader Model</span></span>

<span data-ttu-id="c93dc-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="c93dc-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c93dc-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c93dc-131">Shader Model</span></span>                                                                       | <span data-ttu-id="c93dc-132">支援</span><span class="sxs-lookup"><span data-stu-id="c93dc-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c93dc-133">[著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="c93dc-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="c93dc-134">是</span><span class="sxs-lookup"><span data-stu-id="c93dc-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c93dc-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c93dc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93dc-136">**(DirectX HLSL) 內建函式**</span><span class="sxs-lookup"><span data-stu-id="c93dc-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

