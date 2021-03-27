---
title: 分割
description: 定義要在輪廓著色器中使用的 tesselation 配置。
ms.assetid: 29dc4abb-4d29-4538-8680-a4fcbfd8235b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bf0744481a123998b64693d669e9cb7255599f8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841676"
---
# <a name="partitioning"></a><span data-ttu-id="a6581-103">分割</span><span class="sxs-lookup"><span data-stu-id="a6581-103">partitioning</span></span>

<span data-ttu-id="a6581-104">定義要在輪廓著色器中使用的 tesselation 配置。</span><span class="sxs-lookup"><span data-stu-id="a6581-104">Defines the tesselation scheme to be used in the hull shader.</span></span>


```
partitioning(X)    
```



## <a name="remarks"></a><span data-ttu-id="a6581-105">備註</span><span class="sxs-lookup"><span data-stu-id="a6581-105">Remarks</span></span>

<span data-ttu-id="a6581-106">可以是 **整數**、 **小數 \_ 偶數**、 **小數 \_ 奇數** 或 **pow2**。</span><span class="sxs-lookup"><span data-stu-id="a6581-106">Can be **integer**, **fractional\_even**, **fractional\_odd**, or **pow2**.</span></span>

<span data-ttu-id="a6581-107">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="a6581-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a6581-108">頂點</span><span class="sxs-lookup"><span data-stu-id="a6581-108">Vertex</span></span> | <span data-ttu-id="a6581-109">船體</span><span class="sxs-lookup"><span data-stu-id="a6581-109">Hull</span></span> | <span data-ttu-id="a6581-110">網域</span><span class="sxs-lookup"><span data-stu-id="a6581-110">Domain</span></span> | <span data-ttu-id="a6581-111">幾何</span><span class="sxs-lookup"><span data-stu-id="a6581-111">Geometry</span></span> | <span data-ttu-id="a6581-112">像素</span><span class="sxs-lookup"><span data-stu-id="a6581-112">Pixel</span></span> | <span data-ttu-id="a6581-113">計算</span><span class="sxs-lookup"><span data-stu-id="a6581-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="a6581-114">x</span><span class="sxs-lookup"><span data-stu-id="a6581-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="a6581-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6581-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6581-116">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="a6581-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6581-117">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a6581-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




