---
description: AbortPlayback 方法是用來發出串流錯誤的信號。 它會將 EC \_ ERRORABORT 事件傳送至篩選圖形管理員，並傳送下游的結束資料流程通知。
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: 'CVideoTransformFilter. AbortPlayback 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981877"
---
# <a name="cvideotransformfilterabortplayback-method"></a>CVideoTransformFilter. AbortPlayback 方法

`AbortPlayback`方法是用來發出串流錯誤的信號。 它會將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送至篩選圖形管理員，並傳送下游的結束資料流程通知。

## <a name="syntax"></a>語法


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*小時* 
</dt> <dd>

失敗之作業的 **HRESULT** 值。 這個值是用來做為 EC ERRORABORT 事件的第一個事件參數 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 *hr* 參數的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




