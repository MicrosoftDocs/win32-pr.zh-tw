---
description: CBaseInputPin 方法-非使用中方法會通知 pin，篩選已不再有效。
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: 'CBaseInputPin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dec73f0c691c7c644ead6456cc76fb1758202497ffcd968893780b2f0f61f93b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403457"
---
# <a name="cbaseinputpininactive-method"></a>CBaseInputPin 方法

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

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




