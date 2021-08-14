---
description: FixTimes2 方法會將指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。 這個方法相當於 IAMTimelineObj：： FixTimes，但會接受 REFTIME 的值。
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'IAMTimelineObj：： FixTimes2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74890c2b094172ac3ced0c9fd192a755d051b56df22301b4d64d9003eaa74e9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400903"
---
# <a name="iamtimelineobjfixtimes2-method"></a>IAMTimelineObj：： FixTimes2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `FixTimes2` 指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。 這個方法相當於 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md)，但會接受 [**REFTIME**](reftime.md) 的值。

## <a name="syntax"></a>語法


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStart* 
</dt> <dd>

包含開始時間（以秒為單位）之變數的指標。 如果呼叫成功，這個變數會設定為舍入時間。

</dd> <dt>

*pStop* 
</dt> <dd>

包含停止時間（以秒為單位）之變數的指標。 如果呼叫成功，這個變數會設定為舍入時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK， \_ 如果物件不是群組的一部分，則傳回 E NOTINTREE。

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

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




