---
description: 從 ASCII 或二進位效果描述建立效果。 此函式是 D3DXCreateEffect 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: 'D3DXCreateEffectEx 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19321dde9f44a2262ee3875d40bd5822e65eff9b84d1fc01656993ea584a8dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988648"
---
# <a name="d3dxcreateeffectex-function"></a>D3DXCreateEffectEx 函式

從 ASCII 或二進位效果描述建立效果。 此函式是 [**D3DXCreateEffect**](d3dxcreateeffect.md) 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
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

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

包含效果描述之緩衝區的指標。

</dd> <dt>

*SrcDataLen* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

效果資料的長度（以位元組為單位）。

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

*pSkipConstants* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

效果系統將忽略效果參數的字串。 字串必須以 **Null** 結束，且必須包含每個應用程式管理的常數名稱（以分號分隔）。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

如果 *pSrcData* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcData* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。 Direct3D 10 HLSL 編譯器現在是預設值。 請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。

</dd> <dt>

*pPool* \[在\]
</dt> <dd>

類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。 如果這個值為 **Null**，則不會共用任何參數。

</dd> <dt>

*ppEffect* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

傳回 [**ID3DXEffect**](id3dxeffect.md) 介面的指標。

</dd> <dt>

*ppCompilationErrors* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含編譯錯誤清單的緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函式是 [**D3DXCreateEffect**](d3dxcreateeffect.md) 的延伸版本，可讓應用程式指定應用程式要管理哪些效果常數。 效果系統會忽略應用程式所管理的常數。 也就是說，應用程式會負責初始化常數，並在適當時儲存和還原其狀態。

此函式會檢查 pSkipConstants 中的每個常數，以查看：

-   它會系結至常數暫存器。
-   它只會在 HLSL 著色器程式碼中使用。

如果常數是在不存在於效果中的字串中命名，則會忽略它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果函數](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
