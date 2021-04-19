---
description: 取得字串。
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'ID3DXBaseEffect：： GetString 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001485"
---
# <a name="id3dxbaseeffectgetstring-method"></a>ID3DXBaseEffect：： GetString 方法

取得字串。

## <a name="syntax"></a>語法


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*ppString* \[擴展\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***

傳回 hParameter 所識別的字串。

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

[**SetString**](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
