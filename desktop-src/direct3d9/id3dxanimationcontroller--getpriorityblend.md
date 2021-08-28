---
description: 取得動畫控制器所使用的目前優先權混合權數。
ms.assetid: ceaf611e-e85b-4958-b8ac-7e60b98b1aad
title: 'ID3DXAnimationController：： GetPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f66e4f0d6c36d2de655c8dee5f0cfbee3b5aa03d4750c5e2a8faaea43a24c657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373148"
---
# <a name="id3dxanimationcontrollergetpriorityblend-method"></a>ID3DXAnimationController：： GetPriorityBlend 方法

取得動畫控制器所使用的目前優先權混合權數。

## <a name="syntax"></a>語法


```C++
FLOAT GetPriorityBlend();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

傳回目前的優先順序混合加權。

## <a name="remarks"></a>備註

優先權混合權數可用來將高優先順序和低優先順序的追蹤結合在一起。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
