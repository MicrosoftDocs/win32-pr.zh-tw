---
description: CSourceSeeking. SetPositions 方法-SetPositions 方法會設定目前的位置和停止位置。 這個方法會實 IMediaSeeking：： SetPositions 方法。
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: 'CSourceSeeking. SetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085166"
---
# <a name="csourceseekingsetpositions-method"></a>CSourceSeeking. SetPositions 方法

`SetPositions`方法會設定目前的位置和停止位置。 這個方法會實 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrent* 
</dt> <dd>

變數的指標，該變數會指定目前的位置。

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

旗標的位組合。 請參閱＜備註＞。

</dd> <dt>

*pStop* 
</dt> <dd>

指定停止時間之變數的指標，以目前時間格式的單位為單位。

</dd> <dt>

*StopFlags* 
</dt> <dd>

旗標的位組合。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                  | Description                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | Success<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 不正確旗標<br/>             |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

以下是支援的旗標：

-   \_搜尋 \_ NoPositioning
-   \_搜尋 \_ AbsolutePositioning
-   \_搜尋 \_ RelativePositioning
-   正在 \_ 搜尋 \_ IncrementalPositioning (僅 *pStop*) 

如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)。

這個方法會更新 [**CSourceSeeking：： m \_ RtStart**](csourceseeking-m-rtstart.md) 和 [**CSourceSeeking：： m \_ rtStop**](csourceseeking-m-rtstop.md) 成員變數的值，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md) 和 [**CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




