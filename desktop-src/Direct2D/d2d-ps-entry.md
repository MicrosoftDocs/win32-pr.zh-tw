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
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983954"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="4303c-104">D2D \_ PS \_ 輸入函式</span><span class="sxs-lookup"><span data-stu-id="4303c-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="4303c-105">使用指定的函數名稱定義圖元著色器進入點的宏。</span><span class="sxs-lookup"><span data-stu-id="4303c-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="4303c-106">語法</span><span class="sxs-lookup"><span data-stu-id="4303c-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="4303c-107">參數</span><span class="sxs-lookup"><span data-stu-id="4303c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4303c-108">*Entryname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4303c-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4303c-109">圖元著色器的進入點名稱。</span><span class="sxs-lookup"><span data-stu-id="4303c-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4303c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4303c-110">Return value</span></span>

<span data-ttu-id="4303c-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4303c-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4303c-112">備註</span><span class="sxs-lookup"><span data-stu-id="4303c-112">Remarks</span></span>

<span data-ttu-id="4303c-113">使用這個宏，而不是以一般方式指定進入點的輸入簽章：在編譯期間，所有參數都是隱含的，而且 Direct2D 會根據編譯目標型別 (完整著色器或匯出函式) 來新增。</span><span class="sxs-lookup"><span data-stu-id="4303c-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

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

<span data-ttu-id="4303c-114">在這個簡短的範例中，請注意，不會宣告任何函式參數，每個輸入的輸入和類型數目是在輸入函式之前宣告，而是藉由呼叫 [D2DGetInput](d2dgetinput.md)來取出輸入，而且必須先定義預處理器指示詞，才能包含 helper 檔案。</span><span class="sxs-lookup"><span data-stu-id="4303c-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="4303c-115">連結相容的著色器必須同時提供一般的單一傳遞圖元著色器和匯出著色器函數。</span><span class="sxs-lookup"><span data-stu-id="4303c-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="4303c-116">當您 \_ \_ 搭配著色器編譯腳本使用時，D2D PS 專案宏可讓您從相同的程式碼產生這些專案。</span><span class="sxs-lookup"><span data-stu-id="4303c-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="4303c-117">編譯完整的著色器時，宏會展開至下列程式碼，其中包含與 D2D 效果相容的輸入簽章。</span><span class="sxs-lookup"><span data-stu-id="4303c-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

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

<span data-ttu-id="4303c-118">當編譯相同程式碼的匯出函數版本時，會產生下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="4303c-118">When compiling an export function version of the same code, the following code is generated:</span></span>

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

<span data-ttu-id="4303c-119">請注意，通常透過取樣 Texture2D 來取出的材質輸入已被函式輸入 input0 取代。</span><span class="sxs-lookup"><span data-stu-id="4303c-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="4303c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4303c-120">Requirements</span></span>



| <span data-ttu-id="4303c-121">需求</span><span class="sxs-lookup"><span data-stu-id="4303c-121">Requirement</span></span> | <span data-ttu-id="4303c-122">值</span><span class="sxs-lookup"><span data-stu-id="4303c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4303c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4303c-123">Header</span></span><br/> | <dl> <span data-ttu-id="4303c-124"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="4303c-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="4303c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4303c-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="4303c-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4303c-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="4303c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4303c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4303c-128">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="4303c-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="4303c-129">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="4303c-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





