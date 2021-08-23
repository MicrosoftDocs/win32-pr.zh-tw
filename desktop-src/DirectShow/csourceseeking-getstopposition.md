---
description: GetStopPosition 方法會捕獲播放將會停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetStopPosition 方法。
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: 'CSourceSeeking. GetStopPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 870ddbf77d1a29a34703d4b43ee21d02b676e8fafac9ee688384246339465732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073322"
---
# <a name="csourceseekinggetstopposition-method"></a>CSourceSeeking. GetStopPosition 方法

此 `GetStopPosition` 方法會抓取播放將停止的時間（相對於資料流程的持續時間）。 這個方法會實 [**IMediaSeeking：： GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStop* 
</dt> <dd>

接收停止時間之變數的指標，以目前時間格式的單位為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | 描述                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

## <a name="remarks"></a>備註

停止時間是由 [**CSourceSeeking：： m \_ rtStop**](csourceseeking-m-rtstop.md) 成員變數所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




