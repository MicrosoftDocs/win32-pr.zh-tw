---
title: WaveGetLaneIndex 函式
description: 傳回目前 wave 內目前通道的索引。
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- WaveGetLaneIndex 函式 HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991031"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="7be60-104">WaveGetLaneIndex 函式</span><span class="sxs-lookup"><span data-stu-id="7be60-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="7be60-105">傳回目前 wave 內目前通道的索引。</span><span class="sxs-lookup"><span data-stu-id="7be60-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be60-106">語法</span><span class="sxs-lookup"><span data-stu-id="7be60-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="7be60-107">參數</span><span class="sxs-lookup"><span data-stu-id="7be60-107">Parameters</span></span>

<span data-ttu-id="7be60-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="7be60-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7be60-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7be60-109">Return value</span></span>

<span data-ttu-id="7be60-110">目前的航道索引。</span><span class="sxs-lookup"><span data-stu-id="7be60-110">The current lane index.</span></span> <span data-ttu-id="7be60-111">結果會介於0和從 [**WaveGetLaneCount**](wavegetlanecount.md)傳回的結果之間。</span><span class="sxs-lookup"><span data-stu-id="7be60-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7be60-112">備註</span><span class="sxs-lookup"><span data-stu-id="7be60-112">Remarks</span></span>

<span data-ttu-id="7be60-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7be60-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="7be60-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7be60-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be60-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="7be60-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="7be60-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="7be60-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




