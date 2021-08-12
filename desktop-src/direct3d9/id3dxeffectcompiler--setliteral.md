---
description: 切換參數的常值狀態。 常值參數的值不會在效果的存留期間變更。
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler：： SetLiteral 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d28ee64c1d1e52b4005c1a81ef4690c539a09e06eb7a8378a246184cf4d2fd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295829"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>ID3DXEffectCompiler：： SetLiteral 方法

切換參數的常值狀態。 常值參數的值不會在效果的存留期間變更。

## <a name="syntax"></a>語法


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

參數的唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*常* \[ 值在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果設定為 **TRUE** ，則將參數設為常值，如果參數可以在著色器存留期間變更值，則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這種方法只會變更參數是否為常值。 若要變更參數的值，請使用 [**ID3DXBaseEffect：： SetBool**](id3dxbaseeffect--setbool.md) 或 [**ID3DXBaseEffect：： SetValue**](id3dxbaseeffect--setvalue.md)之類的方法。

在編譯效果之前，必須先呼叫此函式。 以下是一個使用此函數的範例：


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[ (Direct3D 9) 的使用方式和常值 ](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::GetLiteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
