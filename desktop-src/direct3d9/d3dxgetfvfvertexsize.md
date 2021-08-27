---
description: 傳回 (FVF) 的彈性頂點格式頂點的大小。
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: 'D3DXGetFVFVertexSize 函式 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f00faa489481faf436a30fe6e6313429d446cd8000173131d823442e960b5a08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119208"
---
# <a name="d3dxgetfvfvertexsize-function"></a>D3DXGetFVFVertexSize 函式

傳回 (FVF) 的彈性頂點格式頂點的大小。

## <a name="syntax"></a>語法


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FVF* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要查詢的 FVF。 [D3DFVF](d3dfvf.md)的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

FVF 頂點大小（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
