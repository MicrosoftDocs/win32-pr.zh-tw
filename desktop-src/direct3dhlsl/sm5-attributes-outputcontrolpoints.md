---
title: outputcontrolpoints
description: 定義將在輪廓著色器中建立的每個執行緒)  (的輸出控制點數目。
ms.assetid: 0bd7e5af-29b0-4814-ab96-06e15cc390ff
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 68f933293f86a368bf333ec6d18b909b4d2e5bbd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679156"
---
# <a name="outputcontrolpoints"></a><span data-ttu-id="35757-103">outputcontrolpoints</span><span class="sxs-lookup"><span data-stu-id="35757-103">outputcontrolpoints</span></span>

<span data-ttu-id="35757-104">定義將在輪廓著色器中建立的每個執行緒)  (的輸出控制點數目。</span><span class="sxs-lookup"><span data-stu-id="35757-104">Defines the number of output control points (per thread) that will be created in the hull shader.</span></span>


```
outputcontrolpoints(X)
```



## <a name="remarks"></a><span data-ttu-id="35757-105">備註</span><span class="sxs-lookup"><span data-stu-id="35757-105">Remarks</span></span>

<span data-ttu-id="35757-106">這將會是執行主要函式的次數。</span><span class="sxs-lookup"><span data-stu-id="35757-106">This will be the number of times the main function will be executed.</span></span>

<span data-ttu-id="35757-107">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="35757-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="35757-108">頂點</span><span class="sxs-lookup"><span data-stu-id="35757-108">Vertex</span></span> | <span data-ttu-id="35757-109">船體</span><span class="sxs-lookup"><span data-stu-id="35757-109">Hull</span></span> | <span data-ttu-id="35757-110">網域</span><span class="sxs-lookup"><span data-stu-id="35757-110">Domain</span></span> | <span data-ttu-id="35757-111">幾何</span><span class="sxs-lookup"><span data-stu-id="35757-111">Geometry</span></span> | <span data-ttu-id="35757-112">像素</span><span class="sxs-lookup"><span data-stu-id="35757-112">Pixel</span></span> | <span data-ttu-id="35757-113">計算</span><span class="sxs-lookup"><span data-stu-id="35757-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="35757-114">x</span><span class="sxs-lookup"><span data-stu-id="35757-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="35757-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="35757-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35757-116">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="35757-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="35757-117">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="35757-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




