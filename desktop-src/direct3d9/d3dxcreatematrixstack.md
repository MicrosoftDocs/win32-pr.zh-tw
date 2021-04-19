---
description: 建立 ID3DXMATRIXStack 介面的實例。
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: 'D3DXCreateMatrixStack 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986122"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a>D3DXCreateMatrixStack 函式 (D3dx9math) 

建立 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 介面的實例。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

未實作。 指定零。

</dd> <dt>

*ppStack* \[擴展\]
</dt> <dd>

類型： **LPD3DXMATRIXSTACK \***

如果函式成功，則為以 [**ID3DXMATRIXStack**](id3dxmatrixstack.md) 介面指標填滿之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
