---
description: SetProperties 方法會指定要配置的緩衝區數目和每個緩衝區的大小。
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: 'CMemAllocator. SetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000833"
---
# <a name="cmemallocatorsetproperties-method"></a>CMemAllocator. SetProperties 方法

`SetProperties`方法會指定要配置的緩衝區數目和每個緩衝區的大小。

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

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                 | Description                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                        | 成功。<br/>                                                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>                   | **Null** 指標引數。<br/>                                 |
| <dl> <dt>**VFW \_ E \_ 已 \_ 認可**</dt> </dl>   | 當篩選準則為作用中時，無法變更配置的記憶體。<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | 指定了不正確對齊方式。<br/>                        |
| <dl> <dt>**未處理的 VFW \_ E \_ 緩衝區 \_**</dt> </dl> | 一或多個緩衝區仍在使用中。<br/>                      |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法。

由配置器 **\_ 屬性** 結構的 **cbAlign** 成員所指定的緩衝區對齊，必須是2的乘冪。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMemAllocator 類別**](cmemallocator.md)
</dt> </dl>

 

 




