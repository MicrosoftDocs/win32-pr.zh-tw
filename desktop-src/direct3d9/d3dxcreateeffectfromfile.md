---
description: 從 ASCII 或二進位效果描述建立效果。
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: 'D3DXCreateEffectFromFile 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f34d0cdb3ae19772f21d8307fffb395c4d1ac9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696796"
---
# <a name="d3dxcreateeffectfromfile-function"></a>D3DXCreateEffectFromFile 函式

從 ASCII 或二進位效果描述建立效果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

將建立效果之裝置的指標。 請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。

</dd> <dt>

*pSrcFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

檔案名的指標。 此參數支援 Unicode 和 ANSI 字串。 請參閱＜備註＞。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***

預處理器巨集定義的選擇性 Null 結束陣列。 請參閱 [**D3DXMACRO**](d3dxmacro.md)。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。 如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

如果 *pSrcFile* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcFile* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。 Direct3D 10 HLSL 編譯器現在是預設值。 請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。

</dd> <dt>

*pPool* \[在\]
</dt> <dd>

類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。 如果這個值為 **Null**，則不會共用任何參數。

</dd> <dt>

*ppEffect* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

傳回包含已編譯效果的緩衝區指標。 請參閱 [**ID3DXEffect**](id3dxeffect.md)。

</dd> <dt>

*ppCompilationErrors* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含編譯錯誤清單的緩衝區指標。 請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，LPCTSTR 資料類型會解析為 LPCSTR。

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectFromFileW。 否則，函式呼叫會解析為 D3DXCreateEffectFromFileA，因為正在使用 ANSI 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果函數](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
