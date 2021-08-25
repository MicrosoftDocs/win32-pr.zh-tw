---
description: 傳回頂點宣告中的元素數目。
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: 'D3DXGetDeclLength 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc6a44c73d9b7127bb382cfbf18587a84d8cc179feabf48da6e29b908204b1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857037"
---
# <a name="d3dxgetdecllength-function"></a>D3DXGetDeclLength 函式

傳回頂點宣告中的元素數目。

## <a name="syntax"></a>語法


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDecl* \[在\]
</dt> <dd>

Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

頂點宣告的指標。 請參閱 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

頂點宣告中的元素數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
