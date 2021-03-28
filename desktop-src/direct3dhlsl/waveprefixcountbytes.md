---
title: WavePrefixCountBits 函式
description: 傳回所有在所有作用中的通道上，所有指定的布林值變數設定為 true 的總和，其索引小於目前的航道。
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- WavePrefixCountBits 函式 HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024331"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="9107d-104">WavePrefixCountBits 函式</span><span class="sxs-lookup"><span data-stu-id="9107d-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="9107d-105">傳回所有在所有作用中的通道上，所有指定的布林值變數設定為 true 的總和，其索引小於目前的航道。</span><span class="sxs-lookup"><span data-stu-id="9107d-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="9107d-106">語法</span><span class="sxs-lookup"><span data-stu-id="9107d-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="9107d-107">參數</span><span class="sxs-lookup"><span data-stu-id="9107d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9107d-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="9107d-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="9107d-109">指定的布林值變數。</span><span class="sxs-lookup"><span data-stu-id="9107d-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9107d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9107d-110">Return value</span></span>

<span data-ttu-id="9107d-111">所有指定之布林值變數的總和在所有作用中的通道上都設為 true，且索引小於目前的通道。</span><span class="sxs-lookup"><span data-stu-id="9107d-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="9107d-112">備註</span><span class="sxs-lookup"><span data-stu-id="9107d-112">Remarks</span></span>

<span data-ttu-id="9107d-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="9107d-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="9107d-114">範例</span><span class="sxs-lookup"><span data-stu-id="9107d-114">Examples</span></span>

<span data-ttu-id="9107d-115">下列程式碼說明如何將壓縮的寫入實作為已排序的資料流程，其中每個通道所寫入的元素數目是1或0。</span><span class="sxs-lookup"><span data-stu-id="9107d-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a><span data-ttu-id="9107d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9107d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9107d-117">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="9107d-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="9107d-118">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="9107d-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




