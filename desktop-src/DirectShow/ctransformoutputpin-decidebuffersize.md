---
description: DecideBufferSize 方法會設定緩衝區需求。
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: 'CTransformOutputPin. DecideBufferSize 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993454"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>CTransformOutputPin. DecideBufferSize 方法

`DecideBufferSize`方法會設定緩衝區需求。

## <a name="syntax"></a>語法


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlloc* 
</dt> <dd>

配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

指向配置 [**器 \_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含輸入釘選的緩衝區需求。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 方法。 它會呼叫篩選準則的純虛擬 [**CTransformFilter：:D ecidebuffersize**](ctransformfilter-decidebuffersize.md) 方法，該方法必須是篩選準則的衍生類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




