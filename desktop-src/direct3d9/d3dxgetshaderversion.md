---
description: 傳回已編譯著色器的著色器版本。
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: 'D3DXGetShaderVersion 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116221"
---
# <a name="d3dxgetshaderversion-function"></a>D3DXGetShaderVersion 函式

傳回已編譯著色器的著色器版本。

## <a name="syntax"></a>語法


```C++
DWORD D3DXGetShaderVersion(
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

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

傳回指定著色器的著色器版本，如果著色器函式為 **Null**，則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器函式](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
