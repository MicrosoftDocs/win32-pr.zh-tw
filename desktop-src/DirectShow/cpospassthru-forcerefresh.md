---
description: ForceRefresh 方法已淘汰。
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: 'CPosPassThru. ForceRefresh 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 738a528562afd04e27105691b001958f130e353ec52aa60da86bec47c81b5ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915518"
---
# <a name="cpospassthruforcerefresh-method"></a>CPosPassThru. ForceRefresh 方法

`ForceRefresh`方法已淘汰。

## <a name="syntax"></a>語法


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

此類別原本是設計來快取連接的釘選 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的指標。 `ForceRefresh`方法會釋放這些介面。

目前已執行，這個類別不會快取這些介面。 為了提供相容性， `ForceRefresh` 仍會包含方法，但不會執行任何作業，而會傳回 \_ [確定]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




