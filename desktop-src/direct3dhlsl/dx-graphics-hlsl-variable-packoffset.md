---
title: packoffset
description: 選用的著色器常數封裝關鍵字，使用下列語法
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312459"
---
# <a name="packoffset"></a>packoffset

選用的著色器常數封裝關鍵字，使用下列語法：



|                                                 |
|-------------------------------------------------|
| ： packoffset ( c \[ 子元件 \] \[ 。元件 \] )  |



 

## <a name="parameters"></a>參數



| 項目                                                                                                                                                                                 | 描述                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | 必要關鍵字。<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**C**<br/>                                                                                                                             | 封裝僅適用于 (c) 的常數暫存器。 <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[子 \] \[ 元件\]**<br/> | 選擇性的子元件和元件。 子元件是一個暫存器號碼，這是一個整數。 元件的格式為 \[ xyzw \] 。<br/> |



 

## <a name="remarks"></a>備註

當宣告 [變數類型](dx-graphics-hlsl-variable-syntax.md)時，請使用這個關鍵字手動封裝著色器常數。

當封裝常數時，您無法混合常數類型。

針對全域常數和統一常數，編譯器的行為稍有不同：

-   全域常數。 全域變數會以全域常數的形式加入至編譯器所 cbuffer 的 *$Global* 。 自動封裝的元素 (不含 packoffset 的宣告) 將會出現在最後一個手動封裝的變數之後。 您可以在封裝全域常數時混合類型。
-   統一常數。 當著色器是在效果架構之外編譯時，編譯器會將函式參數清單中的統一參數加入至 *$Param* 常數緩衝區。 在效果架構內編譯時，統一常數必須解析為全域範圍中定義的統一變數。 統一常數不能手動位移;它們的建議用途只是用來將著色器的別名特製化回全域，而不是將應用程式資料傳遞給著色器的方法。

以下是一些其他範例： [使用著色器模型4的封裝常數](dx-graphics-hlsl-packing-rules.md)。

## <a name="examples"></a>範例

以下是一些手動封裝著色器常數的範例。

封裝其大小夠大以防止暫存器界限的向量和純量子元件。 例如，這些都是有效的：


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[語法變數](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[ (DirectX HLSL) 的變數 ](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





