---
description: D3DXGetShaderConstantTable 函式-取得內嵌在著色器中的著色器常數資料表。
ms.assetid: eb965074-819f-44d2-889b-6c6eada4f062
title: 'D3DXGetShaderConstantTable 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTable
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a1375dfcf1bc75d6f2dee6f9923360b1b90fef01df5489f9f710175e7e1c2652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045006"
---
# <a name="d3dxgetshaderconstanttable-function"></a>D3DXGetShaderConstantTable 函式

取得內嵌在著色器中的著色器常數資料表。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetShaderConstantTable(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

函數 DWORD 資料流程的指標。

</dd> <dt>

 *ppConstantTable* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

傳回常數資料表介面 (查看管理常數資料表的 [**ID3DXConstantTable**](id3dxconstanttable.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

常數資料表是由 [**D3DXCompileShader**](d3dxcompileshader.md) 所產生，並內嵌在著色器主體中。 如果您需要額外的虛擬位址空間，請參閱 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
