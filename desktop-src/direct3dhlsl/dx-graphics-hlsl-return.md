---
title: return 陳述式
description: Return 語句表示函式的結尾。
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- return 語句 HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8b7a8cc846e165c1c0bafa435bd4f4fe655ace5605b03b9821a08109fd65431
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726458"
---
# <a name="return-statement"></a>return 陳述式

Return 語句表示函式的結尾。

傳回 \[ 值 \] ;



 

最簡單的 return 語句會從函式將控制權傳回給呼叫的程式。它不會傳回任何值。


```
void main()
{
    return ;
}
```



不過，return 語句可以傳回一或多個值。 此範例會傳回常值：


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



這個範例會傳回運算式的純量結果。


```
return  light.enabled = true ;
```



這個範例會傳回由區域變數和常值所構成的四個元件向量。


```
return  float4(color.rgb, 1) ;
```



這個範例會傳回四個元件的向量，這個向量是從內建函式所傳回的結果以及常值所構成。


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



這個範例會傳回包含一或多個成員的結構。


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (DirectX HLSL) 的函式 ](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




