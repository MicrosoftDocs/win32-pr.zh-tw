---
description: 此函式會建立著色器反映物件，以抓取已編譯著色器的相關資訊--不存在。 請改用 D3DReflect 或 D3D11Reflect。
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: 'D3DX10ReflectShader 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000599"
---
# <a name="d3dx10reflectshader-function"></a>D3DX10ReflectShader 函式

此函式會建立著色器反映物件，以抓取已編譯著色器的相關資訊--不存在。 請改用 [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) 或 [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md)。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pShaderBytecode* \[在\]
</dt> <dd>

類型： **const void \***

已編譯之著色器的指標。 若要取得此指標，請參閱 [取得已編譯著色器的指標](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)。

</dd> <dt>

*BytecodeLength* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

PShaderBytecode 的長度。

</dd> <dt>

*ppReflector* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

著色器反映介面的位址 (查看 [**ID3D10ShaderReflection1 介面**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回下列其中一個 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)。

## <a name="remarks"></a>備註

以下是建立著色器反映物件的範例。 此範例假設您開始使用編譯的著色器 (顯示為


```
pVSBuf
```



您可以在 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)) 中看到。


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
