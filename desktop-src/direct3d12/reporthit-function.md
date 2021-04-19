---
description: 由交集著色器呼叫以報告光線交集。
ms.assetid: ''
title: ReportHit 函式
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973593"
---
# <a name="reporthit-function"></a><span data-ttu-id="6e4e1-103">ReportHit 函式</span><span class="sxs-lookup"><span data-stu-id="6e4e1-103">ReportHit function</span></span>

<span data-ttu-id="6e4e1-104">由 [交集著色器](intersection-shader.md) 呼叫以報告光線交集。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e4e1-105">Syntax</span></span>
<span data-ttu-id="6e4e1-106">此內建函式定義相當於下列函式範本：</span><span class="sxs-lookup"><span data-stu-id="6e4e1-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="6e4e1-107">參數</span><span class="sxs-lookup"><span data-stu-id="6e4e1-107">Parameters</span></span>

`THit`

<span data-ttu-id="6e4e1-108">浮點值，指定交集的參數距離。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="6e4e1-109">識別所發生點擊類型的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="6e4e1-110">這是在0-127 範圍內的使用者指定值。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="6e4e1-111">您可以使用 **HitKind** 內建的 [任何命中](any-hit-shader.md)或 [最接近的點擊](closest-hit-shader.md)著色器來讀取該值。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="6e4e1-112">指定交集屬性的使用者定義 [**交集屬性結構**](intersection-attributes.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="6e4e1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e4e1-113">Return Value</span></span>

<span data-ttu-id="6e4e1-114">**bool** 如果已接受點擊則為 True。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="6e4e1-115">如果 *賦值* 超出目前的光線間隔，或任何點擊著色器呼叫 [**IgnoreHit**](ignorehit-function.md)，則會拒絕點擊。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="6e4e1-116">目前的光線間隔是由 **RayTMin** 和 **RayTCurrent** 定義。</span><span class="sxs-lookup"><span data-stu-id="6e4e1-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e4e1-117">備註</span><span class="sxs-lookup"><span data-stu-id="6e4e1-117">Remarks</span></span>

<span data-ttu-id="6e4e1-118">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="6e4e1-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="6e4e1-119">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="6e4e1-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="6e4e1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e4e1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4e1-121">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="6e4e1-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




