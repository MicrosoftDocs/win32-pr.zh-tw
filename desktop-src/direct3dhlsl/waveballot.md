---
title: WaveActiveBallot 函式
description: 傳回 uint4，其中包含目前 wave 中所有使用中通道的布林運算式評估的位元遮罩。
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- WaveActiveBallot 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508196"
---
# <a name="waveactiveballot-function"></a>WaveActiveBallot 函式

傳回 uint4，其中包含目前 wave 中所有使用中通道的布林運算式評估的位元遮罩。 

## <a name="syntax"></a>語法

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*expr* 
</dt> <dd>

要評估的布林運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

Uint4，包含目前 wave 中所有使用中通道的布林運算式評估的位元遮罩。 最不重要的位會對應至索引為零的通道。 對應到非使用中通道的位將會是零。 大於或等於 [**WaveGetLaneCount**](wavegetlanecount.md) 的位將會是零。

## <a name="remarks"></a>備註

不同的 Gpu 具有不同的 SIMD 處理器寬度， (航道計數) 。 這些 **WaveXXX** 函數大多都能在 SIMD 電腦寬度隱藏的抽象層級上運作。 若要最大化跨 Gpu 的程式碼可攜性，請使用不依賴電腦寬度的內建函式。 例如，使用：

``` syntax
uint result = WaveActiveCountBits( bBit );
```

不要這樣撰寫：

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




