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
ms.openlocfilehash: 048b63d24e87d97f0e0223083a91694c0471b9e38ad21afbc487c02d711d720d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504674"
---
# <a name="waveprefixcountbits-function"></a>WavePrefixCountBits 函式

傳回所有在所有作用中的通道上，所有指定的布林值變數設定為 true 的總和，其索引小於目前的航道。

## <a name="syntax"></a>語法


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bBit* 
</dt> <dd>

指定的布林值變數。

</dd> </dl>

## <a name="return-value"></a>傳回值

所有指定之布林值變數的總和在所有作用中的通道上都設為 true，且索引小於目前的通道。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

下列程式碼說明如何將壓縮的寫入實作為已排序的資料流程，其中每個通道所寫入的元素數目是1或0。

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

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




