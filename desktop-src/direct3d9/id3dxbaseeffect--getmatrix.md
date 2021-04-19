---
description: 取得 nontransposed 矩陣。
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'ID3DXBaseEffect：： GetMatrix 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993913"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a>ID3DXBaseEffect：： GetMatrix 方法

取得 nontransposed 矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

唯一識別碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pMatrix* \[擴展\]
</dt> <dd>

類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***

傳回 nontransposed 矩陣。 請參閱 [**D3DXMATRIX**](d3dxmatrix.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

Nontransposed 矩陣包含資料列主要資料;也就是說，每個向量都包含在資料列中。

如果目的地矩陣大於來源矩陣，則只會填入目的地矩陣的左上角元件，其餘元件則會設定為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrix**](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




