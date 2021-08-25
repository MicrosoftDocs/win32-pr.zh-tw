---
description: 傳回已排定在指定事件之後發生之下一個優先權 blend 事件的事件控制碼。
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController：： GetUpcomingPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c58bf5e2a8736db98e0461988f984709e756d269d09c74dd673356676702ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849078"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>ID3DXAnimationController：： GetUpcomingPriorityBlend 方法

傳回已排定在指定事件之後發生之下一個優先權 blend 事件的事件控制碼。

## <a name="syntax"></a>語法


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hEvent* \[在\]
</dt> <dd>

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

指定事件的事件控制碼，之後會在此搜尋下列優先權 blend 事件。 如果設定為 **Null**，則方法會傳回下一個排程的 priority blend 事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

下一個排程優先權 blend 事件的事件控制碼。 如果未排定新的優先權 blend 事件，則會傳回 **Null** 。

## <a name="remarks"></a>備註

您可以重複傳遞 **Null** 來 hEvent，以反復使用這個方法來尋找所需的優先順序 blend 事件。

> [!Note]  
> 當方法傳回 **Null** 之後，請勿再逐一查看。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




