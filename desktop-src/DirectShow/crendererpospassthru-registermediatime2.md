---
description: RegisterMediaTime 方法會快取目前範例中的時間戳記。 這個方法會使用 *StartTime* 和 *EndTime* 參數。
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) -StartTime 和 EndTime 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 944d78af6247e7237040f0260a51203a13ef506db36856cfb554d0f2982c0d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084108"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) -StartTime 和 EndTime 參數

[**RegisterMediaTime**](crendererpospassthru-registermediatime.md)方法會快取目前範例中的時間戳記。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartTime* 
</dt> <dd>

範例開始時間，以 100-毫微秒單位表示。

</dd> <dt>

*EndTime* 
</dt> <dd>

範例結束時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                          | 描述         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會儲存 *StartTime* 和 *EndTime* 中提供的時間戳記值。 [**CRendererPosPassThru：： GetMediaTime**](crendererpospassthru-getmediatime.md)方法會抓取相同的值。

篩選應該針對它收到的每個範例呼叫這個方法。 方法會多載，以接受範例的指標或時間戳記值本身。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | Ctlutil (包含： .h)                                                                                    |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |



 

 




