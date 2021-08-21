---
description: Remove 方法會從時間軸中移除此物件 (包括子物件，而不是子系) ，可供其他地方 reinsertion。
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'IAMTimelineObj：： Remove 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356f7239cbdbe3972f11fcc95dd9bf44dc1b06d086a8e44c9131c0061f3ec211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155261"
---
# <a name="iamtimelineobjremove-method"></a>IAMTimelineObj：： Remove 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`Remove`方法會從時間軸中移除此物件 (包括子物件，而不是子系) ，可供其他地方 reinsertion。

## <a name="syntax"></a>語法


```C++
HRESULT Remove();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有在應用程式會立即將物件插入至時間軸時，才呼叫這個方法。 這是不正確作業，無法在不重新插入物件的情況下呼叫這個方法。 若要永久移除物件，請呼叫 [**IAMTimelineObj：： RemoveAll**](iamtimelineobj-removeall.md)。

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

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




