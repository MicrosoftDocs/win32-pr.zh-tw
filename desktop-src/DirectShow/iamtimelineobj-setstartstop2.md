---
description: SetStartStop2 方法會設定物件的開始和停止時間，相對於物件的父系。 這個方法相當於 IAMTimelineObj：： SetStartStop，但會接受 REFTIME 的值。
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'IAMTimelineObj：： SetStartStop2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 30e7f9e6ce54cb86e2eee486937841842311dd498b42ec42e101128612bf16d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086828"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>IAMTimelineObj：： SetStartStop2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetStartStop2`方法會設定物件的開始和停止時間，相對於物件的父系。 這個方法相當於 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md)，但會接受 [**REFTIME**](reftime.md) 的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*開始* 
</dt> <dd>

新的開始時間（以秒為單位），或-1 會保留現有的開始時間。

</dd> <dt>

*停止* 
</dt> <dd>

新的停止時間（以秒為單位），或-1 會保留現有的停止時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                  | 描述                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>    | 未實作。<br/>  |



 

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

 

 




