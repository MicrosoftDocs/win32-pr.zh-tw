---
description: GetDuration 方法會捕獲資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetDuration 方法。
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: 'CSourceSeeking. GetDuration 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978766"
---
# <a name="csourceseekinggetduration-method"></a>CSourceSeeking. GetDuration 方法

`GetDuration`方法會捕獲資料流程的持續時間。 這個方法會實 [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDuration* 
</dt> <dd>

接收持續時間之變數的指標，以目前時間格式的單位為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

## <a name="remarks"></a>備註

持續期間是由 [**CSourceSeeking：： m \_ rtDuration**](csourceseeking-m-rtduration.md) 成員變數所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




