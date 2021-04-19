---
description: SetConfigInfo 方法會指定 IGraphConfig 指標和 stop 事件。
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: 'CDynamicOutputPin. SetConfigInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977498"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>CDynamicOutputPin. SetConfigInfo 方法

`SetConfigInfo`方法會指定 [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)指標和停止事件。

## <a name="syntax"></a>語法


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pGraphConfig* 
</dt> <dd>

[**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)介面的指標，或 **為 Null**。

</dd> <dt>

*hStopEvent* 
</dt> <dd>

當篩選準則停止時所發出之事件的控制碼，或 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

篩選器加入篩選圖形時，必須呼叫這個方法。 篩選圖形管理員支援 **IGraphConfig**。 針對 *hStopEvent* 參數，建立手動重設事件。 當篩選準則離開篩選圖形時，請針對這兩個參數，以 **Null** 呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




