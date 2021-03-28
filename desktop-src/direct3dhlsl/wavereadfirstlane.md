---
title: WaveReadLaneFirst 函式
description: 傳回目前 wave （具有最小索引）之使用中通道的運算式值。
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- WaveReadLaneFirst 函式 HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971816"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="7ea6b-104">WaveReadLaneFirst 函式</span><span class="sxs-lookup"><span data-stu-id="7ea6b-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="7ea6b-105">傳回目前 wave （具有最小索引）之使用中通道的運算式值。</span><span class="sxs-lookup"><span data-stu-id="7ea6b-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea6b-106">語法</span><span class="sxs-lookup"><span data-stu-id="7ea6b-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="7ea6b-107">參數</span><span class="sxs-lookup"><span data-stu-id="7ea6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea6b-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="7ea6b-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea6b-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="7ea6b-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea6b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ea6b-110">Return value</span></span>

<span data-ttu-id="7ea6b-111">產生的值會在 wave 之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="7ea6b-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea6b-112">備註</span><span class="sxs-lookup"><span data-stu-id="7ea6b-112">Remarks</span></span>

<span data-ttu-id="7ea6b-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7ea6b-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="7ea6b-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ea6b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea6b-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="7ea6b-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="7ea6b-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="7ea6b-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




