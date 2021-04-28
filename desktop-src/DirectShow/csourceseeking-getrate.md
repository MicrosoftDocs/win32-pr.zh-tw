---
description: CSourceSeeking. GetRate 方法-GetRate 方法會捕獲播放速率。 這個方法會實 IMediaSeeking：： GetRate 方法。
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: 'CSourceSeeking. GetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085226"
---
# <a name="csourceseekinggetrate-method"></a>CSourceSeeking. GetRate 方法

`GetRate`方法會捕獲播放速率。 這個方法會實 [**IMediaSeeking：： GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdRate* 
</dt> <dd>

接收播放速率之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

## <a name="remarks"></a>備註

播放速率是由 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) 成員變數所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




