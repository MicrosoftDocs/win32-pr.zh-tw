---
description: Stop 方法會停止篩選。
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: 'CBaseRenderer. Stop 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979582"
---
# <a name="cbaserendererstop-method"></a>CBaseRenderer. Stop 方法

`Stop`方法會停止篩選。

## <a name="syntax"></a>語法


```C++
HRESULT Stop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseFilter：： Stop**](cbasefilter-stop.md) 方法。 其會執行下列動作：

-   呼叫 [**CBaseFilter：： Stop**](cbasefilter-stop.md)。
-   解除配置器。  (參閱 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)。 ) 
-   取消任何排程的轉譯，並釋放串流執行緒。
-   等候任何擱置的 **接收** 呼叫完成。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




