---
description: CPosPassThru. GetCapabilities 方法-GetCapabilities 方法會抓取資料流程的所有搜尋功能。 這個方法會實 IMediaSeeking：： GetCapabilities 方法。
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: 'CPosPassThru. GetCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3f9c47022ece0305e3111fe21f365544ed495cfe3c1343b908309f801a1a0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073541"
---
# <a name="cpospassthrugetcapabilities-method"></a>CPosPassThru. GetCapabilities 方法

**GetCapabilities** 方法會抓取資料流程的所有搜尋功能。 這個方法會實 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCapabilities* 
</dt> <dd>

變數的指標，此變數會接收搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 旗標之 AM 的位元組合。

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

 

 




