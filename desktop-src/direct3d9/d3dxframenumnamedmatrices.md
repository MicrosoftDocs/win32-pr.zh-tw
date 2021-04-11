---
description: 計運算元樹中具有非 null 名稱的框架數目。
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: 'D3DXFrameNumNamedMatrices 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946098"
---
# <a name="d3dxframenumnamedmatrices-function"></a>D3DXFrameNumNamedMatrices 函式

計運算元樹中具有非 null 名稱的框架數目。

## <a name="syntax"></a>語法


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFrameRoot* \[在\]
</dt> <dd>

Type： **Const [**D3DXFRAME**](d3dxframe.md) \***

子樹根節點的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

傳回框架計數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
