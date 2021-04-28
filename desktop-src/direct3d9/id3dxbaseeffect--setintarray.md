---
description: ID3DXBaseEffect：： SetIntArray 方法：設定整數的陣列。
ms.assetid: 4491bffd-ce5e-4f84-ac11-0314a1b16d63
title: 'ID3DXBaseEffect：： SetIntArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a14e837a0903290c3197bbb17ec4b2da3f68b419
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093756"
---
# <a name="id3dxbaseeffectsetintarray-method"></a>ID3DXBaseEffect：： SetIntArray 方法

設定整數的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hParameter,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pn* \[在\]
</dt> <dd>

類型： **Const [**INT**](../winprog/windows-data-types.md) \***

整數的陣列。

</dd> <dt>

*計數* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列中的整數數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetIntArray**](id3dxbaseeffect--getintarray.md)
</dt> </dl>

 

 
