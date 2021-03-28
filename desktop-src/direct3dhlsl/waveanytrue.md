---
title: WaveActiveAnyTrue 函式
description: 如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- WaveActiveAnyTrue 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991030"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="d9bcb-104">WaveActiveAnyTrue 函式</span><span class="sxs-lookup"><span data-stu-id="d9bcb-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="d9bcb-105">如果目前 wave 的任何使用中通道中的運算式為 true，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="d9bcb-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bcb-106">語法</span><span class="sxs-lookup"><span data-stu-id="d9bcb-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="d9bcb-107">參數</span><span class="sxs-lookup"><span data-stu-id="d9bcb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9bcb-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="d9bcb-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="d9bcb-109">要評估的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="d9bcb-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9bcb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9bcb-110">Return value</span></span>

<span data-ttu-id="d9bcb-111">如果任何通道中的運算式為 true，則為 true。</span><span class="sxs-lookup"><span data-stu-id="d9bcb-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bcb-112">備註</span><span class="sxs-lookup"><span data-stu-id="d9bcb-112">Remarks</span></span>

<span data-ttu-id="d9bcb-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d9bcb-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="d9bcb-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9bcb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9bcb-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="d9bcb-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="d9bcb-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="d9bcb-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




