---
title: 函式宣告語法
description: HLSL 函式會使用下列語法來宣告。
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce8c6ec83963dac74dce32d248b23548c767192a604ddb8afbe35cf932dedee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514603"
---
# <a name="function-declaration-syntax"></a>函式宣告語法

HLSL 函式會使用下列語法來宣告。

\[*StorageClass* \]\[clipplanes () \] \[精確的傳回 \] \_ 值 *名稱* ( \[ *ArgumentList* \] ) \[ ：*語義* \] { \[ *StatementBlock* \] };



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

重新定義函式宣告的修飾詞。 **內嵌** 是目前唯一的修飾詞值。 修飾詞值必須是 **內嵌** 的，因為它也是預設值。 因此，不論您是否指定 **inline**，函式都會內嵌，而 HLSL 中的所有函式都是內嵌的。 內嵌函式會在編譯每個函式呼叫的) 時，產生函數主體的複本 (。 這樣做的目的是要降低呼叫函式的額外負荷。

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

選擇性的剪輯平面清單，最多可有6個使用者指定的剪輯平面。 這是在[功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)9 x 和更高版本上運作的[SV \_ ClipDistance](dx-graphics-hlsl-semantics.md)替代機制 \_ 。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

能唯一識別著色器函式名稱的 ASCII 字串。

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

選擇性引數清單，此清單是傳遞至函式的 [引數](dx-graphics-hlsl-function-parameters.md) 清單（以逗號分隔）。

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*語義*
</dt> <dd>

選擇性字串，可識別傳回資料的預期使用方式 (請參閱 [ (DIRECTX HLSL) ](dx-graphics-hlsl-semantics.md)) 的語義。

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

組成函數主體的選擇性 [語句](dx-graphics-hlsl-statement-blocks.md) 。 未定義主體的函式稱為函式原型。原型函式的主體必須定義在可呼叫函式之前的其他地方。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回型別可以是下列其中一種 [HLSL 類型](dx-graphics-hlsl-data-types.md)。

## <a name="remarks"></a>備註

此頁面上的語法幾乎描述每種類型的 HLSL 函式，包括頂點著色器、圖元著色器和 helper 函式。 雖然幾何著色器也會使用函式來執行，但其語法有點複雜，因此有個別的頁面可定義幾何著色器函式宣告 (請參閱 [幾何著色器物件 (DIRECTX HLSL) ](dx-graphics-hlsl-geometry-shader.md)) 。

只要指定了參數類型和/或參數順序的唯一組合，就可以多載函式。 HLSL 也會執行一些內建或 [**內建函式**](dx-graphics-hlsl-intrinsic-functions.md)。

您可以使用 **clipplanes** 屬性來指定使用者特定的剪輯平面。 Windows 將這些剪切平面套用至所有繪製的基本專案。 **Clipplanes** 屬性的運作方式類似 [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) ，但適用于所有硬體 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)9 \_ x 和更高。 如需詳細資訊，請參閱「 [功能等級9硬體上的使用者剪輯平面](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)」。

## <a name="examples"></a>範例

此範例來自 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)中的 BasicHLSL10。


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



此範例來自 [AdvancedParticles 範例](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)中的 AdvancedParticles，說明如何使用傳回型別的語義。


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的函式 ](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
