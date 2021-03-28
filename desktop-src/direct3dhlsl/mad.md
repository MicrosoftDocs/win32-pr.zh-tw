---
title: mad 函式
description: 針對三個值執行算術乘法/add 運算。
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- mad 函數 HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462589"
---
# <a name="mad-function"></a>mad 函式

針對三個值執行算術乘法/add 運算。

## <a name="syntax"></a>語法

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*mvalue* \[在\]
</dt> <dd>

類型： **數值**

乘法值。

</dd> <dt>

*值* \[在\]
</dt> <dd>

類型： **數值**

第一個加法值。

</dd> <dt>

*其中 bvalue system.boolean.true* \[在\]
</dt> <dd>

類型： **數值**

第二個加法值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **數值**

*Mvalue* \* *值*  +  *其中 bvalue system.boolean.true* 的結果。

## <a name="remarks"></a>備註

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

著色器作者可以使用 **mad** 內部，在編譯的著色器輸出中明確地以 **mad** 硬體指令作為目標，這在使用 [精確](dx-graphics-hlsl-appendix-keywords.md) 關鍵字標記結果的著色器中特別有用。 您可以在硬體中將 **mad** 指令實作為「融合的」，這可提供比起執行 **mul** 指令的精確度更高的精確度，並在後面加上「**新增** 指令」或 **mul**  +  **加入**。

如果著色器作者使用 **mad** 內部來計算著色器標示為精確的結果，則會指出硬體使用任何有效的 **mad** 指令實行 (融合或不) ，只要該 **mad** 內建在該硬體上任何著色器中的所有用法都一致。 著色器可以利用原生的 **mad** 指令 (與 **mul**  +  在某些硬體上 **新增**) ，來利用潛在的效能改進。 執行原生 **mad** 硬體指令的結果可能不會與執行 **mul** 後再執行 **add** 的結果不同。 但是，無論結果為何，結果都必須一致，才能讓相同的作業發生在多個著色器或著色器的不同部分中。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




