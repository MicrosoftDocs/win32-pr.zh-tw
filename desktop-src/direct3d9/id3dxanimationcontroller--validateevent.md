---
description: 檢查指定的事件控制碼是否有效，以及動畫事件是否尚未完成。
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'ID3DXAnimationController：： ValidateEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992354"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>ID3DXAnimationController：： ValidateEvent 方法

檢查指定的事件控制碼是否有效，以及動畫事件是否尚未完成。

## <a name="syntax"></a>語法


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hEvent* \[在\]
</dt> <dd>

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

動畫事件的事件控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

\_如果事件控制碼有效且事件尚未完成，則傳回 S OK。

\_如果事件控制碼無效及/或事件已完成，則傳回 E 失敗。

## <a name="remarks"></a>備註

方法將表示事件控制碼有效，即使事件正在執行，但尚未完成。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




