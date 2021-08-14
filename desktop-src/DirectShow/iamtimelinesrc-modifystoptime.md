---
description: ModifyStopTime 方法會設定相對於時程表的停止時間。
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'IAMTimelineSrc：： ModifyStopTime 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6d611395ad8989ea551fb98d1a3d538786881b0a5afc908a030367cac52ee80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952817"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>IAMTimelineSrc：： ModifyStopTime 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ModifyStopTime`方法會設定相對於時程表的停止時間。

## <a name="syntax"></a>語法


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*停止* 
</dt> <dd>

新的停止時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果指定的時間無效，則傳回 S OK 或 E \_ INVALIDARG。

## <a name="remarks"></a>備註

這個方法相當於呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 與原始開始時間和新的停止時間。

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

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




