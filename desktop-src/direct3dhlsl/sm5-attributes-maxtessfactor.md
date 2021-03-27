---
title: maxtessfactor
description: 指出輪廓著色器針對任何鑲嵌因數傳回的最大值。
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841679"
---
# <a name="maxtessfactor"></a><span data-ttu-id="9cc22-103">maxtessfactor</span><span class="sxs-lookup"><span data-stu-id="9cc22-103">maxtessfactor</span></span>

<span data-ttu-id="9cc22-104">指出輪廓著色器針對任何鑲嵌因數傳回的最大值。</span><span class="sxs-lookup"><span data-stu-id="9cc22-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="9cc22-105">備註</span><span class="sxs-lookup"><span data-stu-id="9cc22-105">Remarks</span></span>

<span data-ttu-id="9cc22-106">這個屬性會在所要求的鑲嵌量上放置上限，以協助驅動程式判斷鑲嵌所需的資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="9cc22-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="9cc22-107">下列著色器類型支援此屬性：</span><span class="sxs-lookup"><span data-stu-id="9cc22-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9cc22-108">頂點</span><span class="sxs-lookup"><span data-stu-id="9cc22-108">Vertex</span></span> | <span data-ttu-id="9cc22-109">船體</span><span class="sxs-lookup"><span data-stu-id="9cc22-109">Hull</span></span> | <span data-ttu-id="9cc22-110">網域</span><span class="sxs-lookup"><span data-stu-id="9cc22-110">Domain</span></span> | <span data-ttu-id="9cc22-111">幾何</span><span class="sxs-lookup"><span data-stu-id="9cc22-111">Geometry</span></span> | <span data-ttu-id="9cc22-112">像素</span><span class="sxs-lookup"><span data-stu-id="9cc22-112">Pixel</span></span> | <span data-ttu-id="9cc22-113">計算</span><span class="sxs-lookup"><span data-stu-id="9cc22-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9cc22-114">x</span><span class="sxs-lookup"><span data-stu-id="9cc22-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="9cc22-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cc22-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc22-116">著色器模型5屬性</span><span class="sxs-lookup"><span data-stu-id="9cc22-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="9cc22-117">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="9cc22-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




