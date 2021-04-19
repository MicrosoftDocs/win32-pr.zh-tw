---
description: 取得以 [**DispatchRaysDimensions**](dispatchraysdimensions.md) 系統值內建的寬度、高度和深度所取得的目前位置。
title: DispatchRaysIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2020
ms.locfileid: "106969946"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="a0fef-103">DispatchRaysIndex</span><span class="sxs-lookup"><span data-stu-id="a0fef-103">DispatchRaysIndex</span></span>

<span data-ttu-id="a0fef-104">取得以 [**DispatchRaysDimensions**](dispatchraysdimensions.md) 系統值內建的寬度、高度和深度所取得的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a0fef-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fef-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0fef-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="a0fef-106">備註</span><span class="sxs-lookup"><span data-stu-id="a0fef-106">Remarks</span></span>

<span data-ttu-id="a0fef-107">您可以從下列 raytracing 著色器類型呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="a0fef-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="a0fef-108">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="a0fef-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="a0fef-109">**可呼叫著色器**</span><span class="sxs-lookup"><span data-stu-id="a0fef-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="a0fef-110">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="a0fef-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="a0fef-111">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="a0fef-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="a0fef-112">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="a0fef-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="a0fef-113">**光線產生著色器**</span><span class="sxs-lookup"><span data-stu-id="a0fef-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="a0fef-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0fef-114">See also</span></span>

* [<span data-ttu-id="a0fef-115">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="a0fef-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
