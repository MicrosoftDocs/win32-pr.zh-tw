---
title: WaveActiveBitOr 函式
description: 傳回目前 wave 中所有使用中通道的所有運算式值位 OR，然後將其複寫回所有使用中的通道。
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- WaveActiveBitOr 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024327"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="be8ca-104">WaveActiveBitOr 函式</span><span class="sxs-lookup"><span data-stu-id="be8ca-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="be8ca-105">傳回目前 wave 中所有使用中通道的所有運算式值位 OR，然後將其複寫回所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="be8ca-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8ca-106">語法</span><span class="sxs-lookup"><span data-stu-id="be8ca-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="be8ca-107">參數</span><span class="sxs-lookup"><span data-stu-id="be8ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be8ca-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="be8ca-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="be8ca-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="be8ca-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be8ca-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="be8ca-110">Return value</span></span>

<span data-ttu-id="be8ca-111">位 OR 值。</span><span class="sxs-lookup"><span data-stu-id="be8ca-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be8ca-112">備註</span><span class="sxs-lookup"><span data-stu-id="be8ca-112">Remarks</span></span>

<span data-ttu-id="be8ca-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="be8ca-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="be8ca-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be8ca-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8ca-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="be8ca-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="be8ca-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="be8ca-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




