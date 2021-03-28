---
title: WaveActiveBitAnd 函式
description: 傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將它複製回所有使用中的通道。
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- WaveActiveBitAnd 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024333"
---
# <a name="waveactivebitand-function"></a><span data-ttu-id="4818e-104">WaveActiveBitAnd 函式</span><span class="sxs-lookup"><span data-stu-id="4818e-104">WaveActiveBitAnd function</span></span>

<span data-ttu-id="4818e-105">傳回目前 wave 中所有使用中通道的所有運算式值的位 AND，然後將它複製回所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="4818e-105">Returns the bitwise AND of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4818e-106">語法</span><span class="sxs-lookup"><span data-stu-id="4818e-106">Syntax</span></span>


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="4818e-107">參數</span><span class="sxs-lookup"><span data-stu-id="4818e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4818e-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4818e-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4818e-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="4818e-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4818e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4818e-110">Return value</span></span>

<span data-ttu-id="4818e-111">位 AND 值。</span><span class="sxs-lookup"><span data-stu-id="4818e-111">The bitwise AND value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4818e-112">備註</span><span class="sxs-lookup"><span data-stu-id="4818e-112">Remarks</span></span>

<span data-ttu-id="4818e-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="4818e-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="4818e-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4818e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4818e-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="4818e-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="4818e-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="4818e-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




