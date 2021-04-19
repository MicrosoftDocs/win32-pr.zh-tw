---
description: 終結根目錄下的框架子樹，包括根。
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: 'D3DXFrameDestroy 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982013"
---
# <a name="d3dxframedestroy-function"></a>D3DXFrameDestroy 函式

終結根目錄下的框架子樹，包括根。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFrameRoot* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFRAME**](d3dxframe.md)**

根節點的指標。

</dd> <dt>

*pAlloc* \[在\]
</dt> <dd>

類型： **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

配置介面，用來解除組態架構階層的節點。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




