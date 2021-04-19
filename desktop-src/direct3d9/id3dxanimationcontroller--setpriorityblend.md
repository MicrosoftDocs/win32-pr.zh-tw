---
description: 設定動畫控制器所使用的優先順序混合權數。
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController：： SetPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000613"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a>ID3DXAnimationController：： SetPriorityBlend 方法

設定動畫控制器所使用的優先順序混合權數。

## <a name="syntax"></a>語法


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BlendWeight* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

動畫控制器所使用的優先順序混合權數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

Blend 權數是用來將高優先順序和低優先順序的追蹤一起結合在一起。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
