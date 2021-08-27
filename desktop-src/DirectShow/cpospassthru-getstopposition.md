---
description: GetStopPosition 方法會捕獲播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetStopPosition 方法。
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: 'CPosPassThru. GetStopPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9c6798d03e2935c991e12cded4d85a4972d54e7800d6aa79c70525b10276f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084068"
---
# <a name="cpospassthrugetstopposition-method"></a>CPosPassThru. GetStopPosition 方法

`GetStopPosition`方法會抓取播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 [**IMediaSeeking：： GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) 方法。

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

從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




