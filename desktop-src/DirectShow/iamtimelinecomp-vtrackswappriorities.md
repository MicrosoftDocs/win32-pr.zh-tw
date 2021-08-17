---
description: VTrackSwapPriorities 方法會切換兩個追蹤的優先權層級。
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'IAMTimelineComp：： VTrackSwapPriorities 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eb67e07f96ec2e8377690a5cd5233ba6cdb40242870da6d5f23b5f404b77b890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999281"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>IAMTimelineComp：： VTrackSwapPriorities 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`VTrackSwapPriorities`方法會切換兩個追蹤的優先權層級。

由於有兩個優先權層級，此方法會將虛擬追蹤切換至這些優先順序。 當方法傳回時，位於第一個優先權層級的追蹤現在會在第二個優先權層級，反之亦然。

## <a name="syntax"></a>語法


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

要交換虛擬追蹤的第一個優先權層級。

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

要交換虛擬追蹤的第二個優先權等級。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineComp 介面**](iamtimelinecomp.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




