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
# <a name="waveactivecountbits-function"></a>WaveActiveCountBits 函式

計算在目前 wave 的所有作用中通道上評估為 true 的布林值變數數目，並將結果複製到 wave 中的所有通道。

## <a name="syntax"></a>語法


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bBit* 
</dt> <dd>

要評估的布林值變數。 提供明確的 true 布林值會傳回使用中的通道數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

在目前 wave 的所有作用中通道上評估為 true 的數目。

## <a name="remarks"></a>備註

所有著色器階段中的著色器模型6.0 都支援此函數。 



 

## <a name="examples"></a>範例

這可以比完整的 WaveActiveSum 更有效率地執行，如下列範例所述：

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型6總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[著色器模型6](shader-model-6-0.md)
</dt> </dl>

 

 




