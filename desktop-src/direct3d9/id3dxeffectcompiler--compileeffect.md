---
description: 編譯效果。
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'ID3DXEffectCompiler：： CompileEffect 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322716"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a>ID3DXEffectCompiler：： CompileEffect 方法

編譯效果。

## <a name="syntax"></a>語法


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

不同旗標所識別的編譯選項。 Direct3D 10 HLSL 編譯器現在是預設值。 如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。

</dd> <dt>

*ppEffect* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含已編譯效果的緩衝區。 如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> <dt>

*ppErrorMsgs* \[退出，retval\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

包含至少發生第一個編譯錯誤訊息的緩衝區。 這包括對編譯器錯誤和高階語言編譯錯誤的影響。 如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。

如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。

如果方法失敗，傳回值將會是 E \_ 失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 
