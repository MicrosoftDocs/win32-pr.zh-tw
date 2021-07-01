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
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119583"
---
# <a name="return-statement"></a><span data-ttu-id="5d1db-104">return 陳述式</span><span class="sxs-lookup"><span data-stu-id="5d1db-104">return Statement</span></span>

<span data-ttu-id="5d1db-105">Return 語句表示函式的結尾。</span><span class="sxs-lookup"><span data-stu-id="5d1db-105">A return statement signals the end of a function.</span></span>

<span data-ttu-id="5d1db-106">傳回 \[ 值 \] ;</span><span class="sxs-lookup"><span data-stu-id="5d1db-106">return \[value\];</span></span>



 

<span data-ttu-id="5d1db-107">最簡單的 return 語句會從函式將控制權傳回給呼叫的程式。它不會傳回任何值。</span><span class="sxs-lookup"><span data-stu-id="5d1db-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="5d1db-108">不過，return 語句可以傳回一或多個值。</span><span class="sxs-lookup"><span data-stu-id="5d1db-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="5d1db-109">此範例會傳回常值：</span><span class="sxs-lookup"><span data-stu-id="5d1db-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="5d1db-110">這個範例會傳回運算式的純量結果。</span><span class="sxs-lookup"><span data-stu-id="5d1db-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="5d1db-111">這個範例會傳回由區域變數和常值所構成的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="5d1db-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="5d1db-112">這個範例會傳回四個元件的向量，這個向量是從內建函式所傳回的結果以及常值所構成。</span><span class="sxs-lookup"><span data-stu-id="5d1db-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="5d1db-113">這個範例會傳回包含一或多個成員的結構。</span><span class="sxs-lookup"><span data-stu-id="5d1db-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="5d1db-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d1db-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1db-115"> (DirectX HLSL) 的函式 </span><span class="sxs-lookup"><span data-stu-id="5d1db-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




