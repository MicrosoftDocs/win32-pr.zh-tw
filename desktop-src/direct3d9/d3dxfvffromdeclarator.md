---
description: 傳回彈性頂點格式 (從宣告子 FVF) 程式碼。
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: 'D3DXFVFFromDeclarator 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f9bad9968a52fb6c3b11de96936f48e432bd038e172318cb52f21fad4b08ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525645"
---
# <a name="d3dxfvffromdeclarator-function"></a>D3DXFVFFromDeclarator 函式

傳回彈性頂點格式 (從宣告子 FVF) 程式碼。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDeclaration* \[在\]
</dt> <dd>

Type： **Const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素的陣列，描述 FVF 程式碼。

</dd> <dt>

*pFVF* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

DWORD 值的指標，代表傳回的 [D3DFVF](d3dfvf.md) 組合，其描述從宣告子傳回的頂點格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

未直接對應至 FVF 的任何宣告子，此函式將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
