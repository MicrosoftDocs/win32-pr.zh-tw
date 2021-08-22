---
description: ID3DXSkinInfo：： GetDeclaration 方法-取得頂點宣告。
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'ID3DXSkinInfo：： GetDeclaration 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8188094801ed3a9cef4be3c441d6afb5032e86178da50d837017c0836a702c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800948"
---
# <a name="id3dxskininfogetdeclaration-method"></a>ID3DXSkinInfo：： GetDeclaration 方法

取得頂點宣告。

## <a name="syntax"></a>語法


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>參數

<dl> <dt>

宣告 \[in、out\]
</dt> <dd>

類型： **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

描述網格頂點頂點格式的 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 元素陣列。 此宣告子陣列的上限是 [**\_ FVF \_ DECL \_ SIZE 的最大**](./max-fvf-decl-size.md)值。 頂點元素陣列的結尾是 [**D3DDECL \_ END**](d3ddecl-end.md) 宏。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

專案的陣列包含結束宣告的 [**D3DDECL \_ 結束**](d3ddecl-end.md) 宏。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
