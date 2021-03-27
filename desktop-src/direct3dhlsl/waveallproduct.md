---
title: WaveActiveProduct 函式
description: 將運算式的值與目前 wave 中所有使用中的車道相乘，並將其複寫回所有使用中的通道。
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- WaveActiveProduct 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842884"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="2f22e-104">WaveActiveProduct 函式</span><span class="sxs-lookup"><span data-stu-id="2f22e-104">WaveActiveProduct function</span></span>

<span data-ttu-id="2f22e-105">將運算式的值與目前 wave 中所有使用中的車道相乘，並將其複寫回所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="2f22e-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f22e-106">語法</span><span class="sxs-lookup"><span data-stu-id="2f22e-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="2f22e-107">參數</span><span class="sxs-lookup"><span data-stu-id="2f22e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f22e-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="2f22e-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="2f22e-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="2f22e-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f22e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f22e-110">Return value</span></span>

<span data-ttu-id="2f22e-111">產品值。</span><span class="sxs-lookup"><span data-stu-id="2f22e-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f22e-112">備註</span><span class="sxs-lookup"><span data-stu-id="2f22e-112">Remarks</span></span>

<span data-ttu-id="2f22e-113">作業的順序未定義。</span><span class="sxs-lookup"><span data-stu-id="2f22e-113">The order of operations is undefined.</span></span>

<span data-ttu-id="2f22e-114">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2f22e-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="2f22e-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f22e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f22e-116">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="2f22e-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="2f22e-117">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="2f22e-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




