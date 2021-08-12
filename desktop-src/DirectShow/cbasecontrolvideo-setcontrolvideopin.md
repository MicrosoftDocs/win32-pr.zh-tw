---
description: SetControlVideoPin 方法會設定篩選所使用的 pin。
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: 'CBaseControlVideo. SetControlVideoPin 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6169b5d2ec71148cd868e340c5a2f4e206355044ce55e0905c20787ddb3a263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660783"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>CBaseControlVideo. SetControlVideoPin 方法

`SetControlVideoPin`方法會設定篩選所使用的 pin。

## <a name="syntax"></a>語法


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

用來同步處理介面之 pin 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

只有在成功連接篩選器時，才能呼叫介面。 物件會透過這個方法傳遞給與其進行同步處理的 pin;在大部分的情況下，它會在有介面方法被呼叫時，判斷 pin 是否已連接，如果失敗，則會傳回 VFW \_ E \_ 未 \_ 連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




