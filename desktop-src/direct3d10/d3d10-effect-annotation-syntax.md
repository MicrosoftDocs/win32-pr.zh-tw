---
description: 批註是以下列語法宣告的使用者定義資訊片段。
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: " (Direct3D 10) 的批註語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847615"
---
# <a name="annotation-syntax-direct3d-10"></a> (Direct3D 10) 的批註語法

批註是以下列語法宣告的使用者定義資訊片段。



| <*DataType* *名稱*  =  *值*; ...;> |
|--------------------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                                                                   | 描述                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*資料類型*<br/> | \[在 \] 資料類型中，包含任何純量 [HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) 類型以及 [字串類型](../direct3dhlsl/dx-graphics-hlsl-scalar.md)。<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*<br/>                 | \[\]表示批註名稱的 ASCII 字串。<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*價值*<br/>             | \[在 \] 批註的初始值中。<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[在 \] 其他批註中 (名稱/值組) 。<br/>                                                                                                                     |



 

## <a name="remarks"></a>備註

您可以在角括弧內加入多個注釋，每一個都以分號分隔。 效果架構 Api 會辨識全域變數上的注釋;所有其他注釋都會被忽略。

## <a name="example"></a>範例

以下是一些範例。


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果變數語法](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
