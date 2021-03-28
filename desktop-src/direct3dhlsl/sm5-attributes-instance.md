---
title: instance
description: 使用這個屬性來建立幾何著色器的實例。
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022839"
---
# <a name="instance"></a><span data-ttu-id="cba5e-103">instance</span><span class="sxs-lookup"><span data-stu-id="cba5e-103">instance</span></span>

<span data-ttu-id="cba5e-104">使用這個屬性來建立幾何著色器的實例。</span><span class="sxs-lookup"><span data-stu-id="cba5e-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="cba5e-105">備註</span><span class="sxs-lookup"><span data-stu-id="cba5e-105">Remarks</span></span>

<span data-ttu-id="cba5e-106">X 是一個整數索引，表示要針對每個繪製的專案執行的實例數目 (例如，針對每個三角形) 。</span><span class="sxs-lookup"><span data-stu-id="cba5e-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="cba5e-107">使用這個屬性時，請使用 [SV \_ GSInstanceID](sv-gsinstanceid.md) 來識別正在執行之幾何著色器的實例。</span><span class="sxs-lookup"><span data-stu-id="cba5e-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="cba5e-108">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="cba5e-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cba5e-109">頂點</span><span class="sxs-lookup"><span data-stu-id="cba5e-109">Vertex</span></span> | <span data-ttu-id="cba5e-110">船體</span><span class="sxs-lookup"><span data-stu-id="cba5e-110">Hull</span></span> | <span data-ttu-id="cba5e-111">網域</span><span class="sxs-lookup"><span data-stu-id="cba5e-111">Domain</span></span> | <span data-ttu-id="cba5e-112">幾何</span><span class="sxs-lookup"><span data-stu-id="cba5e-112">Geometry</span></span> | <span data-ttu-id="cba5e-113">像素</span><span class="sxs-lookup"><span data-stu-id="cba5e-113">Pixel</span></span> | <span data-ttu-id="cba5e-114">計算</span><span class="sxs-lookup"><span data-stu-id="cba5e-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="cba5e-115">x</span><span class="sxs-lookup"><span data-stu-id="cba5e-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="cba5e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="cba5e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba5e-117">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="cba5e-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="cba5e-118">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="cba5e-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




