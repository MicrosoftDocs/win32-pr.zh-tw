---
description: 從 ASCII 或二進位效果描述建立效果。 此函式是 D3DXCreateEffectFromFile 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: 'D3DXCreateEffectFromFileEx 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5f0b329502e6b5e957e1d8c0761fe19fa6bc1e8420269a6329435ba27a53f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526552"
---
# <a name="d3dxcreateeffectfromfileex-function"></a>D3DXCreateEffectFromFileEx 函式

從 ASCII 或二進位效果描述建立效果。 此函式是 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
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

*pSkipConstants* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

效果系統將忽略效果參數的字串。 字串必須以 **Null** 結束，且必須包含每個應用程式管理的常數名稱（以分號分隔）。

</dd> <dt>

*旗標* \[在\]
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

此函式是 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) 的延伸版本，可讓應用程式指定應用程式要管理哪些效果常數。 效果系統會忽略應用程式所管理的常數。 也就是說，應用程式會負責初始化常數，並在適當時儲存和還原其狀態。

此函式會檢查 pSkipConstants 中的每個常數，以查看：

-   它會系結至常數暫存器。
-   它只會在 HLSL 著色器程式碼中使用。

如果常數是在不存在於效果中的字串中命名，則會忽略它。

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

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
