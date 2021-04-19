---
title: 'Raytracing HLSL 結構 (Direct3D 12) '
description: 下列 HLSL 結構支援 Direct3D 12 raytracing 管線。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c48ad6bac76e200587ec76d42dfa9c86b23cd23
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "106968266"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a><span data-ttu-id="f6df5-103">Raytracing HLSL 結構 (Direct3D 12) </span><span class="sxs-lookup"><span data-stu-id="f6df5-103">Raytracing HLSL structures (Direct3D 12)</span></span>

<span data-ttu-id="f6df5-104">下列 HLSL 結構支援 Direct3D 12 raytracing 管線。</span><span class="sxs-lookup"><span data-stu-id="f6df5-104">The following HLSL structures support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6df5-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f6df5-105">In this section</span></span>



| <span data-ttu-id="f6df5-106">主題</span><span class="sxs-lookup"><span data-stu-id="f6df5-106">Topic</span></span>                                                                                                       | <span data-ttu-id="f6df5-107">描述</span><span class="sxs-lookup"><span data-stu-id="f6df5-107">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6df5-108">**呼叫參數結構**</span><span class="sxs-lookup"><span data-stu-id="f6df5-108">**Call Parameter Structure**</span></span>](call-parameter-structure.md)<br/>                              | <span data-ttu-id="f6df5-109">以 inout 引數形式提供給 CallShader 呼叫的使用者定義結構，以及可呼叫著色器的 inout 參數。</span><span class="sxs-lookup"><span data-stu-id="f6df5-109">A user-defined structure provided as an inout argument to a CallShader call, and as an inout parameter for the callable shader.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f6df5-110">**交集屬性結構**</span><span class="sxs-lookup"><span data-stu-id="f6df5-110">**Intersection Attributes Structure**</span></span>](intersection-attributes.md)<br/>                              | <span data-ttu-id="f6df5-111">在 [**TraceRay**](traceray-function.md) 呼叫中提供作為 inout 引數的使用者定義結構，以及可存取光線承載之著色器類型中的 inout 參數。</span><span class="sxs-lookup"><span data-stu-id="f6df5-111">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f6df5-112">**光線承載結構**</span><span class="sxs-lookup"><span data-stu-id="f6df5-112">**Ray Payload Structure**</span></span>](ray-payload.md)<br/>                              | <span data-ttu-id="f6df5-113">在 [**TraceRay**](traceray-function.md) 呼叫中提供作為 inout 引數的使用者定義結構，以及可存取光線承載之著色器類型中的 inout 參數。</span><span class="sxs-lookup"><span data-stu-id="f6df5-113">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f6df5-114">**RayDesc 結構**</span><span class="sxs-lookup"><span data-stu-id="f6df5-114">**RayDesc Structure**</span></span>](raydesc.md)<br/>                              | <span data-ttu-id="f6df5-115">傳遞至 [**TraceRay**](traceray-function.md) 函式的旗標，可覆寫透明度、剔除和早期輸出行為。</span><span class="sxs-lookup"><span data-stu-id="f6df5-115">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span><br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a><span data-ttu-id="f6df5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6df5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6df5-117">核心參考</span><span class="sxs-lookup"><span data-stu-id="f6df5-117">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="f6df5-118">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="f6df5-118">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





