---
description: CTransformOutputPin。通知方法-通知方法會通知 pin，要求品質變更。 這個方法會執行 IQualityControl：： Notify 方法。
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: 'CTransformOutputPin： Notify 方法 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69cff051ecab1a93d9fdceac20143bef7d1959ff523aa5893e5ae9c633aa80f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538138"
---
# <a name="ctransformoutputpinnotify-method"></a>CTransformOutputPin。通知方法

`Notify`方法會通知 pin，要求品質變更。 這個方法會 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSelf* 
</dt> <dd>

傳遞品質控制訊息之篩選準則的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標。

</dd> <dt>

*問* 
</dt> <dd>

包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                       | 描述                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                                        |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 找不到接受訊息的物件。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫篩選準則的 [**CTransformFilter：： AlterQuality**](ctransformfilter-alterquality.md) 方法。 如果篩選器不會處理品質訊息，這個方法會在篩選的輸入圖釘上呼叫 [**CBaseInputPin：:P assnotify**](cbaseinputpin-passnotify.md) 方法。 **PassNotify** 方法會將高品質訊息傳遞給上游 (或自訂品質管制員（如果已安裝) ）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




