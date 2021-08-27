---
title: 'D2D_PS_ENTRY 函式 (D2d1effecthelpers) '
description: 使用指定的函數名稱定義圖元著色器進入點的宏。
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY 函式 Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26369ef5be8c9dea81bf95e60c09ca0041d4275114c8892b85b6b5525f45504b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087780"
---
# <a name="d2d_ps_entry-function"></a>D2D \_ PS \_ 輸入函式

使用指定的函數名稱定義圖元著色器進入點的宏。

## <a name="syntax"></a>語法

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*Entryname* \[在\]
</dt> <dd>

圖元著色器的進入點名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用這個宏，而不是以一般方式指定進入點的輸入簽章：在編譯期間，所有參數都是隱含的，而且 Direct2D 會根據編譯目標型別 (完整著色器或匯出函式) 來新增。

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

在這個簡短的範例中，請注意，不會宣告任何函式參數，每個輸入的輸入和類型數目是在輸入函式之前宣告，而是藉由呼叫 [D2DGetInput](d2dgetinput.md)來取出輸入，而且必須先定義預處理器指示詞，才能包含 helper 檔案。

連結相容的著色器必須同時提供一般的單一傳遞圖元著色器和匯出著色器函數。 當您 \_ \_ 搭配著色器編譯腳本使用時，D2D PS 專案宏可讓您從相同的程式碼產生這些專案。

編譯完整的著色器時，宏會展開至下列程式碼，其中包含與 D2D 效果相容的輸入簽章。

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

當編譯相同程式碼的匯出函數版本時，會產生下列程式碼：

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

請注意，通常透過取樣 Texture2D 來取出的材質輸入已被函式輸入 input0 取代。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果著色器連結](effect-shader-linking.md)
</dt> <dt>

[HLSL 協助程式](hlsl-helpers.md)
</dt> </dl>

 

 





