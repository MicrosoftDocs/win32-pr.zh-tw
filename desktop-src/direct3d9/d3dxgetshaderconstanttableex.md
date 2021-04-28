---
description: D3DXGetShaderConstantTableEx 函式-取得內嵌在著色器中的著色器常數資料表。
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: 'D3DXGetShaderConstantTableEx 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114426"
---
# <a name="d3dxgetshaderconstanttableex-function"></a>D3DXGetShaderConstantTableEx 函式

取得內嵌在著色器中的著色器常數資料表。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
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

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

使用 D3DXCONSTTABLE \_ LARGEADDRESSAWARE 旗標可存取最多 4 gb 的虛擬位址空間 (而不是預設的 2 gb) 。 如果您不需要額外的虛擬位址空間，請使用 [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)。

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

常數資料表是由 [**D3DXCompileShader**](d3dxcompileshader.md) 所產生，並內嵌在著色器主體中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
