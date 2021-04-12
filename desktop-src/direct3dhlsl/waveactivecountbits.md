---
title: WaveActiveCountBits 函式
description: 計算在目前 wave 的所有作用中通道上評估為 true 的布林值變數數目，並將結果複製到 wave 中的所有通道。
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- WaveActiveCountBits 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2020
ms.locfileid: "104316867"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="72f52-104">WaveActiveCountBits 函式</span><span class="sxs-lookup"><span data-stu-id="72f52-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="72f52-105">計算在目前 wave 的所有作用中通道上評估為 true 的布林值變數數目，並將結果複製到 wave 中的所有通道。</span><span class="sxs-lookup"><span data-stu-id="72f52-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f52-106">語法</span><span class="sxs-lookup"><span data-stu-id="72f52-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="72f52-107">參數</span><span class="sxs-lookup"><span data-stu-id="72f52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f52-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="72f52-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="72f52-109">要評估的布林值變數。</span><span class="sxs-lookup"><span data-stu-id="72f52-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="72f52-110">提供明確的 true 布林值會傳回使用中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="72f52-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f52-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="72f52-111">Return value</span></span>

<span data-ttu-id="72f52-112">在目前 wave 的所有作用中通道上評估為 true 的數目。</span><span class="sxs-lookup"><span data-stu-id="72f52-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f52-113">備註</span><span class="sxs-lookup"><span data-stu-id="72f52-113">Remarks</span></span>

<span data-ttu-id="72f52-114">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="72f52-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="72f52-115">範例</span><span class="sxs-lookup"><span data-stu-id="72f52-115">Examples</span></span>

<span data-ttu-id="72f52-116">這可以比完整的 WaveActiveSum 更有效率地執行，如下列範例所述：</span><span class="sxs-lookup"><span data-stu-id="72f52-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="72f52-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72f52-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f52-118">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="72f52-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="72f52-119">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="72f52-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




