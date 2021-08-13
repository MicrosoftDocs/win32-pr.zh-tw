---
description: 建立動畫控制器物件。
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: 'D3DXCreateAnimationController 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0edda07aa5ae443a268bd5df50a154aa2a7f2ec9ca1873dc486e8e46532ae468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526633"
---
# <a name="d3dxcreateanimationcontroller-function"></a>D3DXCreateAnimationController 函式

建立動畫控制器物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MaxNumAnimationOutputs* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制器可支援的動畫輸出數目上限。

</dd> <dt>

*MaxNumAnimationSets* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

可以混合的動畫集合數目上限。

</dd> <dt>

*MaxNumTracks* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

可以同時混合的動畫集合數目上限。

</dd> <dt>

*MaxNumEvents* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制器將支援的未完成事件數目上限。

</dd> <dt>

*ppAnimController* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

建立的動畫控制器物件的指標。 請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

動畫控制器會控制動畫混音器。 控制器會新增方法來修改一段時間的混合參數，以啟用平滑轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動畫函數](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
