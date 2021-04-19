---
description: SetAllocator 方法會指定連接的配置器。
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: 'CTransInPlaceOutputPin. SetAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990149"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>CTransInPlaceOutputPin. SetAllocator 方法

方法會指定連接的配置器 `SetAllocator` 。

## <a name="syntax"></a>語法


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAllocator* 
</dt> <dd>

配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此篩選器的輸出 pin 永遠不會提供配置器。 這個方法會指定輸出圖釘的配置器。 它會設定 [**CBaseOutputPin：： m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) 成員變數的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceOutputPin 類別**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




