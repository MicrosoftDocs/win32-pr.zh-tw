---
description: FindPin 方法會取得具有指定識別碼的 pin。 這個方法會實 IBaseFilter：： FindPin 方法。
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: 'CTransformFilter. FindPin 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995756"
---
# <a name="ctransformfilterfindpin-method"></a>CTransformFilter. FindPin 方法

**FindPin** 方法會取得具有指定識別碼的 pin。 這個方法會實 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

包含 pin 識別碼的寬字元字串。

</dd> <dt>

*ppPin* 
</dt> <dd>

接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。 如果方法失敗， `*ppPin` 會設為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                       | Description                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | 記憶體不足。<br/>                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>         | **Null** 指標引數。<br/>                 |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 找不到具有此識別碼的 pin。<br/> |



 

## <a name="remarks"></a>備註

> [!IMPORTANT]
> 此方法的執行不會呼叫 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 來符合 pin 識別碼。 相反地，此方法會假設輸入的 pin 名為 "In"，且輸出的 pin 名為 "Out"。 如果您使用一組不同的 pin 識別碼，請覆寫這個方法。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




