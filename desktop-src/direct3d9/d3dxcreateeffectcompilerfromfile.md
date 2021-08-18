---
description: D3DXCreateEffectCompilerFromFile 函式-從 ASCII 效果描述建立效果編譯器。
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: 'D3DXCreateEffectCompilerFromFile 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f955c62bed0e449ddc2f9c9b1e4d7fe1c57df388f7ae99647a6b6cbce9d4fa48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857258"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a>D3DXCreateEffectCompilerFromFile 函式

從 ASCII 效果描述建立效果編譯器。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

檔案名的指標。 此參數支援 Unicode 和 ANSI 字串。 請參閱＜備註＞。

</dd> <dt>

*pDefines* \[在\]
</dt> <dd>

Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***

[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。 這個值可以是 **Null**。

</dd> <dt>

*pInclude* \[在\]
</dt> <dd>

類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。 如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

不同旗標所識別的編譯選項 (參閱 [D3DXSHADER 旗標](d3dxshader-flags.md)) 。 Direct3D 10 HLSL 編譯器現在是預設值。 請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。

</dd> <dt>

*ppEffectCompiler* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

[**ID3DXEffectCompiler**](id3dxeffectcompiler.md)介面指標的位址，其中包含效果編譯器。

</dd> <dt>

*ppParseErrors* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含在編譯期間發生的任何錯誤訊息。 這個參數可以設定為 **Null** ，以忽略錯誤訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，LPCTSTR 資料類型會解析為 LPCSTR。

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectCompilerFromFileW。 否則，函式呼叫會解析為 D3DXCreateEffectCompilerFromFileA，因為正在使用 ANSI 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果函數](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
