---
description: SetProperties 方法會指定要配置的緩衝區數目和每個緩衝區的大小。 這個方法會實 IMemAllocator：： SetProperties 方法。
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: 'CBaseAllocator. SetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987833"
---
# <a name="cbaseallocatorsetproperties-method"></a>CBaseAllocator. SetProperties 方法

`SetProperties`方法會指定要配置的緩衝區數目和每個緩衝區的大小。 這個方法會實 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRequest* 
</dt> <dd>

配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含緩衝區需求。

</dd> <dt>

*pActual* 
</dt> <dd>

配置器 **\_ 屬性** 結構的指標，此結構會接收實際的緩衝區屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                                 | Description                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                        | 成功。<br/>                                                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>                   | **Null** 指標引數。<br/>                                 |
| <dl> <dt>**VFW \_ E \_ 已 \_ 認可**</dt> </dl>   | 當篩選準則為作用中時，無法變更配置的記憶體。<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | 指定了不正確對齊方式。<br/>                        |
| <dl> <dt>**未處理的 VFW \_ E \_ 緩衝區 \_**</dt> </dl> | 一或多個緩衝區仍在使用中。<br/>                      |



 

## <a name="remarks"></a>備註

這個方法會指定緩衝區需求，但不會配置任何緩衝區。 呼叫 [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法以配置緩衝區。

呼叫端會配置兩個配置器 \_ 屬性結構。 *PRequest* 參數包含呼叫端的緩衝區需求，包括緩衝區數目和每個緩衝區的大小。 當方法傳回時， *pActual* 參數會包含實際的緩衝區屬性（由配置器所設定）。 在基類中，假設方法成功，則實際的屬性一律會符合要求的屬性。 衍生類別可能會覆寫此行為。

配置器不得認可，且不能有未處理的緩衝區。 在基類中，對齊必須等於1。 [**CMemAllocator**](cmemallocator.md)類別會覆寫這項需求。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




