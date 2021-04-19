---
description: GetAllocatorRequirements 方法會抓取 pin 所要求的配置器屬性。 這個方法會實 IMemInputPin：： GetAllocatorRequirements 方法。
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: 'CTransInPlaceInputPin. GetAllocatorRequirements 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001920"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>CTransInPlaceInputPin. GetAllocatorRequirements 方法

方法會抓取 `GetAllocatorRequirements` pin 所要求的配置器屬性。 這個方法會實 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) 方法。

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

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                               | Description                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                                                                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 輸出針腳未連接，或下游輸入 pin 不支援方法。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數<br/>                                                                 |



 

## <a name="remarks"></a>備註

如果輸出連接已連線，這個方法會將呼叫傳遞給下游輸入 pin。 否則，它會傳回 E \_ >notimpl。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceInputPin 類別**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




