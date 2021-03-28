---
title: 'ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc 方法 (D3dx11effect .h) '
description: 取得修補程式常數簽章描述。
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- GetPatchConstantSignatureElementDesc 方法 Direct3D 11
- GetPatchConstantSignatureElementDesc 方法 Direct3D 11，ID3DX11EffectShaderVariable 介面
- ID3DX11EffectShaderVariable 介面 Direct3D 11，GetPatchConstantSignatureElementDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992355"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a>ID3DX11EffectShaderVariable：： GetPatchConstantSignatureElementDesc 方法

取得修補程式常數簽章描述。

## <a name="syntax"></a>語法


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

以零為基底的著色器索引。

</dd> <dt>

*Element* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

以零為基底的元素索引。

</dd> <dt>

*pDesc* 
</dt> <dd>

Type： **[ **D3D11 \_ SIGNATURE \_ 參數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

參數描述的指標 (參閱 [**D3D11 \_ 簽名 \_ 參數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

> [!Note]  
> DirectX SDK 不提供任何已編譯的二進位檔來產生效果。 您必須使用效果11來源來建立效果類型的應用程式。 如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx11effect。h</dt> </dl>                                                    |
| 程式庫<br/> | <dl> <dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

