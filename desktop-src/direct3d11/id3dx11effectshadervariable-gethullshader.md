---
title: 'ID3DX11EffectShaderVariable GetHullShader 方法 (D3dx11effect .h) '
description: 取得輪廓著色器。
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- GetHullShader 方法 Direct3D 11
- GetHullShader 方法 Direct3D 11，ID3DX11EffectShaderVariable 介面
- ID3DX11EffectShaderVariable 介面 Direct3D 11，GetHullShader 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534e29d68402cba797a44d060782fe7a362fef6dfd01388902b7617d31f5c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533274"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a>ID3DX11EffectShaderVariable：： GetHullShader 方法

取得輪廓著色器。

## <a name="syntax"></a>語法


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

著色器的索引。

</dd> <dt>

*ppPS* 
</dt> <dd>

類型： **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***

[**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)指標的指標，會在傳回時設定為輪廓著色器。

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

 

