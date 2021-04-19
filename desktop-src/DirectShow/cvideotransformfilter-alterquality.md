---
description: AlterQuality 方法會通知篩選要求品質變更。 這個方法會覆寫 CTransformFilter：： AlterQuality 方法。
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: 'CVideoTransformFilter. AlterQuality 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999318"
---
# <a name="cvideotransformfilteralterquality-method"></a>CVideoTransformFilter. AlterQuality 方法

`AlterQuality`方法會通知篩選準則，要求品質變更。 這個方法會覆寫 [**CTransformFilter：： AlterQuality**](ctransformfilter-alterquality.md) 方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*問* 
</dt> <dd>

包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ 失敗。

## <a name="remarks"></a>備註

當輸出圖釘透過 [**IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法)  (收到品質訊息時，就會呼叫這個方法。

*Q* 的延遲值儲存在 **m \_ itrLate** 成員變數中。 E 的傳回值表示轉譯器 \_ 應該藉由捨棄框架來趕上，雖然 **CVideoTransformFilter** 類別也會在適當的條件下卸載框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> <dt>

[**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




