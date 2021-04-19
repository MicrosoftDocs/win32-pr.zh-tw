---
description: GetAllocatorRequirements 方法會抓取輸入 pin 所要求的配置器屬性。
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: 'CBaseInputPin. GetAllocatorRequirements 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990552"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>CBaseInputPin. GetAllocatorRequirements 方法

方法會抓取 `GetAllocatorRequirements` 輸入 pin 所要求的配置器屬性。

## <a name="syntax"></a>語法


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProps* 
</dt> <dd>

配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，該結構會填入需求。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

當輸出釘選初始化記憶體配置器時，它可以呼叫這個方法來判斷輸入的 pin 是否有任何緩衝區需求。 如需詳細資訊，請參閱 [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md)。

您可以選擇是否要執行此方法。 如果篩選準則有特定的對齊或首碼需求，請覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




