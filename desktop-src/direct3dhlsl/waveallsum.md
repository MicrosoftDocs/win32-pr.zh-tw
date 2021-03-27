---
title: WaveActiveSum 函式
description: 加總目前 wave 中所有使用中通道的運算式值，並將其複製到目前 wave 中的所有通道。
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- WaveActiveSum 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933718"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="00cb9-104">WaveActiveSum 函式</span><span class="sxs-lookup"><span data-stu-id="00cb9-104">WaveActiveSum function</span></span>

<span data-ttu-id="00cb9-105">加總目前 wave 中所有使用中通道的運算式值，並將其複製到目前 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="00cb9-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cb9-106">語法</span><span class="sxs-lookup"><span data-stu-id="00cb9-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="00cb9-107">參數</span><span class="sxs-lookup"><span data-stu-id="00cb9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00cb9-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="00cb9-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="00cb9-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="00cb9-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00cb9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="00cb9-110">Return value</span></span>

<span data-ttu-id="00cb9-111">總和值。</span><span class="sxs-lookup"><span data-stu-id="00cb9-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00cb9-112">備註</span><span class="sxs-lookup"><span data-stu-id="00cb9-112">Remarks</span></span>

<span data-ttu-id="00cb9-113">作業的順序未定義。</span><span class="sxs-lookup"><span data-stu-id="00cb9-113">The order of operations is undefined.</span></span>

<span data-ttu-id="00cb9-114">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="00cb9-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="00cb9-115">範例</span><span class="sxs-lookup"><span data-stu-id="00cb9-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="00cb9-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00cb9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00cb9-117">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="00cb9-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="00cb9-118">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="00cb9-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




