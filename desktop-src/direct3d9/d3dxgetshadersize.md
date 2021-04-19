---
description: 傳回著色器位元組程式碼的大小（以位元組為單位）。
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: 'D3DXGetShaderSize 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986738"
---
# <a name="d3dxgetshadersize-function"></a>D3DXGetShaderSize 函式

傳回著色器位元組程式碼的大小（以位元組為單位）。

## <a name="syntax"></a>語法


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

函數 DWORD 資料流程的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

傳回著色器位元組程式碼的大小（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
