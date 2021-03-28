---
title: earlydepthstencil
description: 在著色器執行之前強制進行深度樣板測試。
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990815"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="2f160-103">earlydepthstencil</span><span class="sxs-lookup"><span data-stu-id="2f160-103">earlydepthstencil</span></span>

<span data-ttu-id="2f160-104">在著色器執行之前強制進行深度樣板測試。</span><span class="sxs-lookup"><span data-stu-id="2f160-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="2f160-105">備註</span><span class="sxs-lookup"><span data-stu-id="2f160-105">Remarks</span></span>

<span data-ttu-id="2f160-106">深度樣板測試通常是在圖元著色器的圖元處理期間進行。</span><span class="sxs-lookup"><span data-stu-id="2f160-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="2f160-107">強制較早深度樣板測試會導致在著色器執行之前完成測試;其目的是要藉由剔除/減少/避免不必要的圖元處理來改善每個圖元的效能。</span><span class="sxs-lookup"><span data-stu-id="2f160-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="2f160-108">應用程式可以藉由提供屬性來強制進行早期深度樣板測試，或者硬體可能會執行較早的深度樣板測試，但前提是不會寫入任何深度值，而且不會在著色器中執行任何未排序的存取作業作為優化。</span><span class="sxs-lookup"><span data-stu-id="2f160-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="2f160-109">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="2f160-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2f160-110">頂點</span><span class="sxs-lookup"><span data-stu-id="2f160-110">Vertex</span></span> | <span data-ttu-id="2f160-111">船體</span><span class="sxs-lookup"><span data-stu-id="2f160-111">Hull</span></span> | <span data-ttu-id="2f160-112">網域</span><span class="sxs-lookup"><span data-stu-id="2f160-112">Domain</span></span> | <span data-ttu-id="2f160-113">幾何</span><span class="sxs-lookup"><span data-stu-id="2f160-113">Geometry</span></span> | <span data-ttu-id="2f160-114">像素</span><span class="sxs-lookup"><span data-stu-id="2f160-114">Pixel</span></span> | <span data-ttu-id="2f160-115">計算</span><span class="sxs-lookup"><span data-stu-id="2f160-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2f160-116">x</span><span class="sxs-lookup"><span data-stu-id="2f160-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="2f160-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f160-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f160-118">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="2f160-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f160-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2f160-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




