---
description: 分解效果。
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: 'D3DXDisassembleEffect 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e4fa48418513cd9f4f70bc8356965a45499d1c6d822eaa1c1952d25ebe4b1ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119218"
---
# <a name="d3dxdisassembleeffect-function"></a>D3DXDisassembleEffect 函式

分解效果。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pEffect* \[在\]
</dt> <dd>

類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)**

包含效果的 [**ID3DXEffect**](id3dxeffect.md) 介面指標。

</dd> <dt>

*EnableColorCode* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

啟用色彩編碼，讓反組解碼更容易閱讀。

</dd> <dt>

*ppDisassembly* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

傳回包含已拆解著色器的緩衝區。 請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果函數](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
