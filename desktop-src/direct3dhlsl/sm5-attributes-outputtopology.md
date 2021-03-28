---
title: outputtopology
description: 定義鑲嵌的輸出基本類型。
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932819"
---
# <a name="outputtopology"></a><span data-ttu-id="9580d-103">outputtopology</span><span class="sxs-lookup"><span data-stu-id="9580d-103">outputtopology</span></span>

<span data-ttu-id="9580d-104">定義鑲嵌的輸出基本類型。</span><span class="sxs-lookup"><span data-stu-id="9580d-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="9580d-105">備註</span><span class="sxs-lookup"><span data-stu-id="9580d-105">Remarks</span></span>

<span data-ttu-id="9580d-106">X 必須是 [**點**](dx-graphics-hlsl-geometry-shader.md)、 **線條**、 **三角形的 \_ cw** 或 **三角形 \_ ccw** ，而且必須在引號內。</span><span class="sxs-lookup"><span data-stu-id="9580d-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="9580d-107">以下是此屬性的有效選項：</span><span class="sxs-lookup"><span data-stu-id="9580d-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="9580d-108">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="9580d-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9580d-109">頂點</span><span class="sxs-lookup"><span data-stu-id="9580d-109">Vertex</span></span> | <span data-ttu-id="9580d-110">船體</span><span class="sxs-lookup"><span data-stu-id="9580d-110">Hull</span></span> | <span data-ttu-id="9580d-111">網域</span><span class="sxs-lookup"><span data-stu-id="9580d-111">Domain</span></span> | <span data-ttu-id="9580d-112">幾何</span><span class="sxs-lookup"><span data-stu-id="9580d-112">Geometry</span></span> | <span data-ttu-id="9580d-113">像素</span><span class="sxs-lookup"><span data-stu-id="9580d-113">Pixel</span></span> | <span data-ttu-id="9580d-114">計算</span><span class="sxs-lookup"><span data-stu-id="9580d-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9580d-115">x</span><span class="sxs-lookup"><span data-stu-id="9580d-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="9580d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9580d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9580d-117">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="9580d-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="9580d-118">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9580d-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




