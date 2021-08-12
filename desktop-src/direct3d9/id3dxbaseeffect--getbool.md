---
description: 取得 BOOL 值。
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: 'ID3DXBaseEffect：： GetBool 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 13fa69c8fd20798f683003bd561193a4079ba48c291248f7d4ce6fe1d0fc5fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522317"
---
# <a name="id3dxbaseeffectgetbool-method"></a>ID3DXBaseEffect：： GetBool 方法

取得 BOOL 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pb* \[擴展\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)\***

傳回布林值。

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

[**SetBool**](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
