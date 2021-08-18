---
title: D3D11Reflect 函式
description: 取得反映介面的指標。
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect 函式 HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b980d955dcd37197c8d8ed05a6602025d1e21731ca6d22302b76cc2f2e53da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986878"
---
# <a name="d3d11reflect-function"></a>D3D11Reflect 函式

取得反映介面的指標。

## <a name="syntax"></a>語法

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

作為已編譯 HLSL 程式碼之來源資料的指標。

</dd> <dt>

*SrcDataSize* \[在\]
</dt> <dd>

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**

*PSrcData* 的長度。

</dd> <dt>

*ppReflector* \[擴展\]
</dt> <dd>

類型： **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

傳回 [Direct3D 11 傳回碼](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)主題中所述的其中一個傳回碼。

## <a name="remarks"></a>備註

內嵌 **D3D11Reflect** 編譯器函數是 [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) 編譯器函式的包裝函式。 **D3D11Reflect** 只能從著色器取出 [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) 介面。 **D3DReflect** 可以取出 **ID3D11ShaderReflection** 介面或 direct3d 10 或 direct3d 10.1 反映介面，例如 [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection)。

著色器程式碼包含可使用反映 Api 檢查的中繼資料。

下列程式碼示範如何從著色器取出 [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) 介面。


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DCompiler. .inl</dt> </dl>     |
| 程式庫<br/> | <dl> <dt>D3dcompiler \_ 47 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>請參閱

<dl> <dt>

[函式](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

