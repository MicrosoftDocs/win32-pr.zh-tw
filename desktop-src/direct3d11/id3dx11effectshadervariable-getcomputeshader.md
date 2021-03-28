---
title: 'ID3DX11EffectShaderVariable GetComputeShader 方法 (D3dx11effect .h) '
description: 取得計算著色器。
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- GetComputeShader 方法 Direct3D 11
- GetComputeShader 方法 Direct3D 11，ID3DX11EffectShaderVariable 介面
- ID3DX11EffectShaderVariable 介面 Direct3D 11，GetComputeShader 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196464"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a>ID3DX11EffectShaderVariable：： GetComputeShader 方法

取得計算著色器。

## <a name="syntax"></a>語法


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

計算著色器的索引。

</dd> <dt>

*ppPS* 
</dt> <dd>

類型： **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***

[**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)指標的指標，會在傳回時設定為計算著色器。

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

 

