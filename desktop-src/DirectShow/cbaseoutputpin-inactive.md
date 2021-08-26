---
description: CBaseOutputPin 方法-非使用中方法會通知 pin，篩選已不再有效。
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: 'CBaseOutputPin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0600402301bf416dc0863c4ccff05cac698ec53871b03fd8a84f3873fd43163a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983418"
---
# <a name="cbaseoutputpininactive-method"></a>CBaseOutputPin 方法

`Inactive`方法會通知 pin，篩選已不再有效。

## <a name="syntax"></a>語法


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                          | 描述                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                 | 成功。<br/>                          |
| <dl> <dt>**VFW \_ E \_ NO 配置器 \_**</dt> </dl> | 沒有記憶體配置器可用。<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。 它會呼叫 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) 方法來取消認可記憶體配置器。

如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




