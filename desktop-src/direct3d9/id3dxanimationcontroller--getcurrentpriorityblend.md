---
description: 傳回目前正在執行之優先順序 blend 事件的事件控制碼。
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'ID3DXAnimationController：： GetCurrentPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c02e65bb17e07b3d75c4949730141831e5b146011e77478d95c8976b792c1c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094553"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a>ID3DXAnimationController：： GetCurrentPriorityBlend 方法

傳回目前正在執行之優先順序 blend 事件的事件控制碼。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

目前正在執行之優先權 blend 事件的事件控制碼。 如果目前沒有任何優先權 blend 事件正在執行，則會傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




