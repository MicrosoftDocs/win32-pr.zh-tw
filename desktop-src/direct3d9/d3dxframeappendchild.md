---
description: 將子框架新增至框架。
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: 'D3DXFrameAppendChild 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b6bc06eecb036f285e03b984e0fcd645d5c2416377684455dce491a3159d070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988468"
---
# <a name="d3dxframeappendchild-function"></a>D3DXFrameAppendChild 函式

將子框架新增至框架。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFrameParent* \[在\]
</dt> <dd>

類型： **[ **LPD3DXFRAME**](d3dxframe.md)**

父節點的指標。

</dd> <dt>

*pFrameChild* \[在\]
</dt> <dd>

Type： **Const [**D3DXFRAME**](d3dxframe.md) \***

子節點的指標。

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

 

 




