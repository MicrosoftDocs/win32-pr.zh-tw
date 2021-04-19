---
description: 原始 DispatchRays 呼叫中所指定之 D3D12_DISPATCH_RAYS_DESC 結構的寬度、高度和深度值。
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972578"
---
# <a name="dispatchraysdimensions"></a><span data-ttu-id="3e9b4-103">DispatchRaysDimensions</span><span class="sxs-lookup"><span data-stu-id="3e9b4-103">DispatchRaysDimensions</span></span>

<span data-ttu-id="3e9b4-104">原始 [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)呼叫中所指定之 **D3D12 \_ 分派 \_ 放射放射 \_** 值結構的寬度、高度和深度值。</span><span class="sxs-lookup"><span data-stu-id="3e9b4-104">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e9b4-105">Syntax</span></span>

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a><span data-ttu-id="3e9b4-106">備註</span><span class="sxs-lookup"><span data-stu-id="3e9b4-106">Remarks</span></span>

<span data-ttu-id="3e9b4-107">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="3e9b4-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="3e9b4-108">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="3e9b4-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="3e9b4-109">**可呼叫著色器**</span><span class="sxs-lookup"><span data-stu-id="3e9b4-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="3e9b4-110">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="3e9b4-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="3e9b4-111">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="3e9b4-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="3e9b4-112">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="3e9b4-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="3e9b4-113">**光線產生著色器**</span><span class="sxs-lookup"><span data-stu-id="3e9b4-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="3e9b4-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e9b4-114">See also</span></span>

* [<span data-ttu-id="3e9b4-115">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="3e9b4-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
