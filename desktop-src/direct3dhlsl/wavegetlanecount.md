---
title: WaveGetLaneCount 函式
description: 傳回 wave 在此架構上的航道數目。
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount 函式 HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383285"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="87133-104">WaveGetLaneCount 函式</span><span class="sxs-lookup"><span data-stu-id="87133-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="87133-105">傳回 wave 在此架構上的航道數目。</span><span class="sxs-lookup"><span data-stu-id="87133-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="87133-106">語法</span><span class="sxs-lookup"><span data-stu-id="87133-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="87133-107">參數</span><span class="sxs-lookup"><span data-stu-id="87133-107">Parameters</span></span>

<span data-ttu-id="87133-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="87133-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87133-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="87133-109">Return value</span></span>

<span data-ttu-id="87133-110">結果會介於4到128之間，並且包含所有的波浪：作用中、非作用中和/或 helper 通道。</span><span class="sxs-lookup"><span data-stu-id="87133-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="87133-111">從這個函式傳回的結果可能會因為驅動程式的執行而有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="87133-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="87133-112">備註</span><span class="sxs-lookup"><span data-stu-id="87133-112">Remarks</span></span>

<span data-ttu-id="87133-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="87133-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="87133-114">範例</span><span class="sxs-lookup"><span data-stu-id="87133-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="87133-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87133-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87133-116">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="87133-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="87133-117">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="87133-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




