---
description: 傳回目前在指定動畫播放軌上執行的事件的事件控制碼。
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController：： GetCurrentTrackEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d61902765c29808941637d4ce7ebb7f4b361ac6904abc1fae5907738162347a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094509"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>ID3DXAnimationController：： GetCurrentTrackEvent 方法

傳回目前在指定動畫播放軌上執行的事件的事件控制碼。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*追蹤* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

追蹤識別碼。

</dd> <dt>

*事件* \[ 的在\]
</dt> <dd>

類型： **[ **D3DXEVENT \_ 類型**](./d3dxevent-type.md)**

要查詢的事件種類。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

目前在指定的追蹤上執行的事件的事件控制碼。如果未在指定的追蹤上執行任何事件，就會傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
