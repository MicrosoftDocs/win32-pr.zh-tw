---
description: ModifyStopTime2 方法會設定停止時間。 這個方法相當於 IAMTimelineSrc：： ModifyStopTime，但會接受 REFTIME 值。
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'IAMTimelineSrc：： ModifyStopTime2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993643"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>IAMTimelineSrc：： ModifyStopTime2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ModifyStopTime2`方法會設定停止時間。 這個方法相當於 [**IAMTimelineSrc：： ModifyStopTime**](iamtimelinesrc-modifystoptime.md)，但會接受 [**REFTIME**](reftime.md) 值。

## <a name="syntax"></a>語法


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*停止* 
</dt> <dd>

新的停止時間（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK， \_ 如果指定的時間無效，則傳回 E INVALIDARG。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

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

 

 




