---
description: SetPositions 方法會設定目前的位置和停止位置。 這個方法會實 IMediaSeeking：： SetPositions 方法。
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: 'CPosPassThru. SetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991237"
---
# <a name="cpospassthrusetpositions-method"></a>CPosPassThru. SetPositions 方法

`SetPositions`方法會設定目前的位置和停止位置。 這個方法會實 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrent* 
</dt> <dd>

變數的指標，該變數會指定目前的位置，以目前時間格式的單位為單位。

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

旗標的位組合。 如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 。

</dd> <dt>

*pStop* 
</dt> <dd>

指定停止時間之變數的指標，以目前時間格式的單位為單位。

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

旗標的位組合。 如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 。

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

 

 




