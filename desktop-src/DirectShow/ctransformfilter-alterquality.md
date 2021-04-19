---
description: AlterQuality 方法會通知篩選要求品質變更。
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: 'CTransformFilter. AlterQuality 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997672"
---
# <a name="ctransformfilteralterquality-method"></a>CTransformFilter. AlterQuality 方法

`AlterQuality`方法會通知篩選準則，要求品質變更。

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

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | Description                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 未處理品質訊息。 訊息應通過上游傳遞。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 處理品質訊息。 不需要進行其他動作。<br/>               |



 

## <a name="remarks"></a>備註

如果篩選準則可以執行品質控制，請覆寫這個方法。 如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




