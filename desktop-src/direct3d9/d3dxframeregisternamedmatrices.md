---
description: 針對框架階層，在動畫混音器中註冊所有命名的矩陣。
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: 'D3DXFrameRegisterNamedMatrices 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997393"
---
# <a name="d3dxframeregisternamedmatrices-function"></a>D3DXFrameRegisterNamedMatrices 函式

針對框架階層，在動畫混音器中註冊所有命名的矩陣。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFrameRoot* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFRAME**](d3dxframe.md)**

框架階層中的最上層節點。

</dd> <dt>

*pAnimController* \[在\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

動畫控制器物件的指標。

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

 

 




