---
description: DecideBufferSize 方法會設定輸出 pin 的緩衝區需求。
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: 'CTransInPlaceFilter. DecideBufferSize 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990157"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>CTransInPlaceFilter. DecideBufferSize 方法

`DecideBufferSize`方法會設定輸出釘選的緩衝區需求。

## <a name="syntax"></a>語法


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlloc* 
</dt> <dd>

輸出釘選所使用之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 物件的指標。

</dd> <dt>

*pProperties* 
</dt> <dd>

依配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構所指定的計數、大小和對齊所要求配置器屬性的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                            | Description        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | Success<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 失敗<br/> |



 

## <a name="remarks"></a>備註

當 **CTransInPlaceFilter** 類別需要提供緩衝區大小給下游篩選準則時，就會呼叫這個方法。 如果 **CTransInPlaceFilter** 篩選已連接上游，則會使用上游連接上的配置器屬性。 否則，它會將緩衝區大小設定為1個位元組，以做為暫時的預留位置值。 當上游篩選連接時， **CTransInPlaceFilter** 類別會重新配置下游配置器。 如需此類別中 pin 連接程式的詳細資訊，請參閱 [**CTransInPlaceFilter 類別**](ctransinplacefilter.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




