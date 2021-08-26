---
description: RegisterMediaTime 方法會快取目前範例中的時間戳記。
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: 'CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) '
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
ms.openlocfilehash: 69688bb011fc8a75b0ec52effaef3afd7972fb7a198a4cdedf20c07a40c4fa7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054378"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) 

**RegisterMediaTime** 方法會快取目前範例中的時間戳記。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                                  | 描述                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                        |
| <dl> <dt>**\_ \_ \_ \_ 未設定 VFW E 媒體 \_ 時間**</dt> </dl> | 此範例不會加上時間戳記。<br/> |



 

## <a name="remarks"></a>備註

這個方法會儲存目前範例中的時間戳記。 [**CRendererPosPassThru：： GetMediaTime**](crendererpospassthru-getmediatime.md)方法會抓取相同的值。

篩選應該針對它收到的每個範例呼叫這個方法。 方法會多載，以接受範例的指標或時間戳記值本身。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




