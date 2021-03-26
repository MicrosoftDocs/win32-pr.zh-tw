---
title: WaveIsFirstLane 函式
description: 只針對目前 wave 中具有最小索引的使用中通道傳回 true。
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane 函式 HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316777"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="2b34e-104">WaveIsFirstLane 函式</span><span class="sxs-lookup"><span data-stu-id="2b34e-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="2b34e-105">只針對目前 wave 中具有最小索引的使用中通道傳回 true。</span><span class="sxs-lookup"><span data-stu-id="2b34e-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b34e-106">語法</span><span class="sxs-lookup"><span data-stu-id="2b34e-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="2b34e-107">參數</span><span class="sxs-lookup"><span data-stu-id="2b34e-107">Parameters</span></span>

<span data-ttu-id="2b34e-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="2b34e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b34e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b34e-109">Return value</span></span>

<span data-ttu-id="2b34e-110">僅適用于目前 wave 中具有最小索引的現用通道。</span><span class="sxs-lookup"><span data-stu-id="2b34e-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b34e-111">備註</span><span class="sxs-lookup"><span data-stu-id="2b34e-111">Remarks</span></span>

<span data-ttu-id="2b34e-112">您可以使用此函式來識別每個 wave 只執行一次的作業。</span><span class="sxs-lookup"><span data-stu-id="2b34e-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="2b34e-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2b34e-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="2b34e-114">範例</span><span class="sxs-lookup"><span data-stu-id="2b34e-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="2b34e-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b34e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b34e-116">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="2b34e-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="2b34e-117">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="2b34e-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




